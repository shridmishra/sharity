# Sharity — API Design & Router Specification

> **Detailed tRPC Router Hierarchy & Endpoint Specification**  
> Companion to [System Architecture](file:///Users/shrid/sharity/apps/docs/architecture/system_architecture.md) and [Database Schema](file:///Users/shrid/sharity/apps/docs/architecture/database_schema.md)

---

## 1. Overview & Protocol Setup

Sharity utilizes **tRPC v11** mounted inside the Hono backend server (`apps/server`) at `/trpc/*`. tRPC ensures end-to-end type safety between frontend web packages (`apps/web`, `apps/landing`) and backend routers (`packages/api`).

### Middleware & Auth Procedure Hierarchy

```text
publicProcedure (Unauthenticated access - read projects, search, map pins)
    │
    ├── protectedProcedure (Enforces ctx.user !== null - create project, contribute, volunteer)
    │
    └── adminProcedure (Enforces ctx.user.role === 'admin' or 'reviewer' - approve project, verify milestone)
```

---

## 2. Comprehensive Procedure Specifications

### 2.1 `project` Router (`packages/api/src/routers/project.ts`)

#### `project.list` (`publicProcedure`)
- **Input (Zod):**
  ```typescript
  z.object({
    category: z.string().optional(),
    location: z.string().optional(),
    status: z.enum(["approved", "live", "in_progress", "completed"]).optional(),
    search: z.string().optional(),
    limit: z.number().min(1).max(50).default(12),
    cursor: z.string().optional()
  })
  ```
- **Output:** Array of project card objects + `nextCursor`.

#### `project.getBySlug` (`publicProcedure`)
- **Input:** `z.object({ slug: z.string() })`
- **Output:** Complete project details including creator info, needs list, milestones, health status, and public ledger feed.

#### `project.create` (`protectedProcedure`)
- **Input (Zod):**
  ```typescript
  z.object({
    title: z.string().min(5).max(100),
    summary: z.string().min(10).max(250),
    problemStatement: z.string().min(20),
    desiredOutcome: z.string().min(20),
    category: z.string(),
    locationName: z.string(),
    coverImageUrl: z.string().url().optional(),
    needs: z.array(z.object({
      needType: z.enum(["financial", "item", "volunteer", "skill"]),
      title: z.string(),
      quantityTarget: z.number().positive(),
      unit: z.string().optional()
    })),
    milestones: z.array(z.object({
      stepNumber: z.number().positive(),
      title: z.string(),
      expectedResult: z.string(),
      budgetAllocation: z.number().positive(),
      evidenceRequirement: z.string()
    }))
  })
  ```
- **Output:** `{ id: string, slug: string, status: "under_review" }`

---

### 2.2 `milestone` Router (`packages/api/src/routers/milestone.ts`)

#### `milestone.submitEvidence` (`protectedProcedure`)
- **Input:**
  ```typescript
  z.object({
    milestoneId: z.string(),
    files: z.array(z.object({
      fileUrl: z.string().url(),
      fileType: z.enum(["image", "video", "document", "invoice"]),
      caption: z.string().optional()
    })),
    notes: z.string()
  })
  ```
- **Behavior:** Attaches evidence records to the milestone and updates milestone status to `'under_review'`.

#### `milestone.verify` (`adminProcedure`)
- **Input:**
  ```typescript
  z.object({
    milestoneId: z.string(),
    decision: z.enum(["approve", "reject", "request_clarification"]),
    feedback: z.string().optional()
  })
  ```
- **Behavior (Approve):** Releases milestone funds, updates milestone status to `'approved'`, records public ledger event `milestone_approved`, and advances project stage.

---

### 2.3 `contribution` Router (`packages/api/src/routers/contribution.ts`)

#### `contribution.initiate` (`protectedProcedure`)
- **Input:** `z.object({ projectId: z.string(), amount: z.number().positive(), isAnonymous: z.boolean().default(false) })`
- **Output:** Payment gateway parameters and temporary reference ID.

#### `contribution.getProjectLedger` (`publicProcedure`)
- **Input:** `z.object({ projectId: z.string() })`
- **Output:** Array of chronological `public_ledger_events`.

---

### 2.4 `admin` Router (`packages/api/src/routers/admin.ts`)

#### `admin.getReviewQueue` (`adminProcedure`)
- **Output:** List of project proposals with status `'under_review'`.

#### `admin.reviewProject` (`adminProcedure`)
- **Input:** `z.object({ projectId: z.string(), decision: z.enum(["approve", "reject", "request_revisions"]), notes: z.string().optional() })`
- **Output:** `{ success: boolean, updatedStatus: string }`

---

## 3. Error Codes & Standard Formats

| TRPC Error Code | HTTP Status | Use Case |
|---|---|---|
| `UNAUTHORIZED` | 401 | User missing active session token |
| `FORBIDDEN` | 403 | User lacks required role (`adminProcedure`) |
| `NOT_FOUND` | 404 | Project slug or milestone ID does not exist |
| `BAD_REQUEST` | 400 | Zod schema validation failure or invalid budget math |
| `INTERNAL_SERVER_ERROR` | 500 | Database connection failure or unhandled exception |
