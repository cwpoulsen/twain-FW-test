# Wave 41 Blocker Fix Report — Decision Signoff Tracker Routing Patch

Date: 2026-02-20  
Scope: remove remaining active-live legacy primary-route dependency in `ops/decision-signoff-tracker-wave28.md` called out by Wave 40 final recheck.

## Strategy-control first
Applied latest `ops/strategy-control-log.md` entry first: `2026-02-20T01:23-05:00` (decision-first cadence, consolidation-only, merge/annotate over net-new).

## File patched
- `ops/decision-signoff-tracker-wave28.md`

## Before/after snippet (routing note)

**Before**
```md
Routing note (Wave 30): supporting decision execution tracker; primary decision-call route remains `ops/unresolved-decisions-brief-wave26.md` until explicit final signoff closure.
```

**After**
```md
Routing note (Wave 41): supporting decision execution tracker; active decision-call route is `ops/decision-quickfill-card-wave32.md`, signoff sequencing is `ops/decision-finalization-queue-wave33.md`, and final capture/apply route is `ops/decision-capture-sheet-wave36.md` (legacy `ops/unresolved-decisions-brief-wave26.md` retained for provenance/history only).
```

## Result
- Removed live dependency on legacy primary route (`wave26`) from the Wave 28 tracker.
- Realigned active routing to W32/W33/W36 surfaces.
- Preserved historical provenance by keeping explicit legacy mention as history-only.
- Supersedes metadata line remains unchanged.
