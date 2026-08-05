# Sharity — Public Ledger & Escrow Model Specification

> **Feature Specification**  
> Companion to [Database Schema](file:///Users/shrid/sharity/apps/docs/architecture/database_schema.md) and [Trust & Verification Spec](file:///Users/shrid/sharity/apps/docs/features/trust_and_verification.md)

---

## 1. Overview

The **Public Ledger** turns complex financial movements into an auditable, human-readable timeline displayed directly on every project detail page.

It answers three fundamental contributor questions:
- *Where is my money right now?*
- *Has this milestone's work been verified?*
- *When were funds released to the creator?*

---

## 2. Ledger Event Lifecycle

```text
1. Contribution Received  ──> Funds committed & held for Project X
2. Milestone Submitted     ──> Creator posts proof for Stage 1 (₹30,000)
3. Milestone Approved      ──> Moderator verifies proof; releases Stage 1 funds
4. Outcome Recorded        ──> Milestone marked completed; Stage 2 unlocks
```

---

## 3. Auditable Event Types

| Event Type | Public Description Format | Financial State |
|---|---|---|
| `contribution_received` | "Asha contributed ₹1,000 to this project" | Funds held in escrow |
| `funds_held` | "₹30,000 assigned to Milestone 1: Materials Purchase" | Allocated to stage target |
| `milestone_submitted` | "Creator uploaded proof for Milestone 1" | Under review |
| `milestone_approved` | "Milestone 1 proof verified by Sharity Team" | Stage verified |
| `funds_released` | "₹30,000 released to creator for Milestone 1" | Funds transferred |
| `refund_issued` | "₹500 unallocated balance refunded to Contributor" | Returned to user |
| `project_completed` | "Project completed! Final Impact Report generated" | Finalized |

---

## 4. Unallocated Funds & Failure Redirection Options

If a project cannot be completed or is cancelled:
- Spent funds tied to approved milestones are documented in the audit report.
- Unreleased remaining contributor funds offer the user three choices in their dashboard (`/my-sharity/contributions`):
  1. **Direct Refund:** Refund back to original payment method.
  2. **Redirect Contribution:** Reallocate balance to another verified project in the same city or category.
  3. **Community Pool (Future):** Allocate balance to local emergency micro-grant pool.
