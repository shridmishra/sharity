# Sharity — Admin Operations & Reviewer SOP

> **Standard Operating Procedures for Reviewers & Platform Moderation**  
> Companion to [Trust & Verification Spec](file:///Users/shrid/sharity/apps/docs/features/trust_and_verification.md) and [Phases Roadmap](file:///Users/shrid/sharity/apps/docs/phases.md)

---

## 1. Overview

This document details the Standard Operating Procedures (SOP) for Sharity administrators, reviewers, and operational staff managing project proposals, milestone evidence verification, community flags, and exception handling.

---

## 2. Reviewer Operations Dashboard

Admin operators access queues via `/admin`:
- `/admin/reviews` — New Impact Project submissions awaiting review.
- `/admin/milestones` — Submitted milestone evidence pending validation.
- `/admin/flags` — Triaging user-submitted safety or content flags.

---

## 3. Project Proposal Review SOP (`/admin/reviews`)

1. **Verify Creator Identity:** Confirm name, email verification, and contact phone number.
2. **Review Budget Math:** Ensure `totalFinancialTarget` equals the sum of all milestone `budgetAllocation` amounts.
3. **Assess Feasibility:** Check if the problem statement, desired outcome, and location are realistic and clear.
4. **Action Selection:**
   - **Approve:** Project transitions to `'approved'` / `'live'`.
   - **Request Changes:** Send notes to creator detailing required fixes (e.g., breakdown milestone 2 budget further).
   - **Reject:** Reject proposals violating community safety or ethical guidelines.

---

## 4. Milestone Evidence Verification SOP (`/admin/milestones`)

1. **Inspect Submitted Evidence:** Open uploaded photos, receipts, or invoices.
2. **Check Criteria:** Verify photo matches the target location and expected milestone result.
3. **Action Selection:**
   - **Approve Milestone:** Triggers fund release for approved amount, updates project milestone status, and posts an event to the Public Ledger.
   - **Request Clarification:** Ask creator for clearer receipts or additional before/after photos.
