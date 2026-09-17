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
SOURCE OF TRUTH: outline.md (kept in ../../SUSE/CNDS-Norway-2026/outline.md)
describes Jeroen's original v1, 19-slide order. This file has diverged from
that numbering after a 2026-09-17 storytelling pass (added a "the fix,
formalized" slide, cut a redundant "sovereignty as culture" slide, briefly
merged "the other lens" + "from the fjord to the stack" then split them
back apart, added a presenter-intro slide, added a "the money behind it"
slide) and is at 21 slides — treat outline.md as content/timing reference
only, never as a slide-number map for this file. This file replaces
deck.html as the editable source; palette/type conventions from HANDOFF.md
are in style.css. Speaker split not yet confirmed with Jeroen (options
a/b/c in brief.md). S8-S12 currently carry Andrés's drafted notes for
split option (a); adjust the handoff lines in S7/S8/S12 notes if the
split changes.
-->

<div class="kicker">Cloud Native Days Norway · 26–27 Oct 2026</div>

# Friheten i Koden
### Digital Sovereignty for the Nordic Age

<div class="mt-6 muted">Jeroen van Erp · Andrés Valero · SUSE</div>

<svg class="longship-motif absolute bottom-10 right-10 w-40 opacity-80" viewBox="0 0 200 90" fill="none" stroke="#E2A63D" stroke-width="1.6">
  <path d="M10 70 Q100 95 190 70 L175 75 Q100 88 25 75 Z" />
  <path d="M25 70 L25 20 Q35 10 45 20 L45 70" />
  <path d="M35 20 L35 5" />
  <path d="M20 30 L50 30 M18 45 L52 45 M18 58 L52 58" />
</svg>

---
layout: default
class: text-center
---

<div class="kicker">S2 · your speakers</div>

# Two voices, one deck

<div class="flex items-start justify-center gap-20 mt-16">
<div class="text-center">
<div class="mx-auto" style="width:140px;height:140px;border-radius:50%;border:1.6px solid #E2A63D;display:flex;align-items:center;justify-content:center;font-family:var(--fk-serif);font-size:2.4rem;color:#E2A63D">JE</div>
<div class="mt-4 text-xl" style="font-family:var(--fk-serif)">Jeroen van Erp</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
<div class="text-center">
<div class="mx-auto" style="width:140px;height:140px;border-radius:50%;border:1.6px solid #E2A63D;display:flex;align-items:center;justify-content:center;font-family:var(--fk-serif);font-size:2.4rem;color:#E2A63D">AV</div>
<div class="mt-4 text-xl" style="font-family:var(--fk-serif)">Andrés Valero</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
</div>

<!--
Added 2026-09-17 per Andrés: presenter-intro slide, both speakers on one
slide, right after the title. PLACEHOLDER PHOTOS: the circles are just
initials on a thin gold ring (matches the deck's no-photos-yet, line-icon
aesthetic) since no headshot files have been provided. To swap in real
photos: replace each placeholder div's content with
<img src="./jeroen.jpg" style="width:140px;height:140px;border-radius:50%;
object-fit:cover;border:1.6px solid #E2A63D"/> (same for Andrés), add the
image files to this repo, and reference them by relative path. Title line
is intentionally identical for both per Andrés ("same title as me") —
Andrés's fuller title (Arm Ambassador, focus areas) was deliberately left
off to keep both entries symmetric; ask if Jeroen wants his own expanded.
-->

---
layout: default
---

<div class="kicker">S3 · the image we carry</div>

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

<div class="kicker">S4 · the other lens</div>

# The engineering story

<div class="grid-4 mt-6">
<div class="panel">
<div class="stat-num">1</div>
Knowledge and tools: they built their own ships (oak, rope, sails, iron), made where they lived
</div>
<div class="panel">
<div class="stat-num">2</div>
The world was open. They traded and explored from Newfoundland to Baghdad, and never needed to source capability from another power
</div>
<div class="panel">
<div class="stat-num">3</div>
And they defended it: they protected themselves and their families
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

<div class="kicker">S5 · from the fjord to the stack</div>

<div class="text-left max-w-3xl mx-auto mt-10 text-xl">
Today's cloud demands the same mindset. AWS/Azure/GCP are not the enemy.
This talk won't pretend otherwise.
</div>

<div class="text-left max-w-4xl mx-auto mt-10 text-6xl gold" style="font-family:var(--fk-serif); font-weight:600; line-height:1.15">
Dependency without contingency is.
</div>

<!--
Split back out 2026-09-17 per Andrés: this was briefly merged into S3, then
un-merged on request. S4 no longer opens with the old "They sailed their
own ships, charted their own routes..." quote (that repeated panel 1 of
S3), just the two closing lines: the pivot to today's cloud, then the
thesis line, now sized way up (text-6xl, serif) since it's the central,
most important line on the slide, not a secondary punctuation line.
-->

---
layout: default
---

<div class="kicker">S6 · the spine</div>

# Sovereignty as an engineering property

<div class="muted mt-2">The boardroom talks about it. But sovereignty gets built, or broken, in pull requests.</div>

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

<div class="kicker">S7 · the threat model techies should know</div>

# The US CLOUD Act

<div class="mt-4 text-xl">A remote-access API you can't close.</div>
<div class="muted mt-2 max-w-3xl">
It applies to any US-jurisdiction entity: US authorities can compel disclosure
of data the company "controls," including data sitting in <code>eu-west-1</code>.
The region logo is not a firewall.
</div>

<div class="quote-block mt-8">
"No, I cannot guarantee it."
</div>
<div class="muted text-sm">Anton Carniaux, Microsoft France director of public &amp; legal affairs, under oath · French Senate inquiry commission, 10 June 2025</div>

<div class="mt-6 muted text-sm">GDPR/DPF don't block it (DPF upheld at General Court, Sep 2025, on appeal; Schrems II context).</div>

<div class="mt-8 text-xl">
The fix: <span class="gold">control the keys, know your jurisdiction chain, keep an off-ramp.</span>
</div>

<!--
Fixed quote (was invented and longer in deck.html v1, see deck-review-notes.md
#3). Real event: French Senate inquiry hearing, 10 Jun 2025. Real speaker:
Anton Carniaux (named individual, not "Microsoft's French subsidiary").
Handoff bridge into S8 (Andrés, if split option a/b holds):
"So that's the threat model. What does actually fixing it get called?"

(This used to bridge straight into a procurement-budget line, but that
belongs to the EU pivot, not here. S8 now carries it into S9 instead. See
S8's own comment for the storytelling rationale.)
-->

---
layout: default
---

<div class="kicker">S8 · the fix, formalized</div>

# Two words for "keep an off-ramp"

<div class="muted mt-2 max-w-2xl">S7 ended on a fix, not a framework. Here's a name for it.</div>

<div class="panel mt-6 max-w-2xl">
<div class="steel font-mono text-sm">SUSE · OPERATIONAL DEFINITION OF SOVEREIGNTY</div>
<div class="mt-3"><span class="gold">Exit velocity</span>: how fast, and how costly, it actually is to leave a provider.</div>
<div class="mt-2"><span class="gold">Pivotability</span>: can you adapt when the conditions around you change, not just when you plan to.</div>
<div class="mt-3 muted">An industry framework (Jun 2026), anchored in open architecture, not contract terms. Not a product.</div>
</div>

<div class="mt-8 muted max-w-2xl">Why it matters: gives engineers something to build against, not just legal language to sign. The architecture section of this talk (S13 onward) is this axis in practice.</div>

<!--
ANDRÉS: rewritten 2026-09-17 per Andrés's own storytelling review, NOT yet
reviewed by Jeroen. Original version of this slide compared the EU Cloud
Sovereignty Framework side by side with SUSE's definition, but that
duplicated work S9-S12 already do for the EU side (S9's timeline literally
names "the SEAL rubric" and S11 is titled "Borrow the vocabulary", so
pre-naming SEAL here undercut that reveal), and it competed with S6's own
"PORTABILITY" attribute for the audience's attention. Cut the EU panel
entirely. This slide now does one job only: put an industry name on the
"control the keys, know your jurisdiction chain, keep an off-ramp" line S7
already ended on, so "exit velocity" and "pivotability" read as a
formalization of what was just said, not a competing framework.

Source: SUSE "What Is Digital Sovereignty? An Operational Framework for IT
Leaders" (suse.com/c/an-operational-definition-for-digital-sovereignty, 16
Jun 2026, Andreas Prins). Naming SUSE here is still a deliberate exception
to the "no vendor pitching" rule for CNCF-adjacent talks: this cites SUSE's
own public research and vocabulary, like citing Gartner, not a product. No
product names appear. Still worth Jeroen's explicit sign-off given the
house rule, since he owns final content decisions on the deck.

Handoff bridge from S7 (Andrés, if split option a/b holds): "So that's the
threat model. What does actually fixing it get called?" Then walk the two
terms, don't read them verbatim.

Handoff bridge into S9's timeline (moved here from S7's old bridge line,
since it fits the EU regulatory pivot better than it fit right after the
CLOUD Act): "So that's the engineer's definition. Now, why is this
suddenly a line item in a procurement budget, and not just a compliance
footnote?"
-->

---
layout: default
---

<div class="kicker">S9 · why now: three dates that matter to engineers</div>

# Nine months, four dates

<div class="grid-2 mt-6">
<div class="panel">
<div class="gold font-mono">12 Sep 2025</div>
Data Act Art. 25 in force for new data-processing contracts. Switching rights become contractual: interoperable export, no artificial obstacles, "without undue delay." Legacy long-term contracts covered by 2027.
</div>
<div class="panel">
<div class="gold font-mono">20 Oct 2025</div>
EC publishes Cloud Sovereignty Framework (CSF) + €180M sovereign cloud tender.
</div>
<div class="panel">
<div class="gold font-mono">17 Apr 2026</div>
Tender awarded to 4 providers, scored on the SEAL rubric. Sovereignty is now a procurement line item with budget.
</div>
<div class="panel">
<div class="gold font-mono">3 Jun 2026</div>
Technological Sovereignty Package / CADA generalizes it + unblocks EUCS certification.
</div>
</div>

<div class="mt-6 muted">Gartner: sovereign IaaS spend $6.9B ('25) → $23.1B ('27). Structural shift, not a fad.</div>

<!--
ANDRÉS: ~90s. Target block S8-S12, drafted for split option (a). Not yet
confirmed with Jeroen, see brief.md.

Frame before the dates: "Four things happened in about nine months that
turned this from a policy conversation into a budget line."

- 12 Sep 2025, Data Act: the one that actually touches your contracts.
  A provider can't just say no anymore, and can't drag it out indefinitely.
- 20 Oct 2025, Cloud Sovereignty Framework: EU didn't just regulate, they
  built a scoring system, and put €180M behind a tender using it.
- 17 Apr 2026, tender awarded: not theoretical, four named providers won,
  scored against the framework in the next slide.
- 3 Jun 2026, Technological Sovereignty Package: be careful with this one
  (see optional CADA aside below).
- Close on the Gartner number as the "why should I, a techie, care" payoff.

[OPTIONAL, verbal only, not on slide] CADA aside: "One thing worth knowing
if you go looking afterward: this same package created a second sovereignty
scale, with different numbers, for public-sector workloads, and its top
tiers require a certificate that hasn't been written yet." Say it dry, same
energy as "no such thing as a SEAL-3 product" in S11.

[OPTIONAL, verbal only] Gaia-X aside if the audience clearly knows the name:
"If you're thinking 'didn't Europe already try this with Gaia-X?', yes,
and it ran into the same sovereignty-washing problem we're about to see in
this tender award." Only if it flows naturally.

DORA (application 17 Jan 2025) / NIS2 (transposition 17 Oct 2024) are
intentionally not on the slide. Mention only as a spoken one-liner if time
allows: "regulators now ask: if your provider fails or is compelled, what's
your plan?"
-->

---
layout: default
---

<div class="kicker">S10 · the money behind it</div>

# $23.1B by 2027

<div class="flex items-stretch justify-center gap-3 mt-6 text-center" style="max-width:1300px; margin-left:auto; margin-right:auto">
<div class="panel" style="flex:1">
<div class="gold text-3xl" style="font-family:var(--fk-serif)">$6.9B</div>
<div class="steel font-mono text-xs mt-1">2025</div>
</div>
<div class="steel flex items-center text-xl">→</div>
<div class="panel" style="flex:1">
<div class="gold text-3xl" style="font-family:var(--fk-serif)">$12.6B</div>
<div class="steel font-mono text-xs mt-1">2026</div>
</div>
<div class="steel flex items-center text-xl">→</div>
<div class="panel" style="flex:1">
<div class="gold text-3xl" style="font-family:var(--fk-serif)">$23.1B</div>
<div class="steel font-mono text-xs mt-1">2027</div>
</div>
</div>

<div class="mt-3 muted text-sm text-center">Gartner: worldwide sovereign cloud IaaS spend. A budget line, not a marketing trend.</div>

<div class="mt-6 panel">
<div class="steel font-mono text-sm">CADA · TECHNOLOGICAL SOVEREIGNTY PACKAGE, 3 JUN 2026</div>
<div class="mt-2">A second sovereignty scale, separate from SEAL, for public-sector and critical workloads. Its top tiers legally require an EUCS certificate that doesn't exist yet, worth knowing before someone asks you for "a CADA score."</div>
</div>

<div class="mt-6 text-lg max-w-3xl">What it means for engineering and ops teams: procurement starts asking for a score, not a promise. Keep an exit-plan doc, an SBOM, and an answer to "who holds the keys" ready before the RFP does.</div>

<!--
Added 2026-09-17 per Andrés, NOT yet reviewed by Jeroen. New slide, S9 left
untouched on purpose. Does three things: (1) gives the Gartner number its
own slide with the full 3-point trajectory (2025/2026/2027) instead of the
compressed 2-point version in S9's footline, (2) puts CADA on screen for
the first time, it was previously only an "[OPTIONAL, verbal only]" aside
in S9's speaker notes, easy to cut under time pressure and never seen by
anyone reading the deck without audio, (3) translates both into one
concrete, simple action for engineering/ops instead of leaving "why should
I care" implicit.

Source for the fuller Gartner trajectory: press release 9 Feb 2026
(gartner.com/en/newsroom/press-releases/2026-02-09-gartner-says-worldwide-
sovereign-cloud-iaas-spending-will-total-us-dollars-80-billion-in-2026),
corroborated by ITPro and Computerworld coverage, cross-checked in this
project's deck-review-notes.md (2026-09-11 session). CADA facts sourced
the same place as the CADA aside already in S9's notes.

ANDRÉS: ~30-40s, keep it tight, this is a bridge slide not a deep dive.
Say, roughly: "One numbers slide, then we'll move fast." Walk the three
numbers as one beat, don't over-explain the trajectory. On CADA: "One
thing worth knowing so you're never caught flat-footed: there's a second
sovereignty scale, not the one we're about to cover, with a certificate
requirement that literally doesn't exist yet." Land the closing line as
the "so what" and move straight into S11's SEAL vocabulary.

Housekeeping: S9's speaker notes still carry the original "[OPTIONAL,
verbal only, not on slide] CADA aside" — that's now redundant since CADA
is on-screen here. Left it alone per instruction not to touch S9 yet;
worth trimming from S9's notes in a follow-up pass so the same fact isn't
duplicated in two places with different framing.
-->

---
layout: default
---

<div class="kicker">S11 · SEAL: the cloud sovereignty maturity model</div>

# Borrow the vocabulary

<div class="mt-6">
<div class="seal-row"><div class="seal-bar" style="width:8%"></div><div><b class="gold">SEAL-0</b> no sovereignty: us-east-1 because it was cheaper, the default</div></div>
<div class="seal-row"><div class="seal-bar" style="width:28%"></div><div><b class="gold">SEAL-1</b> jurisdictional: EU region, GDPR; parent still US</div></div>
<div class="seal-row"><div class="seal-bar" style="width:50%"></div><div><b class="gold">SEAL-2</b> data: BYOK in EU HSM, audit rights, exit clauses</div></div>
<div class="seal-row"><div class="seal-bar" style="width:72%"></div><div><b class="gold">SEAL-3</b> digital resilience: EU entity, EU operators, EU certification</div></div>
<div class="seal-row"><div class="seal-bar" style="width:95%"></div><div><b class="gold">SEAL-4</b> full: EU-only supply chain in the critical path (rare)</div></div>
</div>

<div class="quote-block mt-8">SEAL-1 is GDPR compliance with a Brussels accent, not sovereignty.</div>

<div class="mt-6 muted">Ratings are per objective, per procurement. There's no such thing as "a SEAL-3 product."</div>

<!--
ANDRÉS: ~90s.

Open: "The EU didn't just write policy, they gave us a maturity model, and
if you've ever worked with a CMMI or DevOps maturity model, this will feel
familiar."

Walk the ladder fast, add one beat of color per level (don't repeat the
on-screen lines verbatim):
- SEAL 0: "The default nobody chose on purpose, just where it was cheapest."
- SEAL 1: land "Brussels accent" as the laugh line, then move on quickly.
- SEAL 2: "This is where it starts costing engineering time, not just a
  contract signature. BYOK means someone owns key rotation now."
- SEAL 3: "For most regulated workloads, this is the realistic ceiling."
- SEAL 4: one line, don't dwell. "Rare, and usually not worth it unless
  you're told to be there."

SLOW DOWN for the footline: "Ratings are per objective, per procurement.
There is no such thing as 'a SEAL-3 product.'" Pause after. This is the
line that stops someone asking procurement for "a SEAL-3 vendor."
-->

---
layout: default
---

<div class="kicker">S12 · the 8 objectives, in engineer-speak</div>

# What the Commission actually scores

<div class="muted mt-1 text-sm">8 Sovereignty Objectives (SOV), each rated 0–4 on the SEAL scale from the last slide. The weights below add up to that rating.</div>

<table class="table-tight mt-3">
<thead>
<tr><th>Objective</th><th>Weight</th><th>Engineer-speak</th></tr>
</thead>
<tbody>
<tr><td>SOV-1 Strategic</td><td>15%</td><td>Can it keep operating if the vendor's government pulls the plug?</td></tr>
<tr><td>SOV-2 Legal</td><td>10%</td><td>Jurisdiction of the entity that controls the keys and the code</td></tr>
<tr><td>SOV-3 Data &amp; AI</td><td>10%</td><td>Cryptographic control, auditable access, EU-governed models</td></tr>
<tr><td>SOV-4 Operational</td><td>15%</td><td>Can EU people run/migrate it? docs, operator pool</td></tr>
<tr><td><b class="gold">SOV-5 Supply chain</b></td><td><b class="gold">20%</b></td><td>SBOMs, firmware/hardware provenance: "hardest to fake"</td></tr>
<tr><td>SOV-6 Technology</td><td>15%</td><td>Open, documented APIs; open source; CNCF-aligned tooling</td></tr>
<tr><td>SOV-7 Security</td><td>10%</td><td>ISO 27001, SecNumCloud/BSI C5, EUCS, audit rights</td></tr>
<tr><td>SOV-8 Environmental</td><td>5%</td><td>PUE, carbon/water disclosure</td></tr>
</tbody>
</table>

<div class="mt-4 muted">The Commission's own words: "hardest to fake" = supply chain. Translation: what's actually in your stack?</div>

<!--
ANDRÉS: ~60s. This is the droppable block if behind schedule (Jeroen's
stated fallback: fold into S11).

Added 2026-09-17: the "8 Sovereignty Objectives... add up to that rating"
line under the title, so the table doesn't land cold. Say it, don't skip
it: "The SEAL rating you just saw isn't one number, it's a blend of eight
of these, each weighted." Then: "Here's the translation, engineer to
engineer." Don't read all eight. The table is meant to be scanned. Call out
the two extremes by weight:
- Lightest: SOV-8, environmental, 5%. One breath, move on.
- Heaviest: SOV-5, supply chain, 20%. Spend remaining seconds here.

[OPTIONAL, verbal only] SOV-5: name SLSA (supply-chain levels for software
artifacts) as the real standard behind "SBOMs, firmware/hardware provenance."
[OPTIONAL, verbal only] SOV-6: CNCF shipped a conformance program late last
year specifically to stop AI/GPU workloads locking into one cloud's stack.
That's what "CNCF-aligned" cashes out to. (No vendor pitching: CNCF program
only, not a SUSE product.)

Handback to Jeroen: "So that's what's being measured, and by whom. Jeroen's
going to show you what actually building toward it looks like."
-->

---
layout: default
---

<div class="kicker">S13 · what "off-ramp ready" looks like</div>

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

<div class="kicker">S14 · lock-in anti-patterns</div>

# Each one seals the ramp: the one-line fix

<div class="mt-4 text-sm">

| Anti-pattern | Fix |
|---|---|
| Serverless as a black hole: business logic in proprietary functions | Extract to containers/K8s, keep vendor functions as thin glue |
| Proprietary SDK-only features on hot paths | Wrap behind an interface; keep the abstraction at the seam |
| Vendor-specific SQL / stored procedures / managed-DB magic | Stay on portable Postgres surface |
| Telemetry/DNS/identity glued to one vendor | Self-hosted alternatives (OpenTelemetry, own DNS/identity) |
| "We'll figure out the exit when we need it" | The default that makes SEAL-2 impossible |

</div>

---
layout: default
---

<div class="kicker">S15 · walk one workload up the ladder</div>

# Fintech, 4 years, one workload

<div class="grid-4 mt-4 text-sm">
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-0</div>us-east-1 · <span class="muted">the starting point</span>
<div class="mt-2 steel font-mono" style="font-size:0.7rem">DEVELOPER</div>
<div class="muted">Lambda + RDS, AWS SDK hardcoded in handlers. No exit in mind.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-1</div>EU region · <span class="muted">"almost nothing changed"</span>
<div class="mt-2 steel font-mono" style="font-size:0.7rem">DEVELOPER</div>
<div class="muted">One Terraform variable: region. Zero app code touched.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-2</div>BYOK in EU HSM · <span class="muted">audit rights, 60-day exit</span>
<div class="mt-2 steel font-mono" style="font-size:0.7rem">DEVELOPER</div>
<div class="muted">KMS wrapped behind an interface, envelope encryption. Key rotation now owned.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-3</div>EU provider · <span class="muted">self-managed Postgres, EU entity</span>
<div class="mt-2 steel font-mono" style="font-size:0.7rem">DEVELOPER</div>
<div class="muted">The big refactor: Lambda → containers on K8s. RDS → vanilla Postgres.</div>
</div>
</div>

<div class="mt-6 text-lg gold">≈ €500K over 4 years ≈ 6 basis points of annual volume at maturity.</div>
<div class="mt-1 muted">Affordable if you start now. Under a regulator's deadline, it's a project, not an option.</div>

<!--
Added 2026-09-17 per Andrés: developer-adaptation row under each SEAL stage,
so the ladder isn't just a procurement/legal view. It shows what actually
changes in the codebase at each step. Mirrors the S14 anti-pattern fixes
and the S8 "exit velocity" framing (SEAL-1 costs nothing in code; SEAL-2/3
is where engineering time actually goes). Say the DEVELOPER line per panel
instead of reading the top line. The top line is the procurement/legal
view.

Layout note: content was overflowing the 1080px canvas after adding the
DEVELOPER rows (checked via `npx slidev export --format png --range 13`,
see the fix commit). Panel copy trimmed, padding tightened, and the old
separate "each step is specific engineering work" line dropped since the
DEVELOPER rows now say that directly. Re-check with the same export command
after any further edits to this slide.
-->

---
layout: default
class: text-center
---

<div class="kicker">S16 · measure yourself: be honest</div>

# Four questions

<div class="text-left max-w-2xl mx-auto mt-4 grid gap-3">
<div class="panel" style="padding:0.7rem 1.1rem">1. Where does your primary provider's parent pay taxes and answer to law?</div>
<div class="panel" style="padding:0.7rem 1.1rem">2. Who holds the encryption keys for your most sensitive data, and under whose jurisdiction?</div>
<div class="panel" style="padding:0.7rem 1.1rem">3. Do you have a documented, tested exit plan? (Actually run one.)</div>
<div class="panel" style="padding:0.7rem 1.1rem">4. If your provider received a non-EU legal order tomorrow, would you know, and could you keep operating?</div>
</div>

<div class="mt-4 kicker">keep your hand up if you can answer, out loud, right now</div>

<div class="mt-2 text-xl gold">Answer honestly and you have a sovereignty posture.</div>

<!--
Audience-interaction moment. This is a live show-of-hands bit, not a silent
pause. Facilitation:

1. Before Q1, tell the room the rule: "Put your hand up. Keep it up only if
   you can answer this one out loud, right now, with a straight face. No
   Googling, no 'I'd have to check.'"
2. Read Q1, pause 3-4 seconds, scan the room. Most hands stay up (it's the
   easy one).
3. Read Q2, pause. Expect the first real drop. Don't comment on the drop
   yet, just keep going.
4. Read Q3, pause. This is usually where most hands go down ("tested exit
   plan" filters out "we have a plan" from "we've run it").
5. Read Q4, pause. Land the beat: "Look around. However many hands are
   still up, that's how many people in this room actually have a
   sovereignty posture today. Everyone else has a belief."
6. Then deliver the gold line: "Answer honestly and you have a sovereignty
   posture." Don't call on anyone by name or ask people to justify a raised
   or lowered hand. It's a private gut-check made visible, not a quiz.

Do not rush this slide. If the room is too big or too formal for hands
(seated theater style, streamed talk), fall back to: "Count on your own
fingers, don't show anyone" and still do the beat in step 5 verbally
("some of you just ran out of fingers").
Cut 2026-09-17 (storytelling review, applied per Andrés): a slide called
"sovereignty as culture, not bolt-on" used to sit here. Its 3 lines didn't
add new information: one restated the portability-gate action slide almost
verbatim, one restated the architecture/anti-patterns slides, one restated
the deck's own early thesis. The title also promised an
organizational/culture angle the bullets never delivered (no ownership,
incentives, or onboarding, just more architecture). This slide (the
self-assessment questions) now leads straight into bring-home below, which
is a clean transition on its own: "answer honestly and you have a
sovereignty posture" into "three things you can do Monday morning."
-->

---
layout: default
class: text-center
---

<div class="kicker">S17 · bring-home</div>

# Three things you can do Monday morning

<div class="muted mt-2">No executive sign-off required.</div>

<div class="flex items-stretch justify-center gap-4 mt-10 text-left" style="max-width:1400px; margin-left:auto; margin-right:auto">
<div class="panel" style="flex:1">
<div class="stat-num">01</div>
<div class="gold text-xl mt-2">BUILD it</div>
<div class="muted mt-2 text-sm">One PR, ~1 day. Ship one off-ramp.</div>
</div>
<div class="steel flex items-center text-2xl">→</div>
<div class="panel" style="flex:1">
<div class="stat-num">02</div>
<div class="gold text-xl mt-2">TEST it</div>
<div class="muted mt-2 text-sm">Quarterly. Run it like a DR drill.</div>
</div>
<div class="steel flex items-center text-2xl">→</div>
<div class="panel" style="flex:1">
<div class="stat-num">03</div>
<div class="gold text-xl mt-2">make it a HABIT</div>
<div class="muted mt-2 text-sm">Three lines in every PR or ADR.</div>
</div>
</div>

<!--
Made more visual 2026-09-17 per Andrés: was 3 gold words floating in a
4-column grid (asymmetric for 3 items) with a lot of dead space below.
Reused existing motifs instead of inventing new ones: the big serif
.stat-num numerals from S4, the panel style used everywhere else, and the
→ arrow glyph from S4's "own ships → transparency/control" mapping, to
keep this consistent with the rest of the deck rather than a one-off
design. Each panel's description previews the next 3 slides (S18, S19,
S20) so this doubles as a visual table of contents for the closing block,
not just 3 disconnected words. No icon-topper cards, no gradients, per
HANDOFF.md's established "do not revert" design rules.
-->

---
layout: default
---

<div class="kicker">S18 · action 1</div>

# Ship one off-ramp

<div class="muted">One PR, ~1 day.</div>

<div class="mt-6 grid gap-3">
<div class="panel">Second region in the IaC: exit becomes a variable, not a project</div>
<div class="panel">Customer-managed keys (BYOK) on your most sensitive store</div>
<div class="panel">One proprietary SDK call wrapped behind an interface</div>
</div>

<div class="mt-6 muted">Deliverable: a merged PR. No new tooling, no budget, no exec sign-off.</div>
<div class="quote-block mt-6">You don't have to leave today. You just have to be able to leave.</div>

---
layout: default
---

<div class="kicker">S19 · action 2</div>

# Run an off-ramp test

<div class="muted">On your most lock-in-exposed workload, quarterly. Run it like a DR drill.</div>

<div class="mt-6 panel">
Snapshot + export + import into a second environment (other region, other provider, or an on-prem VM).
</div>

<div class="mt-6">
Verify: does export work in standard formats? Do keys follow? Does the app start on vanilla Postgres / S3-compatible storage?
</div>

<div class="mt-6 muted">Data Act Art. 25 makes switching rights contractual. Learn the gaps now, not at contract renewal in 2027.</div>

---
layout: default
---

<div class="kicker">S20 · action 3</div>

# A portability gate in your review habit

<div class="mt-6 panel">
Every new managed service / SDK / proprietary feature answers three lines in the PR or ADR:
</div>

<div class="mt-6 grid gap-3 text-xl">
<div class="gold">What's the cost to leave?</div>
<div class="gold">Who holds the keys?</div>
<div class="gold">What's the off-ramp?</div>
</div>

<div class="mt-8 muted">A team norm, not a tool. One line in the PR description is enough. That's the habit that turns sovereignty from policy into code.</div>

---
layout: default
class: text-center
---

<div class="kicker">S21 · close</div>

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
