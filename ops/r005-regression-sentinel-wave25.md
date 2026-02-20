# R-005 Regression Sentinel — Wave 25 (2026-02-20)

Evidence: `ops/evidence/wave25-r005-regression-sentinel-2026-02-20.txt`
Baseline compared: `ops/evidence/wave24-r005-gate-check-2026-02-20.txt`

## Scope
- `series/scene-packets-books1-4-v1.md`
- `series/scene-packets-books5-7-bridge-v1.md`
- `series/scene-packets-books8-10-endgame-bridge-v1.md`

## ST-1..ST-4 results
- **ST-1 (template-lock block present): PASS**
- **ST-2 (required field coverage counts): PASS**
- **ST-3 (required field order): PASS**
- **ST-4 (lightweight packet lint): PASS**

## Regression comparison vs Wave 24
- Prior status: PASS/PASS/PASS/PASS
- Current status: PASS/PASS/PASS/PASS
- Packet coverage counts unchanged from Wave 24 baseline (24 / 20 / 24 packet sets).
- No new regressions detected.

## Compliance patches
- None required.
- No canon-lock or story-content edits made in this sentinel pass.

## Gate disposition
- **Wave 25 R-005 regression sentinel: PASS**
- `R-005` remains **OPEN (monitor)** with no new compliance misses in this cycle.
