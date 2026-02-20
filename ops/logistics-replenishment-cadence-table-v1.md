# Stewards of Progress — Logistics Replenishment Cadence Table v1

Status: **Operational tempo constraint reference**  
Purpose: prevent infinite-ammo/infinite-repair pacing and enforce replenishment realism.

Cross-refs:
- Logistics architecture: `tech/operational-logistics.md`
- Technical architecture: `tech/technical-architecture-v1.md`
- Timeline policy: `ops/timeline-policy.md`
- Master sequence: `timeline/master-timeline-sequence-v1.md`

---

## 1) Cadence Bands by Echelon

| Echelon | Primary Function | Planned Replenishment Cadence | Surge Cadence (max 10 days) | Failure Trigger |
|---|---|---|---|---|
| E1 Contact Zone | Patch armor, seals, ammo packs, med kits | every 8–16 hours | every 4–8 hours | >24h gap causes combat-readiness cliff |
| E2 Mobile Sustainment | Restore vehicle systems + powered armor modules | every 36–60 hours | every 24–36 hours | >72h gap forces cannibalization |
| E3 Theater Industrial Core | Component replacement, reactor modules, sensor stacks | every 5–9 days | every 3–5 days | >12d gap pushes TRI above 96h |
| E4 Strategic Mobility Layer | Theater reinforcement and heavy hull transfer | every 18–35 days | every 12–18 days | >45d gap collapses campaign initiative |
| E5 Sovereign Regeneration | Rebuild strategic reserves and key fabs | every 60–120 days | every 45–60 days | >150d gap creates state-level depletion panic |

---

## 2) Consumable Replenishment Baselines (Marine/Small-Team Scale)

| Consumable / Module Class | Normal Burn Rate | Standard Resupply Interval | Degraded Mode Interval |
|---|---|---|---|
| AP/kinetic magazines | high during contact | 12–24 hours | 36 hours max |
| Armor actuator cartridges | moderate-high | 48–72 hours | 96 hours max |
| Sealant + pressure patch kits | variable | 24–48 hours | 72 hours max |
| Field med compounds (Class 3 grade) | moderate | 24–72 hours | 96 hours max |
| Sensor mast/calibration blocks | moderate | 5–8 days | 12 days max |
| Governor-diagnostic consumables | low but mandatory | 10–14 days | 21 days max (requires waiver) |

**Rule:** three consecutive degraded-mode intervals force explicit readiness downgrade in scene notes.

---

## 3) Route Reliability and Buffer Requirements

| Route Condition | Expected Throughput Retention | Minimum Buffer to Carry | Narrative Effect |
|---|---:|---:|---|
| Green corridor | 88–96% | 12% | Forces can keep offensive tempo |
| Contested corridor | 70–87% | 25% | Frequent mission reprioritization |
| Interdicted corridor | 50–69% | 40% | Aggressive cannibalization and doctrine contraction |
| Collapse condition | <50% | n/a | Campaign enters structural retreat logic |

---

## 4) Continuity Enforcement Rules

1. Any operation lasting >72h must cite an active replenishment chain or explicitly show depletion.
2. If cadence exceeds failure trigger for the echelon in play, units cannot remain at prior effectiveness.
3. Plot-critical "sudden capability" moments require source declaration (captured stockpile, prepositioned cache, or alliance transfer).
4. Cadence violations must be logged against continuity checks in `ops/continuity-holes-register-v1.md`.
