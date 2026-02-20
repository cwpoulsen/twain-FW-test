# Continuity Holes Register v1 (Wave 3 Updated)

Status: active continuity audit ledger  
Owner: bible maintenance pass  
Last updated: 2026-02-19

Cross-refs:
- Dependency map: `ops/continuity-dependency-map-v1.md`
- Scanner checklist: `ops/contradiction-scanner-checklist-v1.md`
- Canon patch sets: `canon/continuity-patch-wave2-v1.md`, `canon/continuity-patch-wave3-v1.md`
- Master timeline authority: `timeline/master-timeline-sequence-v1.md`

---

## Severity Key
- **P0:** breaks causality or core arc readability now
- **P1:** high drift risk across books if unresolved
- **P2:** quality/clarity gap; does not yet break canon

---

## Hole Ledger

| Hole ID | Severity | Type | Problem Statement | Affected Docs | Resolution Status |
|---|---|---|---|---|---|
| H-001 | P0 | Sequence contradiction | Databank reveal ordering conflict with betrayal lock. | `series/book-and-series-arc-scaffolds-v1.md`, timeline docs | **FIXED** |
| H-002 | P0 | Character-arc timing conflict | Valerie brother timing split across Book 1/2 layers. | character + timeline docs | **FIXED** |
| H-003 | P1 | Mechanism gap | Escape intervention lacked latency-grounded mechanism. | timeline + canon + tech | **FIXED** |
| H-004 | P1 | Identity chain ambiguity | Unknown helper identity/trust chain underdefined. | canon + future scenes | **PARTIAL (intentional unknown)** |
| H-005 | P2 | Evidence chain fragility | Strategic proof lacked explicit custody requirements. | timeline + canon | **FIXED** |
| H-006 | P0 | Payload contradiction | Box contents underdefined; now required to contain new AI seed/system. | canon + timeline | **FIXED (Wave 3 CP-005)** |
| H-007 | P0 | Strategic-balance contradiction | Class 1 monopoly assumption conflicted with new Belt capability directive. | canon + timeline + tech | **FIXED (Wave 3 CP-006)** |
| H-008 | P1 | Arc-scale mismatch | 4-book scaffold no longer matched 10-book reconquest directive. | timeline docs | **FIXED (Books 1–10 map added)** |
| H-009 | P1 | Quantitative transit gap | Need equations/assumptions for travel realism. | tech + ops | **FIXED** |
| H-010 | P1 | Governor autonomy ambiguity | Needed explicit governor-module autonomy bands. | tech + canon | **FIXED** |
| H-011 | P1 | Destabilizer ecology gap | Missing faction model for ex-EDF rejection -> piracy/mercenary strife and Consensus intent link. | factions + canon + timeline + series | **FIXED (FVB lock integrated)** |

---

## Remaining Risks (next pass)
1. **R-005 (P2):** Add standardized scene packet template with required transit/comms/governor fields.
2. **R-006 (P2):** Add Asterion League internal governance charter constraints to prevent faction behavior drift.
3. **R-007 (P2):** Add AI-seed safety doctrine (containment, test protocol, failure escalation ladder).
4. **R-008 (P2):** Track FVB sub-faction drift to avoid flattening into single villain bloc.

---

## Wave 8 Reconciliation Scan (2026-02-19)

Scope executed: repo-wide grep scan for pre-lock residue categories: old EDF-present framing, wrong AI acquisition timing, generic Belters usage, omniscient tracking assumptions, missing low-g physics anchors.

### Closed this pass
- **W8-001 (Closed):** Legacy EDF-present framing in series authority docs.
  - Patched `series/series-architecture-v2.md` lens definition to primary post-EDF free-operator framing.
  - Patched `series/worldbuilding-core-pack-v1.md` narrative placement to opening-in-EDF -> rapid post-EDF transition.
- **W8-002 (Closed):** Legacy naming residue (`Solar Defense Force`) in discovery reservoir.
  - Patched to canonical `Earth Defense Force (EDF)` and expanded doctrine prompt to include low-g anchoring/recoil.
- **W8-003 (Closed):** Missing explicit low-g rule at series-level constraints.
  - Added non-negotiable continuity constraint for anchoring/attitude control/recoil consequences in `series/series-architecture-v2.md`.

### Open / monitor
- **W8-R1 (Open, P2 monitor):** `series/worldbuilding-core-pack-v1.md` remains a provisional ideation reservoir and still contains early-draft language in historical sections. Current authority precedence note is present; keep under drift watch when promoting content into canon-layer docs.

### Grep Evidence (pre-fix findings)
- `series/worldbuilding-core-pack-v1.md:67` -> `Solar Defense Force` naming residue.
- `series/worldbuilding-core-pack-v1.md:312` -> `EDF marine squad inbound to Belt engagement.`
- `series/series-architecture-v2.md:16` -> `Primary lens: EDF marine cohort ...` (pre-fix).
- `canon/ops/faction-naming-policy.md:14` -> only sanctioned mention of forbidden generic `Belters` label (policy context).

### Contradiction-Check Summary
- **AI acquisition timing:** no contradictory `databank-first AI acquisition` statements found in active canon/series docs.
- **Generic Belters usage:** no active narrator-canon misuse found outside policy/archival mention.
- **Omniscient tracking:** no active omniscient-control assertions found; existing references are anti-omniscience guardrails.
- **Low-g physics:** strengthened by adding series-level hard constraint; no conflicting Earthlike-combat rule found in active ops/canon constraints.
- **Result:** No remaining P0/P1 contradiction introduced by this pass; residual risk is P2 legacy-language drift in provisional reservoir docs only.
