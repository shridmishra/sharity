# AGENTS.md

## Project Overview

**Sharity** is a modern, type-safe full-stack web application built as a monorepo. It features a Next.js App Router frontend, a Hono API server with tRPC end-to-end type safety, a SQLite/Turso database managed with Drizzle ORM, and Better-Auth authentication.

### Key Technologies
- **Monorepo Tooling**: Turborepo, Bun
- **Frontend**: Next.js 15+, React, Tailwind CSS, `@sharity/ui` (shadcn/ui primitives), `@tanstack/react-query`
- **Backend API**: Hono (`apps/server`), tRPC (`packages/api`)
- **Database & ORM**: Drizzle ORM (`packages/db`), libSQL / SQLite / Turso (`@libsql/client`)
- **Authentication**: Better-Auth (`packages/auth`) with Drizzle SQLite adapter
- **Environment Validation**: `@t3-oss/env-core` (`packages/env`)

---

## Setup Commands

- **Install dependencies**:
  ```bash
  bun install
  ```
- **Database local server (SQLite/Turso)**:
  ```bash
  bun run db:local
  ```
- **Apply schema / Push database migrations**:
  ```bash
  bun run db:push
  ```
- **Open Drizzle Studio (Database GUI)**:
  ```bash
  bun run db:studio
  ```

---

## Development Workflow

- **Start all applications (Web + Server)**:
  ```bash
  bun run dev
  ```
- **Start Next.js frontend only** (`http://localhost:3001`):
  ```bash
  bun run dev:web
  ```
- **Start Landing web application only** (`http://localhost:3002`):
  ```bash
  bun run dev:landing
  ```
- **Start Hono backend server only** (`http://localhost:3000`):
  ```bash
  bun run dev:server
  ```
- **Environment variables**:
  - `apps/server/.env` contains `DATABASE_URL`, `BETTER_AUTH_SECRET`, `BETTER_AUTH_URL`, and `CORS_ORIGIN`.

---

## Monorepo Instructions

```
sharity/
├── apps/
│   ├── web/                     # Next.js web application (port 3001)
│   ├── landing/                 # Next.js landing page application (port 3002)
│   └── server/                  # Hono backend API server (port 3000)
│       └── src/index.ts         # Server entrypoint (CORS, auth handler, tRPC endpoint)
├── packages/
│   ├── api/                     # Type-safe tRPC routers & context definition
│   ├── auth/                    # Better-Auth server configuration & Drizzle adapter
│   ├── db/                      # Drizzle ORM schemas, db client, & drizzle.config.ts
│   ├── env/                     # Type-safe environment variable validation (server & web)
│   └── ui/                      # Shared shadcn/ui components & global CSS tokens
```

- When adding dependencies to a workspace package:
  ```bash
  bun add <package_name> --filter <workspace_name>
  ```

---

## Code Style & Guidelines

- **TypeScript**: Strict type checking. Always run `bun run check-types` before merging or finishing tasks.
- **UI Primitives**: Prefer using shared primitives from `@sharity/ui` ([packages/ui](file:///Users/shrid/sharity/packages/ui)) over custom HTML elements to ensure design consistency.
- **Design Tokens**: Global CSS variables and styles reside in [packages/ui/src/styles/globals.css](file:///Users/shrid/sharity/packages/ui/src/styles/globals.css).
- **API Safety**: Maintain type safety using tRPC procedures (`packages/api/src/routers/`) and Zod validation.

---

## Testing & Type Checking

- **Run TypeScript checks across all packages**:
  ```bash
  bun run check-types
  ```

---

## Build and Deployment

- **Build production bundles for all packages**:
  ```bash
  bun run build
  ```

---

## Pull Request Guidelines

- Ensure `bun run check-types` passes with zero errors.
- Never commit binary `.db` files (`local.db`, `*.db-wal`, `*.db-shm`) or `.env` files with production secrets.
