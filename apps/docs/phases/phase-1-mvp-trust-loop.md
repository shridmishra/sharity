# Phase 1 — Core MVP Launch (Validate the Trust Loop)

> **Status:** 🔄 Active Implementation  
> **Goal:** Prove that a small, verified Impact Project can move cleanly from proposal to milestone funding, evidence verification, and completed Impact Report.

---

## 1. Feature Deliverables by Priority Order

To build Phase 1 efficiently, deliverables are ordered strictly by technical dependencies:

```text
Priority 1: Auth & Profiles  ──>  Priority 2: Project & Needs Engine  ──>  Priority 3: Review & Discovery
                                                                                    │
                                                                                    ▼
Priority 5: Impact Reports  <──  Priority 4: Milestones, Escrow & Ledger
```

---

## 2. Detailed Deliverables & Checklists

### Priority 1: Auth & User Profiles
- [x] Email/password sign-up and sign-in flows (Better-Auth).
- [x] Session context propagation across Hono & tRPC context.
- [ ] User Profile setup page (`/my-sharity/profile`).
- [ ] Account Privacy toggles (anonymous contributions option).
- [ ] Public Impact Portfolio view showing projects supported and outcomes achieved.

### Priority 2: Impact Project Creation & Needs Engine
- [ ] Multi-step Project Proposal creation wizard (`/projects/create`).
- [ ] Project metadata capture (title, summary, problem statement, location, category, cover media).
- [ ] Multi-Modal Needs Engine:
  - [ ] Financial Need target & payment breakdown.
  - [ ] Item / Material Need target & quantity unit (e.g. 50 books).
  - [ ] Volunteer Need target & roles (e.g. 10 volunteers).
  - [ ] Skill Need target (e.g. 1 carpenter, 1 photographer).
- [ ] Milestone Budget Builder (splitting financial target into stages with expected proof).

### Priority 3: Proposal Review & Discovery Engine
- [ ] Pre-submission budget and required field validation.
- [ ] Admin Review Queue UI (`/admin/reviews`) for platform moderators.
- [ ] Proposal decision actions (Approve, Request Changes, Reject).
- [ ] Explore Page (`/explore`) with category filters, status badges, and search.
- [ ] Interactive Impact Map (`/map`) rendering location pins with list fallback.

### Priority 4: Milestones, Escrow & Public Ledger
- [ ] Project Detail View (`/projects/[id]`) with health status and needs progress bars.
- [ ] One-time monetary contribution checkout interface.
- [ ] Human-readable **Public Ledger** timeline recording auditable events (Contribution received, Funds held, Milestone approved, Released).
- [ ] Milestone Evidence Upload interface for project creators (photos, receipts, proof notes).
- [ ] Admin Milestone Verification Queue (`/admin/milestones`) to review proof and release funds.
- [ ] Failure handling & refund/redirection options for cancelled projects (`/my-sharity/contributions`).

### Priority 5: Impact Reports & Completed Stories
- [ ] Automated generation of permanent public Impact Report page upon final milestone approval.
- [ ] Completed Stories gallery (`/stories`) showcasing before/after evidence and community outcome summaries.

---

## 3. Phase 1 Definition of Done

Phase 1 is complete when:
1. A creator can submit a project proposal with financial, volunteer, and item needs.
2. An admin can review and approve the proposal into a live project.
3. A contributor can fund the project, viewing their money recorded on the Public Ledger timeline.
4. The creator can upload milestone evidence, an admin can approve it to release funds, and a final Impact Report is published.
