---
theme: default
title: Friheten i Koden
info: |
  ## Friheten i Koden: Digital Sovereignty for the Nordic Age
  Cloud Native Days Norway 2026 · Jeroen van Erp + Andrés Valero
class: text-center
transition: fade
mdc: true
voyage: false
routerMode: hash
fonts:
  sans: -apple-system
  serif: Georgia
  mono: ui-monospace
---

<!--
Friheten i Koden: Digital Sovereignty for the Nordic Age
Cloud Native Days Norway, Bergen, 26-27 Oct 2026. Jeroen van Erp and Andrés Valero.

STORY LINE: the talk is one voyage with seven chapters. The three ship legs
are planted in I, named against the keel in II, and cashed in out loud in VI.
  I    The myth            S3-S6
  II   The keel            S7
  III  Foreign waters      S8
  IV   The charts          S9-S12
  V    Shipbuilding        S13-S20
  VI   Remember the ships  S21
  VII  Home port           S22-S26
  Feedback                 S27
Ship legs used everywhere: own ships = control + transparency; open seas, no
foreign master = jurisdiction + supply chain; built to turn back = the off-ramp.

Theme: style.css (Viking motifs, no runes or co-opted symbols) and
global-top.vue (the voyage bar). Timing: about 22 minutes of content in a
30-minute slot, with Q&A over the feedback slide.
-->

<Aurora />

<div class="kicker">Cloud Native Days Norway · 26–27 Oct 2026</div>

# Friheten i Koden

## Digital Sovereignty for the Nordic Age

<div class="mt-6 muted">Jeroen van Erp · Andrés Valero · SUSE</div>

<img src="/cnd/cnd-norway-logo.png" alt="Cloud Native Days Norway" class="absolute top-10 left-12" style="height:64px" />

<Longship :width="290" class="absolute bottom-12 right-12" />

---
layout: default
class: text-center
voyage: false
---

<div class="kicker">the crew</div>

# Two voices, one ship

<div class="flex items-start justify-center gap-20 mt-10">
<Axe :size="70" class="self-center opacity-90 flex-none" />
<div class="text-center">
<Shield class="mx-auto" :size="280" photo="/jeroen.jpg" a="#D0573F" b="#F3F0E8" />
<div class="mt-4 text-xl serif">Jeroen van Erp</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
<div class="text-center">
<Shield class="mx-auto" :size="280" photo="/andres.jpg" a="#4FA3A0" b="#E2A63D" />
<div class="mt-4 text-xl serif">Andrés Valero</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
<Axe :size="70" class="self-center opacity-90 flex-none" style="transform:scaleX(-1)" />
</div>

<!--
Quick intro, one line each: who we are and why two voices.
-->

---
layout: default
chapter: "I · The myth"
class: voyage-open
transition: view-transition
---

<div class="kicker">I · the myth</div>

# Picture what you saw as a kid

<div class="grid-2 mt-10">
<div class="term text-xl" style="line-height:1.8">
$ ls<br/>beard<br/>axe<br/>longship<br/><span class="muted"># that's all we remember</span>
</div>
<div class="panel flex items-center gap-5 text-lg">
<Viking variant="myth" :size="130" class="flex-none" style="view-transition-name:viking" />
<div>
Bearded men. Axes. Burning ships.<br/>
Conquering, raiding, sailing the oceans and taking what other people <span class="gold">built</span>.
<div class="mt-3 red text-xs font-mono">QUICK CHECK: WHO PICTURED HORNS?</div>
</div>
</div>
</div>

<div class="mt-12 text-3xl serif gold">Now look through the other lens.</div>

<!--
Ask the quick-check question out loud and wait for hands.

"Keep them up if you think Vikings actually wore them." Beat. "None did.
The horns come from costume designs for Wagner's Ring cycle, 1876. The
picture in your head was made up much later. Keep that in mind for the
rest of this talk."

Then pause after "Now look through the other lens." Let it breathe.
-->

---
layout: default
---

<div class="kicker">I · the other lens</div>

# Now picture the other image

<div class="grid-3 mt-6">
<div class="panel" v-click style="transition:opacity .4s ease .6s">
<div class="flex items-center gap-3"><Axe :size="44" /><div class="serif text-lg">Their own ships</div></div>
<div class="muted mt-1 text-sm">The knowledge and the tools to build them: oak, rope, sails, iron nails. Made where they lived.</div>
</div>
<div class="panel" v-click>
<div class="flex items-center gap-3"><Sail :size="44" /><div class="serif text-lg">Open seas</div></div>
<div class="muted mt-1 text-sm">They traded and sailed from Newfoundland to Baghdad. They never had to source their capability from another power.</div>
</div>
<div class="panel" v-click>
<div class="flex items-center gap-3"><Portage :size="44" /><div class="serif text-lg">Built to turn back</div></div>
<div class="muted mt-1 text-sm">Shallow hulls, the same shape at both ends. If the route closed, they turned round or hauled the ship overland to the next river.</div>
</div>
</div>

<div class="flex items-center gap-5 mt-6 helmet-row" :class="$clicks === 0 ? 'is-big' : 'is-moved'">
<div class="flex-none helmet-viking" :class="$clicks === 0 ? 'is-big' : 'is-moved'"><Viking variant="real" :size="70" style="view-transition-name:viking" /></div>
<div style="width:350px" class="flex-none" :class="{ 'helmet-text': $clicks === 0 }">
<div class="quote-block">The film shows their ships. The history shows people who could build them.</div>
<div class="mt-2 teal text-xs font-mono">THE REAL HELMET: ROUND, WITH AN EYE GUARD · GJERMUNDBU, NORWAY, 10TH CENTURY</div>
</div>
</div>

<!--
Plant the three legs and keep them simple: own ships, open seas,
built to turn back. Don't explain what they map to yet. The icons (axe,
sail, ship on rollers) come back every time a leg returns later in the talk. The keel slide names
it, and the "remember the ships" slide (S21) cashes it in.

Point at the helmet: "And this one is real. Found at Gjermundbu, right
here in Norway. Round, no horns." The open-seas leg answers "is this an anti-cloud talk?" before anyone asks.
-->

---
layout: default
---

<div class="kicker">I · two words people mix up</div>

# Who owns the ship? Who sails it?

<div class="grid-2 mt-6">
<div class="panel" v-click>
<div class="flex items-center gap-3"><Boathouse :size="44" /><div class="serif text-xl gold">Ownership</div></div>
<div class="steel font-mono text-xs mt-2">WHO OWNS THE SHIP?</div>
<div class="mt-2">The asset. The contract. The data in your region.</div>
<div class="muted mt-3 text-sm">The name on the hull, the deed to the boathouse.</div>
</div>
<div class="panel" v-click>
<div class="flex items-center gap-3"><Compass :size="44" /><div class="serif text-xl gold">Control</div></div>
<div class="steel font-mono text-xs mt-2">WHO SAILS THE SHIP?</div>
<div class="mt-2">Who sets the course? Who can stop it, or leave port when they choose?</div>
<div class="muted mt-3 text-sm">The hand on the tiller, and the freedom to turn the bow.</div>
</div>
</div>

<div class="mt-8 text-3xl serif" v-click>Ownership alone is not <span class="gold">sovereignty</span>. Control makes it real.</div>


<!--
Two words people mix up: Ownership = who owns the ship, Control =
who sails it. Keep it short, about 30 seconds.

Land it on the longship: nobody calls you free because your name is on the
hull if someone else holds the tiller. The next slide turns it into an
engineering test (cost to leave, can you audit), and the keel slide makes
CONTROL one of the four timbers.

Tie-back for later in the talk: dependency without contingency is what
ownership without control looks like. Lock-in is the same thing seen from
the migration side.
-->

---
layout: default
---

<div class="kicker">I · from the fjord to the stack</div>

<div class="flex items-center gap-6 mt-8">
<Mooring :size="90" class="flex-none" />
<div class="text-5xl gold serif" style="line-height:1.15;font-weight:600">The enemy is dependency without contingency.</div>
</div>

<div class="grid-2 mt-10">
<div class="panel flex items-center" style="min-height:8.5rem">
<div class="flex items-baseline gap-4"><div class="stat-num">01</div><div class="text-2xl">What does it cost you to leave?<div class="muted text-lg mt-2">Money, time, risk.</div></div></div>
</div>
<div class="panel flex items-center" style="min-height:8.5rem">
<div class="flex items-baseline gap-4"><div class="stat-num">02</div><div class="text-2xl">Can you audit who runs your systems?</div></div>
</div>
</div>

<div class="mt-8 text-xl gold text-center">Answer "we don't know" to either one, and what you bought is a dependency.</div>

<!--
The big thesis line on the left, the commercial test on the right. The test
lands before any EU material on purpose, so the room hears it as a global
engineering question.

Say before the big line: "Today's cloud asks for the same mindset. AWS,
Azure and GCP are great ports, and this talk won't pretend otherwise."

Say after the test: "This is global and commercial. Norway, Singapore or
Ohio, no regulator required."
-->

---
layout: default
chapter: "II · The keel"
class: voyage-open
opener: keel
---

<div class="kicker">II · the keel</div>

# Sovereignty is an engineering property

<div class="muted mt-2">Every longship starts with a keel. This one has four timbers, and the boardroom doesn't lay them. Pull requests do.</div>

<div class="grid-4 mt-8 keel">
<div class="panel" v-click><div class="gold font-mono text-sm">JURISDICTION</div>Whose law reaches your workload and the infra it runs on? Follow the parent entity, not the region logo.<span class="leg leg-icon"><Sail :size="24" /> open seas</span></div>
<div class="panel" v-click><div class="gold font-mono text-sm">CONTROL</div>Who holds the keys, the identity, the data?<span class="leg leg-icon"><Axe :size="20" /> their own ships</span></div>
<div class="panel" v-click><div class="gold font-mono text-sm">PORTABILITY</div>How hard is it to leave? No off-ramp? That's <span class="gold">vendor lock-in.</span><span class="leg leg-icon"><Portage :size="24" /> built to turn back</span></div>
<div class="panel" v-click><div class="gold font-mono text-sm">TRANSPARENCY</div>Can you audit the stack? Open source, docs, SBOMs.<span class="leg leg-icon"><Planks :width="34" /> planks in sight</span></div>
</div>

<div class="mt-8 muted">All four live in your architecture. You can measure them, and you can change them one PR at a time.</div>

<!--
About 60 seconds. One click per timber, one line each, then the tag:
Jurisdiction, open seas. Control, their own ships. Portability, built to
turn back. Transparency, planks in sight.

This is the one lens for the whole talk. Every later framework
points back here (the SOV table). Read the small tags
out loud once: "this is where the ships come back."

Transparency gets its own picture: Viking ships were clinker-built, planks
overlapping and riveted, every joint in plain sight. "Anyone on the beach
could see exactly how the ship was built. That's what an auditable stack
looks like."
-->

---
layout: default
chapter: "III · Foreign waters"
class: voyage-open
---

<div class="kicker">III · foreign waters</div>

<h1 style="font-size:2.1rem;max-width:80%">The CLOUD Act: a remote-access API you can't close</h1>

<div class="mt-4 text-xl muted" v-click="1">Sail in someone else's waters and you sail under their law.</div>

<div class="mt-8 text-3xl serif" v-click="1">The region logo is <span class="gold">not a firewall</span>.</div>

<div class="quote-block mt-12 cannot-quote" :class="$clicks === 0 ? 'is-big' : 'is-moved'" style="font-size:2.2rem">"No, I cannot guarantee it."</div>
<div class="muted text-sm mt-3" v-click="1">Anton Carniaux, Microsoft France director of public &amp; legal affairs, under oath · French Senate inquiry commission, June 2025</div>

<div class="mt-10 foot" v-click="1">GDPR and the EU–US Data Privacy Framework don't block it (DPF upheld at the General Court, Sep 2025, now on appeal).</div>

<!--
The emotional core of the talk. Let the five-word quote sit for a
second before reading the source line.

Explain the mechanism before the quote: "It applies to any US-jurisdiction
entity, wherever the data sits. US authorities can compel disclosure of data
the company controls, including data in eu-west-1."

Bridge: "That's the storm. So how do you navigate it? Time for the charts."
-->

---
layout: default
chapter: "IV · The charts"
class: voyage-open
---

<div class="kicker">IV · follow the trade</div>

# Sovereignty has a budget now

<div class="flex items-stretch justify-center gap-3 mt-14 text-center" style="max-width:1300px;margin-left:auto;margin-right:auto">
<div class="panel flex flex-col justify-center" v-click="1" style="flex:1;min-height:9.5rem">
<div class="gold text-6xl serif">$6.9B</div>
<div class="steel font-mono text-sm mt-2">2025</div>
</div>
<div class="steel flex flex-col items-center justify-center px-1" v-click="2"><div class="font-mono text-sm">+83%</div><div class="text-2xl">→</div></div>
<div class="panel flex flex-col justify-center" v-click="2" style="flex:1;min-height:9.5rem">
<div class="gold text-6xl serif">$12.6B</div>
<div class="steel font-mono text-sm mt-2">2026</div>
</div>
<div class="steel flex flex-col items-center justify-center px-1" v-click="3"><div class="font-mono text-sm">+84%</div><div class="text-2xl">→</div></div>
<div class="panel flex flex-col justify-center" v-click="3" style="flex:1;min-height:9.5rem">
<div class="gold text-6xl serif">$23.1B</div>
<div class="steel font-mono text-sm mt-2">2027</div>
</div>
</div>

<div class="mt-5 muted text-base text-center" v-click="4">Sovereign cloud IaaS spend in Europe. This is where budgets are moving.</div>

<div class="mt-10 text-xl max-w-3xl mx-auto text-center" v-click="5">IT and engineering teams are the ones who turn it into something real.</div>

<div class="foot text-center" style="position:absolute;left:0;right:0;bottom:5.8rem">Source: Gartner · <a href="https://www.gartner.com/en/newsroom/press-releases/2026-02-09-gartner-says-worldwide-sovereign-cloud-iaas-spending-will-total-us-dollars-80-billion-in-2026" target="_blank">gartner.com/en/newsroom</a>, 9 Feb 2026</div>

<!--
About 20 to 30 seconds. A bridge slide, keep it tight.

Open: "The Vikings followed the trade routes. So let's follow the money."
Five clicks, top to bottom: one per year box (the growth arrow comes in
with the box it points to), then the Europe line, then the closing line.
The Gartner source stays on screen the whole time. Keep the box clicks quick, one beat each, then
land the closing line plainly.

Move on with: "So what's actually driving that number? Four rules. One of
them went live this autumn."

These are the European figures, not worldwide (worldwide is about $80B for
2026). Gartner Table 1 (February 2026), Europe row in $M: 6,868 (2025) / 12,587 (2026) / 23,118 (2027).
Rounded on the slide to $6.9B / $12.6B / $23.1B. +83% in 2026; Europe
overtakes North America ($21.1B) in 2027. Worldwide: $80.4B in 2026.
Full URL: https://www.gartner.com/en/newsroom/press-releases/2026-02-09-gartner-says-worldwide-sovereign-cloud-iaas-spending-will-total-us-dollars-80-billion-in-2026
Q&A line if useful: "Europe passes North America next year."
-->

---
layout: default
---

<div class="kicker">IV · the charts</div>

# From nice-to-have to enforced

<div class="grid-4 mt-8 text-base">
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">DATA ACT · ART. 25</div>
<div class="mt-2 flex-1">Switching providers is a contractual right now. A provider can't just say no.</div>
<div class="mt-4 steel text-xs">Effective Sep 2025</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">CLOUD SOVEREIGNTY FRAMEWORK</div>
<div class="mt-2 flex-1">The EU's own scoring system, SEAL 0–4. A €180M tender was awarded on it to four providers.</div>
<div class="mt-4 steel text-xs">Published Oct 2025</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">TECH SOVEREIGNTY PACKAGE</div>
<div class="mt-2 flex-1">Brings <span class="gold">CADA</span>: a second sovereignty scale, numbered differently from SEAL. Unblocks EUCS.</div>
<div class="mt-4 steel text-xs">Proposed Jun 2026</div>
</div>
<div class="panel hot flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">CYBER RESILIENCE ACT</div>
<div class="mt-2 flex-1">Report exploited vulnerabilities within 24h/72h. SBOMs become mandatory by Dec 2027.</div>
<div class="mt-4 gold text-xs">Effective Sep 2026</div>
</div>
</div>

<div class="mt-8 text-lg">Two are law. One decides who wins public contracts. One is <span class="gold">on its way</span>.</div>

<div class="mt-6 foot">SEAL = Sovereignty Effective Assurance Levels · CADA = Cloud and AI Development Act · EUCS = European Cybersecurity Certification Scheme for Cloud Services · CRA = Cyber Resilience Act</div>

<!--
About 70 seconds. Lead with the rule's name, dates are secondary.
The one exception is CRA: "six weeks ago" is the hook, so say it.

- Data Act: the one that touches your contracts. Your provider can't drag an exit out forever.
- Cloud Sovereignty Framework: the EU built a scoring system and put €180M behind it. Four providers won, scored on the objectives and the ladder coming up.
  Winners, if asked (awarded 17 Apr 2026, up to €180M over six years, SEAL-2
  was the entry bar): Post Telecom (Luxembourg, with OVHcloud and Clever
  Cloud), STACKIT (Germany) and Scaleway (France) at SEAL-3; Proximus
  (Belgium, with S3NS, Thales-controlled, built with Google Cloud) at SEAL-2. CISPE
  called the Proximus/S3NS award "sovereignty washing" because S3NS runs on
  Google Cloud technology. Facts only, no opinion on any provider.
- Tech Sovereignty Package: say this one slowly. "CADA is a second scale with different numbers from SEAL. Its top tiers need an EUCS certificate that doesn't exist yet."
- CRA: "This one isn't coming. It started six weeks ago, and it's why SBOMs stopped being optional."

[OPTIONAL, verbal only] Gaia-X, if the room clearly knows the name: "Didn't
Europe try this with Gaia-X? Yes. It hit the same sovereignty-washing
problem we'll see in this tender."

DORA and NIS2 stay off the slide. One spoken line if time allows: "Regulators
now ask: if your provider fails or gets compelled, what's your plan? DORA
Art. 28 already requires audit rights and an exit plan for financial
entities."

Closing line, accuracy: Data Act and CRA are binding law. The Cloud
Sovereignty Framework is procurement scoring and CADA is still a proposal,
so don't say "all four are mandatory" out loud.
-->

---
layout: default
---

<div class="kicker">IV · what gets scored</div>

# The 8 objectives, in engineer-speak

<div class="mt-3">
<table class="table-tight">
<thead>
<tr><th>Objective</th><th>Weight</th><th>Engineer-speak</th></tr>
</thead>
<tbody>
<tr class="dim"><td>SOV-1 Strategic</td><td>15%</td><td>Can it keep running if the vendor's government pulls the plug?</td></tr>
<tr class="dim"><td>SOV-2 Legal</td><td>10%</td><td>Jurisdiction of whoever controls the keys and the code</td></tr>
<tr class="dim"><td>SOV-3 Data &amp; AI</td><td>10%</td><td>Cryptographic control, auditable access, EU-governed models</td></tr>
<tr><td><b>SOV-4 Operational</b></td><td>15%</td><td>Can EU people run and migrate it? No skilled <span class="gold">crew</span>, no voyage.</td></tr>
<tr><td><b class="gold">SOV-5 Supply chain</b></td><td><b class="gold">20%</b></td><td>"Hardest to fake": SBOMs and provenance. Since CRA, a legal deadline too.</td></tr>
<tr><td><b>SOV-6 Technology</b></td><td>15%</td><td>Open, documented APIs. Open source. CNCF-aligned tooling.</td></tr>
<tr class="dim"><td>SOV-7 Security</td><td>10%</td><td>ISO 27001, SecNumCloud / BSI C5, EUCS, audit rights</td></tr>
<tr class="dim"><td>SOV-8 Environmental</td><td>5%</td><td>PUE, carbon and water disclosure</td></tr>
</tbody>
</table>
</div>

<style>
table.table-tight th, table.table-tight td { padding: 0.4rem 0.9rem; font-size: 1rem; }
table.table-tight td:first-child { white-space: nowrap; }
</style>

<!--
About 60 seconds. If we're behind, skim it in about 20 seconds:
say only the SOV-5 line. Don't skip it, the SEAL slide refers back to it.

Open: "Before the scale, what actually gets scored: eight objectives,
weighted into one score."
Don't read all eight, the dimmed rows are there for completeness. Talk about
the three bright ones:
- SOV-4: "A perfect stack with nobody who can run it goes nowhere. That's the silent failure point."
- SOV-5: the heaviest, 20%. "Hardest to fake," and CRA made it a legal deadline.
- SOV-6: open APIs and open source, the part this room builds every day.

Close: "The heaviest weight is supply chain. The engineer's translation:
what's actually in your stack?"

[OPTIONAL, verbal only] SOV-5: name SLSA as the real standard behind
provenance. SOV-6: the CNCF conformance program for AI workloads, if it fits.
-->

---
layout: default
---

<div class="kicker">IV · the depth scale</div>

# SEAL: borrow the vocabulary

<div class="flex flex-col justify-center" style="height:calc(100% - 4rem)">
<div>
<div class="seal-row"><div class="seal-gauge"><i class="seg"></i><i class="seg"></i><i class="seg"></i><i class="seg"></i></div><div><b class="gold">SEAL-0</b> no sovereignty: us-east-1 because it was cheaper. The default.</div></div>
<div class="seal-row"><div class="seal-gauge"><i class="seg on" style="background:#E07B3C;border-color:#E07B3C"></i><i class="seg"></i><i class="seg"></i><i class="seg"></i></div><div><b class="gold">SEAL-1</b> jurisdictional: EU region, GDPR, parent still US</div></div>
<div class="seal-row"><div class="seal-gauge"><i class="seg on" style="background:#E2A63D;border-color:#E2A63D"></i><i class="seg on" style="background:#E2A63D;border-color:#E2A63D"></i><i class="seg"></i><i class="seg"></i></div><div><b class="gold">SEAL-2</b> data: BYOK, keys stay in the EU, audit rights, exit clauses</div></div>
<div class="seal-row"><div class="seal-gauge"><i class="seg on" style="background:#4FA3A0;border-color:#4FA3A0"></i><i class="seg on" style="background:#4FA3A0;border-color:#4FA3A0"></i><i class="seg on" style="background:#4FA3A0;border-color:#4FA3A0"></i><i class="seg"></i></div><div><b class="gold">SEAL-3</b> resilience: EU entity, EU operators, EU certification</div></div>
<div class="seal-row"><div class="seal-gauge"><i class="seg on" style="background:#5B8CC9;border-color:#5B8CC9"></i><i class="seg on" style="background:#5B8CC9;border-color:#5B8CC9"></i><i class="seg on" style="background:#5B8CC9;border-color:#5B8CC9"></i><i class="seg on" style="background:#5B8CC9;border-color:#5B8CC9"></i></div><div><b class="gold">SEAL-4</b> full: EU-only supply chain in the critical path. Rare.</div></div>
</div>

<div class="quote-block mt-10">SEAL-1 is GDPR compliance with a Brussels accent.</div>
</div>

<style>
.seal-gauge { display: flex; gap: 5px; flex: none; width: 26%; }
.seal-gauge .seg { flex: 1; height: 20px; border: 1px solid var(--fk-line); background: var(--fk-panel); border-radius: 2px; }
.seal-row { margin: 0.95rem 0; font-size: 1.3rem; }
</style>

<!--
About 90 seconds.

Open: "Sailors measure depth before they trust the water. The EU gave us a
depth scale: the 0 to 4 scale every one of those 8 objectives is rated on.
If you've used a CMMI or DevOps maturity model, it'll feel familiar."

One beat of color per level, don't read the lines:
- SEAL 0: "The default nobody picked on purpose."
- SEAL 1: land "Brussels accent" as the laugh line, move on fast.
- SEAL 2: "This is where it costs engineering time. BYOK means someone owns key rotation now."
  If asked where the keys live: in a hardware security module (HSM) in the
  EU. A foreign subpoena then gets ciphertext. Stronger still is HYOK: the
  key stays outside the provider and it calls out for each use.
- SEAL 3: "For most regulated workloads, this is the realistic ceiling."
- SEAL 4: "Rare, and only worth it if you're told to be there."

Closing line, now spoken only: "Ratings are per procurement. There's no
such thing as a SEAL-3 product." Slow down and pause after it. That's the
line that stops someone asking procurement for "a SEAL-3 vendor."

Bridge: "Every level above SEAL-1 comes down to one question: could you
leave if you had to? Having no answer to that is vendor lock-in. So let's
look at what being ready to leave looks like."

Q&A, if asked "is SEAL mandatory?": "No. It's the Commission's own buying
criteria, used in its €180M tender. It matters because it shows what the EU
rewards, and other public buyers may copy it."
-->

---
layout: default
chapter: "V · Shipbuilding"
class: voyage-open
---

<div class="kicker">V · shipbuilding</div>

# What "off-ramp ready" looks like

<div class="mt-3 text-2xl gold serif">How do you prevent vendor lock-in?</div>

<div class="grid-4 mt-8 text-base">
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">PORTABLE PRIMITIVES</div>
<div class="mt-2 flex-1">Open standards and open source any provider can run.</div>
<div class="mt-4 steel text-xs">S3 API · Postgres · OCI · K8s with CNI/CSI</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">IDENTITY + KEYS</div>
<div class="mt-2 flex-1">Open identity and your own encryption.</div>
<div class="mt-4 steel text-xs">Keycloak · OpenBao · BYOK/HYOK</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">IAC + OPEN FORMATS</div>
<div class="mt-2 flex-1">Leaving is a variable change and an export.</div>
<div class="mt-4 steel text-xs">OpenTofu · Crossplane · Velero</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="gold font-mono text-xs" style="min-height:2.4em">ENTERPRISE OPEN SOURCE</div>
<div class="mt-2 flex-1">Enterprise-ready open source platform layer: your vendor is a choice, not a cage.</div>
<div class="mt-4 steel text-xs">Cluster API · KubeVirt · RKE2</div>
</div>
</div>

<!--
Open with the question: "How do you prevent vendor lock-in?" Then the
answer: "Every box here works because it's open: open source code, or an
open standard you can take elsewhere." One line per click.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · leaks in the hull</div>

# Quiz: lock-in trap, or seaworthy?

<div class="flex items-center justify-center gap-6 mt-6">
<Axe :size="60" />
<Viking variant="real" :size="96" beard="#E2A63D" />
<Axe :size="60" style="transform:scaleX(-1)" />
</div>

<div class="mt-4 text-xl max-w-2xl mx-auto">Six real architecture choices.</div>
<div class="mt-4 text-lg muted max-w-2xl mx-auto">One at a time. Make your call before the click.</div>

<!--
The axe marks a trap (chop it out), the longship marks a seaworthy
choice. Make it a real pause: "Six real choices, one at a time. Before each
one, decide: trap, or something you'd ship? Then I click." Keep it light,
this is the fun beat. Two of the six are fine, so don't let the room
settle on "always trap" by item 3.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 1 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">Your workloads run in the EU region of a US hyperscaler. Data never leaves Europe.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Axe :size="34" /><span class="red font-mono text-lg">LOCK-IN TRAP</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">An EU region is SEAL-1 at best. The parent company's law still reaches it: the region logo is not a firewall.</div>
</div>

<!--
The trick opener: it sounds safe. "Hands up if you'd ship this." Pause,
then click. Callback: "Remember slide 8, the CLOUD Act." It's strictly a
sovereignty trap, not lock-in; don't split that hair on stage.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 2 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">Your checkout flow's business logic lives entirely inside serverless functions.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Axe :size="34" /><span class="red font-mono text-lg">LOCK-IN TRAP</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">Move it to containers on K8s. Keep vendor functions as thin glue.</div>
</div>

<!--
Read it, pause 3 to 4 seconds, then click. Don't say "black hole" before the
click, it gives the answer away.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 3 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">You use a proprietary SDK feature on your hottest code path, wrapped behind your own interface.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Longship :width="56" /><span class="teal font-mono text-lg">SEAWORTHY</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">The seam is yours. Swap the SDK later and no caller notices.</div>
</div>

<!--
The one most likely to fool the room. Read the whole sentence before the
pause: "wrapped behind your own interface" is the whole point.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 4 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">Your database leans on the provider's managed extensions and stored procedures.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Axe :size="34" /><span class="red font-mono text-lg">LOCK-IN TRAP</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">Stay on a portable open-source database, without the vendor magic.</div>
</div>

<!--
Examples to name out loud if useful: Postgres, MySQL, MariaDB. Don't present
Postgres as the only answer.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 5 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">Telemetry runs on OpenTelemetry, with your own DNS and identity provider.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Longship :width="56" /><span class="teal font-mono text-lg">SEAWORTHY</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">No single vendor holds your observability or your identity hostage.</div>
</div>

<!--
The quiet layers people forget: telemetry, DNS, identity. If your provider
owns all three, you can move the workload and still be blind and locked out.
OpenTelemetry means the data goes to whatever backend you choose.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 6 of 6</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">"We don't have a tested exit plan yet. We'll write one if we ever need it."</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Axe :size="34" /><span class="red font-mono text-lg">LOCK-IN TRAP</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">The default that makes SEAL-2 impossible.</div>
</div>

<!--
Land this one heavier. It's the attitude behind every other trap.
-->

---
layout: default
chapter: "VI · Remember the ships"
class: voyage-open
---

<div class="kicker">VI · remember the ships</div>

# Sovereignty lives in the crew

<div class="grid-3 mt-8">
<div class="panel" v-click style="min-height:10rem;padding:1.1rem 1.3rem">
<div class="flex flex-col items-start gap-3"><Axe :size="50" /><div class="serif text-xl whitespace-nowrap">Their own ships</div></div>
<div class="mt-2 gold text-lg">Control + transparency</div>
<div class="muted text-base mt-2">You hold the keys and you can audit the stack.</div>
</div>
<div class="panel" v-click style="min-height:10rem;padding:1.1rem 1.3rem">
<div class="flex flex-col items-start gap-3"><Sail :size="50" /><div class="serif text-xl whitespace-nowrap">Open seas</div></div>
<div class="mt-2 gold text-lg">Jurisdiction + supply chain</div>
<div class="muted text-base mt-2">You trade with everyone and answer to no foreign master.</div>
</div>
<div class="panel" v-click style="min-height:10rem;padding:1.1rem 1.3rem">
<div class="flex flex-col items-start gap-3"><Portage :size="50" /><div class="serif text-xl whitespace-nowrap">Built to turn back</div></div>
<div class="mt-2 gold text-lg">The off-ramp</div>
<div class="muted text-base mt-2">You can leave, and you've tested it.</div>
</div>
</div>

<div class="mt-8 text-xl" v-click>So make "cost to leave" a required field in every architecture review, right next to <code>RPO / RTO</code>.</div>

<!--
About 45 seconds. The callback that closes the loop planted in S4.
Open: "Remember the ships? This is them." One click per ship, read the gold
line only:
- Their own ships: control and transparency. "Transparency rides with
  control: you can't hold what you can't see."
- Open seas: jurisdiction and supply chain.
- Built to turn back: the off-ramp.

Title callback to SOV-4: "And none of it sails without a crew that can run it."
Land the culture line slowly: "Cost to leave, a required field, right next
to RPO and RTO."
-->

---
layout: default
class: text-center
chapter: "VII · Home port"
---

<div class="kicker">VII · home port</div>

# Three things you can do Monday morning

<div class="muted mt-2">No executive sign-off required.</div>

<div class="flex items-stretch justify-center gap-4 mt-10 text-left" style="max-width:1400px;margin-left:auto;margin-right:auto">
<div class="panel" v-click="1" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">01</div><Axe :size="40" /></div>
<div class="gold text-xl mt-2">CONTROL it</div>
<div class="steel font-mono text-xs mt-1">THEIR OWN SHIPS</div>
</div>
<div class="steel flex items-center text-2xl" v-click="2">→</div>
<div class="panel" v-click="2" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">02</div><Sail :size="40" /></div>
<div class="gold text-xl mt-2">INSPECT it</div>
<div class="steel font-mono text-xs mt-1">OPEN SEAS</div>
</div>
<div class="steel flex items-center text-2xl" v-click="3">→</div>
<div class="panel" v-click="3" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">03</div><Portage :size="40" /></div>
<div class="gold text-xl mt-2">make it a HABIT</div>
<div class="steel font-mono text-xs mt-1">BUILT TO TURN BACK</div>
</div>
</div>

<div class="quote-block mt-8 mx-auto" v-click="4" style="max-width:fit-content">You don't have to leave. You have to be able to leave.</div>

<!--
Rule of three, a visual table of contents for the next three slides.
Each action is one of the ships from the previous slide: say it out loud.
"Their own ships: you control it. Open seas: you inspect what comes aboard.
Built to turn back: you make the off-ramp test a habit." Then land the quote, it's the message of the talk.
-->

---
layout: default
---

<div class="flex items-center gap-3"><Axe :size="30" /><div class="kicker">VII · action 1 · control · their own ships</div></div>

# Control it

<div class="muted">Hold your own keys.</div>

<div class="grid-2 mt-8">
<div class="panel flex flex-col" v-click>
<div class="flex items-baseline gap-3"><div class="stat-num">01</div><div class="gold text-xl">Hold the keys</div></div>
<div class="mt-3">Customer-managed keys (BYOK) on your most sensitive store.</div>
<div class="term text-sm mt-auto" style="padding:0.6rem 0.8rem;line-height:1.8;margin-top:1rem">encryption:<br/>&nbsp;&nbsp;key: <span class="gold">customer-managed</span><br/>&nbsp;&nbsp;revoke: you</div>
</div>
<div class="panel flex flex-col" v-click>
<div class="flex items-baseline gap-3"><div class="stat-num">02</div><div class="gold text-xl">Wrap the SDK</div></div>
<div class="mt-3">One proprietary SDK call behind an interface you own.</div>
<div class="term text-sm mt-auto" style="padding:0.6rem 0.8rem;line-height:1.8;margin-top:1rem">type <span class="gold">BlobStore</span> interface {<br/>&nbsp;&nbsp;Put(key string, r io.Reader) error<br/>}</div>
</div>
</div>

<div class="mt-8 text-xl text-center">Deliverable: <span class="gold">one merged PR</span>. No new tooling, no budget.</div>

<!--
Callback: "Their own ships. Whoever holds the keys holds the ship."
Say: "Keys go on your most sensitive store. The wrapper goes around the SDK
call you'd least like to rewrite."
The BYOK line is SOV-3, the SDK wrapper is SOV-6, if anyone asks.
-->

---
layout: default
---

<div class="flex items-center gap-3"><Sail :size="30" /><div class="kicker">VII · action 2 · inspect · open seas</div></div>

# Inspect it

<div class="mt-2 text-xl">Know what's in the hold, then decide what gets on board.</div>

<div class="term mt-6 text-2xl" style="line-height:2;max-width:fit-content">
<span class="gold">$</span> SBOM for every image (SPDX or CycloneDX)<br/>
<span class="gold">$</span> signed, with provenance (SLSA)<br/>
<span class="gold">$</span> policy gate: unsigned or unknown? It doesn't ship.
</div>

<div class="mt-6 text-xl">CRA writes SBOMs into law. <span class="gold">SOV-5, the heaviest objective, scores them.</span></div>

<!--
Callback: "Open seas. You trade with everyone, but you inspect what comes
aboard." Planks in sight from the keel: you can only inspect what you can
see, and the SBOM is how you see it. The policy gate is where inspection
turns into a decision: OPA/Kyverno from slide 13.

Accuracy: the CRA's vulnerability reporting started 11 Sep 2026; the full
manufacturer obligations, SBOM included, apply from Dec 2027. Say "the law
already requires it" only for products in CRA scope.
-->

---
layout: default
---

<div class="flex items-center gap-3"><Portage :size="30" /><div class="kicker">VII · action 3 · habit · built to turn back</div></div>

# Make it a habit

<div class="muted">Run an off-ramp test. Quarterly and on the calendar, like any DR drill.</div>

<div class="flex items-stretch gap-3 mt-8">
<div class="panel" v-click="1" style="flex:1">
<div class="flex items-baseline gap-3"><div class="stat-num">01</div><div class="gold text-xl">Add</div></div>
<div class="mt-3">A second region or provider in the IaC. Leaving becomes a variable change.</div>
</div>
<div class="steel flex items-center text-2xl" v-click="2">→</div>
<div class="panel" v-click="2" style="flex:1">
<div class="flex items-baseline gap-3"><div class="stat-num">02</div><div class="gold text-xl">Move</div></div>
<div class="mt-3">Snapshot, export, import: another region, another provider or an on-prem VM.</div>
</div>
<div class="steel flex items-center text-2xl" v-click="3">→</div>
<div class="panel" v-click="3" style="flex:1.25">
<div class="flex items-baseline gap-3"><div class="stat-num">03</div><div class="gold text-xl">Verify</div></div>
<div class="term text-sm mt-3 whitespace-nowrap" style="padding:0.6rem 0.8rem;line-height:1.9">□ export in open formats?<br/>□ do the keys follow?<br/>□ runs on open standards?</div>
</div>
</div>

<div class="mt-8 text-xl text-center" v-click="4">Find the gaps on a quiet Tuesday, <span class="gold">not during an outage</span>.</div>

<!--
Callback: "Built to turn back. The off-ramp you've never driven is a
hope, not a plan." Same habit as a DR drill: small, scheduled, boring.

Walk the three steps fast. Start with one non-critical service. The
checklist is the point: every "no" is a gap you found on your own terms.
Slide 13 is where the open formats, keys and open standards come from.
If asked what "open standards" means here: an open-source database, an
S3-compatible object API, OCI images, plain Kubernetes.
-->

---
layout: default
class: text-center
---

<Aurora />

<div class="kicker">VII · landfall</div>

<div class="flex items-end justify-center gap-6" style="position:relative"><Longship :width="96" /></div>

<img src="/cnd/cnd-norway-logo.png" alt="Cloud Native Days Norway" class="absolute top-6 left-8" style="height:56px" />

<h1 style="font-size:2.9rem">Your longship should be yours to sail.</h1>

<div class="mt-4 mx-auto gold text-xl whitespace-nowrap">Exit plan. SBOM. Your own keys. Have them before someone makes them mandatory.</div>

<div class="kicker mt-5">github.com/SUSE-Technical-Marketing/cnds-norway-2026-slides</div>

<div class="grid grid-cols-3 gap-8 mt-4 mx-auto justify-items-center" style="max-width:720px">
<div class="flex flex-col items-center"><img src="/qr/linkedin-jeroen.svg" alt="QR: Jeroen van Erp on LinkedIn" style="width:135px;height:135px;border-radius:6px" /><div class="text-sm mt-2">Jeroen van Erp</div><div class="steel font-mono text-xs">in/jvanerp</div></div>
<div class="flex flex-col items-center"><img src="/qr/slides.svg" alt="QR: these slides online" style="width:135px;height:135px;border-radius:6px;outline:3px solid #E2A63D;outline-offset:2px" /><div class="text-sm gold mt-2">These slides</div><div class="steel font-mono text-xs">open on your phone</div></div>
<div class="flex flex-col items-center"><img src="/qr/linkedin-andres.svg" alt="QR: Andrés Valero on LinkedIn" style="width:135px;height:135px;border-radius:6px" /><div class="text-sm mt-2">Andrés Valero</div><div class="steel font-mono text-xs">in/avaleror</div></div>
</div>

<!--
The longship from the title slide comes home. Read the headline, pause,
then the gold line: "Exit plan. SBOM. Your own keys. Have them before
someone makes them mandatory." Point at the middle QR: "The slides and
every source are in the repo." Click to the feedback slide for Q&A.
-->

---
layout: default
class: text-center
voyage: false
---

<img src="/cnd/cnd-norway-logo.png" alt="Cloud Native Days Norway" class="absolute top-6 left-8" style="height:56px" />

<div class="kicker mt-6">feedback</div>

# Tell us how we did

<img src="/qr/feedback-code-ns4g5w-friheten-i-koden-digital-sovereignty-for.png" alt="QR: session feedback" class="mx-auto mt-6" style="width:240px;height:240px;border-radius:8px" />

<div class="mt-6 text-xl">Scan to rate the session. <span class="gold">Takes 30 seconds.</span></div>

<!--
Leave this up during Q&A. The QR comes from the Cloud Native Days speaker
portal.
-->
