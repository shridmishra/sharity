# Sharity — Trust, Verification & Moderation Operations

> **Feature Specification & Governance Blueprint**  
> Companion to [Master Product Blueprint](file:///Users/shrid/sharity/apps/docs/Sharity_Master_Document.md) and [Admin Operations SOP](file:///Users/shrid/sharity/apps/docs/guides/admin_operations.md)

---

## 1. Trust Principles

Trust is Sharity’s core product differentiator. To eliminate the "donation black box", Sharity enforces:
1. **Upfront Review:** Money-funded projects are verified before publishing.
2. **Milestone Evidence Gate:** Funds for stage $N+1$ are held until stage $N$ evidence is approved.
3. **Public Auditability:** All approvals, evidence uploads, and release events are recorded on the public timeline.

---

## 2. Verification Workflows

### 2.1 Initial Proposal Verification (`/admin/reviews`)
When a creator submits an Impact Project, platform moderators inspect:
- **Creator Identity / Org Credibility:** Government ID, organization registration, or local verifier reference.
- **Problem & Solution Feasibility:** Is the proposed outcome realistic for the location and budget?
- **Budget Math & Milestone Breakdown:** Are stage allocations logical and supported by quotes/invoices where applicable?

### 2.2 Milestone Evidence Review (`/admin/milestones`)
Before funds allocated to a milestone are released to the creator:
1. Creator uploads evidence: photos (with EXIF location data where available), video updates, vendor receipts, or invoices.
2. Moderator cross-references submitted proof against the agreed milestone target.
3. Moderator actions:
   - **Approve:** Authorizes fund release; advances project to next stage; records public ledger event.
   - **Request Revision:** Asks creator for clearer photos or missing receipt details.
   - **Reject / Hold:** Pauses milestone release if evidence is fraudulent or inadequate.

---

## 3. Flagging & Community Moderation

- Any community member can flag a project or update for:
  - Suspicious financial activity or missing proof.
  - Misleading project details or location errors.
  - Inappropriate content or privacy violations.
- Flagged items enter the **Admin Flag Queue** for triage within 24 hours.
