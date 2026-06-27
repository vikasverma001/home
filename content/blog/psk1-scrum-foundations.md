+++
title = "PSK-I Part A: Scrum Foundations"
date = 2026-06-26
image = "/img/blog/psk1-scrum-foundations.svg"
category = "Certifications"
tags = ["PSK-I", "Scrum", "Agile", "Certifications"]
summary = "Empiricism, lean thinking, the three pillars, the five values, and Scrum as a lightweight framework — the theory layer every PSK-I question is built on."
readtime = "8 min read"
+++

*This is Part A of the [PSK-I Exam Prep series](/blog/psk1-overview/). It covers the theoretical foundations: empiricism, the three pillars, lean thinking, the five Scrum values, and what it means for Scrum to be a lightweight, immutable framework.*

---

## A1. Empiricism

**What it is.** Empiricism holds that knowledge comes from experience and that decisions should be based on what is *observed*, not on speculation. It is one of the two foundations of Scrum (paired with lean thinking).

**Why it matters.** Product development is complex work — the link between what you do and what results is only clear in hindsight. Predictive control ("plan it all, then execute") assumes a stable, well-understood process. Empiricism handles complexity with short cycles: build a little, observe the real result, decide the next step from evidence.

**Key nuances.**
- Empiricism is not "no planning." Planning is continuous and just-in-time, re-grounded in observation.
- It requires the *ability to act* on what's learned — observation without adaptation is wasted.
- The Scrum Guide is specific: the two foundations are **empiricism *and* lean thinking** (not empiricism alone).

**Misconception to avoid.** "The ceremonies *are* empiricism." They're not — the events are just where inspection and adaptation happen. Empiricism is the underlying *theory*.

**Worked example.** A team is told to lock scope and date for a 12-month build. By Sprint 3, working software plus user feedback reveals the central assumption was wrong. An empirical team would have inspected a usable Increment each Sprint and adapted early. The lock-it-all-up-front approach hides problems until they're expensive — that's the anti-empirical mindset Scrum rejects.

**How questions come.**
- *"Scrum is founded on which two things?"* → **empiricism and lean thinking**. Trap: "defined process control," "Six Sigma."
- *"Which approach best fits complex work?"* → inspect-and-adapt in **short cycles**. Trap: "complete all analysis up front."
- *Scenario: sponsor demands fixed 12-month scope+date* → conflicts with **empiricism**.

---

## A2. The Three Pillars: Transparency, Inspection, Adaptation

**What they are.** Three pillars uphold every implementation of empirical process control. They form a dependency chain — each pillar depends on the one before it.

**The chain.**

1. **Transparency** — the process and work must be *visible* to those performing and receiving it, against agreed standards (e.g., a shared Definition of Done). Because decisions are made on the *perceived state of the artifacts*, transparency is the precondition for everything else. Low transparency → decisions that decrease value and increase risk.

2. **Inspection** — artifacts and progress toward goals are inspected frequently and diligently to detect undesirable variances. Only as good as the transparency feeding it.

3. **Adaptation** — when the process or product deviates outside acceptable limits, adjust *as soon as possible* to minimise further deviation. Inspection without adaptation is pointless.

**Key nuances.**
- Adaptation is *immediate*, not deferred — a self-managing team adapts the moment it learns something material.
- The commitments (Product Goal, Sprint Goal, Definition of Done) give each artifact a standard to be transparent *against*.
- Transparency is a **pillar**, not a value. (The values are covered in A4.)

**Misconception to avoid.** "We have dashboards, so we have transparency." Transparency is a *shared, accurate understanding* for decisions — not the volume of reporting, and certainly not individual surveillance.

**Worked example.** A team's board shows every item green, but known defects are quietly omitted. Transparency is broken first — so the Sprint Review inspects a false picture, and any adaptation decided there is based on fiction. Fixing downstream symptoms won't help until the artifact reflects reality.

**Kanban mapping.** Visualization → **transparency**; flow metrics → **inspection**; limiting WIP / active management → **adaptation**.

**How questions come.**
- *"A team inspects flow metrics daily but never changes how it works."* → failing pillar is **Adaptation**.
- *"Important decisions are based on the ___ of the artifacts."* → **perceived state**.
- *"Which is NOT a pillar?"* → Commitment / Focus / Courage (those are values).

---

## A3. Lean Thinking

**What it is.** Lean thinking reduces waste and focuses on the essentials — the second foundation alongside empiricism.

**Why it matters.** In flow terms, "waste" includes partially done work, waiting, handoffs, context-switching, and excess WIP. This is the conceptual bridge to Kanban: limiting WIP and optimising flow are direct applications of lean's core idea.

**Key nuance.** Lean's "focus" is about *value*, not keeping people busy. High utilisation with lots of half-done work is the *opposite* of lean.

**Misconception to avoid.** "Lean = maximise resource utilisation." That usually *creates* waste through queues and multitasking.

**Worked example.** A team has 12 items started and only 2 finishing per week. The 10 unfinished items are inventory and waste — aging, risking rework, hiding problems. Lean thinking says cut the WIP and finish; the Kanban practice that enacts it is *limiting WIP*.

**How questions come.**
- *"What does lean thinking add to Scrum's empirical base?"* → **reduce waste, focus on essentials**. Trap: "maximise utilisation," "front-load analysis."

---

## A4. The Five Scrum Values

**The values.** Commitment, Focus, Openness, Respect, Courage.

Scrum's successful use depends on people becoming **more proficient in living all five**.

**Each value, precisely.**

| Value | What it actually means |
|---|---|
| **Commitment** | To the *goals* (Product/Sprint Goal) and to *each other* — not to a fixed scope or plan |
| **Focus** | Concentrate on the work of the Sprint and the Sprint Goal |
| **Openness** | Be open about the work and the challenges |
| **Respect** | Respect each other as capable, independent people |
| **Courage** | Do the right thing and tackle tough problems; raise uncomfortable truths |

**Key nuance: Courage vs Openness.** Openness is the steady habit of being transparent. Courage is the harder act of confronting a problem or speaking an unwelcome truth. These are the two most commonly confused values on the exam.

**Misconception to avoid.** Adding non-values to the list — Trust, Simplicity, and especially **Transparency** (that's a pillar, not a value).

**Worked example.** Mid-Sprint, a Developer realises the Sprint Goal no longer delivers value after a competitor's launch. Speaking up is **Courage**. The team then re-plans with the PO. Clinging to the now-pointless plan "to honour our commitment" misreads Commitment — which is to the *goal and each other*, not a sunk plan.

**How questions come.**
- *"Which value drives a Developer to raise an unpopular truth about quality?"* → **Courage** (not Openness).
- *"Which value keeps the team working toward the Sprint Goal despite distractions?"* → **Focus**.
- *"Which is NOT a Scrum value?"* → **Transparency**.
- *"Success with Scrum depends on ___."* → becoming **more proficient in living all five values**.

---

## A5. Scrum as a Framework (lightweight, immutable, incomplete)

**What it is.** Scrum is a **lightweight framework** that is **purposefully incomplete** and, as defined in the Guide, **immutable**.

**How immutable and incomplete coexist.**
- **Incomplete**: Scrum defines only the minimum — accountabilities, events, artifacts, and the rules binding them — as a *container* for other techniques. You add what your context needs. Kanban practices are exactly such an addition.
- **Immutable**: you can implement only parts, but the result is *not Scrum*. The components are interdependent, so removing one undermines the rest.

**Misconception to avoid.** "Immutable means we can't change how we work." No — it means you can't *drop* Scrum's defined elements. You're expected to add complementary practices around them.

**Worked example.** A team keeps Sprints and Planning but permanently cancels the Retrospective "to save time." Because the parts are interdependent, the result is not Scrum — they've removed the team's primary inspect-and-adapt-the-process loop.

**How questions come.**
- *"Why is the Scrum Guide intentionally incomplete?"* → teams **adapt practices to their context**; it's a framework, not a methodology.
- *"A team uses only some of Scrum."* → possible, but **the result is not Scrum**.
- *"Adding Kanban changes Scrum?"* → **No** — Kanban adds practices within the unchanged framework.

---

*Next: [Part B — The Scrum Team](/blog/psk1-scrum-team/) — structure, the three accountabilities, and the self-management questions that trip people up.*
