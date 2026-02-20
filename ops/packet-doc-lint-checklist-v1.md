# Packet Doc Lint Checklist v1 (Lightweight)

Purpose: quick human lint pass for scene packet docs before/after weekly monitor evidence capture.
Scope: `series/scene-packets-books1-4-v1.md`, `series/scene-packets-books5-7-bridge-v1.md`, `series/scene-packets-books8-10-endgame-bridge-v1.md`

Cross-refs:
- `ops/monitor-pack-wave21.md`
- `ops/continuity-holes-register-v1.md`
- `ops/reality-gate-enforcement-pack-v1.md`

---

## Lint Checks (10-minute pass)

Mark each line PASS / FAIL / N/A.

1. [ ] `## Scene Packet Template Lock (R-005)` block exists in each packet authority doc.
2. [ ] Every `### Packet ...` entry includes all required fields:
   - Mission seed (or mission-chain anchor)
   - Objective
   - Conflict
   - Tactical geometry
   - Reality gate row
   - Emotional turn
   - Consequence ledger
   - Continuity refs
3. [ ] Required fields appear in canonical order (no swaps/reordering).
4. [ ] `Reality gate row` is explicit (not implied) and includes latency + logistics/fatigue + bounded certainty language.
5. [ ] `Tactical geometry` includes at least one concrete operational constraint (distance, burn class, timing window, heat/radiator, comm lag, etc.).
6. [ ] `Consequence ledger` includes at least two time layers (Immediate + Delayed) and one broader cost (`Cross-book dependency` or `Moral debt`).
7. [ ] `Continuity refs` point to concrete anchors (timeline seq and/or canon/ops dependency refs), not generic “see docs.”
8. [ ] No packet silently assumes perfect realtime command across latency-constrained space.
9. [ ] No packet uses Earthlike-combat phrasing that ignores anchoring/recoil behavior in low-g contexts.
10. [ ] Any packet FAIL is logged to `ops/continuity-holes-register-v1.md` with owner + recheck date.

---

## Recording format (optional)

```md
### Packet lint run — YYYY-MM-DD
- Scope: Books 1-4 / 5-7 / 8-10 packet docs
- Result: PASS/WARN/FAIL
- Fails: none / (list packet IDs)
- Logged to continuity register: yes/no
- Reviewer: ...
```
