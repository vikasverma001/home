+++
title = "PSK-I Part D: Artifacts & Commitments"
date = 2026-06-26
image = "/img/blog/psk1-artifacts.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Agile", "Certifications"]
summary = "Three artifacts, three commitments — and why confusing which commitment belongs to which artifact is the most common mistake on the PSK-I. Deep coverage of the Product Backlog, Sprint Backlog, Increment, and Definition of Done."
readtime = "9 min read"
+++

*This is Part D of the [PSK-I Exam Prep series](/blog/psk1-overview/). It covers all three Scrum artifacts and their commitments in depth.*

---

## D0. The System: Artifacts & Commitments

Scrum has **three artifacts**, each with **exactly one commitment** that brings transparency and focus to that artifact's progress.

| Artifact | Commitment | The commitment answers… |
|---|---|---|
| **Product Backlog** | Product Goal | *Where is the product going?* |
| **Sprint Backlog** | Sprint Goal | *Why is this Sprint valuable?* |
| **Increment** | Definition of Done | *Is the work actually finished and usable?* |

**Why this matters.** Pre-2020, the Sprint Goal and "done" were loosely attached to artifacts. The 2020 Guide gave each artifact a *named commitment* so progress can be measured against something concrete — directly serving transparency.

**The #1 artifact mistake on the exam:** mixing up which commitment belongs to which artifact. Memorise the table above.

**How questions come.**
- *"Match each artifact to its commitment."* → use the table above.
- *"Which is a commitment, not an artifact?"* → Product Goal / Sprint Goal / Definition of Done are commitments; the two backlogs and the Increment are artifacts.

---

## D1. Product Backlog & Product Goal

**What the Product Backlog is.** An **emergent, ordered list** of what's needed to improve the product — the **single source of work**. It is *never complete*; it evolves with the product and environment.

**What the Product Goal is.** The product's **future target state** — a single, longer-term objective the team pursues **one at a time**. A team fulfils (or abandons) one Product Goal before the next.

**Refinement.** Items become "ready" through **refinement** — the *ongoing activity* of breaking down items and adding detail and order. Refinement is **not an event and has no timebox**. It happens continuously, not on a mandated schedule.

**Key nuances.**
- Ordering is the **PO's** call; the Developers who'll do the work typically size items.
- There is **one Product Backlog per product**, even with multiple teams.
- The team pursues **one Product Goal at a time** — pursuing two simultaneously is wrong.

**Misconception to avoid.** "Refinement is a mandatory, timeboxed event." It's an *activity* — continuous, flexible, and never a sixth Scrum event.

**Worked example.** A team treats "refinement" as a fixed 2-hour Friday meeting and calls it an event. That mislabels it — refinement is an ongoing activity; the team refines a little continuously, whenever it adds clarity.

**How questions come.**
- *"How is Product Backlog refinement best described?"* → an **ongoing activity** (not a formal, timeboxed event).
- *"How many Product Goals at once?"* → **one**.
- *"What is the Product Backlog?"* → an **emergent, ordered, never-complete** single source of work.

---

## D2. Sprint Backlog & Sprint Goal

**What the Sprint Backlog is.**
> Sprint Goal (why) + selected Product Backlog items (what) + an actionable plan to deliver them (how)

It is **by and for the Developers** — a real-time picture of the work they plan to do to meet the Sprint Goal; **updated throughout** the Sprint as they learn.

**What the Sprint Goal is.** The **single objective** giving the Sprint coherence and focus. Crafted in Sprint Planning as a **whole-team** commitment. It **stays fixed** for the duration of the Sprint.

**The crucial distinction: scope vs Goal.**

Scope *can* be clarified and renegotiated with the PO as more is learned — but the **Sprint Goal stays fixed**. This flexibility is how the team keeps the Goal intact while details shift.

**Mid-Sprint changes.** Belong to the Developers to manage. New work that would *endanger the Sprint Goal* should not enter the Sprint without explicit negotiation.

**Misconception to avoid.** "The PO adds items to the Sprint Backlog at will." Changes are *negotiated* with the Developers, who own it.

**Worked example.** Halfway through, the Developers discover an item is bigger than thought. They renegotiate scope with the PO — drop a lower-value item — while keeping the Sprint Goal intact. The PO unilaterally injecting new items that threaten the Goal would be wrong.

**How questions come.**
- *"What are the parts of the Sprint Backlog?"* → **Sprint Goal + selected items + plan**.
- *"As Developers learn more, what may change vs stay fixed?"* → **scope may be renegotiated; the Sprint Goal stays**.
- *"Who owns/updates the Sprint Backlog?"* → the **Developers**, throughout the Sprint.

---

## D3. Increment & Definition of Done

**What an Increment is.** A **concrete stepping stone toward the Product Goal** — it must be **usable** and **verifiably meet the Definition of Done**.

**Key mechanics.**
- Each Increment *adds to* prior Increments and is verified to work with them.
- An Increment is "born" the **moment an item meets the DoD** — so **multiple Increments can exist within one Sprint**, not just one at Sprint end.
- Releasing is separate from being Done: the Increment must be *usable*, but the decision to *release* is the **PO's** — releasing every Sprint is not required.

**What the Definition of Done is.** The **formal description of the state** the Increment must reach to be considered complete and usable. It creates transparency about quality — one shared meaning of "done."

**Organisational DoD rules.**
- If an org DoD exists, it is a **minimum all teams must meet**.
- A team **may make it stricter, never weaker**.
- If no org DoD exists, the team creates one.
- **Multiple teams on one product share the same DoD.**

**When an item doesn't meet the DoD.** It cannot be released or presented as done. It **returns to the Product Backlog**.

**Misconception to avoid.**
- "One Increment per Sprint." No — potentially many.
- "A team can relax the org DoD." No — only stricter.
- "The Increment must ship each Sprint." No — the PO decides.

**Worked example.** The org DoD requires automated tests + security scan. A team wants to also require a performance benchmark. That's *allowed* (stricter than the minimum). Skipping the security scan "just this Sprint" is *not* allowed — the work isn't Done and goes back to the Product Backlog.

**How questions come.**
- *"An org DoD exists; can a team add stricter checks?"* → **Yes** (exceed the minimum, never weaken).
- *"An item doesn't meet the DoD at Sprint end."* → back to the **Product Backlog**, not shown as done.
- *"How many Increments in a Sprint?"* → **one or more** (born when an item meets the DoD).
- *"Must the Increment be released each Sprint?"* → **No** — usable yes; releasing is the **PO's** call.

---

*Next: [Part E — Kanban Core](/blog/psk1-kanban-core/) — the definition of Kanban, its relationship to Scrum, the four practices, the Definition of Workflow, WIP limits, and pull systems.*
