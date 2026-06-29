+++
title = "Service Cloud rebuild for a national retail brand — Case Study"
description = "Consolidating three disconnected support tools into one Service Cloud org — and cutting average handle time by more than a third."
css = "case-study"
date = 2025-09-01
weight = 10
emoji = "🛒"
industry = "Retail"
headcolor = "proj-head-sage"
filters = "salesforce service"
summary_short = "Three support tools consolidated into one org with omni-channel routing. −38% handle time."
metrics = ["−38% avg. handle time", "3→1 tools consolidated", "+22pts CSAT", "65% cases self-served"]
stack = ["Service Cloud", "Omni-Channel", "Flows", "Knowledge", "Experience Cloud"]
+++
<div class="page-wrap cs-wrap">
<a class="cs-back" href="/projects/">← All projects</a>
<div class="cs-hero">
<div class="cs-eyebrow"><span class="cs-emoji">🛒</span> Retail · Case Study</div>
<h1>Service Cloud rebuild for a national retail brand</h1>
<p class="cs-tagline">Consolidating three disconnected support tools into one Service Cloud org — and cutting average handle time by more than a third.</p>
<div class="cs-meta"><div class="cs-meta-item"><span class="cs-meta-label">Role</span><span class="cs-meta-val">Lead Solutions Architect</span></div><div class="cs-meta-item"><span class="cs-meta-label">Timeframe</span><span class="cs-meta-val">~9 months</span></div><div class="cs-meta-item"><span class="cs-meta-label">Industry</span><span class="cs-meta-val">Retail</span></div></div>
</div>
<div class="cs-metrics"><div class="cs-metric"><div class="cs-metric-num">−38%</div><div class="cs-metric-label">Avg. handle time</div></div><div class="cs-metric"><div class="cs-metric-num">3→1</div><div class="cs-metric-label">Support tools</div></div><div class="cs-metric"><div class="cs-metric-num">+22pts</div><div class="cs-metric-label">CSAT</div></div><div class="cs-metric"><div class="cs-metric-num">65%</div><div class="cs-metric-label">Cases self-served</div></div></div>

<section class="cs-section"><h2>The challenge</h2><p>The brand ran customer support across three overlapping systems — a legacy ticketing tool, a shared inbox, and a spreadsheet-driven escalation process. Agents toggled between tabs, context was lost on every handoff, and reporting was effectively impossible.</p><p>Leadership wanted a single source of truth, faster resolution, and a self-service layer to absorb the most common requests — without disrupting the busy holiday support season.</p></section>
<section class="cs-section"><h2>Approach</h2><div class="cs-phases"><div class="cs-phase"><div class="cs-phase-num">01</div><div class="cs-phase-body"><h3>Discovery &amp; audit</h3><p>Mapped every channel, queue, and escalation path across the three tools, and quantified volume by request type to find the highest-leverage consolidation targets.</p></div></div><div class="cs-phase"><div class="cs-phase-num">02</div><div class="cs-phase-body"><h3>Unified case model</h3><p>Designed one case object and data model that all channels write into, with record types and a clean status lifecycle replacing three incompatible schemas.</p></div></div><div class="cs-phase"><div class="cs-phase-num">03</div><div class="cs-phase-body"><h3>Omni-channel routing</h3><p>Implemented skills-based Omni-Channel routing so cases land with the right agent the first time, with presence-based load balancing.</p></div></div><div class="cs-phase"><div class="cs-phase-num">04</div><div class="cs-phase-body"><h3>Self-service deflection</h3><p>Stood up a Help Center on Experience Cloud backed by a curated knowledge base, deflecting the top request types before they became cases.</p></div></div><div class="cs-phase"><div class="cs-phase-num">05</div><div class="cs-phase-body"><h3>Rollout &amp; enablement</h3><p>Phased migration by region with agent training, macros, and a two-week hypercare window to stabilize before peak season.</p></div></div></div></section>
<section class="cs-section"><h2>How it fit together</h2><div class="cs-arch"><div class="cs-arch-row"><div class="cs-arch-tag">System of record</div><p>Service Cloud holds the canonical case, contact, and account state — every channel reads from and writes to it.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">Channel layer</div><p>Email-to-case, web-to-case, and chat all feed the unified case model through Omni-Channel.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">Automation</div><p>Flows, assignment rules, and macros handle triage, routing, and repetitive agent actions.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">Self-service</div><p>Experience Cloud Help Center surfaces knowledge articles and deflects common requests.</p></div></div><div class="cs-diagram">Architecture / flow diagram — to add</div></section>
<section class="cs-section"><h2>Outcomes</h2><ul class="cs-outcomes"><li>Average handle time dropped 38% within two quarters of go-live.</li><li>Three tools collapsed into one, eliminating duplicate licensing and tab-switching.</li><li>Self-service resolved roughly 65% of the most common request types.</li><li>CSAT rose 22 points as routing accuracy and first-contact resolution improved.</li></ul></section>
<section class="cs-section"><h2>Tools &amp; tech</h2><div class="cs-stack"><span>Service Cloud</span><span>Omni-Channel</span><span>Flows</span><span>Knowledge</span><span>Experience Cloud</span></div></section>
<section class="cs-section cs-reflection"><h2>Reflections</h2><p>The biggest win was not the technology — it was agreeing on one case lifecycle everyone trusted. Once the data model was clean, automation and reporting fell into place quickly.</p></section>
<div class="cs-next"><a href="/projects/">← Back to all projects</a><a href="/contact/">Discuss this work →</a></div>
</div>