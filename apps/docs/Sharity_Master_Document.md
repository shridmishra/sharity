# Sharity Master Document

> **Internal Product Blueprint · v1.0 · India-first · Web-first**  
> A concise product direction for turning community intent into verified real-world impact.

---

## 1. Executive Summary

**Sharity is a community impact platform where people identify local problems, gather the right kinds of support, fund solutions transparently, verify progress, and celebrate completed impact together.**

It is not simply a donation website. It is a shared operating layer for local action. A person can propose a safer playground, stock a community library, fund animal rescue equipment, repair a public amenity, organise a cleanup, or respond to a verified local need. Others can contribute money, time, skills, materials, verification, or awareness.

The product’s differentiator is a trust loop: money-funded Impact Projects are reviewed before funding, funds are held and released against visible milestones, progress evidence is public, and completed work becomes a lasting Impact Report. The goal is to make contributing feel less like sending money into a black box and more like helping build something real.

**Launch posture**

- India only, beginning with a small number of communities or cities.
- Responsive web product first; mobile-native apps follow only after the core loop works.
- Sharity manages project review and milestone approval in the early stages.
- Funds are treated as milestone-bound, with contributor choice when projects cannot continue.
- The language of the platform is inclusive: users **contribute** rather than only donate; projects are **Impact Projects**, not campaigns.

**The product thesis:** community willingness is abundant; confidence that a contribution will become real impact is not. Sharity is designed to close that confidence gap.

---

## 2. Vision, Mission, and Positioning

### Mission

> Empower communities to transform ideas into verified real-world impact through transparency, collaboration, and trust.

### Long-term vision

Improving one’s community should be as easy as posting online. Instead of an endless feed of passive content, people should be able to discover a nearby problem, see a credible solution, take a useful action, and watch the result unfold.

Over time, Sharity can become a living map of community action across India: neighbourhoods, towns, and cities represented not by abstract statistics but by visible projects, verified outcomes, and the people who made them happen.

### Positioning

| Sharity is | Sharity is not |
|---|---|
| A platform for collective action | A generic crowdfunding clone |
| An impact record with public proof | A donation black box |
| A place to contribute money, time, skills, and trust | A money-only charity app |
| A positive social experience built around outcomes | A popularity contest |
| A system that helps communities act locally | A replacement for NGOs, government, or local groups |

### Elevator pitch

> Sharity helps communities turn local problems into verified Impact Projects—supported through money, time, skills, and awareness; delivered through transparent milestones; and remembered through measurable outcomes.

---

## 3. The Problem

People routinely see needs around them: a broken public facility, children without school supplies, a stray-animal rescue need, a neglected park, a community space that could be made usable, or an urgent local hardship. Most people want to help. Yet intent rarely becomes coordinated action.

### What breaks today

1. **Trust is fragmented.** Contributors cannot easily tell whether a request is genuine, whether funds are used as promised, or whether work was completed.
2. **Support is narrowly defined.** Many people cannot give money but can offer time, skills, materials, or local knowledge.
3. **Progress disappears after payment.** Conventional donation flows offer little evidence between contribution and final outcome.
4. **Local needs are hard to discover.** Useful opportunities to help are buried in chats, social feeds, and informal networks.
5. **Good work has weak memory.** Communities lose the story, proof, and momentum of projects once they are completed.
6. **Small organisers lack infrastructure.** A credible project needs discovery, coordination, evidence collection, payments, updates, and accountability—too much for an individual to assemble alone.

### Core user questions Sharity must answer

- Is this real?
- Who is responsible?
- What exactly is needed?
- Where does my money go?
- What happens if the project stops?
- Can I help without spending money?
- Did this actually improve anything?

If Sharity cannot answer these clearly on every money-funded project, it has not earned the contribution.

---

## 4. The Solution and Product Model

Sharity gives every Impact Project a clear public structure:

1. **A local problem and proposed outcome**
2. **Specific needs**: money, items, volunteers, skills, or awareness
3. **A review path** appropriate to the type of project
4. **A plan made of milestones** for projects involving funds
5. **Visible updates and evidence** as the work progresses
6. **Verification before the next release of funds**
7. **A permanent Impact Report** after completion or closure

### The four product pillars

| Pillar | Product promise |
|---|---|
| Discover problems | Make credible local needs easy to find and understand. |
| Mobilise community | Let people contribute in the form they can offer. |
| Verify progress | Make evidence and milestone status visible before more funds move. |
| Celebrate success | Turn completed work into a shared story and reusable trust. |

### Three ways to help

- **Contribute money** for a verified, milestone-based need.
- **Volunteer time or skills** such as painting, teaching, carpentry, photography, legal support, or on-site help.
- **Spread the word** by following, sharing, and bringing in people or resources.

In later phases, material contributions and formal verification participation can become equally first-class modes.

### Needs before money

An Impact Project should begin by stating what it needs, not merely how much it wants to raise. A community library project, for example, may need ₹40,000, 50 books, 12 volunteers, a carpenter, and two painters. Sharity should display progress for every relevant need so a person can contribute the most useful thing they have.

Project pages can also support follows, carefully moderated comments, and structured suggestions. These are tools for practical coordination and clarity—not an invitation to recreate a general-purpose social network.

---

## 5. Target Users and Personas

### Primary audiences

| Audience | Need | What Sharity gives them |
|---|---|---|
| Community members | A credible way to make a difference nearby | Discovery, clear actions, visible outcomes |
| Project creators | A way to rally and manage support | Structured project creation, needs, updates, credibility |
| Volunteers and skilled contributors | Meaningful opportunities to help | Relevant local roles and recognition |
| Local groups and NGOs | Transparency and a wider supporter base | Project infrastructure and public trust signals |
| Sharity reviewers | Tools to keep the ecosystem credible | Review queues, evidence, flags, and decisions |

### Core personas

#### 1. Asha — the local contributor

Asha, 28, works in Pune and wants to contribute ₹300–₹1,000 a month to causes she can understand. She has been disappointed by vague fundraising requests online. She wants proof, concise updates, and a choice to support projects near her or in categories she cares about.

**Success for Asha:** “I know what my contribution helped accomplish, and I would confidently support this again.”

#### 2. Rohan — the community organiser

Rohan, 34, wants to improve a shared community library. He can coordinate local volunteers but needs ₹60,000, books, and a carpenter. He needs a credible public page, a way to set realistic milestones, and a respectful review process—not a complex fundraising tool.

**Success for Rohan:** “I can turn a real local plan into a transparent project people want to join.”

#### 3. Meera — the skilled volunteer

Meera, 25, is a designer who wants to offer a few hours each month. She is willing to help projects with posters, social content, or event materials, but needs clarity about expectations and safety.

**Success for Meera:** “I can find useful work, commit with confidence, and see that my skill mattered.”

#### 4. Farhan — the trusted verifier (future role)

Farhan has a strong track record in the community. He wants to help review on-ground evidence for nearby projects. He needs clear criteria, a limited scope of responsibility, and a reputation system that rewards careful judgment rather than popularity.

**Success for Farhan:** “My verification makes the platform more trustworthy without putting me in an impossible position.”

---

## 6. Product Principles

These principles are the decision filter for every feature and design choice.

1. **Transparency by default.** Every funded project should show what is needed, what was approved, what has happened, and what remains.
2. **Impact over popularity.** Visibility may help a project, but meaningful completion is the product’s true reward.
3. **Community before platform.** Sharity enables action; the people closest to the need create the impact.
4. **Verification builds trust.** Claims without appropriate proof cannot unlock the next stage of a funded project.
5. **Contributions are plural.** Money matters, but so do time, skills, materials, and amplification.
6. **Simple enough to act.** A first-time user should understand a project and take one helpful action within a minute.
7. **Dignity and safety matter.** Especially in individual assistance, healthcare, and emergency contexts, visibility must never come at the cost of dignity.
8. **Optimism must be earned.** The product should feel hopeful because it shows real action and honest status—not because it hides setbacks.

---

## 7. End-to-End User Journey

### The contributor journey

```text
Discover → Understand → Trust → Contribute → Follow → See progress → Verify outcome → Share / return
```

1. A user finds an Impact Project via Explore, a local feed, a category, a shared link, or the Impact Map.
2. They quickly see the problem, the desired outcome, the needs, project health, creators, and current milestone.
3. They choose a contribution: funds, volunteering, skills, materials, or sharing.
4. If they contribute funds, they see the milestone plan and the project’s funding/escrow status before confirming.
5. They receive only meaningful updates: funding reached, evidence posted, milestone approved, project completed, or an issue requiring a choice.
6. At completion, they receive the Impact Report and can reflect that impact in their personal portfolio.

### The creator journey

```text
Propose → Review → Publish → Mobilise → Deliver → Evidence → Verify → Complete / close
```

1. A creator chooses a project type and explains the local need.
2. They define an outcome, location, beneficiaries, needs, and—when money is involved—budget and milestones.
3. Sharity reviews the project and requests clarification or evidence if needed.
4. Once published, the creator gathers the right contributions and posts transparent updates.
5. After each milestone, the creator submits evidence for review.
6. Approved milestones unlock the next agreed release; the project finishes with an Impact Report.

### Project status language

`Draft → Under Review → Approved → Live → Funded / In Progress → Milestone Review → Completed`

Alternative endings must be clear and non-punitive: `Paused`, `Needs Attention`, `Closed`, or `Cancelled with contributor options`.

---

## 8. Information Architecture: Sitemap and Navigation

### Public website

```text
Home
├── Explore Impact Projects
│   ├── Impact Map
│   ├── Categories
│   ├── Near Me
│   ├── Emergencies
│   └── Search Results
├── Impact Project Detail
├── Community / Location Pages
├── Stories (completed Impact Reports)
├── How It Works
├── Trust & Safety
├── About Sharity
└── Sign in / Create account
```

### Signed-in workspace

```text
My Sharity
├── Overview
├── My Contributions
├── Saved & Following
├── Volunteer Commitments
├── My Impact Projects
├── Create an Impact Project
├── Notifications
├── Public Profile / Impact Portfolio
└── Settings
```

### Operations workspace

```text
Admin
├── Review Queue
├── Milestone Verification Queue
├── Flags & Incidents
├── Project Management
├── Users & Reputation
├── Refund / Redirection Cases
├── Content & Categories
└── Metrics Dashboard
```

### Primary navigation

For visitors: **Explore**, **Impact Map**, **How It Works**, **Stories**, and a persistent **Create Impact Project** action.

For signed-in users: **Home**, **Explore**, **Create**, **My Sharity**, and **Notifications**. On mobile, these become a compact bottom navigation with a visually prominent Create action.

The structure should prioritise discovery and action over dense account management.

---

## 9. Public Website Pages

### Home

The home page is a promise and a path to action—not a corporate brochure.

**Core sections**

- Clear statement: turn local problems into verified impact.
- Primary paths: Explore projects, see the map, create a project.
- Featured nearby or timely Impact Projects.
- “How Sharity works” in four steps: propose, support, verify, celebrate.
- Category entry points: Education, Environment, Healthcare, Animal Welfare, Public Infrastructure, Community, Food & Hunger, Accessibility, Arts & Culture, Disaster Relief.
- Trust section explaining reviews, milestones, and public updates.
- Completed impact stories with before/after evidence.
- Lightweight aggregate impact figures once genuine data exists.

Avoid invented social proof or inflated counters before launch.

### Explore

Explore is the product’s discovery engine. It should offer calm, useful filters rather than an overwhelming feed.

**Filters:** location, category, type of help needed, project status, urgency, verified status, and accessibility needs.  
**Cards should show:** title, location, outcome, category, key need, funding/volunteer progress, current status, health signal, and a meaningful image.

### Impact Map

The map makes local action tangible. Pins can represent active projects, completed projects, urgent needs, and projects seeking volunteers. Project cover imagery should be location-aware and authentic wherever possible. It should be useful even before the platform has national density: begin city-first, show clustered results, and always provide a list alternative for accessibility and low-bandwidth contexts.

### Impact Project Detail

This is the core trust page. It should answer the user’s questions without requiring them to hunt.

**Sections**

- The problem, desired outcome, location, and category
- Creator and review status
- Specific needs: funds, items, roles, skills
- Progress and Project Health
- Milestones, budget allocation, and current funding state
- Public activity timeline
- Updates, before/during/after photos, video where useful, and receipts or invoices where appropriate
- Contributors and volunteers, respecting chosen visibility
- Comments or structured community questions (moderated)
- Contribution actions and share controls

### Stories / Completed Projects

Stories collect completed Impact Reports. They prove the platform’s value, inspire future projects, and provide a durable record of local improvement. Each story should include the original goal, contribution mix, evidence, outcome, beneficiaries where appropriate, lessons, and acknowledgement of the community.

### How It Works and Trust & Safety

These pages explain the platform in plain language: who can create projects, when review is required, how funded projects use milestones, what proof is expected, how reports/flags work, and what happens if a project cannot proceed. They should not make legal claims beyond what the operation can uphold.

---

## 10. Dashboard Pages

### My Sharity Overview

A personal, motivating overview—not a finance dashboard. It shows current contribution activity, projects followed, volunteer commitments, active projects created, recent updates, and a compact lifetime impact summary.

### My Contributions

Users can see every monetary contribution and its state: committed, held for a project, allocated to an approved milestone, refunded, redirected, or complete. Each record links back to the project timeline and public ledger.

### Saved and Following

This is the user’s shortlist of projects they are considering or want to track. It supports reminders and quiet re-engagement without pressuring them to contribute.

### Volunteer Commitments

Shows roles applied for, confirmed commitments, schedules or instructions where relevant, contribution history, and project-specific contacts only when appropriate. Phase 1 should keep coordination intentionally simple.

### My Impact Projects

For creators, this is an action-oriented workspace: project status, review feedback, funding/needs progress, upcoming milestone requirements, pending evidence, and contributor activity. It should help a creator act on the next step rather than display every possible metric.

### Create an Impact Project

Use a guided, saveable flow:

1. Choose type and category.
2. Describe the problem and desired outcome.
3. Add location and beneficiaries.
4. Define needs: money, items, people, skills.
5. Add budget and milestone plan if funding is requested.
6. Provide identity/organisation information and supporting evidence as required.
7. Review and submit for approval.

The form must explain why each trust-sensitive field is requested. Creators should be encouraged to start with a small, achievable project.

### Public Profile and Impact Portfolio

The profile reflects a person’s contribution to real outcomes: funds contributed, volunteer time, skills offered, projects created, milestones verified (future), and completed projects supported. It should not rank personal worth. Privacy controls must let users hide amounts, identity, or activity as appropriate.

---

## 11. Core MVP Features

### Must ship in Phase 1

| Feature | MVP decision |
|---|---|
| Account and profile | Email/phone-led sign-up; basic identity and privacy controls |
| Impact Project creation | Guided proposal, needs, location, category, review submission |
| Project review | Sharity-led manual review for money-funded projects |
| Explore and search | Filterable project discovery; no complex personalisation required |
| Project detail | Needs, timeline, updates, milestones, contribution CTAs |
| Contributions | One-time monetary contributions to approved projects |
| Volunteer/skill interest | Simple roles and expression of interest / commitment |
| Milestones | Budgeted stages, creator evidence submission, moderator approval |
| Public ledger | Clear human-readable record of contribution, milestone, release, and completion events |
| Updates and evidence | Text, photos, and supporting documentation with moderation |
| Notifications | Essential project and contribution updates |
| Impact Reports | Completion/closure summary with evidence |
| Basic reputation | Project and contributor trust indicators; no gamified complexity |
| Admin operations | Review, milestone, flag, project, and exception queues |

### Explicitly out of scope for the MVP

- Native mobile apps
- Complex community governance or voting
- Open verifier marketplace
- Recurring automatic giving
- Corporate CSR tools
- International projects or multi-currency
- Blockchain, crypto, NFTs, or token rewards
- Direct messaging/chat
- AI assistants and advanced recommendation engines
- Livestreaming, marketplace functions, and creator subscriptions

Saying no to these is a product strategy, not a lack of ambition. The first proof Sharity needs is that a small number of verified projects can move cleanly from proposal to visible completion.

---

## 12. Impact Project Types and Lifecycle

### Project types at launch

| Project type | Funding | Review standard |
|---|---:|---|
| Volunteer-only action | No | Light review for safety and clarity |
| Community proposal / idea | No | Light review or moderation |
| Physical goods or local improvement | Yes | Creator/project review + milestone plan |
| Individual financial assistance | Yes | Higher standard and privacy-aware verification |
| Disaster relief | Yes | Priority review with heightened safeguards |
| NGO / organisation project | Yes | Organisation review and evidence requirements |

**Rule:** if money is involved, trust must be earned.

### The lifecycle

1. **Draft** — creator prepares the project.
2. **Under Review** — Sharity checks identity, clarity, safety, feasibility, and supporting material.
3. **Approved** — the project may go live with approved needs and milestones.
4. **Live** — community contributions and volunteer interest are gathered.
5. **Ready to start** — an agreed funding or readiness threshold is reached.
6. **In Progress** — work begins; the current milestone is visible.
7. **Milestone Review** — evidence is submitted and reviewed.
8. **Next release / continuation** — only after milestone approval, when applicable.
9. **Completed** — outcome and final report are published.
10. **Archived** — permanent public record remains accessible.

### Project Health Score

The Health Score is a readable status signal, not a black-box score. It can draw on:

- Funding and needs progress
- Recency and quality of updates
- Milestone timing
- Review/verification status
- Creator reliability from prior completed work
- Community signals such as unresolved flags

It should always explain *why* a project is healthy, needs attention, or is paused. Start with a small number of explicit statuses; avoid pretending to calculate precision that the early product does not have.

---

## 13. Funding, Milestones, and Failure Handling

### Milestone-based funding

For money-funded projects, the creator proposes a project budget split into clear stages. Each stage defines an expected result, evidence required, and a maximum amount. Sharity’s operational process reviews the project, records contributor funds against it, and authorises movement for an approved stage only when the stated conditions are met.

The public view should show simple language:

```text
Contributed → Held for this project → Milestone evidence reviewed → Amount released for approved work → Outcome recorded
```

This is a **public ledger**, not blockchain. Its value is human clarity.

The product architecture should keep the project and ledger experience separate from the specific fund-holding mechanism. This allows the Phase 1 operational model to evolve toward an appropriate licensed payments or escrow partner without redesigning the user-facing trust loop.

### Example

| Milestone | Expected result | Budget | Status |
|---|---|---:|---|
| 1 | Site preparation and materials purchased | ₹30,000 | Approved / completed |
| 2 | Core work installed | ₹40,000 | In review |
| 3 | Finishing, inspection, and handover | ₹30,000 | Not started |

### If a project cannot continue

Sharity should be direct about what has been completed, what funds were legitimately used under approved milestones, and what remains unallocated. The remaining contributor balance should offer clear choices:

1. **Refund the remaining eligible balance.**
2. **Redirect it to a similar verified Impact Project.**
3. **Leave it for a designated community fund** only in a later phase with explicit consent and clear rules.

The exact financial, payment, tax, KYC, and legal implementation must be established with qualified Indian legal and payments partners before launch. This document describes the intended user experience and fairness principle, not a regulatory determination.

### Operational principle

Completed, approved work should be recognised. Future, unreleased work should not silently consume contributor funds. Every exception should have a documented, auditable decision and a clear user notification.

---

## 14. Reputation, Badges, and Leaderboards

### Reputation system

Reputation should help users judge reliability; it should not become a vanity game.

**Signals by role**

| Role | Useful signals |
|---|---|
| Contributor | Completed projects supported, volunteer commitments honoured, helpful participation |
| Creator | Project approval quality, update reliability, milestones completed, unresolved issues |
| Organisation | Verification status, delivery history, transparency quality |
| Verifier (future) | Accurate reviews, consistency, community trust, moderation outcomes |

Reputation must be explainable, resistant to easy manipulation, and never based solely on amount spent. A person who offers twenty hours of skilled volunteering can be just as valuable as a financial contributor.

### Badges

Badges mark meaningful participation and are earned through real contribution, for example:

- First Impact
- Local Builder
- Helping Hand
- Skill Sharer
- Project Finisher
- Community Connector
- Trusted Reviewer (future)

Badges should be modest, earned, and linked to a clear explanation. Avoid artificial scarcity, streak pressure, or incentives that encourage low-quality activity.

### Leaderboards

Use leaderboards sparingly and only where they reinforce collective progress: city impact, completed projects by community, volunteer hours contributed, or category outcomes. Default presentation should celebrate communities and outcomes ahead of individual spending totals.

The better question is “What did this place accomplish?” rather than “Who gave the most?”

---

## 15. Notifications and Community Communication

Notifications should make people feel informed, not chased.

### Essential notifications

- Project submission received; review outcome or feedback
- A followed project reaches a funding or readiness milestone
- A volunteer role is confirmed, changed, or completed
- New project update or evidence posted
- Milestone submitted, approved, rejected, or requires clarification
- Project completed and Impact Report available
- Project paused, closed, or needs contributor action
- Refund/redirection choice available where relevant
- Flag/report decision where the user is directly involved

### Delivery approach

In-product notifications are the source of truth. Email can support meaningful events; push notifications belong to the future app/PWA strategy. Users should control non-essential alerts by category, location, and frequency.

### Comments and discussion

Phase 1 should favour bounded, moderated comments or questions on projects rather than open-ended social networking. The purpose is clarification, encouragement, and useful coordination—not debate for its own sake.

---

## 16. Trust, Safety, Moderation, and the Admin Panel

Trust is the product, not a background function. The early operating model must be intentionally hands-on.

### Trust and safety foundations

- Identity or organisation verification proportionate to project risk
- Higher requirements for money-funded, individual-assistance, and emergency projects
- Evidence requirements defined before a project is approved
- Clear community reporting and flagging
- Human moderation for impactful decisions
- Privacy-aware treatment of beneficiaries and sensitive images
- Transparent project status changes
- Escalation processes for suspected fraud, harm, or misuse

### Admin panel objectives

The admin panel supports consistency, speed, and a decision record—not merely back-office administration.

| Area | Core capability |
|---|---|
| Project review | Review proposals, request changes, approve/reject, set conditions |
| Milestone queue | Compare planned outcome to submitted evidence and make a recorded decision |
| Flags and incidents | Triage reports, restrict content, investigate, resolve, escalate |
| Project operations | Pause, close, correct statuses, communicate next steps |
| Contributor cases | Handle refund/redirection choices and support requests |
| Users and reputation | Review risk signals, apply restrictions, correct badges/reputation |
| Content controls | Manage categories, guidance, featured stories, and static trust content |
| Metrics | Track operational bottlenecks and ecosystem health |

### Governance progression

| Phase | Who approves milestone progress? |
|---|---|
| Phase 1 | Sharity moderators / operations team |
| Phase 2 | Trusted community reviewers recommend; Sharity retains final control |
| Phase 3 | Reputation-weighted community mechanisms with strong safeguards |

The sequencing matters: open governance before a durable trust system exists creates incentives for collusion and confusion.

---

## 17. Roadmap: Phase 1 to Phase 3

### Phase 1 — Validate the trust loop

**Goal:** prove that Sharity can take a small, credible project from proposal to visible completion.

- India-first, web-first launch
- Curated city/community rollout
- Manual review for funding projects
- One-time contributions and basic volunteer roles
- Needs, milestones, evidence, public ledger, and Impact Reports
- Explore, map/list discovery, user profiles, notifications
- Manual operations for exceptions and milestone approvals
- Small category set, prioritising projects with clear observable outcomes

**Success condition:** users understand the model, contributors follow progress, creators can complete projects, and operations can keep trust high without breaking.

### Phase 2 — Strengthen local networks

**Goal:** improve repeat participation and reduce operational bottlenecks.

- Trusted community reviewer programme
- Better location/community pages and local leaderboards
- Recurring support preferences for verified categories or locations
- Material contribution flows and richer volunteer coordination
- Organisation partnerships and stronger verification workflows
- Improved discovery/recommendations based on user preferences
- PWA enhancements and considered mobile app planning
- More robust reporting, dashboards, and project health signals

### Phase 3 — Scale accountable community action

**Goal:** expand the platform from a curated service into a trusted national network.

- Reputation-weighted participation in verification/governance with safeguards
- Wider city coverage and local partner ecosystems
- Mature verifier pathways and audit processes
- Corporate/CSR participation only if aligned with community-first incentives
- Multilingual support and accessibility expansion
- Advanced impact measurement and longitudinal stories
- Native apps where they materially improve participation

---

## 18. Future Ideas

The following ideas are promising but should wait for evidence that the core system is working:

- **Recurring support:** automatically contribute a chosen amount to verified local education, environment, or other category projects.
- **Neighbourhood communities:** city/district spaces with local feeds, volunteer networks, and shared goals.
- **Material needs marketplace:** books, equipment, supplies, and services requested and fulfilled transparently.
- **Impact map at national scale:** drill from India to state, district, city, neighbourhood, project, and completed story.
- **Community emergency fund:** opt-in redirected balances under explicit transparent governance.
- **Verifier network:** trained, scored local people who help validate evidence on-site.
- **Partner tooling:** purpose-built workflows for trusted NGOs, schools, resident groups, and civic organisations.
- **Corporate participation:** matched support or employee volunteering without letting large funders dominate project direction.
- **Open impact data:** carefully privacy-safe reporting on local impact and completion patterns.

Every future idea must pass the same test: does it make trustworthy community action meaningfully easier, or is it distraction?

---

## 19. Business Model Principles

Sharity’s revenue model must not undermine the promise of transparent impact.

### Potential revenue paths

| Model | Role | Guardrail |
|---|---|---|
| Transparent platform fee | Supports payments, review, support, and operations | Display fee and purpose clearly before contribution |
| Optional contributor support | Lets users help cover platform costs | Never make it confusing or coercive |
| Organisation tooling | Paid services for verified partner organisations | Do not create a pay-to-trust system |
| CSR / matching programmes | Later-stage funding and participation | Preserve community project integrity |
| Premium analytics / reporting | Useful to qualified partners at scale | Protect user and beneficiary privacy |

### Revenue design rules

- Do not bury fees.
- Do not sell influence over review or visibility.
- Do not make impact claims that cannot be supported.
- Keep the contributor’s understanding of where money goes simple and accurate.
- Maintain a clear separation between platform economics and milestone approval standards.

Before accepting, holding, directing, or refunding funds, Sharity must obtain appropriate legal, tax, payments, KYC/AML, and accounting advice for India. Operational design should remain flexible enough to work with qualified payment/escrow partners as the company matures.

---

## 20. Success Metrics

Early metrics should measure trust and completed outcomes—not just registered users or money collected.

### North-star metric

**Verified Impact Projects completed with a satisfactory public Impact Report.**

### Key metrics

| Area | Measures |
|---|---|
| Trust | Approval quality, flag rate, dispute rate, evidence acceptance rate, contributor confidence feedback |
| Project health | Project completion rate, milestone on-time rate, paused/failed project rate |
| Participation | Contributors per project, volunteer commitments, repeat contribution rate, creator repeat rate |
| Impact | Funds appropriately allocated, volunteer hours, materials fulfilled, beneficiaries/outcomes reported |
| Experience | Time to understand a project, project creation completion rate, review turnaround time, support burden |
| Community | Local project density, local repeat participation, number of communities with completed work |
| Sustainability | Cost to review/support a project, transparent platform revenue, operational capacity per project |

### Metrics to treat carefully

Total money raised, follower counts, and leaderboard positions can be useful context but are not proof of value. A smaller number of transparently completed projects is more valuable than a large number of flashy but unresolved ones.

---

## 21. Recommended Tech Stack

This is a directional stack for a web-first MVP, not a low-level specification. Choose a simple, well-supported foundation that lets a small team iterate safely.

| Layer | Recommendation | Why |
|---|---|---|
| Product app | Next.js + React + TypeScript | Strong web performance, flexible rendering, mature ecosystem |
| UI | Tailwind CSS plus accessible component primitives | Fast, consistent interface development without design drift |
| Backend | Next.js server capabilities or a focused TypeScript service layer | Keeps early architecture coherent and team-friendly |
| Data | PostgreSQL with a managed platform | Reliable relational model for users, projects, milestones, and ledgers |
| Auth | Established auth provider or well-tested managed auth | Reduces risk around account/identity flows |
| Storage | Secure object storage | Supports images, evidence, receipts, and project media |
| Payments | India-appropriate regulated payment partner | Enables payments while respecting compliance requirements |
| Maps | Map provider with India coverage and accessible list fallback | Makes location-based discovery tangible |
| Analytics | Privacy-conscious product analytics | Measures activation, completion, and operations health |
| Monitoring | Error tracking and performance monitoring | Essential for reliable contribution and review flows |
| Deployment | Managed cloud deployment with staging | Lets the team move quickly with repeatable releases |

### Technical product principles

- Model the public ledger as auditable events, not editable prose.
- Build permissions and admin review paths early.
- Treat payment, verification, and evidence data as sensitive from the first release.
- Design for exports and operational traceability.
- Do not introduce complex distributed systems, blockchain, or microservices before the product warrants them.

---

## 22. Design Direction

### Desired feeling

Sharity should feel like the opposite of exhausting social media: calm, hopeful, concrete, and trustworthy. It should have the warmth of community work and the clarity of a well-designed financial product.

### Visual principles

- **Human and local:** authentic project imagery and specific locations; avoid generic charity imagery.
- **Clear hierarchy:** outcome, need, current status, and next action should be instantly legible.
- **Proof over persuasion:** evidence, dates, and progress should carry more weight than dramatic copy.
- **Hopeful restraint:** warm colour, optimistic illustrations or icons, and positive language without making hardship decorative.
- **Accessible by default:** high contrast, readable type, keyboard navigation, clear error states, image descriptions, and low-bandwidth consideration.
- **Mobile-native behaviour in a responsive web product:** large tap targets, focused flows, simple maps, and concise project summaries.

### Interface patterns

| Pattern | Role |
|---|---|
| Project cards | Fast discovery with location, need, status, and health clues |
| Milestone timeline | Shows exactly where the project is and what happens next |
| Progress indicators | Explain progress across funding, items, roles, and work—not only money |
| Evidence gallery | Makes before/during/after proof easy to consume |
| Public ledger | Turns complex transactions into understandable events |
| Contribution chooser | Lets money, time, skills, and sharing sit side by side |
| Status badges | Clear labels such as Reviewed, In Progress, Needs Attention, Completed |

### Content voice

Plain, respectful, and action-oriented. Use “contribute,” “help complete,” “show progress,” and “what’s needed.” Avoid guilt, saviour language, hype, or vague claims of changing the world.

---

## 23. Development Roadmap

### Stage 0 — Product foundation (2–4 weeks)

- Validate core legal/payments assumptions with qualified India-based advisers and partners.
- Select a narrow launch community and 2–4 project categories.
- Define review criteria, milestone evidence standards, and project templates.
- Produce a lightweight design system and key user flows.
- Recruit a small group of trusted pilot creators and reviewers.

### Stage 1 — Build the trusted core (6–10 weeks)

- Authentication, profiles, project creation, review queue, Explore, project pages.
- One-time contributions with a compliant payment approach.
- Milestone and public-ledger model.
- Evidence uploads, project updates, core notifications.
- Operations tools for review, flags, and exception handling.

### Stage 2 — Pilot and learn (4–8 weeks)

- Launch with a tightly managed project set.
- Personally observe creator onboarding, contributor hesitation, review time, and evidence quality.
- Complete several projects end-to-end before widening availability.
- Improve the confusing parts of the trust loop before adding new features.

### Stage 3 — Expand deliberately (ongoing)

- Add communities and categories only when operations can preserve quality.
- Improve volunteer/skill workflows, map discovery, and partner pathways.
- Introduce trusted reviewer pilots after a meaningful base of completed work exists.
- Use completed Impact Reports as the main growth asset.

### Build order

```text
Trust model → Information architecture → Key flows → Design system → Pilot product → Completed projects → Expansion
```

The most important early milestone is not a feature count. It is a contributor being able to say: **“I saw the need, understood the plan, helped, and saw the result.”**

---

## 24. Decision Log: Starting Assumptions

| Decision | Rationale |
|---|---|
| Launch in India | Allows focused operations, payment/legal learning, and local community density |
| Web-first responsive product | Reaches users quickly without doubling early product surface area |
| “Impact Project” over “Campaign” | Emphasises collective action and outcomes rather than fundraising alone |
| “Contribute” over “Donate” | Makes time, skills, materials, and awareness visibly valuable |
| Sharity-led milestone approval in Phase 1 | Protects trust while reputation and governance systems are immature |
| Public ledger, not blockchain | Users need clarity and auditability—not technical novelty |
| Milestone-bound funds | Creates a fair, visible link between evidence and future release |
| Contributor choices on unfinished work | Respects agency over unreleased eligible balances |
| Manual review before automation | Quality and learning are more valuable than early scale |

---

## 25. Closing Product Statement

Sharity should make community action feel practical, accountable, and worth repeating. Its success is not measured by how many projects it can list, but by how reliably it helps people move from a local problem to a visible, verified improvement.

The first version should stay focused on one loop:

> **See a need. Support a credible plan. Follow transparent progress. Celebrate real impact.**

If that loop works consistently, Sharity can grow from a useful local platform into the trusted civic infrastructure behind thousands of community-led improvements.
