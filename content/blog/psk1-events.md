+++
title = "PSK-I Part C: The Scrum Events"
date = 2026-06-26
image = "/img/blog/psk1-events.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Agile", "Certifications"]
summary = "The Sprint as container, all five events, every timebox — plus the exact exam traps around cancellation, the three-question myth, and what the Sprint Review actually produces."
readtime = "9 min read"
+++

*This is Part C of the [PSK-I Exam Prep series](/blog/psk1-overview/). It covers all five Scrum events in depth, including timeboxes and the PSK-specific flow additions.*

> **Frame for all events.** The Sprint is the *container* for the other four events. Each event is a formal inspect-and-adapt opportunity that reduces the need for meetings not defined in Scrum. Know the timeboxes cold.

---

## C1. The Sprint

**What it is.** A **fixed-length event of one month or less** — "the heartbeat of Scrum, where ideas are turned into value." The container for all other events.

**How it works.**
- A new Sprint starts **immediately** after the previous one ends. No gaps.
- During a Sprint: no changes that **endanger the Sprint Goal**; quality **does not decrease**; the Product Backlog is **refined** as needed; **scope may be clarified and renegotiated** with the PO as more is learned.
- The Sprint is itself a coarse form of **limiting WIP** — the bridge to Kanban.

**Cancellation rules (exam favourite).**
- **Only the Product Owner** can cancel a Sprint.
- Only valid reason: the **Sprint Goal becomes obsolete**.
- Cancellation is rare.

**Misconception to avoid.** "Extend the Sprint to finish the work." No — scope can flex; the timebox cannot. A team running behind simply finishes the timebox, then carries unfinished work back to the Product Backlog.

**Worked example.** A company pivots away from the product line the current Sprint serves, making the Sprint Goal pointless. The Product Owner *may* cancel the Sprint. If instead the team is merely behind schedule, that is **not** grounds to cancel or extend.

**How questions come.**
- *"Who can cancel a Sprint, and when?"* → **only the PO**, when the **Sprint Goal is obsolete**.
- *"The team is behind — extend the Sprint?"* → **No**.
- *"When does the next Sprint start?"* → **immediately** after the previous ends.

---

## C2. Sprint Planning

**What it is.** The event that **initiates the Sprint** by laying out the work. Timeboxed to **≤ 8 hours for a one-month Sprint** (shorter for shorter Sprints).

**The three topics.**

| Topic | Question answered | Who leads |
|---|---|---|
| **Why** | Why is this Sprint valuable? (Sprint Goal) | Whole team |
| **What** | Which Product Backlog items to select? | Developers, with PO |
| **How** | How will the Increment be built? | Developers |

**Output.** A **Sprint Backlog = Sprint Goal + selected items + plan**.

**With Kanban.** Historical **throughput** informs capacity — replacing (or augmenting) gut feel or fixed velocity targets.

**Misconception to avoid.** "The PO assigns the work / sets capacity." No — Developers decide capacity; the whole team crafts the Sprint Goal together.

**Worked example.** Planning starts with the PO framing the objective; the team shapes it into a Sprint Goal ("enable guest checkout"). The Developers, seeing they average ~9 items per Sprint from historical throughput, pull the items that serve the Goal and sketch the plan.

**How questions come.**
- *"What are the three topics of Sprint Planning?"* → **Why / What / How**.
- *"Max timebox for a one-month Sprint?"* → **8 hours**.
- *"What informs capacity in Scrum with Kanban?"* → **historical throughput**.

---

## C3. Daily Scrum

**What it is.** A **15-minute** event **for the Developers**, each working day, to **inspect progress toward the Sprint Goal** and **adapt the Sprint Backlog**, adjusting the upcoming plan.

**How it works.**
- The **Developers run it**. PO and SM participate only if actively working on Sprint Backlog items.
- **No required structure** — the 2020 Guide removed the three-question format. Any format that meets the purpose is fine.
- It is not the only time Developers can adapt — they meet as needed throughout the day.

**With Kanban.** The most useful inputs are **Current WIP** and **Work Item Age** — reinforcing "stop starting, start finishing." If an item is 6 days old against an 8-day SLE, the team acts on it now rather than waiting for a breach.

**Misconception to avoid.** "It's a status meeting for the SM / managers / stakeholders." No — it is *by and for the Developers*.

**Worked example.** A stakeholder asks to chair the Daily Scrum to collect status. The correct stance: decline — the Daily Scrum is for the Developers; it's not a reporting meeting.

**How questions come.**
- *"Stakeholder wants to run the Daily Scrum for status."* → it's **for the Developers**; decline.
- *"Which metrics are most useful in the Daily Scrum?"* → **Current WIP + Work Item Age**.
- *"Must the Daily Scrum use the three-question format?"* → **No** (no prescribed structure).

---

## C4. Sprint Review

**What it is.** A **working session** (timebox **≤ 4 hours**) where the Scrum Team and **stakeholders** **inspect the outcome** of the Sprint and **adapt the Product Backlog**.

**What it is not.** A one-way demo or status report.

**Output.** An **adapted Product Backlog** — this is the key thing the exam tests. The Review is not "done" until the backlog reflects what was learned.

**With Kanban.** The Review also inspects *flow* — Cycle Time / Throughput trends, a CFD — and may use throughput + Monte Carlo for "what by when" **as projections, not commitments**.

**Worked example.** Mid-Review, stakeholders reveal a regulatory change. The team doesn't just note it for later — they adapt the Product Backlog then and there, reordering and adding items. That's the event's purpose.

**How questions come.**
- *"Which best describes the Sprint Review?"* → a **working session to inspect the outcome and adapt the Product Backlog** (not "demo-only status").
- *"New information appears at the Review — what happens?"* → the **Product Backlog is adapted** collaboratively.

---

## C5. Sprint Retrospective

**What it is.** The event (timebox **≤ 3 hours**) to **plan ways to increase quality and effectiveness**, inspecting how the last Sprint went regarding **individuals, interactions, processes, tools, and the Definition of Done**.

**With Kanban.** This is where the team typically **inspects and adapts the Definition of Workflow and WIP limits**, examining WIP, cycle times, and throughput. The DoW and WIP limits *can* be changed anytime — the Retrospective is just the natural cadence.

**Misconception to avoid.** "The Retro only covers tools and process." It also covers **people, interactions, and the DoD**.

**Worked example.** Reviewing the Sprint's CFD, the team sees the "In Review" band kept widening. In the Retrospective they adapt the Definition of Workflow — lowering the WIP limit on Review and adding a pull policy — to relieve the bottleneck next Sprint.

**How questions come.**
- *"Where is the Definition of Workflow / WIP limits usually adapted?"* → the **Sprint Retrospective**.
- *"What does the Retrospective inspect?"* → **individuals, interactions, process, tools, DoD** (and, with Kanban, flow).

---

## Timebox reference — memorise this table

| Event | Max timebox (one-month Sprint) |
|---|---|
| Sprint | 1 month (4 weeks) |
| Sprint Planning | 8 hours |
| Daily Scrum | 15 minutes |
| Sprint Review | 4 hours |
| Sprint Retrospective | 3 hours |

*Shorter Sprints → shorter events. These are maximums.*

---

*Next: [Part D — Artifacts & Commitments](/blog/psk1-artifacts/) — the three artifacts, their three commitments, and why mixing them up is the most common artifact mistake on the exam.*
