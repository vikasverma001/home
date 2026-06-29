+++
title = "Experience Cloud self-service portal — Case Study"
description = "A secure, CRM-integrated self-service portal that let members resolve common requests on their own."
css = "case-study"
date = 2024-06-01
weight = 10
emoji = "🏦"
industry = "Banking"
headcolor = "proj-head-sage"
filters = "salesforce integration"
summary_short = "Secure Experience Cloud portal integrated to core CRM. Members self-serve common requests. −31% inbound tickets."
metrics = ["−31% inbound tickets", "SSO + role security"]
stack = ["Experience Cloud", "SSO", "CRM Integration"]
+++
<div class="page-wrap cs-wrap">
<a class="cs-back" href="/projects/">← All projects</a>
<div class="cs-hero">
<div class="cs-eyebrow"><span class="cs-emoji">🏦</span> Banking · Case Study</div>
<h1>Experience Cloud self-service portal</h1>
<p class="cs-tagline">A secure, CRM-integrated self-service portal that let members resolve common requests on their own.</p>
<div class="cs-meta"><div class="cs-meta-item"><span class="cs-meta-label">Role</span><span class="cs-meta-val">Solutions Architect</span></div><div class="cs-meta-item"><span class="cs-meta-label">Timeframe</span><span class="cs-meta-val">~7 months</span></div><div class="cs-meta-item"><span class="cs-meta-label">Industry</span><span class="cs-meta-val">Banking</span></div></div>
</div>
<div class="cs-metrics"><div class="cs-metric"><div class="cs-metric-num">−31%</div><div class="cs-metric-label">Inbound tickets</div></div><div class="cs-metric"><div class="cs-metric-num">SSO</div><div class="cs-metric-label">Single sign-on</div></div><div class="cs-metric"><div class="cs-metric-num">24/7</div><div class="cs-metric-label">Self-service</div></div><div class="cs-metric"><div class="cs-metric-num">Role</div><div class="cs-metric-label">Based access</div></div></div>
<div class="cs-note">✎ Draft case study — figures and specifics are illustrative placeholders. We’ll refine these together.</div>
<section class="cs-section"><h2>The challenge</h2><p>Members called or emailed for routine requests — statements, status checks, simple updates — that did not need an agent. Volume was high, costs were rising, and members wanted to self-serve on their own schedule.</p><p>In banking, the catch is security: any portal had to enforce strict identity, least-privilege access, and a defensible sharing model.</p></section>
<section class="cs-section"><h2>Approach</h2><div class="cs-phases"><div class="cs-phase"><div class="cs-phase-num">01</div><div class="cs-phase-body"><h3>Requirements &amp; security model</h3><p>Defined the request types to self-serve and the identity, authentication, and data-access rules each would require.</p></div></div><div class="cs-phase"><div class="cs-phase-num">02</div><div class="cs-phase-body"><h3>Identity &amp; SSO</h3><p>Integrated single sign-on so members authenticate against the existing identity provider, not a separate login.</p></div></div><div class="cs-phase"><div class="cs-phase-num">03</div><div class="cs-phase-body"><h3>Sharing &amp; access</h3><p>Designed a role- and sharing-based access model so members see only their own records, enforced at the platform level.</p></div></div><div class="cs-phase"><div class="cs-phase-num">04</div><div class="cs-phase-body"><h3>Portal build</h3><p>Built the Experience Cloud portal with self-service flows for the highest-volume request types.</p></div></div><div class="cs-phase"><div class="cs-phase-num">05</div><div class="cs-phase-body"><h3>Integration &amp; launch</h3><p>Connected the portal to the core CRM as the system of record and launched in stages with monitoring.</p></div></div></div></section>
<section class="cs-section"><h2>How it fit together</h2><div class="cs-arch"><div class="cs-arch-row"><div class="cs-arch-tag">Identity</div><p>SSO against the existing IdP; no separate credentials to manage or breach.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">Access control</div><p>Role-based sharing ensures members can only ever see and act on their own data.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">Self-service flows</div><p>Guided flows handle the highest-volume requests end to end without an agent.</p></div><div class="cs-arch-row"><div class="cs-arch-tag">CRM integration</div><p>The core CRM remains the system of record; the portal reads and writes through it.</p></div></div><div class="cs-diagram">Architecture / flow diagram — to add</div></section>
<section class="cs-section"><h2>Outcomes</h2><ul class="cs-outcomes"><li>Inbound tickets for routine requests fell roughly 31%.</li><li>Members self-serve 24/7 against a secure, SSO-backed portal.</li><li>A role-based sharing model gives a defensible, least-privilege access posture.</li><li>Agents were freed to focus on complex, high-value member needs.</li></ul></section>
<section class="cs-section"><h2>Tools &amp; tech</h2><div class="cs-stack"><span>Experience Cloud</span><span>SSO</span><span>CRM Integration</span><span>Sharing Model</span><span>Security</span></div></section>
<section class="cs-section cs-reflection"><h2>Reflections</h2><p>In regulated industries the security model is the architecture. Designing access and sharing first — before any UI — is what made this portal launchable.</p></section>
<div class="cs-next"><a href="/projects/">← Back to all projects</a><a href="/contact/">Discuss this work →</a></div>
</div>