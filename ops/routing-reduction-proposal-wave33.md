# Routing Reduction Proposal — Wave 33

Date: 2026-02-20  
Companion to: `ops/route-supersession-matrix-wave32.md`, `ops/routing-archive-prep-wave29.md`, `ops/strategy-control-log.md` (latest entry first).  
Scope: recommend the **next non-destructive archive moves after signoff** for overlapping review-routing docs.

## Decision-first summary
Based on Wave 32 supersession status, the next archive wave should prioritize already-superseded decision-routing intermediates, then one legacy decision surface that is no longer primary.

## Recommended archive candidates (post-signoff)

| Priority | File | Wave32 status | Why archive now | Recommended archive path |
|---|---|---|---|---|
| 1 | `ops/decision-signoff-tracker-wave28.md` | superseded | Intermediate tracker role is replaced by W30 decision packet + W32 quickfill surface; overlaps with newer decision-capture flow. | `ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md` |
| 1 | `ops/decision-resolution-sheet-wave29.md` | superseded | Transitional resolution layer replaced by W30 packet and W31/W32 answer surfaces; now duplicates decision defaults and impacted-files guidance. | `ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md` |
| 1 | `ops/decision-answers-template-wave31.md` | superseded | Explicitly superseded by W32 quickfill card; keeping both invites split-entry risk. | `ops/archive/review-routing-legacy/decision-answers-template-wave31.md` |
| 2 | `ops/unresolved-decisions-brief-wave26.md` | legacy | Wave32 marks it as rationale context, not active decision-call surface; archive after validating all active routes now point to W30/W32 chain. | `ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md` |

## Keep in place (not archive in this step)
- `ops/decision-ready-packet-wave30.md` (primary)
- `ops/decision-quickfill-card-wave32.md` (current quick-answer surface)
- `ops/decision-queue-wave25.md` (supporting upstream analysis)
- `ops/doc-merge-plan-wave25.md`, `ops/supersession-finalize-wave26.md`, `ops/routing-archive-prep-wave29.md` (active routing-control dependencies)

## Rationale
1. **Max overlap reduction with minimal risk:** the three Priority-1 docs are all superseded in Wave32 and can be archived with low operational impact.
2. **Decision-first cadence alignment:** trimming obsolete decision forms reduces reviewer ambiguity and supports one clear answer path (W30 + W32).
3. **Non-destructive safety:** move-only archive action preserves recoverability and audit trail.

## Risk notes and mitigations

| Risk | Impact | Mitigation before move |
|---|---|---|
| Stale internal links to archived docs | Medium | Run a link/grep pass over `ops/*.md` for the four candidate filenames; patch active route docs to W30/W32 targets first. |
| Reviewer habit memory (people still open old forms) | Medium | Leave one-line stub note at original path or add explicit “archived; use W30/W32” banner in archive index. |
| Loss of historical decision context | Low | Keep files in `ops/archive/review-routing-legacy/` unchanged; do not compress content during this move wave. |
| Partial move causing mixed routing state | Medium | Execute all Priority-1 files in one commit; execute Priority-2 only if route checks pass in same review window. |

## Signoff gate (required)
Archive move should proceed only after explicit signoff that:
- W30/W32 are the only active decision answer surfaces,
- route-map/reading-guide references to archived files are removed or marked legacy,
- archive is non-destructive (move only, no deletions).

## Proposed execution order (when approved)
1. Move Priority-1 files.
2. Update `ops/archive-index-wave20.md` and active route docs with legacy pointers.
3. Re-run routing grep check for old filenames.
4. Move Priority-2 (`unresolved-decisions-brief-wave26.md`) only if no active primary-route dependency remains.

## Contradiction/continuity check
- Canon, timeline, and policy semantics changed: none.
- Change class: routing-surface reduction proposal only.
