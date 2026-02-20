# Archive Move Execution — Wave 42

Date: 2026-02-20  
Companion to: `ops/controlled-move-plan-wave39.md`, `ops/routing-cutover-checklist-wave34.md`, `ops/strategy-control-log.md` (latest entry followed first).

## Scope executed
Controlled archive move of four legacy/superseded decision docs into `ops/archive/review-routing-legacy/`.

### Files moved
1. `ops/unresolved-decisions-brief-wave26.md` → `ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md`
2. `ops/decision-signoff-tracker-wave28.md` → `ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md`
3. `ops/decision-resolution-sheet-wave29.md` → `ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md`
4. `ops/decision-answers-template-wave31.md` → `ops/archive/review-routing-legacy/decision-answers-template-wave31.md`

## Active routing/index patch set
Updated direct references in active routing/decision surfaces to preserve valid paths and active-route clarity:

- `ops/decision-ready-packet-wave30.md`
  - `Supersedes:` pointers updated to archive paths for W28/W29 docs.
- `ops/decision-quickfill-card-wave32.md`
  - `Supersedes:` pointer updated to archive path for W31 template.
- `ops/decision-finalization-queue-wave33.md`
  - `Supersedes:` pointer updated to archive path for W31 template.
- `ops/decision-signoff-script-wave34.md`
  - `Supersedes:` pointer updated to archive path for W31 template.
- `ops/route-supersession-matrix-wave32.md`
  - Added archive destination paths for W28/W29/W31 superseded rows.
  - Updated consolidated notes with Wave 42 archive move status.

## Verification checks run

### Existence checks (archive targets)
- PASS: `ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md`
- PASS: `ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md`
- PASS: `ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md`
- PASS: `ops/archive/review-routing-legacy/decision-answers-template-wave31.md`

### Source-cleared checks
- PASS: source absent `ops/unresolved-decisions-brief-wave26.md`
- PASS: source absent `ops/decision-signoff-tracker-wave28.md`
- PASS: source absent `ops/decision-resolution-sheet-wave29.md`
- PASS: source absent `ops/decision-answers-template-wave31.md`

## Rollback commands

```bash
mv ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md ops/
mv ops/archive/review-routing-legacy/decision-signoff-tracker-wave28.md ops/
mv ops/archive/review-routing-legacy/decision-resolution-sheet-wave29.md ops/
mv ops/archive/review-routing-legacy/decision-answers-template-wave31.md ops/
```

## Posture
- Decision-first active surfaces remain unchanged: W30/W32/W33/W36 chain remains the live route.
- Moved files are retained for provenance/history in archive.
