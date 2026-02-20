# Contradiction Hunt — Wave 24

Date: 2026-02-20 (America/New_York)
Scope: targeted contradiction/stale-lock-reference hunt across top authority docs and scene packet index docs, following `ops/strategy-control-log.md` latest entry (targeted depth wave, contradiction-first).

## Files Reviewed (target set)
- `canon/canon-ledger-v2.md`
- `ops/continuity-holes-register-v1.md`
- `ops/continuity-lock-check-matrix-v1.md`
- `ops/reality-gate-enforcement-pack-v1.md`
- `series/scene-packets-books1-4-v1.md`
- `series/scene-packets-books5-7-bridge-v1.md`
- `series/scene-packets-books8-10-endgame-bridge-v1.md`

## Changed Files
1. `canon/canon-ledger-v2.md`
   - Tightened AI timing lock language to explicit first-scene acquisition:
     - "opening spec-ops extraction" -> "**first scene** (opening extraction)".

2. `ops/continuity-lock-check-matrix-v1.md`
   - AI timing row updated to explicit first-scene wording and added `canon/canon-ledger-v2.md` as authority.
   - Fabrication ladder row normalized to lock order `Class 4/3 -> Class 2 (Blackfly) -> fragile Class 1 (Asterion)`.

3. `series/scene-packets-books1-4-v1.md`
   - Resolved AI timing contradiction by moving acquisition implication to first scene packet (B1-S01 custody event context).
   - Reframed B1-S03 databank raid as training/hardening payload for already-held seed (not first acquisition).
   - Updated one stale reference phrase to "Asterion fragile Class 1 context."

## Contradiction-Check Summary

### Canon locks checked
- AI seed first-scene acquisition + databank-later training/upgrade lock: **PASS after patch**.
- Asterion League naming lock (no generic Belter drift in active narrator-canon): **PASS**.
- Fabricator taxonomy lock (Class 4/3/2/1; Blackfly Class 2; Asterion fragile Class 1): **PASS after lock-matrix normalization**.
- Core crew post-defection free-operator framing: **PASS (no regression found in targeted docs)**.
- Realism gate lock (latency, low-g, logistics, fatigue, bounded certainty): **PASS (rows explicit across scene packet indexes)**.

### Contradictions fixed
- **C-24-001 (P0):** Scene packet B1-S03 implied first AI-seed acquisition during databank raid.
  - Fix: B1-S03 now explicitly training/upgrade payload for pre-existing seed.
- **C-24-002 (P1 stale lock phrasing):** Lock matrix used "opening spec-op" wording without explicit first-scene requirement.
  - Fix: first-scene wording made explicit; ledger added as primary authority.
- **C-24-003 (P1 stale taxonomy phrasing):** Lock matrix used "Class 3/4" order.
  - Fix: normalized to canonical `Class 4/3/2/1` expression.
- **C-24-004 (P2 wording drift):** One continuity ref used weaker "Asterion Class 1" phrasing.
  - Fix: changed to "Asterion fragile Class 1 context."

## Keep / Merge / Archive Recommendation
- **Keep:**
  - `canon/canon-ledger-v2.md`
  - `ops/continuity-lock-check-matrix-v1.md`
  - `series/scene-packets-books1-4-v1.md`
  - `ops/continuity-holes-register-v1.md`
  - `ops/reality-gate-enforcement-pack-v1.md`
  - `series/scene-packets-books5-7-bridge-v1.md`
  - `series/scene-packets-books8-10-endgame-bridge-v1.md`
- **Merge:** none required this wave (no duplicate authority surface discovered in target set).
- **Archive:** none recommended this wave (all reviewed docs remain active governance/index surfaces).

## Commit Intent
This wave is a targeted contradiction/stale-reference correction pass only; no net-new canon introduced.
