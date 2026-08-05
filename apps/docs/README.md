# Sharity Documentation Hub

Welcome to the central documentation suite for **Sharity** — a community impact platform built for turning local intent into verified real-world outcomes.

---

## 📚 Documentation Index

### Core Product & Roadmap
- 📘 **[Master Product Blueprint](file:///Users/shrid/sharity/apps/docs/Sharity_Master_Document.md)** — Foundational strategy, positioning, user personas, product principles, and end-to-end vision for Sharity (India-first, web-first).
- 🚀 **[Master Phase Roadmap & Prioritization](file:///Users/shrid/sharity/apps/docs/phases.md)** — Master roadmap overview and strategic phase build order matrix.

---

### Modular Phase Specifications Directory (`/phases`)
- 🟢 **[Phase 0: Infrastructure & Core Foundation](file:///Users/shrid/sharity/apps/docs/phases/phase-0-infrastructure.md)** — Monorepo setup, Bun, Turborepo, Next.js 15, Hono, tRPC, Drizzle ORM, Turso DB, Better-Auth, and `@sharity/ui`. *(✅ Completed)*
- 🟡 **[Phase 1: Core MVP Launch (Trust Loop)](file:///Users/shrid/sharity/apps/docs/phases/phase-1-mvp-trust-loop.md)** — Core MVP deliverables ordered by build priority: Auth, Project & Needs Creation, Review Queue, Explore/Map, Public Ledger, Evidence Verification, and Impact Reports. *(🔄 Active Implementation)*
- 🔵 **[Phase 2: Regional Growth & Local Networks](file:///Users/shrid/sharity/apps/docs/phases/phase-2-local-networks.md)** — Trusted Community Reviewers, City & Neighborhood Hubs, Recurring Support, Material Fulfillment, and NGO Portals. *(📋 Planned)*
- 🟣 **[Phase 3: National Scaling & Governance](file:///Users/shrid/sharity/apps/docs/phases/phase-3-national-scaling.md)** — Reputation Governance, CSR Impact Matching, Multilingual Support, and Open Impact Data API. *(📋 Planned)*
- 💡 **[Future Sandbox & Feature Backlog](file:///Users/shrid/sharity/apps/docs/phases/future-backlog.md)** — Emergency fast-track, AI evidence pre-checks, and offline mobile app capabilities. *(💡 Sandbox)*

---

### Technical Architecture (`/architecture`)
- 🏗️ **[System Architecture Specifications](file:///Users/shrid/sharity/apps/docs/architecture/system_architecture.md)** — Monorepo layout, package dependency graph, request lifecycles, Hono server routing, tRPC context flow, and performance strategy.
- 🗄️ **[Relational Database Schema](file:///Users/shrid/sharity/apps/docs/architecture/database_schema.md)** — Deep Drizzle ORM / Turso SQLite schema specifications, ER diagrams, foreign key constraints, indexes, and column types.
- 🔌 **[API Design & Router Specs](file:///Users/shrid/sharity/apps/docs/architecture/api_design.md)** — Comprehensive specification of tRPC procedure routers (`project`, `milestone`, `contribution`, `admin`), Zod schemas, authorization wrappers, and error codes.

---

### Feature Specifications (`/features`)
- 🎯 **[Impact Projects & Needs Engine](file:///Users/shrid/sharity/apps/docs/features/impact_projects.md)** — Needs Engine classification (Money, Items, Volunteers, Skills), project lifecycle state machine, and Project Health Score computation.
- 🛡️ **[Trust & Verification Operations](file:///Users/shrid/sharity/apps/docs/features/trust_and_verification.md)** — Manual review workflows, milestone evidence standards (photos, receipts, proof of work), and moderation queue logic.
- 📜 **[Public Ledger & Escrow Model](file:///Users/shrid/sharity/apps/docs/features/public_ledger.md)** — Auditable human-readable event ledger specification tracking contribution allocations, held milestone funds, approved releases, and refund choices.

---

### Developer & Admin Guides (`/guides`)
- 💻 **[Development & Workflow Guide](file:///Users/shrid/sharity/apps/docs/guides/development_guide.md)** — Developer setup guide, environment configuration, `shar` CLI commands, database migrations, and UI component usage.
- 🛠️ **[Admin Operations SOP](file:///Users/shrid/sharity/apps/docs/guides/admin_operations.md)** — Standard Operating Procedures for platform moderators handling project reviews, milestone evidence approvals, community flags, and exception handling.

---

## 📁 Directory Layout

```text
apps/docs/
├── README.md                          # Documentation Hub & Navigation Index
├── Sharity_Master_Document.md         # Master Product Blueprint
├── phases.md                          # Master Roadmap & Phase Prioritization Matrix
├── phases/                            # Modular Phase Specifications Directory
│   ├── README.md                      # Index for Phase Specifications
│   ├── phase-0-infrastructure.md      # Completed Phase 0 Specification
│   ├── phase-1-mvp-trust-loop.md      # Active Phase 1 Core MVP Specification
│   ├── phase-2-local-networks.md      # Planned Phase 2 Specification
│   ├── phase-3-national-scaling.md    # Planned Phase 3 Specification
│   └── future-backlog.md              # Future Sandbox Feature Backlog
├── architecture/
│   ├── system_architecture.md         # Monorepo, Data Flow & Build Priorities
│   ├── database_schema.md             # Drizzle Schema & Relational Models
│   └── api_design.md                  # tRPC Procedure Routers & Zod Specs
├── features/
│   ├── impact_projects.md             # Project Lifecycle & Needs Classification
│   ├── trust_and_verification.md      # Moderation, Reviews & Milestone Proof
│   └── public_ledger.md               # Auditable Financial Ledger & Escrow Spec
└── guides/
    ├── development_guide.md           # Developer CLI, Bun & Migration Workflow
    └── admin_operations.md            # Operations SOP for Reviewers & Ops Team
```
