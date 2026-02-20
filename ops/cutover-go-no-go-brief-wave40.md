# Cutover Go/No-Go Brief — Wave 40

Date: 2026-02-20  
Metadata: wave=40 | doc=cutover-go-no-go-brief | scope=controlled-archive-move-decision | verdict=NO-GO-NOW | mode=decision-brief  
Companion to: `ops/strategy-control-log.md` (latest entry first), `ops/archive-cutover-readiness-recheck-wave39.md`, `ops/controlled-move-plan-wave39.md`, `ops/wave39-residual-blocker-patch-report.md`

## Executive verdict for Chris
**NO-GO right now (hold cutover until one final clean recheck passes).**

Why:
- Wave39 fixed major routing blockers, but top-level live docs still contain legacy-path references that can become stale/broken immediately after move (notably references to `decision-answers-template-wave31.md` / `unresolved-decisions-brief-wave26.md` outside pure archive-control artifacts).
- Strategy log requires decision-first + consolidation discipline; safest path is one bounded preflight/recheck cycle, then execute move once clean.

## Prerequisites checklist (must all be true)
- [ ] Working tree clean (`git status --short` returns empty).
- [ ] Baseline SHA captured (`git rev-parse --short HEAD`).
- [ ] Final pre-move grep/review confirms no **active** route/update dependencies on wave26/28/29/31 docs in live decision surfaces.
- [ ] Any remaining legacy mentions are metadata/history only (or patched to archive-path context).
- [ ] Explicit READY verdict recorded in a recheck artifact.

## One-command-at-a-time sequence (commented)
```bash
# 1) Preflight and baseline
# git status --short
# git rev-parse --short HEAD
# mkdir -p ops/archive/review-routing-legacy

# 2) Final dependency check (human-review output)
# grep -nE "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md|primary decision-call route|Decision calls \(primary\)" ops/*.md

# 3) If any ACTIVE-route/update dependency remains, patch first (NO MOVE YET), then re-run step 2.
# git add -A
# git commit -m "ops: wave40 pre-cutover route cleanup for legacy decision-doc move gate"

# 4) Execute controlled move (only after READY)
# mv ops/decision-signoff-tracker-wave28.md ops/archive/review-routing-legacy/
# mv ops/decision-resolution-sheet-wave29.md ops/archive/review-routing-legacy/
# mv ops/decision-answers-template-wave31.md ops/archive/review-routing-legacy/
# mv ops/unresolved-decisions-brief-wave26.md ops/archive/review-routing-legacy/

# 5) Post-move verification
# test -e ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md
# test -e ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md
# test -e ops/archive/review-routing-legacy/decision-answers-template-wave31.md
# test -e ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md
# test ! -e ops/decision-signoff-tracker-wave28.md
# test ! -e ops/decision-resolution-sheet-wave29.md
# test ! -e ops/decision-answers-template-wave31.md
# test ! -e ops/unresolved-decisions-brief-wave26.md
# grep -nE "decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md|primary decision-call route|Decision calls \(primary\)" ops/*.md
# git diff --name-status

# 6) Commit cutover (if verification clean)
# git add -A
# git commit -m "ops: wave40 controlled archive move for legacy decision-routing docs"
```

## Rollback trigger points (stop and reverse immediately)
1. READY gate not explicitly documented at execution time.
2. Any post-move grep indicates live decision flow still depends on moved docs.
3. Any expected moved file missing in archive target, or any source file still present.
4. Diff scope expands beyond intended move + explicitly approved pointer updates.

Rollback commands:
```bash
# mv ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md ops/
# mv ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md ops/
# mv ops/archive/review-routing-legacy/decision-answers-template-wave31.md ops/
# mv ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md ops/
# git diff --name-status
```

## Decision note
If preflight check is clean after one bounded cleanup pass, switch to **GO** and execute immediately in the same session to avoid state drift.
