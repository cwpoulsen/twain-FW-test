# Stewards of Progress — Books 1–4 Operational Sequence Map v1

Status: **Provisional sequence scaffolding for mission-bank placement**  
Authority: extends `timeline/master-timeline-sequence-v1.md` without overriding CORE entries 0010–0190.

---

## Sequence Blocks (Provisional)

| sequence_index | world_datetime_start (UTC) | world_datetime_end (UTC) | block_title | canon_level | notes |
|---:|---|---|---|---|---|
| 0200 | 2055-11-01T00:00:00Z | 2056-01-15T23:59:59Z | Book 1 Late Free-Team Survival Cycle | SOFT | Immediate post-0190 adaptation under active pursuit. |
| 0210 | 2056-01-16T00:00:00Z | 2056-04-30T23:59:59Z | Book 2 Opening: Dead Channels | SOFT | Kill/capture directives and alliance-market emergence. |
| 0220 | 2056-05-01T00:00:00Z | 2056-08-31T23:59:59Z | Book 2 Mid Campaign | SOFT | Brokered compacts, betrayal loops, supply attrition. |
| 0230 | 2056-09-01T00:00:00Z | 2056-12-20T23:59:59Z | Book 2 Climax Window | SOFT | Source extraction and coalition-fragility lock. |
| 0240 | 2057-01-01T00:00:00Z | 2057-04-30T23:59:59Z | Book 3 Opening: Counterintelligence Purge | SOFT | Witness erasure and authenticity-war onset. |
| 0250 | 2057-05-01T00:00:00Z | 2057-08-31T23:59:59Z | Book 3 Mid Campaign | SOFT | Chokepoint operations and elite schism exploitation. |
| 0260 | 2057-09-01T00:00:00Z | 2057-12-31T23:59:59Z | Book 3 Climax Window | SOFT | Synchronized evidence + infrastructure strikes. |
| 0270 | 2058-01-01T00:00:00Z | 2058-04-30T23:59:59Z | Book 4 Opening: Transition Fracture | SOFT | Governance destabilization and supply panic. |
| 0280 | 2058-05-01T00:00:00Z | 2058-08-31T23:59:59Z | Book 4 Mid Campaign | SOFT | Constitutional bargaining under military pressure. |
| 0290 | 2058-09-01T00:00:00Z | 2058-12-31T23:59:59Z | Book 4 Settlement Window | SOFT | Enforceable post-monopoly architecture selection. |

---

## Mapping Rules

1. Seeds in `ops/books1-4-mission-scenario-bank-v1.md` should cite one primary sequence block and optional adjacent block.
2. If a seed is promoted to scene-canon, assign a unique immutable index in `master-timeline-sequence-v1.md`.
3. Book transitions must preserve chain integrity:
   - 0190 -> 0200 -> 0210 (survival to alliance-market)
   - 0230 -> 0240 (source survival triggers purge)
   - 0260 -> 0270 (partial decentralization triggers transition crisis)
4. No mission may imply instantaneous transit or comm certainty across Belt ranges (see `ops/timeline-policy.md`).
