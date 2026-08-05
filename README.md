# Sharity

> **India-first Community Impact Platform**  
> Turning local intent into verified real-world outcomes through transparency, collaboration, and trust.

---

## 📚 Documentation & Roadmap Hub

All product specifications, engineering architecture diagrams, database schemas, and execution roadmaps are maintained inside the [`apps/docs`](file:///Users/shrid/sharity/apps/docs/README.md) workspace:

- 📘 **[Master Product Blueprint](file:///Users/shrid/sharity/apps/docs/Sharity_Master_Document.md)** — Foundational product strategy, personas, principles, and lifecycle.
- 🚀 **[Phases & Feature Checklist Roadmap](file:///Users/shrid/sharity/apps/docs/phases.md)** — Interactive status checklist tracking Phase 0 (Infrastructure), Phase 1 (MVP Trust Loop), Phase 2 (Local Growth), Phase 3 (Scaling), and Future Sandbox Features.
- 🏗️ **[System Architecture](file:///Users/shrid/sharity/apps/docs/architecture/system_architecture.md)** — Monorepo design, Hono server setup, tRPC context, and `@sharity/ui` design system.
- 🗄️ **[Database Schema Blueprint](file:///Users/shrid/sharity/apps/docs/architecture/database_schema.md)** — Drizzle ORM / Turso relational schema for projects, needs, milestones, public ledger, and evidence.
- 💻 **[Developer Workflow Guide](file:///Users/shrid/sharity/apps/docs/guides/development_guide.md)** — Installation, environment setup, `shar` CLI commands, and database migration guide.

---

## 🛠️ Technology Stack

- **Monorepo Engine:** Turborepo, Bun
- **Frontend Applications:** Next.js 15+ (App Router), React, Tailwind CSS
- **Shared UI Library:** `@sharity/ui` (shadcn/ui component primitives)
- **Backend API:** Hono (`apps/server` running on port `3000`)
- **API Type Safety:** tRPC (`packages/api`) with Zod validation
- **Database & ORM:** Drizzle ORM (`packages/db`), libSQL / SQLite / Turso DB (`@libsql/client`)
- **Authentication:** Better-Auth (`packages/auth`) with Drizzle SQLite adapter
- **Environment Validation:** `@t3-oss/env-core` (`packages/env`)

---

## 🚀 Quick Start & CLI Tools

### 1. Install Dependencies

```bash
bun install
```

### 2. Global `shar` CLI Commands

Sharity includes a custom helper CLI to streamline local development:

```bash
shar         # Sync database schema, run type checks, and launch dev servers (server, web, landing)
shar kill    # Terminate all running dev servers on ports 3000, 3001, 3002, 8080
shar push    # Apply Drizzle database schema migrations (bun run db:push)
shar check   # Run TypeScript type checks across all apps (bun run check-types)
shar local   # Start local Turso/SQLite database server (bun run db:local)
```

### 3. NPM Script Shortcuts

- **Start all dev apps:** `bun run dev`
- **Start Web app only (`:3001`):** `bun run dev:web`
- **Start Landing app only (`:3002`):** `bun run dev:landing`
- **Start Backend API server (`:3000`):** `bun run dev:server`
- **Run Type Checks:** `bun run check-types`
- **Open Drizzle Studio (Database GUI):** `bun run db:studio`

---

## 📁 Repository Structure

```text
sharity/
├── apps/
│   ├── web/           # Next.js web application (port 3001)
│   ├── landing/       # Next.js landing page application (port 3002)
│   ├── server/        # Hono backend API server & tRPC handler (port 3000)
│   └── docs/          # Product strategy, architecture & roadmap documentation
├── packages/
│   ├── api/           # tRPC routers & context definition
│   ├── auth/          # Better-Auth server configuration & Drizzle adapter
│   ├── db/            # Drizzle ORM schemas, db client, & drizzle.config.ts
│   ├── env/           # Type-safe environment variable validation
│   └── ui/            # Shared shadcn/ui components & global CSS tokens
```

---

## 🎨 UI Customization & Component Library

React web applications in this monorepo share shadcn/ui primitives via `@sharity/ui` (`packages/ui`).

- Modify design tokens and global styles in `packages/ui/src/styles/globals.css`.
- Add new shared primitives from project root:
  ```bash
  npx shadcn@latest add accordion dialog popover sheet table -c packages/ui
  ```
- Import components into Next.js pages:
  ```tsx
  import { Button } from "@sharity/ui/components/button";
  ```
