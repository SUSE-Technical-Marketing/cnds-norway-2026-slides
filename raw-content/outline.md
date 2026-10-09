# Friheten i Koden: Digital Sovereignty for the Nordic Age
Cloud Native Days Norway, 26–27 Oct 2026 · co-presenter: Andrés Valero
v2 — SOVEREIGNTY FOR TECHIES: tech lens is the spine, EU framework = context.
Draft slide outline, 30-minute talk (~24 min content + buffer)

Spine: sovereignty is an engineering property of your stack. You can measure
it, build it, and test it — the same way you test DR. The EU is just the
reason it stopped being a nice-to-have.

=====================================================================
PART 1 — THE THESIS (~5 min, slides 1–6)
=====================================================================
S1. Title (kicker: CNDS Norway · 26–27 Oct 2026 · Jeroen + Andrés Valero)

S2. Story: the image we carry
   - "Picture what you saw as a kid": bearded men, axes, burning ships —
     conquering, raiding, taking what other people built.
   - Tech joke: terminal box `beard / axe / longship — # that's all we remember`
   - Beat: "Now look through the other lens." (pause)

S3. Story: the other lens (the engineering story)
   1. Knowledge & tools — built their own ships (oak, rope, sails, iron),
      made where they lived
   2. The world was open — traded/explored from Newfoundland to Baghdad;
      didn't need to source their capability from another power
   3. And they defended it — protected themselves and their families
   - Punchline: "The image we carry is a film about their ships. The truth
     is an engineering story about capability."
   - Positioning: sovereignty = CAPABILITY, not isolation. Each leg maps
     forward: own ships → transparency/control; no foreign sourcing →
     jurisdiction/supply chain; self-defense → contingency/off-ramp.
     The trading point pre-empts "is this anti-cloud?"

S4. Pivot: from the fjord to the stack
   - "They sailed their own ships, charted their own routes, and never
     handed control of their journey to a foreign power."
   - "Today's cloud demands the same mindset. AWS/Azure/GCP are not the
     enemy. This talk won't pretend otherwise."
   - "Dependency without contingency is."

S5. The spine: sovereignty as an engineering property
   - "The boardroom talks about it. But sovereignty is being built — or
     broken — in pull requests."
   - Four measurable attributes:
     JURISDICTION  — whose law can reach this workload
     CONTROL       — who holds the keys, the identity, the data
     PORTABILITY   — how hard is it to leave (the off-ramp)
     TRANSPARENCY  — can you audit the stack? (open source, docs, SBOM)
   - All four are properties of your architecture, not of a logo.
   - The talk = how to measure and improve each, one by one.

S6. Why the CLOUD Act is the threat model techies should know
   - Engineering framing: it's a remote-access API you can't close.
     Applies to any US-jurisdiction entity; US authorities can compel
     disclosure of data the company "controls" — including data in
     eu-west-1. The region logo is not a firewall.
   - June 2025: Microsoft's French subsidiary confirmed under oath at a
     French Senate hearing it cannot guarantee sovereignty against US
     authorities — even for its French "sovereign" offering.
   - GDPR/DPF don't block it (DPF upheld at General Court Sep 2025,
     on appeal; Schrems II context).
   - The fix is not "don't use the cloud" — it's: control the keys,
     know your jurisdiction chain, keep an off-ramp.

=====================================================================
PART 2 — WHY NOW: THE EU GAVE IT A MEASURABLE DEFINITION (~4 min,
         slides 7–9 — compressed, this is context, not the show)
=====================================================================

S7. Three dates that matter to engineers (one timeline slide)
   - 12 Sep 2025: Data Act Art. 25 in force for new data-processing
     contracts — switching rights become contractual: interoperable
     export, no artificial obstacles, "without undue delay". Legacy
     long-term contracts covered by 2027. (DORA third-party risk:
     Jan 2025; NIS2 transposition: Oct 2024 — regulators now ask:
     "if your provider fails or is compelled, what's your plan?")
   - 20 Oct 2025: EC publishes Cloud Sovereignty Framework (CSF) +
     €180M sovereign cloud tender.
   - 17 Apr 2026: tender awarded to 4 providers scored on the SEAL
     rubric — sovereignty is now a procurement line item with budget.
     (Jun 2026: Technological Sovereignty Package / CADA will generalize
     it + unblock EUCS certification; Gartner: sovereign IaaS spend
     $6.9B '25 → $23.1B '27. Structural shift, not a fad.)

S8. SEAL: the cloud sovereignty maturity model (borrow the vocabulary)
   - CSF defines 8 Sovereignty Objectives (SOV) scored per objective,
     5 assurance levels:
     SEAL-0 no sovereignty (us-east-1 because it was cheaper — the default)
     SEAL-1 jurisdictional (EU region, GDPR; parent still US)
     SEAL-2 data (BYOK in EU HSM, audit rights, exit clauses)
     SEAL-3 digital resilience (EU entity, EU operators, EU certification)
     SEAL-4 full (EU-only supply chain in critical path; rare)
   - Frame it like the maturity models we already know:
     "SEAL-1 is GDPR compliance with a Brussels accent, not sovereignty."
   - Note: ratings are per objective, per procurement — there's no such
     thing as "a SEAL-3 product".

S9. The 8 objectives, translated to engineer-speak (table)
   - SOV-1 Strategic 15%      → can it keep operating if the vendor's
                               government pulls the plug?
   - SOV-2 Legal 10%          → jurisdiction of the entity that controls
                               the keys and the code
   - SOV-3 Data & AI 10%      → cryptographic control, auditable access,
                               EU-governed models
   - SOV-4 Operational 15%    → can EU people run/migrate it? docs,
                               operator pool
   - SOV-5 Supply chain 20%   → heaviest weight: "hardest to fake" —
                               SBOMs, firmware/hardware provenance
   - SOV-6 Technology 15%     → open, documented APIs; open source;
                               CNCF-aligned tooling
   - SOV-7 Security 10%       → ISO 27001, SecNumCloud/BSI C5, EUCS,
                               audit rights
   - SOV-8 Environmental 5%   → PUE, carbon/water disclosure
   - Point: the Commission says "hardest to fake" = supply chain. The
     techies' translation: what's actually in your stack?

=====================================================================
PART 3 — BUILDING IT: OFF-RAMP ARCHITECTURE (~8 min, slides 10–14)
=====================================================================

S10. What "off-ramp ready" looks like (the architecture slide)
   - Portable primitives: S3-compatible object storage, vanilla Postgres
     (no exotic extensions), OCI images, Kubernetes with standard CNI/CSI
   - Keys under customer control: envelope encryption, BYOK/HYOK; KMS
     abstraction in the platform layer
   - IaC as the off-ramp: a second provider/region in the same IaC is a
     tested exit, not a hope
   - Egress: standard export formats; telemetry/observability pipelines
     that survive a provider change

S11. Lock-in anti-patterns (why each seals the ramp + one-line fix)
   - Serverless as a black hole — business logic in proprietary
     functions → extract to containers/K8s, keep vendor functions as
     thin glue
   - Proprietary SDK-only features on hot paths → wrap behind an
     interface; keep the abstraction at the seam
   - Vendor-specific SQL / stored procedures / managed-DB magic →
     stay on portable Postgres surface
   - Telemetry/DNS/identity glued to one vendor → self-hosted
     alternatives (OpenTelemetry, own DNS/identity)
   - "We'll figure out the exit when we need it" → the default that
     makes SEAL-2 impossible

S12. Walk one workload up the ladder (make it concrete)
   - Fintech example, 4 years: us-east-1 (SEAL-0) → EU region (SEAL-1,
     "almost nothing changed") → BYOK in EU HSM + audit rights + 60-day
     exit clause (SEAL-2) → EU provider, self-managed Postgres, EU legal
     entity (SEAL-3)
   - Each step = specific engineering work: contracts+crypto, then
     migration+refactor (Lambda→K8s, RDS→Postgres)
   - ≈ €500K over 4 years ≈ 6 basis points of annual volume at maturity.
     Affordable — if you start now; under a regulator's deadline it's a
     project, not an option.

S13. Measure yourself: 4 questions, be honest (the interaction slide)
   1. Where does your primary provider's parent pay taxes and answer to
      law? ("US" → SEAL-0/1, "EU" → 3/4, "not sure" → assume 0)
   2. Who holds the encryption keys for your most sensitive data —
      and under whose jurisdiction?
   3. Do you have a documented, tested exit plan? (Actually run one.)
   4. If your provider received a non-EU legal order tomorrow, would
      you know — and could you keep operating?
   - Pause: let the room answer silently. "Answer honestly and you have
     a sovereignty posture."

S14. Sovereignty as culture, not bolt-on
   - Name trade-offs explicitly: "cost to leave" becomes a required
     field in architecture reviews, like RPO/RTO
   - Build abstraction where lock-in risk is highest: data, keys,
     identity, IaC
   - Portability as a first-class architectural concern — not a
     compliance-team afterthought at the end of the project

=====================================================================
PART 4 — BRING-HOME (4–5 min, slides 15–19)
=====================================================================

S15. Three things you can do Monday morning — no executive sign-off
     required. One clean trio: BUILD it / TEST it / make it a HABIT.

S16. Action 1 — Ship one off-ramp (one PR, ~1 day)
   - Pick your most lock-in-exposed workload.
   - Merge ONE concrete change:
     * second region in the IaC — exit becomes a variable, not a project
     * customer-managed keys (BYOK) on your most sensitive store
     * one proprietary SDK call wrapped behind an interface
   - Deliverable: a merged PR.
   - Framing: "You don't have to leave today — you just have to be able
     to leave."
   - No new tooling, no budget, no exec sign-off.

S17. Action 2 — Run an off-ramp test on your most lock-in-exposed
     workload
   - Snapshot + export + import into a second environment (other
     region, other provider, or an on-prem VM) — run it like a DR
     drill, quarterly
   - Verify: does export work in standard formats? Do keys follow?
     Does the app start on vanilla Postgres / S3-compatible storage?
   - Why: Data Act Art. 25 makes switching rights contractual — you'd
     rather learn the gaps now than at contract renewal in 2027.

S18. Action 3 — Add a portability gate to your review habit
   - Every new managed service / SDK / proprietary feature answers three
     lines in the PR or ADR: "What's the cost to leave? Who holds the
     keys? What's the off-ramp?"
   - A team norm, not a tool. One line in the PR description is enough.
   - This is the habit that turns sovereignty from policy into code.

S19. Close — the longship
   - "Your longship should be yours to sail."
   - The EU just gave sovereignty a measurable definition and a budget.
     Ten years from now off-ramp-ready will be the boring default;
     today it's a team habit you can install on Monday.
   - Slides + recording: hierynomus.com/talks/cloud-native-days-norway-2026

=====================================================================
TIMING
=====================================================================
S1–6    ~5 min   story-led opening (Viking two-lens) + spine + CLOUD Act
S7–9    ~4 min   why now (compressed context) + SEAL + SOV table
S10–14  ~8 min   off-ramp architecture, anti-patterns, worked example,
                 self-assessment, culture
S15–19  ~5 min   the 3 actions + close
Total ~21 min heavy content → comfortable 30-min slot with buffer.

=====================================================================
NOTES FOR JEROEN
=====================================================================
- Techies-lens rule of thumb: every regulatory fact must earn its slide
  by answering an engineer's question. CSF/SEAL stays because it gives
  us a measurable vocabulary (the maturity model). Data Act stays because
  it changes contracts and thus our jobs. NIS2/DORA get one line each.
- Split with Andrés (pick one):
  a) he takes S7–S9 (regulatory context), you take S1–S6 + S10–S19; or
  b) you open S1–S6, he runs S7–S9, you close S10–S19; or
  c) alternate by section.
- If time pressure, cut S9 (full SOV table → fold into S8) and the
  cost detail in S12.
- S13 is the audience-interaction moment — pause and let them answer
  silently.
- All dates/facts checked 31 Aug 2026.
- Companion handoff for another agent (Claude): HANDOFF.md in this directory
  — full context, conventions, and next steps.

Sources (fact-check):
- CSF v1.2.1 (20 Oct 2025): ec.europa.eu Cloud Sovereignty Framework
  page + PDF (commission.europa.eu/document/download/09579818-…)
- EC press: €180M tender (10 Oct 2025); awarded to four providers
  (17 Apr 2026)
- "European Technological Sovereignty Package" / CADA (3 Jun 2026),
  ec.europa.eu presscorner ip_26_1187; Lawfare analysis (Jun 2026)
- SEAL explainer: eucloudpatterns.eu/seal-framework (10 May 2026) —
  per-SOV scoring, fintech worked example, S3NS/CISPE dispute, the
  4-question self-assessment
- Data Act Art. 25: data-act-law.eu/article/25; Morgan Lewis (Sep 2025);
  Garrigues (Oct 2025) — in force 12 Sep 2025, legacy contracts 2027
- EUCS: enisa.europa.eu EUCS candidate scheme; qsentinel (CADA
  unblocked EUCS, 2026)
- CLOUD Act reach-through: wire.com CLOUD Act explainer; DanubeData
  (Jun 2025 French Senate, Microsoft under oath)
- Gartner sovereign IaaS figures via CSA Lab Space (Jun 2026)
- DORA application: 17 Jan 2025; NIS2 in force 16 Jan 2023,
  transposition deadline 17 Oct 2024
