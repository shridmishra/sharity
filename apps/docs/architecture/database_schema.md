# Sharity — Relational Database Schema Specification

> **Deep Database Schema & Entity Specification**  
> Companion to [System Architecture](file:///Users/shrid/sharity/apps/docs/architecture/system_architecture.md) and [Drizzle Package](file:///Users/shrid/sharity/packages/db)

---

## 1. ER Diagram & Primary Relationships

```mermaid
erDiagram
    users ||--o{ accounts : "authenticates via"
    users ||--o{ sessions : "maintains"
    users ||--o{ projects : "creates"
    users ||--o{ contributions : "makes"
    users ||--o{ volunteer_commitments : "pledges"
    users ||--o{ evidence_uploads : "uploads"
    
    projects ||--o{ project_needs : "requires"
    projects ||--o{ project_milestones : "structures"
    projects ||--o{ public_ledger_events : "audits"
    projects ||--o{ evidence_uploads : "collects"
    projects ||--o? impact_reports : "publishes"
    
    project_needs ||--o{ volunteer_commitments : "fulfills"
    project_milestones ||--o{ evidence_uploads : "attaches"
    project_milestones ||--o{ public_ledger_events : "records"
```

---

## 2. Table Definitions & Column Specifications

### 2.1 User & Authentication Tables (`packages/db/src/schema/auth.ts`)

#### Table: `users`
| Column | Type | Constraints | Description |
|---|---|---|---|
| `id` | `text` | Primary Key | Unique user identifier (cuid/uuid) |
| `name` | `text` | Not Null | Display name |
| `email` | `text` | Not Null, Unique, Index | User email address |
| `emailVerified` | `boolean` | Not Null, Default `false` | Email verification flag |
| `image` | `text` | Nullable | Avatar image URL |
| `role` | `text` | Not Null, Default `'user'` | Options: `'user'`, `'creator'`, `'reviewer'`, `'admin'` |
| `location` | `text` | Nullable | User's city or region |
| `bio` | `text` | Nullable | Short bio |
| `createdAt` | `timestamp` | Not Null | Record creation timestamp |
| `updatedAt` | `timestamp` | Not Null | Record update timestamp |

---

### 2.2 Impact Project Tables (`packages/db/src/schema/projects.ts`)

#### Table: `projects`
| Column | Type | Constraints | Description |
|---|---|---|---|
| `id` | `text` | Primary Key | Unique project ID |
| `title` | `text` | Not Null | Project title |
| `slug` | `text` | Not Null, Unique, Index | URL-friendly slug |
| `summary` | `text` | Not Null | Brief summary for cards |
| `problemStatement` | `text` | Not Null | Detailed problem description |
| `desiredOutcome` | `text` | Not Null | Targeted community outcome |
| `category` | `text` | Not Null, Index | e.g. `'education'`, `'environment'`, `'healthcare'`, `'infrastructure'` |
| `locationName` | `text` | Not Null, Index | City or district name |
| `latitude` | `real` | Nullable | Geo coordinate latitude |
| `longitude` | `real` | Nullable | Geo coordinate longitude |
| `coverImageUrl` | `text` | Nullable | Cover photo URL |
| `status` | `text` | Not Null, Index, Default `'draft'` | Options: `'draft'`, `'under_review'`, `'approved'`, `'live'`, `'in_progress'`, `'milestone_review'`, `'completed'`, `'paused'`, `'cancelled'` |
| `healthStatus` | `text` | Not Null, Default `'healthy'` | Options: `'healthy'`, `'needs_attention'`, `'paused'` |
| `creatorId` | `text` | Not Null, Foreign Key (`users.id`) | Reference to project creator |
| `totalFinancialTarget` | `integer` | Not Null, Default `0` | Financial target in INR |
| `totalFinancialRaised` | `integer` | Not Null, Default `0` | Total financial raised in INR |
| `createdAt` | `timestamp` | Not Null | Creation timestamp |
| `updatedAt` | `timestamp` | Not Null | Update timestamp |

---

### 2.3 Multi-Modal Needs (`packages/db/src/schema/needs.ts`)

#### Table: `project_needs`
| Column | Type | Constraints | Description |
|---|---|---|---|
| `id` | `text` | Primary Key | Unique need ID |
| `projectId` | `text` | Not Null, Foreign Key (`projects.id`), Index | Parent project ID |
| `needType` | `text` | Not Null | Options: `'financial'`, `'item'`, `'volunteer'`, `'skill'` |
| `title` | `text` | Not Null | e.g. "50 Books", "2 Carpenters" |
| `quantityTarget` | `integer` | Not Null, Default `1` | Total quantity needed |
| `quantityFulfilled` | `integer` | Not Null, Default `0` | Fulfilled quantity |
| `unit` | `text` | Nullable | e.g. "books", "hours", "INR" |
| `status` | `text` | Not Null, Default `'open'` | Options: `'open'`, `'partially_fulfilled'`, `'fulfilled'` |

---

### 2.4 Milestones & Escrow (`packages/db/src/schema/milestones.ts`)

#### Table: `project_milestones`
| Column | Type | Constraints | Description |
|---|---|---|---|
| `id` | `text` | Primary Key | Unique milestone ID |
| `projectId` | `text` | Not Null, Foreign Key (`projects.id`), Index | Parent project ID |
| `stepNumber` | `integer` | Not Null | Sequence index (1, 2, 3...) |
| `title` | `text` | Not Null | Stage title |
| `expectedResult` | `text` | Not Null | Expected verifiable outcome |
| `budgetAllocation` | `integer` | Not Null | Stage budget in INR |
| `releasedAmount` | `integer` | Not Null, Default `0` | Released funds upon approval |
| `evidenceRequirement` | `text` | Not Null | Required proof guidelines |
| `status` | `text` | Not Null, Default `'pending'` | Options: `'pending'`, `'in_progress'`, `'under_review'`, `'approved'`, `'rejected'` |
| `approvedAt` | `timestamp` | Nullable | Milestone approval timestamp |
| `approvedBy` | `text` | Nullable, Foreign Key (`users.id`) | Approving admin ID |

---

### 2.5 Auditable Public Ledger (`packages/db/src/schema/ledger.ts`)

#### Table: `public_ledger_events`
| Column | Type | Constraints | Description |
|---|---|---|---|
| `id` | `text` | Primary Key | Unique ledger event ID |
| `projectId` | `text` | Not Null, Foreign Key (`projects.id`), Index | Parent project ID |
| `eventType` | `text` | Not Null | Options: `'contribution_received'`, `'funds_held'`, `'milestone_submitted'`, `'milestone_approved'`, `'funds_released'`, `'refund_issued'`, `'project_completed'` |
| `description` | `text` | Not Null | Human-readable log string |
| `amount` | `integer` | Nullable | Amount involved in INR |
| `milestoneId` | `text` | Nullable, Foreign Key (`project_milestones.id`) | Associated milestone ID |
| `metadata` | `text` | Nullable | Additional JSON string metadata |
| `createdAt` | `timestamp` | Not Null | Event timestamp |

---

## 3. Indexes & Performance Optimization Strategy

1. `idx_projects_status_category`: Composite index on `projects(status, category)` for fast Explore page filtering.
2. `idx_projects_slug`: Unique index on `projects(slug)` for $O(1)$ page route lookups.
3. `idx_ledger_project`: Index on `public_ledger_events(projectId, createdAt)` for quick timeline rendering.
