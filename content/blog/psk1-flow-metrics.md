+++
title = "PSK-I Part F: Flow Metrics & Forecasting"
date = 2026-06-26
image = "/img/blog/psk1-flow-metrics.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Kanban", "Agile", "Certifications"]
summary = "The four flow metrics, Little's Law with worked calculations, all four charts explained (scatterplot, CFD, throughput run chart, aging chart), the SLE, and Monte Carlo forecasting."
readtime = "12 min read"
+++

*This is Part F of the [PSK-I Exam Prep series](/blog/psk1-overview/). It is the longest section — flow metrics and forecasting are heavily tested and reward deep understanding over surface familiarity.*

---

## F0. The Four Flow Metrics — Overview

These are the **only four** flow metrics in the Kanban Guide. **Velocity and story points are not among them.**

| Metric | Applies to | One-line meaning |
|---|---|---|
| **WIP** | In-progress | Items started but not finished |
| **Cycle Time** | Finished | Elapsed time: start → finish |
| **Work Item Age** | In-progress | Elapsed time since started (so far) |
| **Throughput** | Finished | Items finished per unit of time |

**The two key pairings.**
- **Cycle Time (finished) vs Work Item Age (in-progress)** — same clock, different population.
- **Throughput (raw count) vs velocity (size-weighted)** — throughput ignores item size.

**How questions come.**
- *"Which is NOT one of the four flow metrics?"* → **velocity / story points**.
- *"Which two are flow metrics?"* (multi) → any two of WIP, Cycle Time, Work Item Age, Throughput.

---

## F1. Work in Progress (WIP)

**What it is.** The **number of work items started but not finished**, per the DoW.

Provides transparency into *load*; visualised as the band height on a CFD or a WIP-over-time chart. Don't confuse the *metric* (a count) with the *limit* (a policy). WIP just reports; the WIP limit constrains.

**Worked example.** A board shows 9 items between "In Progress" and "Review." WIP = **9**. If the WIP limit across those states is 6, the metric tells the team they're over their policy and should finish before starting more.

**How questions come.**
- *"WIP is defined as…"* → items **started but not finished**.
- *"Most useful metrics in the Daily Scrum?"* → **WIP + Work Item Age**.

---

## F2. Cycle Time

**What it is.** The **elapsed time** from when an item *starts* to when it *finishes* — measured on **completed** items only.

**Important characteristics.**
- A **lagging indicator** — known *only after* an item finishes.
- Used to understand turnaround, set expectations, and (via percentiles) define the SLE.
- Measured from the team's defined "started" point (per DoW) to "finished" — not from initial idea.

**Misconception to avoid.** "Cycle Time tells me about work in progress." It can't — it's only known *after* finishing. For in-progress risk, use **Work Item Age**.

**Worked example.** An item started June 1 and finished June 6 → Cycle Time = **5 days**. Plotting 100 such items, the 85th-percentile line sits at 8 days → that becomes the **SLE**.

**How questions come.**
- *"When is Cycle Time known?"* → **only after the item finishes** (lagging).
- *"Cycle Time vs Work Item Age?"* → Cycle Time = **finished** items; Age = **in-progress** items.

---

## F3. Work Item Age

**What it is.** The **elapsed time since an in-progress item started**, up to now.

The **live counterpart** to Cycle Time. Because it's available *while work is in progress*, it's the best metric for predicting when a started item will finish and for flagging risk. Compare an item's age to the **SLE** and its position in the workflow.

**Key nuance.** Age alone isn't "bad." A 10-day-old item near "Done" may be fine; the same age near "Start" is a red flag. Read age *together with* workflow position.

**Misconception to avoid.** "Use Cycle Time to spot at-risk work." Too late — Cycle Time is only known after finishing. **Work Item Age** is the in-flight signal.

**Worked example.** At the Daily Scrum, an item is **6 days old against an 8-day SLE** and still mid-workflow. The team acts now — swarms it — to finish before it breaches, rather than waiting.

**How questions come.**
- *"Which metric best predicts when a started item will finish / which item is most at risk?"* → **Work Item Age** (vs the SLE).
- *"Most useful in the Daily Scrum?"* → **Work Item Age + current WIP**.

---

## F4. Throughput

**What it is.** The **number of work items finished per unit of time** (day/week/Sprint).

A **raw count** at the finish line — **no compensation for item size**. That's the crucial difference from *velocity*, which weights by estimate/story points. Throughput drives "how much / by when" forecasting.

**Misconception to avoid.** "Throughput = velocity." No — velocity is size-weighted; throughput is a plain count. Because throughput ignores size, it's most reliable when items are broken down to be small and similar.

**Worked example.** Last six weeks the team finished 4, 5, 3, 6, 5, 4 items (avg ≈ 4.5/week). For a two-week Sprint they plan capacity around ~9 items and feed the same history into a **Monte Carlo** for a probabilistic forecast.

**How questions come.**
- *"How does Throughput differ from velocity?"* → it **counts finished items with no size compensation**.
- *"Which metric informs capacity / 'how many by when'?"* → **Throughput**.

---

## F5. Little's Law

**Practical statement (flow form):**

> **Average Cycle Time ≈ Average WIP ÷ Average Throughput**

**Plain-English meaning.** For a given throughput, *the more items in progress at once, the longer each takes* on average. If cycle times are too long, the **first lever is to lower WIP**.

**Rearrangements for calculation questions.**

| Given | Solve for | Formula |
|---|---|---|
| WIP + Throughput | Cycle Time | WIP ÷ Throughput |
| WIP + Cycle Time | Throughput | WIP ÷ Cycle Time |
| Cycle Time + Throughput | WIP | Cycle Time × Throughput |

**Worked calculations.**

| Scenario | Answer |
|---|---|
| WIP 10, Throughput 2/day → Cycle Time? | **5 days** |
| WIP 15, Cycle Time 5 days → Throughput? | **3/day** |
| Cycle Time 4 days, Throughput 3/day → WIP? | **12** |
| Throughput 5/week, 20 items → time? | **4 weeks** |

**Quick check.** WIP 12, Throughput 3/day → Cycle Time = **4 days**. 18 items at 6/week → **3 weeks**.

**Misconception to avoid.** "Add WIP to raise throughput." No — it lengthens cycle time without raising throughput.

**How questions come.**
- *Calculation:* given two of {WIP, Cycle Time, Throughput}, solve for the third.
- *"Reducing WIP, throughput steady, does what to cycle time?"* → **reduces** it.
- *"Cycle times are too long — first action?"* → **lower WIP**.

---

## F6. The Four Charts

The exam asks you to *read* charts, *match* a metric to the right chart, or *diagnose* a flow problem. Know each chart's axes, what it's best at, and its failure signature.

### Cycle Time Scatterplot

**Axes.** x = date item finished; y = its cycle time (days).

**What it shows.** Every finished item as a single dot. Horizontal percentile lines (50th, 85th, 95th) summarise the distribution.

**How to read it.**
- Low, tight cloud = fast and **predictable** flow.
- Tall, scattered cloud = high variability (low predictability), even if the average looks fine.
- High outliers = individual items that took unusually long — candidates to inspect in the Retrospective.
- The **85th-percentile line** is where you read the **SLE**.

**Worked example.** 100 finished items; the 85th-percentile line sits at **8 days**. Read: *"85% of our items finish within 8 days."* That *is* the SLE. If a stakeholder wants more certainty, quote the **95th** line (a longer number, e.g. 13 days) — higher confidence always means a longer time.

**How questions come.**
- *"Which chart is the basis for a team's SLE?"* → the **scatterplot**.
- *"The 85th-percentile line is at 9 days — what does that mean?"* → ~85% of items finish in **≤ 9 days**.
- Trap: confusing it with the aging chart — the scatterplot is *finished* items; the aging chart is *in-progress* items.

---

### Cumulative Flow Diagram (CFD)

**What it shows.** Stacked cumulative bands over time — one band per workflow state. Each line is a running count of items that have entered that state. The only chart showing all three of WIP, approximate Cycle Time, and Throughput at once.

**The three readings (memorise this mapping).**

| CFD feature | Metric |
|---|---|
| Vertical band height at a date | **WIP** in that state |
| Horizontal distance between arrival and departure lines | Approximate **Cycle Time** |
| Slope of the "Done" departure line | **Throughput** (steeper = more finishing per period) |

**Healthy vs unhealthy.**
- **Healthy:** bands roughly parallel, steady departure slope, stable widths.
- **Bottleneck:** an in-progress band *widens* over time while the Done slope flattens → growing queue.
- **Stalled flow:** flat departure line = nothing is finishing.
- **Scope growth:** top line climbs steeply = work being added faster than done.

**Worked example.** Over two weeks the In-Progress band steadily widens while the Done line flattens → WIP is piling up and throughput is dropping: a **bottleneck**. Fix: stop starting and swarm, not start more work.

**How questions come.**
- *"On a CFD, Throughput is read from ___"* → the **slope of the departure line**.
- *"A steadily widening band indicates ___"* → a **growing queue / bottleneck**.
- Trap: keep *height = WIP, distance = cycle time, slope = throughput* straight.

---

### Throughput Run Chart

**Axes.** x = time period (day/week/Sprint); y = number of items finished in that period.

**What it shows.** The delivery rate over time. Even bars = predictable delivery. Erratic bars = less predictable, requiring wider forecast ranges.

**Used for.** Capacity input at Sprint Planning; the data source for Monte Carlo forecasts; spotting delivery-rate trends.

**How questions come.**
- *"Which metric/chart informs how much the team can take on?"* → **Throughput**.
- *"Is this velocity?"* → **No** — throughput counts items finished, no size compensation.
- Trap: a Sprint burndown or velocity chart is **not** a flow chart.

---

### Aging Work-in-Progress Chart

**What it shows.** A snapshot of *today* — every in-progress item in its current workflow column, with y-axis = its age (days since started). SLE percentile lines are overlaid.

**How to read it.** Items *at or above the SLE line* are **at risk** of being late. Items sitting a long time in *early* columns are stalled. Unlike the scatterplot (history), this is a **live, forward-looking** picture of work you can still act on.

**Worked example.** An item is **6 days old** against an **8-day SLE** and still only in "In Progress" → swarm it now, before it breaches. An item the same age but already in "Review" may be fine.

**Used for.** The team's *active-management* tool, especially in the Daily Scrum — deciding what to finish first and intervening before an SLE breach.

**How questions come.**
- *"Which chart/metric helps the team decide what to focus on in the Daily Scrum?"* → **aging chart / Work Item Age vs SLE**.
- Trap: choosing Cycle Time (only known *after* finishing — too late) instead of Work Item Age.

---

## F7. Service Level Expectation (SLE)

**What it is.** A **forecast of how long a single item should take**, expressed with a **probability**. It has two parts: a **period of elapsed time** + a **probability** (e.g., *"85% of items finish within 8 days"*).

**Mechanics.** Derived from historical cycle time — typically a percentile on the scatterplot (85th is a common starting point). Used to actively manage flow: compare a live item's Work Item Age to the SLE to spot risk. The SLE should be *displayed* for transparency.

**Key rule.** **Higher confidence ⇒ longer time.** An 85% SLE quotes a longer period than a 50% SLE. An SLE is probabilistic — *never* an exact-date guarantee.

**Misconception to avoid.** "SLE = a deadline / SLA you must hit." It's an *expectation/forecast* with a confidence level.

**Worked example.** The team's scatterplot shows 85% of items finishing within 8 days → SLE is "85% within 8 days." A manager asks them to "promise day 8 exactly." That misuses the SLE — it expresses an 85% likelihood; pushing to ~95% confidence would mean quoting a longer time (e.g. 13 days).

**How questions come.**
- *"An SLE consists of…"* → a **period of elapsed time + a probability**.
- *"Team promises an exact date from an 85% SLE."* → wrong; an SLE is **probabilistic**.
- *"An 85% SLE vs a 50% SLE — which quotes a longer time?"* → the **85%** one.

---

## F8. Forecasting & Monte Carlo

**What a forecast is.** A **probabilistic projection** of a future outcome based on historical flow data — explicitly **not a commitment**.

**Decision rule — pick the right basis.**

| Question | Basis |
|---|---|
| When will *this in-progress* item finish? | **Work Item Age** against the SLE / cycle-time history |
| How many items by date X? / When will N items be done? | **Throughput** history, ideally via Monte Carlo |

**Monte Carlo mechanics.** Rather than a single average, it *randomly samples historical throughput* across many simulated runs, producing a **probability distribution** — e.g., "85% chance of finishing the 20 items within 6 weeks." It surfaces uncertainty honestly instead of hiding it behind a false single number.

**Worked example.** Asked "when will these 20 items be done?", the team runs Monte Carlo on recent throughput and reports a range: *50% by week 4, 85% by week 6*. They present it as a **forecast**, not a promise — and would use **Work Item Age** instead if the question were about a single already-started item.

**How questions come.**
- *"Forecast when *this started* item finishes."* → **Work Item Age / SLE**.
- *"Forecast how many items next Sprint / by a date."* → **Throughput** (Monte Carlo).
- *"Is a forecast a commitment?"* → **No** — probabilistic projection.

---

*Next: [Part G — Kanban in the Scrum Events](/blog/psk1-kanban-events/) — how flow metrics slot into each event without changing Scrum's structure.*
