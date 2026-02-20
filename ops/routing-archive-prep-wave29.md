# Routing Archive Prep — Wave 29

Date: 2026-02-20
Companion to: `ops/doc-merge-plan-wave25.md` (legacy-routing archive plan), `ops/doc-routing-prune-wave27.md` (primary-route lock), `ops/routing-consolidation-wave28.md` (latest routing consolidation).
Supersedes: partial execution notes for Wave 25 Phase C archive candidates (non-destructive annotation pass only).

## Objective
Prepare non-destructive archive readiness for legacy routing docs flagged by Wave 25/27 summaries by:
1. adding explicit **Legacy route** annotations,
2. adding target archive-path hints,
3. preserving all current file locations (no move/delete).

## Scope basis (flag source)
- `ops/doc-merge-plan-wave25.md`
  - Phase C planned archive targets (Wave17 routing packs + manifests)
  - Phase D historical baseline keep-in-place note
- `ops/doc-routing-prune-wave27.md`
  - Primary-route lock, clarifying old route/support artifacts should not be treated as current entry points

## Wave 29 annotation changes (completed)

| File | Wave29 annotation added | Target archive hint | Move performed |
|---|---|---|---|
| `ops/release-candidate-index-pack-wave17-v1.md` | Companion/Supersedes metadata + Legacy route note | `ops/archive/review-routing-legacy/release-candidate-index-pack-wave17-v1.md` | No |
| `ops/final-review-pack-wave17-for-chris.md` | Companion/Supersedes metadata + Legacy route note | `ops/archive/review-routing-legacy/final-review-pack-wave17-for-chris.md` | No |
| `ops/release-candidate-index-pack-wave17-commit-manifest.md` | Companion/Supersedes metadata + Legacy route note | `ops/archive/review-routing-legacy/release-candidate-index-pack-wave17-commit-manifest.md` | No |
| `ops/final-review-pack-wave17-commit-manifest.md` | Companion/Supersedes metadata + Legacy route note | `ops/archive/review-routing-legacy/final-review-pack-wave17-commit-manifest.md` | No |
| `ops/final-snapshot-status-wave19.md` | Companion/Supersedes metadata + Legacy route note (keep-in-place default) | `ops/archive/review-routing-legacy/final-snapshot-status-wave19.md` (future optional normalization) | No |

## Non-destructive guarantee
- No file paths changed.
- No archive directory creation required for this prep pass.
- No links were retargeted in active primary-route docs.

## Routing behavior after this prep
- Current primary routes remain unchanged and explicit:
  - `ops/start-here-review-path.md`
  - `ops/reading-guide-60min-quick-review-v1.md`
  - `ops/reading-guide-1day-deep-review-v1.md`
  - `ops/unresolved-decisions-brief-wave26.md`
  - `ops/evidence/evidence-index-wave23.md`

## Recommended next step (separate approved move wave)
If/when archive moves are approved:
1. create `ops/archive/review-routing-legacy/`,
2. move only the four Wave17 pack/manifest files listed above,
3. leave one-line stubs at original paths if link stability is required,
4. keep `final-snapshot-status-wave19.md` in place unless a specific baseline-archive migration decision is made.

## Contradiction/continuity check
- Canon or timeline semantics changed: none.
- Policy/gate criteria changed: none.
- Impact class: routing metadata + archival readiness annotations only.
