# Release-Candidate Index Pack (Wave 17)

Date: 2026-02-19  
Audience: Chris review  
Scope: Bible navigation and release-readiness indexing after post-250k reconciliation closeout.

Supersession note (Wave 25): this is a historical Wave 17 RC index snapshot. For current routing, use `ops/start-here-review-path.md` (primary route), `ops/executive-summary-wave20.md` (status), and `ops/handoff-briefing-wave23.md` (action queue).

---

## 1) Reader Navigation Notes (Start Here)

Recommended read order for fast alignment:
1. `ops/post250k-reconciliation-completion-status-2026-02-19.md` (current release state)
2. `canon/canon-ledger-v2.md` (core truth and lock assumptions)
3. `timeline/master-timeline-sequence-v1.md` + `series/books1-10-arc-dependency-grid-v1.md` (causal spine)
4. Scene packet stacks:
   - `series/scene-packets-books1-4-v1.md`
   - `series/scene-packets-books5-7-bridge-v1.md`
   - `series/scene-packets-books8-10-endgame-bridge-v1.md`
5. Domain deep dives (`tech/`, `factions/`, `locations/`) as needed.

If reviewing for contradictions, run lock checks before prose edits:
- `ops/continuity-lock-check-matrix-v1.md`
- `ops/continuity-guard-grep-recipes-v1.md`
- `ops/contradiction-scanner-checklist-v1.md`

---

## 2) Table of Authorities (Release RC)

| Priority | Authority File | Why It Is Authoritative |
|---:|---|---|
| 1 | `canon/canon-ledger-v2.md` | Canon root: actor naming, core constraints, causality chain, contradiction locks. |
| 2 | `timeline/master-timeline-sequence-v1.md` | Chronology authority for event order and causality timing. |
| 3 | `series/books1-10-arc-dependency-grid-v1.md` | Inter-book dependency and handoff gate authority. |
| 4 | `ops/continuity-lock-check-matrix-v1.md` | Lock domains, failure classes, and severity mapping. |
| 5 | `ops/continuity-guard-grep-recipes-v1.md` | Enforcement commands for pre/post-wave lock scans (A1-E2 families). |
| 6 | `ops/contradiction-scanner-checklist-v1.md` | Structured contradiction triage workflow. |
| 7 | `ops/domain-validation-checklists-v1.md` | Domain-level validation gates across canon/series/timeline/etc. |
| 8 | `ops/post-250k-reconciliation-framework-v1.md` | Reconciliation pass 0-8 operating procedure. |
| 9 | `ops/post250k-reconciliation-completion-status-2026-02-19.md` | Final release audit state and blocker status. |

---

## 3) Lock Summary (RC Gate)

Source basis:
- `ops/continuity-lock-check-matrix-v1.md`
- `ops/evidence/post250k-reconciliation-2026-02-19-final-sweep.txt`
- `ops/post250k-reconciliation-completion-status-2026-02-19.md`

| Lock Domain | Expected State | RC Status |
|---|---|---|
| Naming lock | Asterion League canonical naming preserved | PASS |
| AI timing lock | AI seed/system acquired in opening spec-op; databank later adds training/provenance | PASS |
| Pursuit uncertainty lock | Blackfly position is unknown/probabilistic after masking | PASS |
| Physics realism lock | Low-g anchoring/attitude-control/recoil discipline preserved | PASS |
| Warform agency lock | Full override depicted as non-conscious remote operation | PASS |
| Fabrication ladder lock | Class 3/4 base -> Blackfly Class 2 -> Asterion Class 1 | PASS |
| Process traceability lock | Current file references and audit trail reproducible | PASS |

Release lock status snapshot:
- P0 unresolved: 0
- P1 unresolved: 0
- P2 contradictions from final sweep: 0
- Strategic monitor risks remain (non-blocking): see §7 Known-Risk Ledger.

---

## 4) Major Arc Index (Books 1-10)

Primary arc authority: `series/books1-10-arc-dependency-grid-v1.md`

| Book | Arc Function | Critical Handoff Gate |
|---:|---|---|
| 1 | Betrayal/survival + AI-seed custody origin | Box custody + admissible shard + penetrable sanctuary network |
| 2 | Alliance-market legitimacy + witness/provenance protection | Externalized witness chain + trust protocol |
| 3 | Proof war + monopoly-of-truth fracture | Atrocity proofs become denial-resistant |
| 4 | Transition anti-relapse scaffolding | Interim charter + governor retirement path + conditional handover |
| 5 | Scarcity-governance consolidation | Charter survives first stress cycle |
| 6 | Industrial parity without capture | Multi-party fabrication oversight survives sabotage |
| 7 | Corridor law at chokepoints | Inspection/sanctions/appeals stack functioning |
| 8 | Earth-approach staging with legitimacy constraints | Civil partners + sustainable corridors + shared ROE consensus |
| 9 | Controlled systems seizure without governability collapse | Kernels neutralized/escrowed + services above collapse floor + war-to-law clock |
| 10 | Anti-relapse settlement + founder drawdown | Imperfect but self-correcting order; no unilateral recapture path |

---

## 5) Tech + Faction Index

### 5.1 Tech Index

| File | Role in Bible |
|---|---|
| `tech/technical-architecture-v1.md` | Core technical constraints and scene hard-check checklist. |
| `tech/fusion-transit-assumptions-and-lane-calculus-v1.md` | Quant model for travel/comms envelopes. |
| `tech/interplanetary-transit-and-comms-envelope-v1.md` | Operational transit/latency baseline used in timeline/scene realism. |
| `tech/fabricator-classes.md` | Fabrication class taxonomy lock (4/3/2/1). |
| `tech/governor-module-autonomy-bands-v1.md` | Marine governor autonomy and constraint model. |
| `tech/fabrication-systems.md` | Fabrication ecosystem behavior and vulnerabilities. |
| `tech/operational-logistics.md` | Theater logistics framing aligned to class and transit constraints. |

### 5.2 Faction Index

| File | Role in Bible |
|---|---|
| `factions/factions-doctrine-ledger-v1.md` | Canon faction baseline, means/vulnerabilities, doctrine collision matrix. |
| `factions/major-factions.md` | Expanded faction-level operational details. |
| `factions/doctrine-and-command.md` | Command behavior and doctrine implementation layer. |
| `factions/freed-voider-bands-dossier-v1.md` | FVB destabilizer ecology and policy implications. |
| `factions/conflict-escalation-ladders-v1.md` | Escalation envelopes and deterrence/retaliation logic. |
| `factions/failure-modes-and-escalation.md` | Faction failure pattern catalog for consequence realism. |
| `factions/antagonist-adaptation-cadence-doctrine-books1-4-v1.md` | Antagonist adaptation timing model across early arc. |

---

## 6) Scene Packet Index

Primary packet authorities:
- `series/scene-packets-books1-4-v1.md` (24 packets)
- `series/scene-packets-books5-7-bridge-v1.md` (20 packets)
- `series/scene-packets-books8-10-endgame-bridge-v1.md` (24 packets)

Total indexed scene packets: **68**

| Packet Set | Coverage | Sequence Range Anchor | Notes |
|---|---|---|---|
| Books 1-4 | B1-S01..B4-S06 (24) | ~0160-0290 + bridge to 0300 | Betrayal/proof/transition phase with Wave 14 carryover overlays. |
| Books 5-7 | B5-S01..B7-S06 (20) | ~0310-0415 | Scarcity governance, parity race, chokepoint corridor law. |
| Books 8-10 | B8-S01..B10-S08 (24) | ~0420-0535 | Earth approach, controlled seizure, anti-relapse settlement endgame. |

Packet template lock status:
- R-005 template standardization: OPEN (monitor; canonical ledger).
- Mandatory packet fields and reality-gate row are present across all packet sets.

---

## 7) Known-Risk Ledger (RC Snapshot)

Source basis:
- `ops/continuity-holes-register-v1.md`
- `ops/post250k-reconciliation-completion-status-2026-02-19.md`

### 7.1 Canonical risk status snapshot (normalized)

Canonical source-of-truth: `ops/continuity-holes-register-v1.md` → **Canonical Risk Status Table (R-005..R-008)**.

| Risk ID | Severity | Status | Basis |
|---|---|---|---|
| R-005 | P2 | OPEN (monitor) | Scene packet template standardization remains bounded backlog work. |
| R-006 | P2 | CLOSED (Wave 17) | `ops/asterion-governance-charter-doctrine-pack-v1.md` + wave17 evidence log. |
| R-007 | P2 | CLOSED (Wave 16) | `ops/ai-seed-safety-and-governance-doctrine-pack-v1.md` + wave16 evidence log. |
| R-008 | P2 | CLOSED (Wave 17) | `ops/fvb-subfaction-drift-monitor-and-intervention-playbook-v1.md` + wave17 evidence log. |

Release interpretation:
- No P0/P1 blockers; remaining bounded strategic-depth monitor risk is **R-005 only**.

---

## 8) Repo Map (Chris Review Quick Map)

| Directory | What to review there |
|---|---|
| `canon/` | Canon truths, contradiction locks, governance worldview, patch sets. |
| `timeline/` | Sequence authority, book-phase maps, causality ordering. |
| `series/` | Arc scaffolds, packet packs, dependency grid, closeout mechanics. |
| `tech/` | Physics/logistics/fabrication/governor constraints. |
| `factions/` | Doctrine actors, adaptation models, destabilizer ecology. |
| `characters/` | Core squad and supporting cast causality/behavior docs. |
| `locations/` | Theater atlas and civil governance terrain under scarcity. |
| `ops/` | Governance of process: lock checks, reconciliation evidence, progress/pass logs. |
| `scenes/` | Specific scene drafts and tactical episode artifacts. |

Suggested audit pass for final RC signoff:
1. `ops/` (status + evidence)
2. `canon/` and `timeline/` (truth + sequence)
3. `series/` (arc and packet continuity)
4. `tech/` + `factions/` (mechanism consistency)
5. targeted `characters/` and `locations/` spot checks.

---

## 9) RC Pack File Manifest (this commit)

- `ops/release-candidate-index-pack-wave17-v1.md` (this file)
- `ops/release-candidate-index-pack-wave17-commit-manifest.md` (file list + word counts)
