# Sharity — Developer & Workflow Guide

> **Setup, Development Commands & Monorepo Best Practices**  
> Companion to [AGENTS.md](file:///Users/shrid/sharity/AGENTS.md) and [System Architecture](file:///Users/shrid/sharity/apps/docs/architecture/system_architecture.md)

---

## 1. Prerequisites & Installation

Ensure you have **Bun** (v1.1+) installed on your machine.

Clone the repository and install all monorepo workspace dependencies:

```bash
bun install
```

---

## 2. Global `shar` CLI Binary

The project includes a convenient `shar` binary for quick server control, type checking, and database operations.

```bash
shar         # Sync database schema, run type checks, and launch full development stack
shar kill    # Terminate all running servers on ports 3000, 3001, 3002, 8080
shar push    # Apply Drizzle database schema migrations (`bun run db:push`)
shar check   # Run TypeScript type checks (`bun run check-types`)
shar local   # Start local Turso/SQLite database server (`bun run db:local`)
```

---

## 3. Standard Development Scripts

| Command | Action |
|---|---|
| `bun run dev` | Start full monorepo stack (Server on 3000, Web on 3001, Landing on 3002) |
| `bun run dev:web` | Start frontend web application only (`http://localhost:3001`) |
| `bun run dev:landing` | Start landing page application only (`http://localhost:3002`) |
| `bun run dev:server` | Start Hono backend server only (`http://localhost:3000`) |
| `bun run check-types` | Run strict TypeScript checks across all apps & packages |
| `bun run build` | Build production bundles across all packages |
| `bun run kill-dev` | Force kill dev servers running on ports 3000, 3001, 3002, 8080 |

---

## 4. Database Operations (Drizzle ORM)

```bash
bun run db:local     # Start local SQLite/Turso server
bun run db:push      # Push Drizzle schema changes directly to local database
bun run db:studio    # Open Drizzle Studio database GUI in browser
```

---

## 5. Adding Shared UI Components (`@sharity/ui`)

All shared React UI primitives live in `packages/ui`. To add new shadcn/ui components to `@sharity/ui`:

```bash
npx shadcn@latest add dialog popover sheet table tabs -c packages/ui
```

To use components in frontend web apps:
```tsx
import { Button } from "@sharity/ui/components/button";
import { Dialog } from "@sharity/ui/components/dialog";
```
