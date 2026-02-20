# Controlled Move Execution Plan — Wave 39

Date: 2026-02-20  
Metadata: wave=39 | doc=controlled-move-plan | scope=legacy-decision-doc-archive-cutover | mode=execution-plan-only | gate=READY-required | moves=deferred
Companion to: `ops/strategy-control-log.md` (latest entry first), `ops/archive-cutover-readiness-recheck-wave38.md`, `ops/routing-cutover-checklist-wave34.md`

## Strategy-control first check
Applied first: latest strategy log entry `2026-02-20T01:23-05:00` (decision-first cadence, consolidation-only, avoid unnecessary new surfaces).

Wave38 readiness state is currently **FAIL / NOT READY FOR ARCHIVE MOVE**.  
This Wave39 artifact is a **controlled execution plan only** and does **not** perform any file moves.

## Scope
When gate is READY, move these legacy decision docs to archive target:
- `ops/decision-signoff-tracker-wave28.md`
- `ops/decision-resolution-sheet-wave29.md`
- `ops/decision-answers-template-wave31.md`
- `ops/unresolved-decisions-brief-wave26.md`

Target:
- `ops/archive/review-routing-legacy/`

## Gate condition (must be true before execution)
Proceed only when an explicit recheck verdict is recorded as:
- **READY FOR ARCHIVE MOVE**

Minimum gate evidence required:
1. Route/update-surface blockers listed in Wave38 are resolved.
2. Grep verification no longer shows these four files as active decision-call/update targets in live routing docs.
3. Reviewer signoff confirms W30/W32 remain active decision-answer surfaces.

---

## Controlled command set (commented examples only)

### 1) Preflight (no moves)
```bash
# git status --short
# git rev-parse --short HEAD
# mkdir -p ops/archive/review-routing-legacy
# grep -nE "primary decision-call route|Decision calls \(primary\)|decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
# rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
```

### 2) Execute move set (RUN ONLY AFTER READY)
```bash
# mkdir -p ops/archive/review-routing-legacy
# mv ops/decision-signoff-tracker-wave28.md ops/archive/review-routing-legacy/
# mv ops/decision-resolution-sheet-wave29.md ops/archive/review-routing-legacy/
# mv ops/decision-answers-template-wave31.md ops/archive/review-routing-legacy/
# mv ops/unresolved-decisions-brief-wave26.md ops/archive/review-routing-legacy/
```

### 3) Post-move verification
```bash
# ls -1 ops/archive/review-routing-legacy
# test -e ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md && echo "archive ok: wave28"
# test -e ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md && echo "archive ok: wave29"
# test -e ops/archive/review-routing-legacy/decision-answers-template-wave31.md && echo "archive ok: wave31"
# test -e ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md && echo "archive ok: wave26"
# test ! -e ops/decision-signoff-tracker-wave28.md && echo "source cleared: wave28"
# test ! -e ops/decision-resolution-sheet-wave29.md && echo "source cleared: wave29"
# test ! -e ops/decision-answers-template-wave31.md && echo "source cleared: wave31"
# test ! -e ops/unresolved-decisions-brief-wave26.md && echo "source cleared: wave26"
# rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
# git diff --name-status
```

Expected verification outcome:
- All 4 files present in archive target.
- All 4 source paths absent.
- No active-route regression to archived docs.
- Diff is bounded to move entries (plus any explicitly approved pointer updates).

### 4) Rollback (if verification fails or signoff revoked)
```bash
# mv ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md ops/
# mv ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md ops/
# mv ops/archive/review-routing-legacy/decision-answers-template-wave31.md ops/
# mv ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md ops/
# git diff --name-status
# rg -n "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
```

Rollback triggers:
- READY gate no longer valid at execution time.
- Any active workflow still requires edits against one of the four moved files.
- Incomplete move set, path mismatch, or unexpected diff spread.

---

## Execution control checklist
- [ ] READY verdict explicitly recorded in latest readiness recheck artifact.
- [ ] Working tree clean before cutover.
- [ ] Baseline SHA captured.
- [ ] Move set executed as one bounded change.
- [ ] Verification checks pass.
- [ ] Rollback path validated before final commit.

## Commit guidance for eventual execution wave
(Reference only; do not run as part of this planning artifact.)

```bash
# git add -A
# git commit -m "ops: wave39 controlled move execution plan for legacy decision-doc archive cutover (READY-gated)"
```

## Contradiction / continuity statement
- Canon/timeline/policy semantics changed: none.
- Change class: ops execution planning only (no live doc moves performed).
