# Continuity Lock-Check Matrix v1

| Lock Domain | Core Lock | Detection (grep family) | Primary Authority | Typical Failure | Severity Default |
|---|---|---|---|---|---|
| Naming | Anti-Consensus Belt bloc named **Asterion League** | A1/A2 | `canon/ops/faction-naming-policy.md`, `canon/canon-ledger-v2.md` | Generic labels reintroduced in narrator-canon prose | P1 |
| AI acquisition timing | AI seed/system first acquired in opening spec-op; databank later adds training/provenance | B1/B2 | `canon/continuity-patch-wave3-v1.md`, `timeline/master-timeline-sequence-v1.md` | Databank raid described as first acquisition | P0 |
| Pursuit uncertainty | Post-nuke: asset missing; current location unknown; dragnet probabilistic | C1/C2 | `ops/blackfly-unknown-position-pursuit-model-v1.md` | Omniscient/continuous tracking depiction | P1 |
| Physics realism | Small-body ops require anchoring + attitude control; recoil consequences explicit | D1/D2 | `ops/small-body-combat-and-work-credibility-manual-v1.md` | Earthlike combat language without stabilization | P1 |
| Warform agency | Full-override warforms portrayed as non-conscious remote control | D3 | `canon/canon-ledger-v2.md`, `ops/operations-doctrine-annex-v1.md` | Dialogue/intent assigned to fully overridden operators | P1 |
| Fabrication ladder | Class 3/4 distributed base -> Blackfly constrained Class 2 -> Asterion fragile Class 1 | E1/E2 | `tech/technical-architecture-v1.md`, `tech/fabricator-classes.md` | Taxonomy drift or capability inflation | P0/P1 |
| Process traceability | QA/holes register references point to current continuity ledger | process grep | `ops/continuity-holes-register-v1.md` | Stale file references break auditability | P2 |

## Execution Cadence
- Pre-wave: run A-E scans.
- Post-wave: rerun A-E + update holes register.
- Before commit: attach evidence excerpt (command + hit summary) in commit message/body or companion report.
