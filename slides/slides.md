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
fonts:
  sans: -apple-system
  serif: Georgia
  mono: ui-monospace
---

<!--
MAIN DECK, built 2026-10-06. Merges the two versions that had split apart:
- Jeroen's deck.html of 22 Sep (kept in raw-content/deck.html)
- Andrés's Slidev pass of 17 Sep (archived in archive/2026-09-17-andres-slidev/)
Content rules still come from HANDOFF.md and outline.md in the vault folder.

STORY LINE: the talk is one voyage with seven chapters. The three ship legs
are planted in I, named against the keel in II, and cashed in out loud in VI.
  I    The myth          S3-S5    Jeroen
  II   The keel          S6       Jeroen
  III  Foreign waters    S7       Jeroen
  IV   The charts        S8-S11   Andrés (split option a, still to confirm)
  V    Shipbuilding      S12-S19  Jeroen
  VI   Sea trial         S20-S21  Jeroen
  VII  Home port         S22-S26  Jeroen
Ship legs used everywhere: own ships = control + transparency; open seas, no
foreign master = jurisdiction + supply chain; they defended it = the off-ramp.

Theme: style.css (Viking motifs, no runes or co-opted symbols) and
global-bottom.vue (the voyage bar). Rough timing: about 25 minutes of content
in a 30-minute slot. Needs a timed run-through before Bergen.
-->

<svg class="aurora" viewBox="0 0 980 552" preserveAspectRatio="none" aria-hidden="true"><defs><filter id="aur1" x="-20%" y="-50%" width="140%" height="200%"><feGaussianBlur stdDeviation="16"/></filter></defs><g filter="url(#aur1)" fill="none" stroke-linecap="round"><path d="M-40 130 Q220 30 440 110 T1020 50" stroke="#3FD7A0" stroke-width="46" opacity=".55"/><path d="M-40 185 Q260 80 520 160 T1030 100" stroke="#5B8CC9" stroke-width="34" opacity=".5"/><path d="M180 80 Q420 10 720 80" stroke="#B07CD8" stroke-width="18" opacity=".35"/></g></svg>

<div class="kicker">Cloud Native Days Norway · 26–27 Oct 2026</div>

# Friheten i Koden
### Digital Sovereignty for the Nordic Age

<div class="mt-6 muted">Jeroen van Erp · Andrés Valero · SUSE</div>

<Longship :width="290" class="absolute bottom-12 right-12" />

---
layout: default
class: text-center
voyage: false
---

<div class="kicker">the crew</div>

# Two voices, one ship

<div class="flex items-start justify-center gap-20 mt-10">
<Axe :size="70" class="self-center opacity-90" />
<div class="text-center">
<Shield class="mx-auto" :size="140" label="JE" a="#D0573F" b="#F3F0E8" />
<div class="mt-4 text-xl serif">Jeroen van Erp</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
<div class="text-center">
<Shield class="mx-auto" :size="140" label="AV" a="#4FA3A0" b="#E2A63D" />
<div class="mt-4 text-xl serif">Andrés Valero</div>
<div class="mt-1 steel text-sm">Principal Technology Advocate, SUSE</div>
</div>
<Axe :size="70" class="self-center opacity-90" style="transform:scaleX(-1)" />
</div>

<!--
Initials on painted shields until headshots arrive. To swap in a photo, replace the
<Shield> with <img src="./jeroen.jpg" style="width:140px;height:140px;
border-radius:50%;object-fit:cover;border:1.6px solid #E2A63D"/>.
Same title on both on purpose (Andrés's call). Check with Jeroen that it is
his real title.
-->

---
layout: default
chapter: "I · The myth"
class: voyage-open
---

<div class="kicker">I · the myth</div>

# Picture what you saw as a kid

<div class="grid-2 mt-8">
<div class="term">
$ ls<br/>beard<br/>axe<br/>longship<br/><span class="muted"># that's all we remember</span>
</div>
<div class="panel flex items-center gap-5">
<Viking variant="myth" :size="105" class="flex-none" />
<div>
Bearded men. Axes. Burning ships.<br/>
Conquering, raiding, sailing the oceans and taking what other people <span class="gold">built</span>.
<div class="mt-3 red text-xs font-mono">FUN FACT: THE HORNS COME FROM AN 1876 OPERA COSTUME</div>
</div>
</div>
</div>

<div class="mt-8 text-xl gold">Now look through the other lens.</div>

<!--
JEROEN. Pause after "Now look through the other lens." Let it breathe.

Optional laugh line: "And the horns? Those come from costume designs for
Wagner's Ring cycle, 1876. No Viking ever wore them into a fight."
-->

---
layout: default
---

<div class="kicker">I · the other lens</div>

# Now picture the other image

<div class="grid-3 mt-6">
<div class="panel">
<div class="flex items-center gap-3"><Axe :size="44" /><div class="serif text-lg">Their own ships</div></div>
<div class="muted mt-1 text-sm">The knowledge and the tools to build them: oak, rope, sails, iron nails. Made where they lived.</div>
</div>
<div class="panel">
<div class="flex items-center gap-3"><Longship :width="64" /><div class="serif text-lg">Open seas</div></div>
<div class="muted mt-1 text-sm">They traded and sailed from Newfoundland to Baghdad. They never had to source their capability from another power.</div>
</div>
<div class="panel">
<div class="flex items-center gap-3"><Shield :size="44" a="#2F5D8A" b="#E2A63D" /><div class="serif text-lg">They defended it</div></div>
<div class="muted mt-1 text-sm">They could protect themselves and their families from anyone who came knocking.</div>
</div>
</div>

<div class="flex items-center gap-5 mt-6">
<Viking variant="real" :size="70" class="flex-none" />
<div>
<div class="quote-block">The film shows their ships. The history shows people who could build them.</div>
<div class="mt-2 teal text-xs font-mono">THE REAL HELMET: ROUND, WITH AN EYE GUARD · GJERMUNDBU, NORWAY, 10TH CENTURY</div>
</div>
</div>

<!--
JEROEN. Plant the three legs and keep them simple: own ships, open seas,
they defended it. Don't explain what they map to yet. The icons (axe,
longship, shield) come back every time a leg returns later in the talk. The keel slide names
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
<div class="panel">
<div class="flex items-center gap-3"><Planks :width="48" /><div class="serif text-xl gold">Ownership</div></div>
<div class="steel font-mono text-xs mt-2">WHO OWNS THE SHIP?</div>
<div class="mt-2">The asset. The contract. The data in your region.</div>
<div class="muted mt-3 text-sm">The name on the hull, the deed to the boathouse.</div>
</div>
<div class="panel">
<div class="flex items-center gap-3"><Longship :width="64" /><div class="serif text-xl gold">Control</div></div>
<div class="steel font-mono text-xs mt-2">WHO SAILS THE SHIP?</div>
<div class="mt-2">Who sets the course? Who can stop it, or leave port when they choose?</div>
<div class="muted mt-3 text-sm">The hand on the tiller, and the freedom to turn the bow.</div>
</div>
</div>

<div class="mt-8 text-2xl serif">Ownership alone is not <span class="gold">sovereignty</span>. Control makes it real.</div>


<!--
JEROEN. Two words people mix up: Ownership = who owns the ship, Control =
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

<div class="grid-2 mt-6 items-center">
<div>
<div class="text-lg muted">Today's cloud asks for the same mindset. AWS, Azure and GCP are great ports, and this talk won't pretend otherwise.</div>
<div class="mt-8 text-5xl gold serif" style="line-height:1.15;font-weight:600">The enemy is dependency without contingency.</div>
</div>
<div class="panel">
<div class="steel font-mono text-xs">THE TEST · NO GOVERNMENT MANDATE NEEDED</div>
<div class="mt-3">1. What does it cost you to leave? Money, time, risk.</div>
<div class="mt-2">2. Can you audit who runs your systems?</div>
<div class="mt-4 gold">Answer "we don't know" to either one, and what you bought is a dependency.</div>
</div>
</div>

<div class="mt-8 muted text-sm">Global and commercial: Norway, Singapore or Ohio, no regulator required.</div>

<!--
JEROEN. Merge of both versions: Andrés's big thesis line on the left,
Jeroen's commercial test (22 Sep) on the right. The test lands before any EU
material on purpose, so the room hears it as a global engineering question.
-->

---
layout: default
chapter: "II · The keel"
class: voyage-open
---

<div class="kicker">II · the keel</div>

# Sovereignty is an engineering property

<div class="muted mt-2">Every longship starts with a keel. This one has four timbers, and the boardroom doesn't lay them. Pull requests do.</div>

<div class="grid-4 mt-8 keel">
<div class="panel"><div class="gold font-mono text-sm">JURISDICTION</div>Whose law can reach this workload? Follow the parent entity, not the region logo.<span class="leg leg-icon"><Longship :width="34" /> open seas</span></div>
<div class="panel"><div class="gold font-mono text-sm">CONTROL</div>Who holds the keys, the identity, the data?<span class="leg leg-icon"><Axe :size="20" /> their own ships</span></div>
<div class="panel"><div class="gold font-mono text-sm">PORTABILITY</div>How hard is it to leave? The off-ramp.<span class="leg leg-icon"><Shield :size="20" a="#2F5D8A" b="#E2A63D" /> they defended it</span></div>
<div class="panel"><div class="gold font-mono text-sm">TRANSPARENCY</div>Can you audit the stack? Open source, docs, SBOMs.<span class="leg leg-icon"><Planks :width="34" /> planks in sight</span></div>
</div>

<div class="mt-8 muted">All four live in your architecture. You can measure them, and you can change them one PR at a time.</div>

<!--
JEROEN. This is the one lens for the whole talk. Every later framework
points back here (the SOV table, the sea trial 2x2). Read the small tags
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

<div class="muted mt-2 max-w-3xl">
It applies to any US-jurisdiction entity, wherever the data sits. US authorities can compel disclosure of
data the company "controls," including data in <code>eu-west-1</code>. Sail in someone else's waters and
you sail under their law.
</div>

<div class="mt-6 text-2xl serif">The region logo is <span class="gold">not a firewall</span>.</div>

<div class="quote-block mt-6">"No, I cannot guarantee it."</div>
<div class="muted text-xs mt-2">Anton Carniaux, Microsoft France director of public &amp; legal affairs, under oath · French Senate inquiry commission, 10 June 2025</div>

<div class="mt-6 text-lg">The fix: <span class="gold">control the keys, know your jurisdiction chain, keep an off-ramp.</span></div>

<div class="mt-3 foot">GDPR and the EU–US Data Privacy Framework don't block it (DPF upheld at the General Court, Sep 2025, now on appeal).</div>

<!--
JEROEN. The emotional core of the talk. Let the five-word quote sit for a
second before reading the source line.

Handoff to Andrés (split option a): "That's the storm. So how do you
navigate it? Andrés has the charts."
-->

---
layout: default
chapter: "IV · The charts"
class: voyage-open
---

<div class="kicker">IV · follow the trade</div>

# $23.1B by 2027

<div class="flex items-stretch justify-center gap-3 mt-8 text-center" style="max-width:1300px;margin-left:auto;margin-right:auto">
<div class="panel" style="flex:1">
<div class="gold text-3xl serif">$6.9B</div>
<div class="steel font-mono text-xs mt-1">2025</div>
</div>
<div class="steel flex items-center text-xl">→</div>
<div class="panel" style="flex:1">
<div class="gold text-3xl serif">$12.6B</div>
<div class="steel font-mono text-xs mt-1">2026</div>
</div>
<div class="steel flex items-center text-xl">→</div>
<div class="panel" style="flex:1">
<div class="gold text-3xl serif">$23.1B</div>
<div class="steel font-mono text-xs mt-1">2027</div>
</div>
</div>

<div class="mt-3 muted text-sm text-center">Gartner (Feb 2026): sovereign cloud IaaS spend in Europe. This is where budgets are moving.</div>

<div class="mt-8 text-lg max-w-3xl mx-auto text-center">The money is growing as fast as the topic. IT and engineering teams are the ones who turn it into something real.</div>

<!--
ANDRÉS. About 20 to 30 seconds. A bridge slide, keep it tight.

Open: "The Vikings followed the trade routes. So let's follow the money."
Walk the three numbers as one beat, then land the closing line plainly.

Move on with: "So what's actually driving that number? Three charts got
drawn in the last year, plus one that went live six weeks ago."

Fact check 2026-10-06: these are the European figures (Computerworld: "European
spending on sovereign cloud IaaS to nearly double in 2026"). The 17 Sep
Slidev version said "worldwide", which was wrong: Gartner puts worldwide at
about $80B for 2026.
-->

---
layout: default
---

<div class="kicker">IV · the charts</div>

# Four rules, one heading

<div class="grid-4 mt-6 text-sm">
<div class="panel">
<div class="gold font-mono text-xs">DATA ACT · ART. 25</div>
<div class="mt-2">Switching providers is a contractual right now. A provider can't just say no.</div>
<div class="mt-3 steel text-xs">In force Sep 2025</div>
</div>
<div class="panel">
<div class="gold font-mono text-xs">CLOUD SOVEREIGNTY FRAMEWORK</div>
<div class="mt-2">The EU's own scoring system, SEAL 0–4. A €180M tender was awarded on it to four providers.</div>
<div class="mt-3 steel text-xs">Oct 2025 · awarded Apr 2026</div>
</div>
<div class="panel">
<div class="gold font-mono text-xs">TECH SOVEREIGNTY PACKAGE</div>
<div class="mt-2">Brings <span class="gold">CADA</span>: a second sovereignty scale, numbered differently from SEAL. Unblocks EUCS.</div>
<div class="mt-3 steel text-xs">Jun 2026</div>
</div>
<div class="panel hot">
<div class="gold font-mono text-xs">CYBER RESILIENCE ACT</div>
<div class="mt-2">Vulnerability reporting within 24h/72h. Also the legal source of the SBOM line coming up.</div>
<div class="mt-3 gold text-xs">11 Sep 2026 · six weeks ago</div>
</div>
</div>

<div class="mt-8 text-lg">Four rules, one heading: sovereignty is something you get scored on now.</div>

<div class="mt-6 foot">SEAL = Sovereignty Effective Assurance Levels · CADA = Cloud and AI Development Act · EUCS = European Cybersecurity Certification Scheme for Cloud Services · CRA = Cyber Resilience Act</div>

<!--
ANDRÉS. About 70 seconds. Lead with the rule's name, dates are secondary.
The one exception is CRA: "six weeks ago" is the hook, so say it.

- Data Act: the one that touches your contracts. Your provider can't drag an exit out forever.
- Cloud Sovereignty Framework: the EU built a scoring system and put €180M behind it. Four providers won, scored on the ladder you'll see next.
- Tech Sovereignty Package: say this one slowly. "CADA is a second scale with different numbers from SEAL. Its top tiers need an EUCS certificate that doesn't exist yet."
- CRA: "This one isn't coming. It started six weeks ago, and it's why SBOMs stopped being optional."

[OPTIONAL, verbal only] Gaia-X, if the room clearly knows the name: "Didn't
Europe try this with Gaia-X? Yes. It hit the same sovereignty-washing
problem we'll see in this tender."

DORA and NIS2 stay off the slide. One spoken line if time allows: "Regulators
now ask: if your provider fails or gets compelled, what's your plan?"
-->

---
layout: default
---

<div class="kicker">IV · the depth scale</div>

# SEAL: borrow the vocabulary

<div class="mt-6">
<div class="seal-row"><div class="seal-track"><div class="seal-bar" style="width:8%;background:#D0573F"></div></div><div><b class="gold">SEAL-0</b> no sovereignty: us-east-1 because it was cheaper. The default.</div></div>
<div class="seal-row"><div class="seal-track"><div class="seal-bar" style="width:24%;background:#E07B3C"></div></div><div><b class="gold">SEAL-1</b> jurisdictional: EU region, GDPR, parent still US</div></div>
<div class="seal-row"><div class="seal-track"><div class="seal-bar" style="width:40%;background:#E2A63D"></div></div><div><b class="gold">SEAL-2</b> data: BYOK in an EU HSM, audit rights, exit clauses</div></div>
<div class="seal-row"><div class="seal-track"><div class="seal-bar" style="width:56%;background:#4FA3A0"></div></div><div><b class="gold">SEAL-3</b> resilience: EU entity, EU operators, EU certification</div></div>
<div class="seal-row"><div class="seal-track"><div class="seal-bar" style="width:72%;background:#5B8CC9"></div></div><div><b class="gold">SEAL-4</b> full: EU-only supply chain in the critical path. Rare.</div></div>
</div>

<div class="quote-block mt-6">SEAL-1 is GDPR compliance with a Brussels accent.</div>

<div class="mt-5 muted">Ratings are per objective, per procurement. There's no such thing as "a SEAL-3 product."</div>

<!--
ANDRÉS. About 90 seconds.

Open: "Sailors measure depth before they trust the water. The EU gave us a
depth scale, and if you've used a CMMI or DevOps maturity model, it'll feel
familiar."

One beat of color per level, don't read the lines:
- SEAL 0: "The default nobody picked on purpose."
- SEAL 1: land "Brussels accent" as the laugh line, move on fast.
- SEAL 2: "This is where it costs engineering time. BYOK means someone owns key rotation now."
- SEAL 3: "For most regulated workloads, this is the realistic ceiling."
- SEAL 4: "Rare, and only worth it if you're told to be there."

Slow down for the last line and pause after it. That's the line that stops
someone asking procurement for "a SEAL-3 vendor."
-->

---
layout: default
---

<div class="kicker">IV · what gets scored</div>

# The 8 objectives, in engineer-speak

<div class="muted mt-1 text-sm">Each objective gets its own SEAL rating. The weights blend them into one score.</div>

<table class="table-tight mt-3">
<thead>
<tr><th>Objective</th><th>Weight</th><th>Engineer-speak</th></tr>
</thead>
<tbody>
<tr class="dim"><td>SOV-1 Strategic</td><td>15%</td><td>Can it keep running if the vendor's government pulls the plug?</td></tr>
<tr class="dim"><td>SOV-2 Legal</td><td>10%</td><td>Jurisdiction of whoever controls the keys and the code</td></tr>
<tr class="dim"><td>SOV-3 Data &amp; AI</td><td>10%</td><td>Cryptographic control, auditable access, EU-governed models</td></tr>
<tr><td><b>SOV-4 Operational</b></td><td>15%</td><td>Can EU people run and migrate it? A perfect ship still needs a <span class="gold">crew</span>: no skilled operators, no voyage.</td></tr>
<tr><td><b class="gold">SOV-5 Supply chain</b></td><td><b class="gold">20%</b></td><td>"Hardest to fake": SBOMs and provenance. Since CRA, a legal deadline too.</td></tr>
<tr><td><b>SOV-6 Technology</b></td><td>15%</td><td>Open, documented APIs. Open source. CNCF-aligned tooling.</td></tr>
<tr class="dim"><td>SOV-7 Security</td><td>10%</td><td>ISO 27001, SecNumCloud / BSI C5, EUCS, audit rights</td></tr>
<tr class="dim"><td>SOV-8 Environmental</td><td>5%</td><td>PUE, carbon and water disclosure</td></tr>
</tbody>
</table>

<div class="mt-4 muted">The heaviest weight is supply chain. The engineer's translation: <span class="gold">what's actually in your stack?</span></div>

<!--
ANDRÉS. About 60 seconds. This is the droppable slide if we're behind:
fold the SOV-5 line into the SEAL slide and skip it.

"The SEAL rating isn't one number, it's a blend of eight of these." Don't
read all eight, the dimmed rows are there for completeness. Talk about the
three bright ones:
- SOV-4: "A perfect stack with nobody who can run it goes nowhere. That's the silent failure point."
- SOV-5: the heaviest, 20%. "Hardest to fake," and CRA made it a legal deadline.
- SOV-6: open APIs and open source, the part this room builds every day.

[OPTIONAL, verbal only] SOV-5: name SLSA as the real standard behind
provenance. SOV-6: the CNCF conformance program for AI workloads, if it fits.

Handback to Jeroen: "So that's what gets measured. Jeroen's going to show
you how to build a ship that scores well."
-->

---
layout: default
chapter: "V · Shipbuilding"
class: voyage-open
---

<div class="kicker">V · shipbuilding</div>

# What "off-ramp ready" looks like

<div class="grid-2 mt-5 text-sm">
<div class="panel"><b class="steel">Portable primitives</b><br/>S3-compatible object storage, vanilla Postgres, OCI images, Kubernetes with standard CNI/CSI</div>
<div class="panel"><b class="steel">Keys under your control</b><br/>Envelope encryption, BYOK/HYOK, a KMS abstraction in the platform layer</div>
<div class="panel"><b class="steel">IaC as the off-ramp</b><br/>A second provider or region in the same IaC is a tested exit</div>
<div class="panel"><b class="steel">Egress</b><br/>Standard export formats, telemetry pipelines that survive a provider change</div>
</div>

<div class="panel mt-3 text-sm"><b class="gold">Named patterns, all open source:</b> Cluster API-style lifecycle management · KubeVirt-style VMs with live migration · service-mesh mTLS plus OPA/Kyverno policy</div>

<div class="mt-4 foot">OCI = Open Container Initiative · CNI/CSI = Container Network/Storage Interface · BYOK/HYOK = Bring/Hold Your Own Key · KMS = Key Management Service · IaC = Infrastructure as Code · mTLS = mutual TLS · OPA = Open Policy Agent</div>

<!--
JEROEN. The named patterns row keeps the abstract's promise: cluster
management, open virtualization, zero-trust security. CNCF project
categories only, no vendor names.
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

<div class="mt-4 text-xl max-w-2xl mx-auto">Five real architecture choices.</div>
<div class="mt-4 text-lg muted max-w-2xl mx-auto">One at a time. Make your call before the click.</div>

<!--
JEROEN. The axe marks a trap (chop it out), the longship marks a seaworthy
choice. Make it a real pause: "Five real choices, one at a time. Before each
one, decide: trap, or something you'd ship? Then I click." Keep it light,
this is the fun beat. Two of the five are fine, so don't let the room
settle on "always trap" by item 3.
-->

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 1 of 5</div>

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

<div class="kicker">V · pattern 2 of 5</div>

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

<div class="kicker">V · pattern 3 of 5</div>

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

<div class="kicker">V · pattern 4 of 5</div>

<div class="text-2xl mt-16 max-w-3xl mx-auto serif">Telemetry runs on OpenTelemetry, with your own DNS and identity provider.</div>

<div v-click class="mt-12">
<div class="inline-flex items-center gap-3"><Longship :width="56" /><span class="teal font-mono text-lg">SEAWORTHY</span></div>
<div class="mt-3 text-lg max-w-2xl mx-auto">No single vendor holds your observability or your identity hostage.</div>
</div>

---
layout: default
class: text-center
---

<div class="kicker">V · pattern 5 of 5</div>

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
---

<div class="kicker">V · a four-year refit</div>

# One workload, up the ladder

<div class="grid-4 mt-4 text-sm">
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-0 · Year 1</div>us-east-1 <span class="muted">· cheaper</span>
<div class="mt-2 steel font-mono" style="font-size:0.65rem">IN THE CODE</div>
<div class="muted">Lambda + RDS, AWS SDK hardcoded in handlers. No exit in mind.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-1 · Year 2</div>EU region <span class="muted">· parent still US</span>
<div class="mt-2 steel font-mono" style="font-size:0.65rem">IN THE CODE</div>
<div class="muted">One Terraform variable: region. Zero app code touched.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-2 · Year 3</div>BYOK in an EU HSM <span class="muted">· audit rights, 60-day exit</span>
<div class="mt-2 steel font-mono" style="font-size:0.65rem">IN THE CODE</div>
<div class="muted">KMS behind an interface, envelope encryption. Key rotation now owned.</div>
</div>
<div class="panel" style="padding:0.8rem 1rem">
<div class="gold">SEAL-3 · Year 4</div>EU provider <span class="muted">· EU legal entity</span>
<div class="mt-2 steel font-mono" style="font-size:0.65rem">IN THE CODE</div>
<div class="muted">The big refactor: Lambda to containers on K8s, RDS to vanilla Postgres.</div>
</div>
</div>

<div class="mt-4 steel text-sm">The SEAL-2 clauses aren't hypothetical: DORA Art. 28 already requires audit rights and an exit plan for financial entities.</div>

<div class="mt-3 text-lg gold">≈ €500K over 4 years ≈ 6 basis points of annual volume.</div>
<div class="mt-1 muted">Affordable if you start now. Wait for a regulator's deadline and it turns into a rushed project.</div>

<!--
JEROEN. Say the "in the code" line for each step, it's what this room cares
about. SEAL-1 costs nothing in code, SEAL-2 and 3 are where engineering time
goes. The DORA line (22 Sep) shows the fintech story is already law.
-->

---
layout: default
chapter: "VI · Sea trial"
class: voyage-open
---

<div class="kicker">VI · sea trial</div>

# The 2×2. <span class="gold">Be honest.</span>

<div class="matrix mt-4" style="height:300px">
<div></div>
<div class="axis">Operational impact</div>
<div class="axis">Existential risk</div>
<div class="row-h">Independence</div>
<div class="cell" v-click>If you had to leave your provider, how fast could you move without rearchitecting?<span class="leg">→ portability</span></div>
<div class="cell" v-click>Long term, what does it cost to never be able to leave? Money and risk.<span class="leg">→ portability, compounded</span></div>
<div class="row-h">Others in control</div>
<div class="cell" v-click>If access to some services were withdrawn, what stops working, and for how long?<span class="leg">→ control</span></div>
<div class="cell" v-click>Who can inspect, maintain and change what runs your system, and does a foreign law reach them?<span class="leg">→ transparency + jurisdiction</span></div>
</div>

<div class="mt-4 text-lg gold">Keep your hand up if you can answer out loud, right now.</div>

<!--
JEROEN. Jeroen's 2x2 (22 Sep) with Andrés's show of hands (17 Sep). Each
quadrant points back to the keel, so it reads as the payoff of S6 and not
a new framework.

1. Before the first click: "Hands up. Keep it up only if you can answer
   this one out loud, right now, with a straight face."
2. Click each quadrant, pause 3 to 4 seconds, scan the room. Don't comment
   on the drop, keep going.
3. After the fourth: "Look around. The hands still up have a sovereignty
   posture. Everyone else has a belief."
4. Big or formal room: "Count on your own fingers, don't show anyone."

Don't call on anyone. Optional European line: "In Europe? Ask if you're
ready for CADA."
-->

---
layout: default
---

<div class="kicker">VI · remember the ships</div>

# Sovereignty lives in the crew

<div class="grid-3 mt-6">
<div class="panel">
<div class="flex items-center gap-3"><Axe :size="40" /><div class="serif text-lg">Their own ships</div></div>
<div class="mt-2 gold">Control + transparency</div>
<div class="muted text-sm mt-1">You hold the keys and you can audit the stack.</div>
</div>
<div class="panel">
<div class="flex items-center gap-3"><Longship :width="58" /><div class="serif text-lg">Open seas</div></div>
<div class="mt-2 gold">Jurisdiction + supply chain</div>
<div class="muted text-sm mt-1">You trade with everyone and answer to no foreign master.</div>
</div>
<div class="panel">
<div class="flex items-center gap-3"><Shield :size="40" a="#2F5D8A" b="#E2A63D" /><div class="serif text-lg">They defended it</div></div>
<div class="mt-2 gold">The off-ramp</div>
<div class="muted text-sm mt-1">You can leave, and you've tested it.</div>
</div>
</div>

<div class="mt-8 text-lg">So make "cost to leave" a required field in every architecture review, right next to <code>RPO / RTO</code>.</div>

<!--
JEROEN. The callback (22 Sep) that closes the loop planted in S4. Say it out
loud: "Remember the ships? This is them." Then the one culture line.

Andrés's 17 Sep cut was right about the old bullets: they repeated the
actions. So only the callback and the RPO/RTO line stay.
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
<div class="panel" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">01</div><Axe :size="40" /></div>
<div class="gold text-xl mt-2">BUILD it</div>
<div class="muted mt-2 text-sm">One PR, about a day. Ship one off-ramp.</div>
</div>
<div class="steel flex items-center text-2xl">→</div>
<div class="panel" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">02</div><Longship :width="60" /></div>
<div class="gold text-xl mt-2">TEST it</div>
<div class="muted mt-2 text-sm">Quarterly. Run it like a DR drill.</div>
</div>
<div class="steel flex items-center text-2xl">→</div>
<div class="panel" style="flex:1">
<div class="flex items-center justify-between"><div class="stat-num">03</div><Shield :size="40" a="#D0573F" b="#E2A63D" /></div>
<div class="gold text-xl mt-2">make it a HABIT</div>
<div class="muted mt-2 text-sm">Three lines in every PR or ADR.</div>
</div>
</div>

<!--
JEROEN. Rule of three, a visual table of contents for the next three slides.
Same icons as the ship legs: the axe builds, the longship sails, the shield holds.
-->

---
layout: default
---

<div class="flex items-center gap-3"><Axe :size="30" /><div class="kicker">VII · action 1 · build</div></div>

# Ship one off-ramp

<div class="muted">One PR, about a day. Pick your most lock-in-exposed workload.</div>

<div class="mt-6 grid gap-3">
<div class="panel">Second region in the IaC: leaving becomes a variable change</div>
<div class="panel">Customer-managed keys (BYOK) on your most sensitive store</div>
<div class="panel">One proprietary SDK call wrapped behind an interface you own</div>
</div>

<div class="mt-5 muted">Deliverable: a merged PR. No new tooling, no budget.</div>
<div class="quote-block mt-5">You don't have to leave today. You just have to be able to leave.</div>

---
layout: default
---

<div class="flex items-center gap-3"><Longship :width="44" /><div class="kicker">VII · action 2 · test</div></div>

# Run an off-ramp test

<div class="muted">Quarterly and on the calendar, like any DR drill.</div>

<div class="grid-2 mt-6 items-start">
<div class="panel">
Snapshot, export, import into a second environment: another region, another provider or an on-prem VM.
</div>
<div class="term text-sm">
# verify<br/>
□ export in standard formats?<br/>
□ do the keys follow?<br/>
□ app boots on vanilla Postgres<br/>
&nbsp;&nbsp;/ S3-compatible storage?
</div>
</div>

<div class="mt-6 muted">Data Act Art. 25 makes switching rights contractual. Find the gaps now, well before contract renewal in 2027.</div>

---
layout: default
---

<div class="flex items-center gap-3"><Shield :size="30" a="#D0573F" b="#E2A63D" /><div class="kicker">VII · action 3 · habit</div></div>

# A portability gate in your reviews

<div class="mt-5 muted">Every new managed service, SDK or proprietary feature answers three lines in the PR or ADR:</div>

<div class="term mt-5 text-xl" style="line-height:2">
<span class="gold">$</span> cost to leave?<br/>
<span class="gold">$</span> who holds the keys?<br/>
<span class="gold">$</span> what's the off-ramp?
</div>

<div class="mt-6 muted">A team norm. No new tool needed, one line in the PR description is enough. That's the habit that turns sovereignty from policy into code.</div>

---
layout: default
class: text-center
---

<svg class="aurora" viewBox="0 0 980 552" preserveAspectRatio="none" aria-hidden="true"><defs><filter id="aur2" x="-20%" y="-50%" width="140%" height="200%"><feGaussianBlur stdDeviation="16"/></filter></defs><g filter="url(#aur2)" fill="none" stroke-linecap="round"><path d="M-40 130 Q220 30 440 110 T1020 50" stroke="#3FD7A0" stroke-width="46" opacity=".55"/><path d="M-40 185 Q260 80 520 160 T1030 100" stroke="#5B8CC9" stroke-width="34" opacity=".5"/><path d="M180 80 Q420 10 720 80" stroke="#B07CD8" stroke-width="18" opacity=".35"/></g></svg>

<div class="kicker">VII · landfall</div>

<Longship :width="200" class="mx-auto mb-2" style="position:relative" />

# Your longship should be yours to sail.

<div class="mt-5 max-w-2xl mx-auto muted">
The EU just gave sovereignty a measurable definition and a budget. Ten years from now, off-ramp ready
will be the boring default. Today, it's a team habit you can start on Monday.
</div>

<div class="mt-6 max-w-2xl mx-auto gold">Have an exit plan, an SBOM and an answer to "who holds the keys" ready before the RFP asks.</div>

<div class="mt-6 kicker">github.com/avaleror/cnds-norway-2026-slides</div>

<!--
JEROEN. The longship from the title slide comes home. The voyage bar ends
here too.
-->
