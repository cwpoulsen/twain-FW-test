# Reviewer Checklist — Wave 21 (Go / No-Go)

Owner: Chris  
Purpose: final practical gate before accepting Wave 21 as canon-safe.  
Decision rule: if any **Critical** item fails, outcome is **NO-GO** until fixed.

---

## How to Use This Checklist

- Mark each line **PASS / FAIL / N/A**.
- Add short notes with file paths and section headings.
- For every FAIL, record one actionable fix owner + due pass.
- Final call:
  - **GO** = all Critical items PASS, and no more than 2 non-critical FAILs with explicit follow-up.
  - **NO-GO** = any Critical FAIL, or missing evidence for a claimed PASS.

---

## A) Canon Consistency Gate

### A1. Canon authority alignment (**Critical**)
- [ ] PASS / [ ] FAIL — No Wave 21 claim contradicts locked CORE canon without explicit retcon note.
- **Pass criteria:** every new/changed claim is compatible with `canon/canon-ledger-v2.md`, or includes explicit retcon + impact statement.
- **Inspect evidence:**
  - `canon/canon-ledger-v2.md`
  - `ops/canon-policy.md`
  - Wave 21 changed docs (git diff against previous commit)

### A2. Naming/term lock integrity (**Critical**)
- [ ] PASS / [ ] FAIL — Canonical actor/system names are stable (no drift variants used as if official).
- **Pass criteria:** no conflicting labels for same canon entity (e.g., organization names, program names, protocol names).
- **Inspect evidence:**
  - `canon/canon-ledger-v2.md`
  - `factions/major-factions.md`
  - `series/series-architecture-v2.md`
  - `ops/evidence/` continuity/guard check outputs

### A3. Rule-layer compliance (CORE/SOFT/RUMOR)
- [ ] PASS / [ ] FAIL — Claim classification is explicit and respected.
- **Pass criteria:** SOFT/RUMOR does not silently overwrite CORE; escalations are documented.
- **Inspect evidence:**
  - `canon/canon-ledger-v2.md`
  - Relevant canon entries changed in Wave 21
  - `ops/continuity-holes-register-v1.md` (if unresolved conflicts exist)

---

## B) Arc Coherence Gate

### B1. Cause→turn→consequence continuity (**Critical**)
- [ ] PASS / [ ] FAIL — Major arc turns in Wave 21 have clear antecedents and downstream effects.
- **Pass criteria:** no “reset-to-baseline” after a major turning point; behavior/policy shifts persist.
- **Inspect evidence:**
  - `series/books1-10-arc-dependency-grid-v1.md`
  - `timeline/master-timeline-sequence-v1.md`
  - `ops/mission-seed-to-scene-consequence-chains-*.md`

### B2. Timeline coherence across impacted arcs (**Critical**)
- [ ] PASS / [ ] FAIL — Event ordering supports emotional and strategic causality.
- **Pass criteria:** no inversion where later outcomes appear before enabling events; travel/comms constraints remain plausible.
- **Inspect evidence:**
  - `timeline/master-timeline-sequence-v1.md`
  - `timeline/books1-10-strategic-reconquest-map-v1.md`
  - Any Wave 21 timeline edits

### B3. Character-state progression integrity
- [ ] PASS / [ ] FAIL — Character relationships/trust/friction changes are earned and retained.
- **Pass criteria:** each major relational or motivation shift is anchored to identifiable prior events and shows later payoff.
- **Inspect evidence:**
  - `characters/` dossiers used by touched arcs
  - scene packets or draft segments changed in Wave 21
  - dependency links in series/timeline docs

---

## C) Scene Consequence Integrity Gate

### C1. Scene output persists beyond the scene (**Critical**)
- [ ] PASS / [ ] FAIL — Key scenes create durable state changes (material, political, relational, legal, tactical).
- **Pass criteria:** each high-impact scene has at least one explicit downstream consequence in later docs/scenes.
- **Inspect evidence:**
  - `ops/mission-seed-to-scene-consequence-chains-*.md`
  - `scenes/` and `drafts/` files touched in Wave 21
  - `ops/book-bible-progress-log.md`

### C2. Mechanism realism (no plot magic) (**Critical**)
- [ ] PASS / [ ] FAIL — Outcomes are supported by actionable mechanisms (access, comms, logistics, risk).
- **Pass criteria:** no unexplained intervention or impossible coordination; constraints are acknowledged.
- **Inspect evidence:**
  - `tech/technical-architecture-v1.md`
  - `ops/small-body-combat-and-work-credibility-manual-v1.md`
  - relevant faction/operations doctrine docs in `ops/`

### C3. Evidence chain integrity for contested claims
- [ ] PASS / [ ] FAIL — High-stakes proof claims retain provenance and survivability assumptions.
- **Pass criteria:** source/timestamp/custody path exists for decisive evidence beats; scrub/loss threat is addressed.
- **Inspect evidence:**
  - `ops/evidence/` artifacts
  - `ops/reality-gate-enforcement-pack-v1.md`
  - contested-lane adjudication docs in `ops/`

---

## D) Closure & Decision

### D1. Reconciliation hygiene
- [ ] PASS / [ ] FAIL — Any contradiction found is either fixed or logged with owner/severity.
- **Pass criteria:** no unlogged known contradiction; no silent deferral.
- **Inspect evidence:**
  - `ops/continuity-holes-register-v1.md`
  - `ops/book-bible-pass-log.md`
  - `ops/book-bible-progress-log.md`

### D2. Review traceability
- [ ] PASS / [ ] FAIL — Reviewer notes identify exactly what was inspected.
- **Pass criteria:** each section has file-level evidence refs and brief rationale.
- **Inspect evidence:**
  - This checklist (completed)
  - Any attached review notes in `ops/evidence/`

---

## Final Decision

- **Canon consistency:** [ ] PASS [ ] FAIL
- **Arc coherence:** [ ] PASS [ ] FAIL
- **Scene consequence integrity:** [ ] PASS [ ] FAIL

### Outcome
- [ ] **GO**
- [ ] **NO-GO**

Reviewer: ____________________  
Date: ____________________  
Commit / Snapshot reviewed: ____________________

## Fail Log (required for any FAIL)

| Gate Item | Failure Summary | Evidence Path(s) | Fix Owner | Recheck Needed By |
|---|---|---|---|---|
|  |  |  |  |  |
