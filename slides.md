---
theme: default
title: Friheten i Koden
info: |
  ## Friheten i Koden: Digital Sovereignty for the Nordic Age
  Cloud Native Days Norway 2026 · Jeroen van Erp + Andrés Valero
class: text-center
transition: fade
mdc: true
fonts:
  sans: -apple-system
  serif: Georgia
  mono: ui-monospace
---

<!--
SOURCE OF TRUTH: outline.md (19-slide structure, timing, sources) — kept in
../../SUSE/CNDS-Norway-2026/outline.md. This file replaces deck.html as the
editable source; palette/type conventions from HANDOFF.md are in style.css.
Speaker split not yet confirmed with Jeroen (options a/b/c in brief.md) —
S7-S9 currently carry Andrés's drafted notes for split option (a); adjust
the handoff lines in S6/S7/S9 notes if the split changes.
-->

<div class="kicker">Cloud Native Days Norway · 26–27 Oct 2026</div>

# Friheten i Koden
### Digital Sovereignty for the Nordic Age

<div class="mt-6 muted">Jeroen van Erp · Andrés Valero — SUSE</div>

<svg class="longship-motif absolute bottom-10 right-10 w-40 opacity-80" viewBox="0 0 200 90" fill="none" stroke="#E2A63D" stroke-width="1.6">
  <path d="M10 70 Q100 95 190 70 L175 75 Q100 88 25 75 Z" />
  <path d="M25 70 L25 20 Q35 10 45 20 L45 70" />
  <path d="M35 20 L35 5" />
  <path d="M20 30 L50 30 M18 45 L52 45 M18 58 L52 58" />
</svg>

---
layout: default
---

<div class="kicker">S2 · the image we carry</div>

# Picture what you saw as a kid

<div class="grid-2 mt-8">
<div class="term">
beard<br/>axe<br/>longship<br/><span class="muted"># that's all we remember</span>
</div>
<div class="panel">
Bearded men. Axes. Burning ships.<br/>
Conquering. Raiding. Taking what other people built.
</div>
</div>

<div class="mt-10 text-xl gold">Now look through the other lens.</div>

<!--
Beat: pause after "Now look through the other lens." Let it breathe before S3.
-->

---
layout: default
---

<div class="kicker">S3 · the other lens</div>

# The engineering story

<div class="grid-4 mt-6">
<div class="panel">
<div class="stat-num">1</div>
Knowledge & tools — built their own ships (oak, rope, sails, iron), made where they lived
</div>
<div class="panel">
<div class="stat-num">2</div>
The world was open — traded and explored from Newfoundland to Baghdad; never needed to source capability from another power
</div>
<div class="panel">
<div class="stat-num">3</div>
And they defended it — protected themselves and their families
</div>
<div class="panel">
Each leg maps forward:<br/>
own ships → <span class="steel">transparency/control</span><br/>
no foreign sourcing → <span class="steel">jurisdiction/supply chain</span><br/>
self-defense → <span class="steel">contingency/off-ramp</span>
</div>
</div>

<div class="quote-block mt-8">The image we carry is a film about their ships. The truth is an engineering story about capability.</div>

<!--
Positioning: sovereignty = CAPABILITY, not isolation. The trading point
pre-empts "is this anti-cloud?" before it's asked.
-->

---
layout: default
class: text-center
---

<div class="kicker">S4 · from the fjord to the stack</div>

<div class="quote-block text-left max-w-3xl mx-auto mt-10">
They sailed their own ships, charted their own routes, and never handed control of their journey to a foreign power.
</div>

<div class="text-left max-w-3xl mx-auto mt-8 text-xl">
Today's cloud demands the same mindset. AWS/Azure/GCP are not the enemy.
This talk won't pretend otherwise.
</div>

<div class="text-left max-w-3xl mx-auto mt-8 text-2xl gold">
Dependency without contingency is.
</div>

---
layout: default
---

<div class="kicker">S5 · the spine</div>

# Sovereignty as an engineering property

<div class="muted mt-2">The boardroom talks about it. But sovereignty is being built — or broken — in pull requests.</div>

<div class="grid-4 mt-8">
<div class="panel"><div class="gold font-mono text-sm">JURISDICTION</div>whose law can reach this workload</div>
<div class="panel"><div class="gold font-mono text-sm">CONTROL</div>who holds the keys, the identity, the data</div>
<div class="panel"><div class="gold font-mono text-sm">PORTABILITY</div>how hard is it to leave (the off-ramp)</div>
<div class="panel"><div class="gold font-mono text-sm">TRANSPARENCY</div>can you audit the stack? (open source, docs, SBOM)</div>
</div>

<div class="mt-8 muted">All four are properties of your architecture, not of a logo.</div>

---
layout: default
---

<div class="kicker">S6 · the threat model techies should know</div>

# The US CLOUD Act

<div class="mt-4 text-xl">A remote-access API you can't close.</div>
<div class="muted mt-2 max-w-3xl">
Applies to any US-jurisdiction entity — US authorities can compel disclosure
of data the company "controls," including data sitting in <code>eu-west-1</code>.
The region logo is not a firewall.
</div>

<div class="quote-block mt-8">
"No, I cannot guarantee it."
</div>
<div class="muted text-sm">— Anton Carniaux, Microsoft France director of public &amp; legal affairs, under oath · French Senate inquiry commission, 10 June 2025</div>

<div class="mt-6 muted text-sm">GDPR/DPF don't block it (DPF upheld at General Court, Sep 2025, on appeal — Schrems II context).</div>

<div class="mt-8 text-xl">
The fix is not "don't use the cloud." It's: <span class="gold">control the keys, know your jurisdiction chain, keep an off-ramp.</span>
</div>

<!--
Fixed quote (was invented/longer in deck.html v1 — see deck-review-notes.md #3).
Real event: French Senate inquiry hearing, 10 Jun 2025. Real speaker: Anton
Carniaux (named individual, not "Microsoft's French subsidiary").
Handoff bridge into S7 (Andrés, if split option a/b holds):
"So that's the threat model. Now — why is this suddenly a line item in a
procurement budget, and not just a compliance footnote?"
-->

---
layout: default
---

<div class="kicker">S7 · why now — three dates that matter to engineers</div>

# Nine months, four dates

<div class="grid-2 mt-6">
<div class="panel">
<div class="gold font-mono">12 Sep 2025</div>
Data Act Art. 25 in force for new data-processing contracts — switching rights become contractual: interoperable export, no artificial obstacles, "without undue delay." Legacy long-term contracts covered by 2027.
</div>
<div class="panel">
<div class="gold font-mono">20 Oct 2025</div>
EC publishes Cloud Sovereignty Framework (CSF) + €180M sovereign cloud tender.
</div>
<div class="panel">
<div class="gold font-mono">17 Apr 2026</div>
Tender awarded to 4 providers, scored on the SEAL rubric — sovereignty is now a procurement line item with budget.
</div>
<div class="panel">
<div class="gold font-mono">3 Jun 2026</div>
Technological Sovereignty Package / CADA generalizes it + unblocks EUCS certification.
</div>
</div>

<div class="mt-6 muted">Gartner: sovereign IaaS spend $6.9B ('25) → $23.1B ('27). Structural shift, not a fad.</div>

<!--
ANDRÉS — ~90s. Target block S7-S9, drafted for split option (a) (not yet
confirmed with Jeroen — see brief.md).

Frame before the dates: "Four things happened in about nine months that
turned this from a policy conversation into a budget line."

- 12 Sep 2025 — Data Act: the one that actually touches your contracts.
  A provider can't just say no anymore, and can't drag it out indefinitely.
- 20 Oct 2025 — Cloud Sovereignty Framework: EU didn't just regulate, they
  built a scoring system, and put €180M behind a tender using it.
- 17 Apr 2026 — tender awarded: not theoretical, four named providers won,
  scored against the framework in the next slide.
- 3 Jun 2026 — Technological Sovereignty Package: be careful with this one
  (see optional CADA aside below).
- Close on the Gartner number as the "why should I, a techie, care" payoff.

[OPTIONAL, verbal only, not on slide] CADA aside: "One thing worth knowing
if you go looking afterward: this same package created a second sovereignty
scale, with different numbers, for public-sector workloads — and its top
tiers require a certificate that hasn't been written yet." Say it dry, same
energy as "no such thing as a SEAL-3 product" in S8.

[OPTIONAL, verbal only] Gaia-X aside if the audience clearly knows the name:
"If you're thinking 'didn't Europe already try this with Gaia-X?' — yes,
and it ran into the same sovereignty-washing problem we're about to see in
this tender award." Only if it flows naturally.

DORA (application 17 Jan 2025) / NIS2 (transposition 17 Oct 2024) are
intentionally not on the slide — mention only as a spoken one-liner if time
allows: "regulators now ask: if your provider fails or is compelled, what's
your plan?"
-->

---
layout: default
---

<div class="kicker">S8 · SEAL — the cloud sovereignty maturity model</div>

# Borrow the vocabulary

<div class="mt-6">
<div class="seal-row"><div class="seal-bar" style="width:8%"></div><div><b class="gold">SEAL-0</b> no sovereignty — us-east-1 because it was cheaper, the default</div></div>
<div class="seal-row"><div class="seal-bar" style="width:28%"></div><div><b class="gold">SEAL-1</b> jurisdictional — EU region, GDPR; parent still US</div></div>
<div class="seal-row"><div class="seal-bar" style="width:50%"></div><div><b class="gold">SEAL-2</b> data — BYOK in EU HSM, audit rights, exit clauses</div></div>
<div class="seal-row"><div class="seal-bar" style="width:72%"></div><div><b class="gold">SEAL-3</b> digital resilience — EU entity, EU operators, EU certification</div></div>
<div class="seal-row"><div class="seal-bar" style="width:95%"></div><div><b class="gold">SEAL-4</b> full — EU-only supply chain in the critical path (rare)</div></div>
</div>

<div class="quote-block mt-8">SEAL-1 is GDPR compliance with a Brussels accent, not sovereignty.</div>

<div class="mt-6 muted">Ratings are per objective, per procurement — there's no such thing as "a SEAL-3 product."</div>

<!--
ANDRÉS — ~90s.

Open: "The EU didn't just write policy, they gave us a maturity model — and
if you've ever worked with a CMMI or DevOps maturity model, this will feel
familiar."

Walk the ladder fast, add one beat of color per level (don't repeat the
on-screen lines verbatim):
- SEAL 0: "The default nobody chose on purpose — just where it was cheapest."
- SEAL 1: land "Brussels accent" as the laugh line, then move on quickly.
- SEAL 2: "This is where it starts costing engineering time, not just a
  contract signature — BYOK means someone owns key rotation now."
- SEAL 3: "For most regulated workloads, this is the realistic ceiling."
- SEAL 4: one line, don't dwell — "Rare, and usually not worth it unless
  you're told to be there."

SLOW DOWN for the footline: "Ratings are per objective, per procurement.
There is no such thing as 'a SEAL-3 product.'" Pause after. This is the
line that stops someone asking procurement for "a SEAL-3 vendor."
-->

---
layout: default
---

<div class="kicker">S9 · the 8 objectives, in engineer-speak</div>

# What the Commission actually scores

<table class="mt-4 text-sm">
<thead>
<tr><th>Objective</th><th>Weight</th><th>Engineer-speak</th></tr>
</thead>
<tbody>
<tr><td>SOV-1 Strategic</td><td>15%</td><td>Can it keep operating if the vendor's government pulls the plug?</td></tr>
<tr><td>SOV-2 Legal</td><td>10%</td><td>Jurisdiction of the entity that controls the keys and the code</td></tr>
<tr><td>SOV-3 Data &amp; AI</td><td>10%</td><td>Cryptographic control, auditable access, EU-governed models</td></tr>
<tr><td>SOV-4 Operational</td><td>15%</td><td>Can EU people run/migrate it? docs, operator pool</td></tr>
<tr><td><b class="gold">SOV-5 Supply chain</b></td><td><b class="gold">20%</b></td><td>SBOMs, firmware/hardware provenance — "hardest to fake"</td></tr>
<tr><td>SOV-6 Technology</td><td>15%</td><td>Open, documented APIs; open source; CNCF-aligned tooling</td></tr>
<tr><td>SOV-7 Security</td><td>10%</td><td>ISO 27001, SecNumCloud/BSI C5, EUCS, audit rights</td></tr>
<tr><td>SOV-8 Environmental</td><td>5%</td><td>PUE, carbon/water disclosure</td></tr>
</tbody>
</table>

<div class="mt-6 muted">The Commission's own words: "hardest to fake" = supply chain. Translation: what's actually in your stack?</div>

<!--
ANDRÉS — ~60s. This is the droppable block if behind schedule (Jeroen's
stated fallback: fold into S8).

Frame: "The Commission scores providers on eight objectives. Here's the
translation, engineer to engineer." Don't read all eight — table is meant
to be scanned. Call out the two extremes by weight:
- Lightest: SOV-8, environmental, 5%. One breath, move on.
- Heaviest: SOV-5, supply chain, 20% — spend remaining seconds here.

[OPTIONAL, verbal only] SOV-5: name SLSA (supply-chain levels for software
artifacts) as the real standard behind "SBOMs, firmware/hardware provenance."
[OPTIONAL, verbal only] SOV-6: CNCF shipped a conformance program late last
year specifically to stop AI/GPU workloads locking into one cloud's stack —
that's what "CNCF-aligned" cashes out to. (No vendor pitching — CNCF program
only, not a SUSE product.)

Handback to Jeroen: "So that's what's being measured, and by whom. Jeroen's
going to show you what actually building toward it looks like."
-->

---
layout: default
---

<div class="kicker">S10 · what "off-ramp ready" looks like</div>

# The architecture slide

<div class="grid-2 mt-6">
<div class="panel"><b class="steel">Portable primitives</b><br/>S3-compatible object storage, vanilla Postgres (no exotic extensions), OCI images, Kubernetes with standard CNI/CSI</div>
<div class="panel"><b class="steel">Keys under customer control</b><br/>Envelope encryption, BYOK/HYOK; KMS abstraction in the platform layer</div>
<div class="panel"><b class="steel">IaC as the off-ramp</b><br/>A second provider/region in the same IaC is a tested exit, not a hope</div>
<div class="panel"><b class="steel">Egress</b><br/>Standard export formats; telemetry/observability pipelines that survive a provider change</div>
</div>

---
layout: default
---

<div class="kicker">S11 · lock-in anti-patterns</div>

# Each one seals the ramp — the one-line fix

<div class="mt-4 text-sm">

| Anti-pattern | Fix |
|---|---|
| Serverless as a black hole — business logic in proprietary functions | Extract to containers/K8s, keep vendor functions as thin glue |
| Proprietary SDK-only features on hot paths | Wrap behind an interface; keep the abstraction at the seam |
| Vendor-specific SQL / stored procedures / managed-DB magic | Stay on portable Postgres surface |
| Telemetry/DNS/identity glued to one vendor | Self-hosted alternatives (OpenTelemetry, own DNS/identity) |
| "We'll figure out the exit when we need it" | The default that makes SEAL-2 impossible |

</div>

---
layout: default
---

<div class="kicker">S12 · walk one workload up the ladder</div>

# Fintech, 4 years, one workload

<div class="grid-4 mt-6 text-sm">
<div class="panel"><div class="gold">SEAL-0</div>us-east-1<br/><span class="muted">the starting point</span></div>
<div class="panel"><div class="gold">SEAL-1</div>EU region<br/><span class="muted">"almost nothing changed"</span></div>
<div class="panel"><div class="gold">SEAL-2</div>BYOK in EU HSM<br/><span class="muted">audit rights, 60-day exit clause</span></div>
<div class="panel"><div class="gold">SEAL-3</div>EU provider<br/><span class="muted">self-managed Postgres, EU legal entity</span></div>
</div>

<div class="mt-8 muted">Each step is specific engineering work: contracts + crypto, then migration + refactor (Lambda→K8s, RDS→Postgres).</div>
<div class="mt-4 text-xl gold">≈ €500K over 4 years ≈ 6 basis points of annual volume at maturity.</div>
<div class="mt-2 muted">Affordable — if you start now. Under a regulator's deadline, it's a project, not an option.</div>

---
layout: default
class: text-center
---

<div class="kicker">S13 · measure yourself — be honest</div>

# Four questions

<div class="text-left max-w-2xl mx-auto mt-6 grid gap-4">
<div class="panel">1. Where does your primary provider's parent pay taxes and answer to law?</div>
<div class="panel">2. Who holds the encryption keys for your most sensitive data — and under whose jurisdiction?</div>
<div class="panel">3. Do you have a documented, tested exit plan? (Actually run one.)</div>
<div class="panel">4. If your provider received a non-EU legal order tomorrow, would you know — and could you keep operating?</div>
</div>

<div class="mt-8 text-xl gold">Answer honestly and you have a sovereignty posture.</div>

<!--
Audience-interaction moment — pause and let the room answer silently before
moving on. Do not rush this slide.
-->

---
layout: default
---

<div class="kicker">S14 · sovereignty as culture, not bolt-on</div>

# Name the trade-offs explicitly

<div class="mt-6 grid gap-4">
<div class="panel">"Cost to leave" becomes a required field in architecture reviews — like RPO/RTO</div>
<div class="panel">Build abstraction where lock-in risk is highest: data, keys, identity, IaC</div>
<div class="panel">Portability as a first-class architectural concern — not a compliance-team afterthought at the end of the project</div>
</div>

---
layout: default
class: text-center
---

<div class="kicker">S15 · bring-home</div>

# Three things you can do Monday morning

<div class="muted mt-2">No executive sign-off required.</div>

<div class="grid-4 mt-10 text-2xl">
<div class="gold">BUILD it</div>
<div class="gold">TEST it</div>
<div class="gold">make it a HABIT</div>
</div>

---
layout: default
---

<div class="kicker">S16 · action 1</div>

# Ship one off-ramp

<div class="muted">One PR, ~1 day.</div>

<div class="mt-6 grid gap-3">
<div class="panel">Second region in the IaC — exit becomes a variable, not a project</div>
<div class="panel">Customer-managed keys (BYOK) on your most sensitive store</div>
<div class="panel">One proprietary SDK call wrapped behind an interface</div>
</div>

<div class="mt-6 muted">Deliverable: a merged PR. No new tooling, no budget, no exec sign-off.</div>
<div class="quote-block mt-6">You don't have to leave today — you just have to be able to leave.</div>

---
layout: default
---

<div class="kicker">S17 · action 2</div>

# Run an off-ramp test

<div class="muted">On your most lock-in-exposed workload, quarterly — run it like a DR drill.</div>

<div class="mt-6 panel">
Snapshot + export + import into a second environment (other region, other provider, or an on-prem VM).
</div>

<div class="mt-6">
Verify: does export work in standard formats? Do keys follow? Does the app start on vanilla Postgres / S3-compatible storage?
</div>

<div class="mt-6 muted">Data Act Art. 25 makes switching rights contractual — learn the gaps now, not at contract renewal in 2027.</div>

---
layout: default
---

<div class="kicker">S18 · action 3</div>

# A portability gate in your review habit

<div class="mt-6 panel">
Every new managed service / SDK / proprietary feature answers three lines in the PR or ADR:
</div>

<div class="mt-6 grid gap-3 text-xl">
<div class="gold">What's the cost to leave?</div>
<div class="gold">Who holds the keys?</div>
<div class="gold">What's the off-ramp?</div>
</div>

<div class="mt-8 muted">A team norm, not a tool. One line in the PR description is enough — the habit that turns sovereignty from policy into code.</div>

---
layout: default
class: text-center
---

<div class="kicker">S19 · close</div>

<svg class="longship-motif w-32 mx-auto mb-6" viewBox="0 0 200 90" fill="none" stroke="#E2A63D" stroke-width="1.6">
  <path d="M10 70 Q100 95 190 70 L175 75 Q100 88 25 75 Z" />
  <path d="M25 70 L25 20 Q35 10 45 20 L45 70" />
  <path d="M35 20 L35 5" />
  <path d="M20 30 L50 30 M18 45 L52 45 M18 58 L52 58" />
</svg>

# Your longship should be yours to sail.

<div class="mt-6 max-w-2xl mx-auto muted">
The EU just gave sovereignty a measurable definition and a budget. Ten years
from now off-ramp-ready will be the boring default; today it's a team habit
you can install on Monday.
</div>

<div class="mt-8 kicker">hierynomus.com/talks/cloud-native-days-norway-2026</div>
