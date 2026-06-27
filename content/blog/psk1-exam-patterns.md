+++
title = "PSK-I Part H: Exam Reasoning Patterns"
date = 2026-06-26
image = "/img/blog/psk1-exam-patterns.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Kanban", "Agile", "Certifications"]
summary = "The trap taxonomy, Little's Law calculation shortcuts, tie-breaker rules, and exam-day tactics. Read this part last — it's the meta-layer that makes everything else click faster under pressure."
readtime = "7 min read"
+++

*This is Part H of the [PSK-I Exam Prep series](/blog/psk1-overview/). Read this after working through Parts A–G. It's the reasoning layer — pattern recognition that turns studied knowledge into correct answers under time pressure.*

---

## H1. The Trap Taxonomy

Almost every wrong answer on the PSK-I belongs to one of eight families. When an option *feels* wrong but you can't say why, check it against this list.

### Trap 1: Structure-Change Trap
**Pattern.** Adds a role/event/artifact, drops the Sprint, or creates a "Kanban variant" of a Scrum event.
**Signature.** "Kanban Master," "Flow meeting," "flow artifact," "replace the Sprint with continuous flow."
**Rule.** Kanban adds four *practices*, not structure. Violates *"Scrum is still Scrum."*

### Trap 2: Push / Utilisation Trap
**Pattern.** "Keep everyone busy," "raise WIP to raise throughput," "push work forward."
**Rule.** Contradicts pull and flow. Raising WIP *lengthens* cycle time without improving throughput.

### Trap 3: Commitment-as-Guarantee Trap
**Pattern.** Treats a forecast, SLE, or projection as an exact date or firm promise.
**Rule.** Forecasts and SLEs are **probabilistic**. "We'll be done by Thursday" from an 85% SLE is false precision.

### Trap 4: Target Trap
**Pattern.** Calls a WIP limit a *goal*, *target*, or *minimum*.
**Rule.** A WIP limit is a **maximum**. Reaching it is a signal to finish, not a score to hit.

### Trap 5: Authority Trap
**Pattern.** SM or manager assigns tasks, sets WIP limits, or owns the Definition of Workflow.
**Rule.** The *Scrum Team* self-manages and owns the DoW. The SM enables — does not direct.

### Trap 6: Replace Trap
**Pattern.** "The DoW replaces the DoD," "Kanban replaces Scrum events," "Kanban supersedes the Scrum Guide."
**Rule.** Kanban *complements*. The Scrum Guide applies in full. The DoW *extends* the DoD, never replaces it.

### Trap 7: Newer-is-Righter Trap
**Pattern.** Expansion-Pack concepts presented as exam truth: "Definition of Outcome Done," "Supporters," "Stakeholders" as a formal accountability, Cynefin.
**Rule.** The exam tests the **2020 Scrum Guide + Kanban Guide for Scrum Teams**, not the Expansion Pack. Anything outside those sources is a distractor.

### Trap 8: Wrong-Metric Trap
**Pattern.** Using Cycle Time to judge in-progress risk, or treating velocity as a flow metric.
**Rule.** Cycle Time is a *lagging* indicator — only known after finishing. For in-flight risk, use **Work Item Age**. Velocity is *not* one of the four flow metrics.

---

## H2. Calculation Patterns (Little's Law)

Keep these three rules in memory. When the exam gives you a numbers question, identify which two variables are known and apply the right one.

| Given | Solve for | Formula |
|---|---|---|
| WIP + Throughput | Cycle Time | **WIP ÷ Throughput** |
| WIP + Cycle Time | Throughput | **WIP ÷ Cycle Time** |
| Cycle Time + Throughput | WIP | **Cycle Time × Throughput** |
| Item count + Throughput | Time to complete | **Count ÷ Throughput** |
| Throughput + time periods | Forecast items | **Throughput × Periods** (a forecast, not a promise) |

**Quick-check drill** (run through these before the exam):

| Scenario | Answer |
|---|---|
| WIP 12, Throughput 3/day → Cycle Time | **4 days** |
| WIP 10, Throughput 2/day → Cycle Time | **5 days** |
| 18 items, Throughput 6/week → time | **3 weeks** |
| Cycle Time 4 days, Throughput 3/day → WIP | **12** |
| WIP 15, Cycle Time 5 days → Throughput | **3/day** |

---

## H3. Tie-Breakers (when two options both look plausible)

Use these in order when stuck:

1. **Keep Scrum intact.** Between two structurally different options, choose the one that doesn't add or remove a Scrum element.
2. **Pull over push.** Finishing over starting. Flow over utilisation.
3. **Probabilistic over guaranteed.** A forecast/SLE is never a promise.
4. **Team over manager.** Self-management over control. The Scrum Team owns its own process.
5. **On True/False, an absolute can be True.** If an option faithfully restates a rule from the Scrum Guide or Kanban Guide, it can be True even if it sounds absolute. Absolutes are not automatically wrong.
6. **Source hierarchy.** 2020 Scrum Guide + Kanban Guide for Scrum Teams > blogs > courseware > dumps. When in doubt, ask: *"Is this in the guide?"*

---

## H4. Exam-Day Tactics

**Time budget.** 45 questions in 60 minutes = **~80 seconds per question**. That's tighter than it sounds. Flag and move — never leave a blank (there's no penalty for guessing under a percentage bar; an unanswered question is a guaranteed zero).

**Multiple-answer questions.** Select *exactly* the number indicated — no more, no less. Partial selections are marked wrong. When the question says "select 2," there are exactly 2 correct answers.

**Reading order.** Read the *question* first, then scan the scenario stem for only the relevant facts. Scenarios often include irrelevant details designed to anchor you to a wrong answer.

**Before booking.** Aim to score **95%+ repeatedly** on the **Scrum with Kanban Open** (free at scrum.org). Keep an error log that maps each miss to the guide section. If you're missing the same category of question more than once, that's the section to revisit, not the ones you're already getting right.

**The single fastest mental check for any answer.** Ask: *"Does this option keep Scrum intact and improve flow without adding structure?"* If yes, it's almost certainly right. If it adds a role, drops an event, guarantees an outcome, or keeps people busy at the expense of finishing work — it's almost certainly wrong.

---

## Series recap

| Part | Core idea |
|---|---|
| **A — Scrum Foundations** | Empiricism + lean thinking; TIA chain; five values; immutable-but-incomplete framework |
| **B — The Scrum Team** | One cohesive unit; three accountabilities; self-management; PO is one person |
| **C — The Events** | Sprint as container; know the timeboxes; only PO cancels Sprint; Review adapts the backlog |
| **D — Artifacts & Commitments** | Match artifact to commitment; DoD can only get stricter; PO decides release |
| **E — Kanban Core** | Strategy, not a board; four practices only; DoW owned by team; WIP limit is a maximum |
| **F — Flow Metrics** | Four metrics only; Cycle Time vs Work Item Age; four charts; SLE is probabilistic; Little's Law |
| **G — Kanban in Events** | No new events; throughput at Planning; WIP+Age at Daily; CFD at Review; DoW at Retro |
| **H — Exam Patterns** | Eight trap families; Little's Law shortcuts; tie-breakers; 80 seconds/question |

Good luck on the assessment. The Scrum with Kanban Open is your best free calibration tool — use it until the score is consistent.

---

*Back to the start: [PSK-I Exam Prep: Complete Study Guide Overview](/blog/psk1-overview/)*
