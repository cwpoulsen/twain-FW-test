# Doc Merge/Archive Plan — Wave 25

Companion to: `ops/doc-map-dedupe-wave24.md` (overlap analysis), `ops/supersession-finalize-wave26.md` (metadata pass), and `ops/doc-routing-prune-wave27.md` (primary-route lock).
Routing note (Wave 28): supporting merge/archive execution plan; primary review entry routes remain in `ops/start-here-review-path.md`.

Date: 2026-02-20  
Input basis: `ops/doc-map-dedupe-wave24.md` + latest strategy entry (`ops/strategy-control-log.md`, 2026-02-20T01:12-05:00).

## 1) Objective
Reduce review-routing duplication and index churn by enforcing single-role ownership:
- route = `ops/start-here-review-path.md`
- status = `ops/executive-summary-wave20.md`
- action queue = `ops/handoff-briefing-wave23.md`
- catalog = `ops/archive-index-wave20.md`

No destructive deletes in this wave.

## 2) Low-risk updates completed in Wave 25
Applied explicit supersession/historical notes (no content removal) to:
1. `ops/reading-guide-60min-quick-review-v1.md`
2. `ops/reading-guide-1day-deep-review-v1.md`
3. `ops/release-candidate-index-pack-wave17-v1.md`
4. `ops/final-review-pack-wave17-for-chris.md`
5. `ops/final-snapshot-status-wave19.md`

Result: readers are now redirected to the primary route/status/action stack without breaking legacy references.

## 3) Actionable merge/archive plan (exact moves + supersession model)

### Phase A — keep active authorities in place (no move)
Keep as active, current-control docs:
- `ops/start-here-review-path.md`
- `ops/executive-summary-wave20.md`
- `ops/handoff-briefing-wave23.md`
- `ops/archive-index-wave20.md`

### Phase B — convert duplicate guides to legacy stubs (planned)
Target files:
- `ops/reading-guide-60min-quick-review-v1.md`
- `ops/reading-guide-1day-deep-review-v1.md`

Planned transformation:
- retain file paths,
- compress bodies into short “legacy variant” stubs,
- point to `ops/start-here-review-path.md` as primary route and `ops/handoff-briefing-wave23.md` for execution sequence.

### Phase C — archive historical Wave17 packs (planned exact moves)
Create archive folder:
- `ops/archive/review-routing-legacy/`

Planned moves (non-destructive, history-preserving):
- `ops/release-candidate-index-pack-wave17-v1.md` → `ops/archive/review-routing-legacy/release-candidate-index-pack-wave17-v1.md`
- `ops/final-review-pack-wave17-for-chris.md` → `ops/archive/review-routing-legacy/final-review-pack-wave17-for-chris.md`
- `ops/release-candidate-index-pack-wave17-commit-manifest.md` → `ops/archive/review-routing-legacy/release-candidate-index-pack-wave17-commit-manifest.md`
- `ops/final-review-pack-wave17-commit-manifest.md` → `ops/archive/review-routing-legacy/final-review-pack-wave17-commit-manifest.md`

Required follow-up edits when executing moves:
- update links in `ops/start-here-review-path.md` optional section,
- update `ops/archive-index-wave20.md` historical references,
- add one-line pointer stub files at original paths if external links must remain stable.

### Phase D — preserve baseline snapshot as historical anchor (no move this wave)
- `ops/final-snapshot-status-wave19.md` stays in place with historical-baseline note.
- Use only for pre-W20 delta reconstruction.

## 4) Suggested command block for Phase C execution (future wave)
```bash
mkdir -p ops/archive/review-routing-legacy
mv ops/release-candidate-index-pack-wave17-v1.md ops/archive/review-routing-legacy/
mv ops/final-review-pack-wave17-for-chris.md ops/archive/review-routing-legacy/
mv ops/release-candidate-index-pack-wave17-commit-manifest.md ops/archive/review-routing-legacy/
mv ops/final-review-pack-wave17-commit-manifest.md ops/archive/review-routing-legacy/
```

## 5) Contradiction/continuity impact check
- Canon locks touched: none.
- Domain authority semantics changed: none.
- Effect is routing clarity/compression only.

## 6) Keep / Merge / Archive decisions (Wave 25)
- KEEP: start-here, executive-summary, handoff-briefing, archive-index.
- MERGE (planned): reading-guide 60m + 1day into start-here/handoff routing sections.
- ARCHIVE (planned exact moves): Wave17 RC/final-review pack + commit manifests.
- HISTORICAL KEEP-IN-PLACE: final-snapshot-wave19.
