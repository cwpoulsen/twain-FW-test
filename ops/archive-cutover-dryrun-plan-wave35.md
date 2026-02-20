# Archive Cutover Dry-Run Plan — Wave 35

Date: 2026-02-20  
Companion to: `ops/routing-cutover-checklist-wave34.md`, `ops/routing-reduction-proposal-wave33.md`, `ops/strategy-control-log.md` (latest entry first).  
Scope: dry-run only for legacy decision-routing archive cutover (no file moves in this wave).

## Decision-first objective
Prepare a reviewer-ready, non-destructive cutover plan that archives legacy routing surfaces only after explicit signoff that W30/W32 remain the active decision path.

## Proposed cutover set (execution wave, not this dry-run)
- `ops/decision-signoff-tracker-wave28.md`
- `ops/decision-resolution-sheet-wave29.md`
- `ops/decision-answers-template-wave31.md`
- `ops/unresolved-decisions-brief-wave26.md`

Target archive directory:
- `ops/archive/review-routing-legacy/`

## Dry-run command preview (no-op / inspection only)
```bash
# 0) Safety: verify clean working tree
 git status --short

# 1) Audit anchor: capture baseline SHA
 git rev-parse --short HEAD

# 2) Ensure archive target path exists (safe if already present)
 mkdir -p ops/archive/review-routing-legacy

# 3) Route-usage scan for legacy filenames in ops docs
 rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md

# 4) Preview move set without executing (render exact commands)
 printf '%s\n' \
  "mv ops/decision-signoff-tracker-wave28.md ops/archive/review-routing-legacy/" \
  "mv ops/decision-resolution-sheet-wave29.md ops/archive/review-routing-legacy/" \
  "mv ops/decision-answers-template-wave31.md ops/archive/review-routing-legacy/" \
  "mv ops/unresolved-decisions-brief-wave26.md ops/archive/review-routing-legacy/"

# 5) Confirm no path changes occurred in dry-run
 git diff --name-status
```

## Expected touched files

### In this dry-run wave (actual)
- `ops/archive-cutover-dryrun-plan-wave35.md` (new plan doc only)

### In live cutover execution wave (expected)
Move operations (same content, new path):
- `ops/decision-signoff-tracker-wave28.md` -> `ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md`
- `ops/decision-resolution-sheet-wave29.md` -> `ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md`
- `ops/decision-answers-template-wave31.md` -> `ops/archive/review-routing-legacy/decision-answers-template-wave31.md`
- `ops/unresolved-decisions-brief-wave26.md` -> `ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md`

Potential pointer/index updates in same or follow-up commit (if signoff requires):
- `ops/archive-index-wave20.md`
- Any active routing docs still referencing legacy paths from `ops/*.md` grep hits

## Verification checklist (for live cutover)
- [ ] Reviewer signoff explicitly confirms W30/W32 are the active decision-answer surfaces.
- [ ] `git status --short` clean before move commit.
- [ ] All four files present under `ops/archive/review-routing-legacy/` after move.
- [ ] Original four root `ops/` paths no longer exist.
- [ ] `rg` scan across `ops/*.md` shows no active-path dependency on old filenames.
- [ ] `git diff --name-status` contains only expected move/rename entries (+ intentional pointer/index updates if any).
- [ ] Commit message clearly marks non-destructive archive move.

## Rollback checklist (if verification fails)
- [ ] Stop and do not layer extra edits until routes are stabilized.
- [ ] Move each file back to original `ops/` path in one bounded rollback commit.
- [ ] Re-run `rg` route-usage scan to verify active routing restored.
- [ ] Re-check `git diff --name-status` for clean rollback state.
- [ ] Record rollback reason (stale route dependency, incomplete move, or revoked signoff).

Rollback command template:
```bash
mv ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md ops/
mv ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md ops/
mv ops/archive/review-routing-legacy/decision-answers-template-wave31.md ops/
mv ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md ops/
```

## Acceptance criteria for this Wave 35 dry-run
1. Plan is explicit, non-destructive, and signoff-gated.
2. Command preview includes inspection-first flow and exact move templates.
3. Expected touched files are enumerated for both dry-run and live cutover.
4. Verification and rollback checklists are complete and executable.

## Contradiction/continuity check
- Canon/timeline/policy semantics changed: none.
- Change class: ops routing procedure planning only.
