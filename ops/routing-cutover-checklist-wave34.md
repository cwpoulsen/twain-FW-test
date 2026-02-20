# Routing Cutover Checklist — Wave 34

Date: 2026-02-20  
Companion to: `ops/routing-reduction-proposal-wave33.md`, `ops/route-supersession-matrix-wave32.md`, `ops/routing-archive-prep-wave29.md`, `ops/strategy-control-log.md` (latest entry first).  
Scope: non-destructive routing cutover for moving legacy decision-routing docs to archive **after signoff**.

## Decision / signoff gate (must be explicit)
Proceed only when a reviewer confirms all of the following:
- [ ] `ops/decision-ready-packet-wave30.md` and `ops/decision-quickfill-card-wave32.md` are the active decision surfaces.
- [ ] No active review path requires direct edits in the legacy docs listed below.
- [ ] Move is non-destructive (move-only; no delete/rewrite of archived content).

## Cutover set (this wave)
Primary archive candidates:
- `ops/decision-signoff-tracker-wave28.md`
- `ops/decision-resolution-sheet-wave29.md`
- `ops/decision-answers-template-wave31.md`
- `ops/unresolved-decisions-brief-wave26.md`

Target archive location:
- `ops/archive/review-routing-legacy/`

## Prerequisites (pre-flight)
- [ ] Working tree is clean (`git status`).
- [ ] Capture baseline SHA for audit trail.
- [ ] Confirm target archive directory exists (or create it).
- [ ] Run route-reference grep checks and review hits for active-path usage.
- [ ] If active-path hits exist, patch routes first and re-check before move.

### Example pre-flight commands (reference only; commented)
```bash
# git status --short
# git rev-parse --short HEAD
# mkdir -p ops/archive/review-routing-legacy
# rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
```

## Execution (move-only cutover)
Perform the archive move as a single bounded change set.

### Exact move commands (examples only; keep commented)
```bash
# mkdir -p ops/archive/review-routing-legacy
# mv ops/decision-signoff-tracker-wave28.md ops/archive/review-routing-legacy/
# mv ops/decision-resolution-sheet-wave29.md ops/archive/review-routing-legacy/
# mv ops/decision-answers-template-wave31.md ops/archive/review-routing-legacy/
# mv ops/unresolved-decisions-brief-wave26.md ops/archive/review-routing-legacy/
```

## Verification checks (post-move)
- [ ] All four files exist under `ops/archive/review-routing-legacy/`.
- [ ] Files no longer exist at original paths.
- [ ] Routing docs reference active surfaces (W30/W32) for primary workflow.
- [ ] `git diff --name-status` shows expected `R`/rename or move entries only.
- [ ] Optional: update/archive index pointers in a follow-up commit if required by reviewer flow.

### Example verification commands (reference only; commented)
```bash
# ls -1 ops/archive/review-routing-legacy
# test ! -e ops/decision-signoff-tracker-wave28.md && echo "moved: wave28"
# test ! -e ops/decision-resolution-sheet-wave29.md && echo "moved: wave29"
# test ! -e ops/decision-answers-template-wave31.md && echo "moved: wave31"
# test ! -e ops/unresolved-decisions-brief-wave26.md && echo "moved: wave26"
# rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
# git diff --name-status
```

## Rollback notes (non-destructive)
If verification fails or signoff is revoked, rollback by moving files back to original paths in one commit.

### Example rollback commands (reference only; commented)
```bash
# mv ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md ops/
# mv ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md ops/
# mv ops/archive/review-routing-legacy/decision-answers-template-wave31.md ops/
# mv ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md ops/
# git diff --name-status
```

Rollback conditions:
- Active routing still points to archived docs for required decisions.
- Reviewer confirms unresolved dependency on a moved file.
- Archive target path mismatch or incomplete move set.

## Commit template (when executing cutover)
Use a single commit for move set plus any minimal routing pointer updates.

```bash
# git add -A
# git commit -m "ops: wave34 non-destructive routing cutover checklist + legacy archive move prep"
```

## Contradiction/continuity check
- Canon/timeline/policy semantics changed: none.
- Change class: ops routing cutover procedure only.
