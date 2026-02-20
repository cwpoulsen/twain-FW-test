# Supersession Finalize — Wave 26 (Consolidation-Only Step 1)

Companion to: `ops/doc-merge-plan-wave25.md` (merge/archive staging), `ops/doc-routing-prune-wave27.md` (primary-route lock), and `ops/start-here-review-path.md` (active entry routes).
Routing note (Wave 28): supporting metadata/supersession control log; primary review entry routes remain in `ops/start-here-review-path.md`.

Date: 2026-02-20
Scope: apply low-risk review-routing supersession/primary-route annotations to remaining overlapping ops guides.
Constraint honored: **CANON LOCKS unchanged** (ops-layer metadata only; no canon-domain edits).

## Changed files
1. `ops/start-here-review-path.md`
2. `ops/executive-summary-wave20.md`
3. `ops/archive-index-wave20.md`
4. `ops/handoff-briefing-wave23.md`
5. `ops/reviewer-checklist-wave21.md`
6. `ops/monitor-pack-wave21.md`
7. `ops/decision-queue-wave25.md`
8. `ops/doc-map-dedupe-wave24.md`

## What was applied
- Added a top-level metadata line to each touched guide:
  - `Companion to: ...`
- Goal: remove routing ambiguity and make primary-route adjacency explicit without deleting or merging files in this step.

## Keep / Merge / Archive recommendation
- **Keep (active routing set):**
  - `ops/start-here-review-path.md` (primary entrypoint)
  - `ops/executive-summary-wave20.md` (status snapshot)
  - `ops/handoff-briefing-wave23.md` (action queue)
  - `ops/doc-map-dedupe-wave24.md` (dedupe/role-boundary governance)
- **Keep (operational companions):**
  - `ops/reviewer-checklist-wave21.md`
  - `ops/monitor-pack-wave21.md`
  - `ops/decision-queue-wave25.md`
- **Keep as catalog/reference (not primary route):**
  - `ops/archive-index-wave20.md`
- **Archive:** none in this consolidation-only step (annotation-first pass).

## Notes
- This pass intentionally avoided structural merges/deletions.
- Follow-on step can execute merge/archive actions once human decision queue confirms final routing ownership.
