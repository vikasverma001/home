+++
title = "PSK-I Part G: Kanban in the Scrum Events"
date = 2026-06-26
image = "/img/blog/psk1-kanban-events.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Kanban", "Agile", "Certifications"]
summary = "How flow metrics slot into Sprint Planning, the Daily Scrum, Sprint Review, and Retrospective — without adding events, changing purposes, or altering Scrum's structure."
readtime = "6 min read"
+++

*This is Part G of the [PSK-I Exam Prep series](/blog/psk1-overview/). It covers how the Kanban practices and flow metrics integrate into Scrum's five events — the integration layer the exam tests directly.*

---

## The overarching rule

> **Kanban adds no new events.** Flow metrics *strengthen empiricism* inside the existing ones.

Teams deliver value **at least once per Sprint** (not "only once at the very end"). The **Sprint itself** is a coarse form of limiting WIP.

The most common trap across all of Part G: *"Add a separate weekly metrics meeting."* → No. Kanban adds no events; use the existing ones.

---

## G1. Sprint Planning with Flow

**What changes.** The team uses **historical throughput** to gauge realistic capacity, and the **SLE** to support achievable forecasts. The outputs of Sprint Planning are *unchanged* — a Sprint Goal and a plan.

Instead of guessing capacity from optimism or a fixed velocity target, the team looks at its actual throughput history: if it has averaged ~8 items/Sprint and that rate has been stable, it plans around that, leaving slack for variability.

**How questions come.**
- *"What informs how much work the team forecasts at Planning?"* → **historical throughput** (not gut feel, not a fixed velocity target).
- *"Does Kanban change the output of Sprint Planning?"* → **No** — Sprint Goal + plan, unchanged.

---

## G2. Daily Scrum with Flow

**What changes.** The emphasis shifts to **Current WIP** and **Work Item Age** as the primary inputs. The mindset becomes *"stop starting, start finishing."* The event remains 15 minutes, *for the Developers*, serving the **Sprint Goal** — nothing changes structurally.

The **aging chart** is the practical tool here: the team scans it, spots items approaching or exceeding the SLE line, and decides to swarm those items rather than start anything new.

**Worked example.** The team scans the aging chart, spots a 6-day item against an 8-day SLE, and decides to swarm it today rather than start a new item.

**How questions come.**
- *"Most useful metrics at the Daily Scrum?"* → **WIP + Work Item Age**.
- *"Does Kanban change the Daily Scrum's purpose?"* → **No** — it still serves the Sprint Goal.
- *"Who runs the Daily Scrum when using Kanban?"* → **Developers** — unchanged.

---

## G3. Sprint Review with Flow

**What changes.** In addition to inspecting the Increment, the team inspects **flow** — Cycle Time/Throughput trends and a CFD. Throughput + Monte Carlo may be used for "what by when" **as projections, not commitments**. The output is still an **adapted Product Backlog**.

Showing a CFD where the in-progress band widened opens a product backlog and process conversation about where value is stuck — and feeds directly into what should be prioritised next.

**How questions come.**
- *"Which flow data is relevant at the Sprint Review?"* → **Cycle Time & Throughput trends** (not individual hours or velocity).
- *"Is a Monte Carlo forecast shown at the Review a commitment?"* → **No** — a probabilistic projection.

---

## G4. Sprint Retrospective with Flow

**What changes.** The Retrospective is where the team typically **inspects and adapts the Definition of Workflow and WIP limits**, reviewing WIP, cycle times, and throughput for improvement opportunities.

The DoW and WIP limits *can* be changed at any time — the Retrospective is just the natural cadence for doing so in a structured, team-agreed way.

**Worked example.** Seeing repeated SLE breaches in a particular column, the team lowers that column's WIP limit and adds an explicit pull policy to the DoW during the Retrospective.

**How questions come.**
- *"Where is the DoW usually adapted?"* → the **Retrospective**.
- *"Can the team change WIP limits mid-Sprint?"* → **Yes** — the Retro is usual, but changes are allowed anytime.

---

## G5. Refinement & the Sprint as WIP

**What changes.** Favour **smaller, similar-sized items** — they flow more predictably and sharpen throughput forecasts. This is the Kanban lens applied to *how the backlog is shaped*, not a new event.

The **Sprint itself** is also explicitly called out as a coarse form of **limiting WIP** — one of the conceptual bridges between Scrum and Kanban.

**How questions come.**
- *"How does Kanban help refinement?"* → smaller, similar-sized items **improve flow predictability**.
- *"The Sprint is a form of ___."* → **limiting WIP**.

---

## Summary: what changes vs what stays the same

| | What changes | What stays the same |
|---|---|---|
| **Sprint Planning** | Use throughput for capacity | Sprint Goal + plan as output |
| **Daily Scrum** | Focus on WIP + Work Item Age | 15 min, for Developers, serves Sprint Goal |
| **Sprint Review** | Inspect flow + CFD, Monte Carlo forecasts | Working session, adapts Product Backlog |
| **Retrospective** | Adapt DoW + WIP limits | Inspects individuals, interactions, process, tools, DoD |
| **Refinement** | Favour small, similar-sized items | Ongoing activity, no timebox |

---

*Next: [Part H — Exam Reasoning Patterns](/blog/psk1-exam-patterns/) — the trap taxonomy, calculation shortcuts, tie-breakers, and exam-day tactics.*
