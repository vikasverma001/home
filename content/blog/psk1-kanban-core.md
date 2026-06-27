+++
title = "PSK-I Part E: Kanban Core"
date = 2026-06-26
image = "/img/blog/psk1-kanban-core.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Kanban", "Agile", "Certifications"]
summary = "What Kanban actually is (and isn't), its relationship to Scrum, the four practices, the Definition of Workflow, WIP limits as a maximum not a target, and how pull systems work."
readtime = "10 min read"
+++

*This is Part E of the [PSK-I Exam Prep series](/blog/psk1-overview/). It covers the Kanban Guide for Scrum Teams in depth — from the official definition through the four practices, Definition of Workflow, WIP limits, and pull systems.*

---

## E1. The Definition of Kanban (parsed)

The official definition from the Kanban Guide for Scrum Teams:

> *Kanban is a strategy for optimising the **flow of value** through a process that uses a **visual**, **work-in-progress-limited** **pull system**.*

**Parsed word by word.**

| Term | What it means |
|---|---|
| **Flow of value** | Optimises the *movement of value* (work items) through the system, not individual busyness |
| **Visual** | The workflow is made transparent — commonly a board |
| **Work-in-progress-limited** | The team caps how many items are in progress at once |
| **Pull system** | Work advances by being *pulled* when capacity exists, not pushed to keep people busy |

**Why it matters.** Optimising flow improves a process's *efficiency, effectiveness, and predictability*. The flow lens enhances and complements Scrum's empiricism — it doesn't replace it.

**Misconception to avoid.** "Kanban is a board" / "a separate process" / "a methodology with roles." It is a *strategy* layered onto Scrum.

**Worked example.** A team says "we do Kanban — here's our board." A board is only the *visualisation* part. Real Kanban also requires WIP limits and the resulting pull system working toward flow; the board alone isn't "Kanban."

**How questions come.**
- *"Which best describes what Kanban is?"* → a **strategy for optimising flow via a visual, WIP-limited pull system**. Trap: "a board," "a process that replaces events," "a method with its own roles."
- *"What is the goal of Kanban?"* → optimise the **flow of value**.

---

## E2. Relation to Scrum ("Scrum is still Scrum")

**The key claim.** The Kanban Guide for Scrum Teams **does not replace or discount any part** of the Scrum Guide; **the Scrum Guide applies in its entirety**. Kanban adds *complementary practices* — not roles, events, or artifacts.

**What stays exactly the same.**
- Three accountabilities (PO, SM, Developers) — no "Kanban Master"
- Five events (Sprint, Planning, Daily Scrum, Review, Retro) — no new "flow meeting"
- Three artifacts (Product Backlog, Sprint Backlog, Increment) — no new "flow artifact"

**Misconceptions / traps.** A "Kanban Master," a new "flow" event, a new artifact, or "drop the Sprint for continuous flow" — all wrong.

**Worked example.** A team proposes adding a "Flow Master" to own WIP limits. Wrong on two counts: Kanban adds *no role*, and WIP limits belong to the *self-managing Scrum Team*, not a new owner.

**How questions come.**
- *"Adding Kanban changes the number of accountabilities to ___."* → **still three**.
- *"A team adds a 'Kanban Master.'"* → wrong; **Kanban adds no role**.
- *"Does the Kanban Guide replace parts of the Scrum Guide?"* → **No** — the Scrum Guide applies in full.
- **Tie-breaker:** between two options, prefer the one that **keeps Scrum intact**.

---

## E3. The Four Practices

The four practices are *enabled by* the Definition of Workflow and owned by the **self-managing Scrum Team**.

### Practice 1: Visualization of the Workflow

Make the flow of work transparent — states, items, policies, WIP limits, and the SLE. A board is the common tool but **not required**. Purpose: surface bottlenecks, blocked items, and aging work.

### Practice 2: Limiting Work in Progress (WIP)

Explicitly cap in-progress items. This is what **creates the pull system** and concentrates the team — directly reinforcing the Scrum value of **Focus**. The **Sprint itself** is a coarse form of limiting WIP.

### Practice 3: Active Management of Work Items in Progress

Continuously attend to in-progress work — unblock blocked items, watch *aging* against the SLE, relieve bottlenecks, keep value flowing. This is the *team* managing *flow*, not managers assigning tasks.

### Practice 4: Inspecting and Adapting the Definition of Workflow

Regularly improve the workflow itself — typically at the **Retrospective**, though it can be changed at any time. This is the empirical loop applied to *how the team works*.

**Critical relationship.** A **pull system** is a *consequence* of limiting WIP — **not a fifth practice**. This distinction comes up directly on the exam.

**Misconception to avoid.** Treating "pull system," "story-point estimation," or "a flow meeting" as one of the four practices.

**How questions come.**
- *"Which is one of the four Kanban practices?"* → one of: visualise / limit WIP / actively manage / inspect-adapt the DoW.
- *"Is a pull system one of the four practices?"* → **No** — it's a **consequence** of limiting WIP.
- *"Select the two practices."* (multi-answer) → any two from the four above.

---

## E4. Definition of Workflow (DoW)

**What it is.** The Scrum Team's **explicit, shared understanding** of the policies it uses to apply the Kanban practices. The **team creates and owns it**.

**Elements (each must be explicit).**

| Element | Notes |
|---|---|
| **Work item types** | Optional but often useful to distinguish item kinds |
| **Defined "started" and "finished" points** | At least one of each; the four flow metrics apply to each span |
| **Workflow states / steps** | Between started and finished |
| **Explicit policies for limiting WIP** | Where and how WIP is capped |
| **Explicit pull policies** | Conditions under which an item may move to the next state |
| **A Service Level Expectation (SLE)** | |

**Why it matters.** Without a shared definition of "started" and "finished," flow data is inconsistent and metrics are meaningless. The DoW makes the practices and metrics reliable and transparent.

**DoW vs Definition of Done.** The DoW *complements* the DoD — it can extend it but **never replaces** it. The DoD still fully applies.

**Misconception to avoid.** "DoW replaces or makes the DoD optional." "A coach/manager owns the DoW." Both wrong.

**Worked example.** A team disagrees about when a card is "started" — when it's pulled into a column, or when coding begins. They resolve it by **defining the 'started' point explicitly in the DoW**, so Work Item Age and Cycle Time are measured consistently.

**How questions come.**
- *"Who creates/owns the Definition of Workflow?"* → the **Scrum Team**.
- *"What must the DoW make explicit?"* → **how WIP is limited** (also started/finished points, policies, SLE).
- *"DoW vs DoD?"* → **complements / may extend**, never replaces.

---

## E5. Limiting WIP — WIP vs WIP Limit

Two different things people consistently confuse:

- **WIP (the metric):** the *count* of items started but not finished.
- **WIP limit (the policy):** a *constraint / maximum* the team sets to shape flow and reduce actual WIP.

**How a WIP limit works.**
- It is a **maximum, not a target and not a minimum**.
- Reaching it is a signal to **stop starting** and **finish** (swarm) in-progress work — *not* to raise the limit.
- Limiting WIP *creates pull*: capping what can be in-flight means new work enters only when capacity frees up.

**The anti-pattern.** Raising WIP to keep people "busy" → more multitasking and handoffs → **longer cycle time** with no throughput gain. Idle time may instead signal a bottleneck to swarm on.

**Link to Little's Law.** Holding throughput steady, **lower WIP ⇒ lower cycle time**.

**Worked example.** The Test column (limit 3) is full, so a Developer can't pull a 4th item. Correct response: **help finish a Test item (swarm)**, not bump the limit to 4 or start something new upstream. The full column is a *signal*, not a failure.

**How questions come.**
- *"A WIP limit is best described as…"* → a **maximum** number of items allowed at once.
- *"WIP limit reached, can't pull new work — do what?"* → **swarm to finish** in-progress work.
- *"Increase WIP to raise throughput?"* → **wrong** (lengthens cycle time).

---

## E6. Pull Systems & Explicit Policies

**What a pull system is.** An item advances to the next state *only when that state has capacity (within its WIP limit) and the explicit pull policy is satisfied* — the downstream *draws* work, rather than upstream *pushing* it.

**Explicit pull policies** state the concrete, checkable conditions for movement. They make the system transparent and cut ad-hoc decisions.

**Good vs bad policy example.**

| | |
|---|---|
| *"Be productive at all times"* | Vague — states no checkable condition. Not a real policy. |
| *"Pull to Review only when Review has < 2 items and all tests pass"* | Concrete conditions, capacity-aware. This is a proper explicit pull policy. |

**Misconception to avoid.** "Push work forward to keep everyone busy" is the *opposite* of pull. High utilisation isn't the goal — flow is.

**How questions come.**
- *"What triggers an item to move in a pull system?"* → **downstream capacity within WIP limits** (and the pull policy being met).
- *"Which is an example of an explicit pull policy?"* → the one stating **concrete, checkable conditions**.
- *"Pull vs push?"* → pull = **draw on capacity**; push = keep busy.

---

*Next: [Part F — Flow Metrics & Forecasting](/blog/psk1-flow-metrics/) — the four metrics, Little's Law, all four charts in depth, the SLE, and Monte Carlo forecasting.*
