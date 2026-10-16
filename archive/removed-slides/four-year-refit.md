<!-- Removed 2026-10-16 after the 14 Oct sync. Paste back into slides/slides.md after the last quiz pattern (V · pattern 5 of 5) to restore. -->

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

