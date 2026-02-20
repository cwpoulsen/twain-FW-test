# Wave 38 Route Dependency Rewire Report

Date: 2026-02-20
Scope executed: `ops/cutover-blocker-map-wave37.md` safe patch bundle **Step 1** (route declaration patch only).
Canon locks: unchanged.
Change type constraint: header/note/routing only.

## Changed files
1. `ops/start-here-review-path.md`
2. `ops/route-map-single-page-wave31.md`
3. `ops/decision-ballot-pack-wave27.md`
4. `ops/decision-queue-wave25.md`
5. `ops/reviewer-question-bank-top50-v1.md`

## Before/after snippets

### 1) `ops/start-here-review-path.md`
**Before**
```md
- **Decision calls (primary):** `ops/unresolved-decisions-brief-wave26.md`
```
**After**
```md
- **Decision calls (primary):** `ops/decision-quickfill-card-wave32.md` (summary context: `ops/decision-ready-packet-wave30.md`)
```

### 2) `ops/route-map-single-page-wave31.md`
**Before**
```md
## 3) DECISIONS (Primary entry)
- **Primary:** `ops/unresolved-decisions-brief-wave26.md`
- **Supporting docs:**
  - `ops/decision-queue-wave25.md` (priority + overlap analysis)
  - `ops/reviewer-question-bank-top50-v1.md` (decision prompts)
  - `ops/decision-ballot-pack-wave27.md` (one-screen ballot support)
  - `ops/decision-signoff-tracker-wave28.md` (execution tracker)
  - `ops/decision-resolution-sheet-wave29.md` (resolution recording sheet)
  - `ops/decision-ready-packet-wave30.md` (decision-ready summary packet)
```
**After**
```md
## 3) DECISIONS (Primary entry)
- **Primary:** `ops/decision-quickfill-card-wave32.md`
- **Supporting docs:**
  - `ops/decision-queue-wave25.md` (priority + overlap analysis)
  - `ops/reviewer-question-bank-top50-v1.md` (decision prompts)
  - `ops/decision-ballot-pack-wave27.md` (one-screen ballot support)
  - `ops/decision-ready-packet-wave30.md` (decision-ready summary packet)
  - `ops/decision-finalization-queue-wave33.md` (finalization tracking)
  - `ops/decision-capture-sheet-wave36.md` (capture + auto-update sheet)
```

### 3) `ops/decision-ballot-pack-wave27.md`
**Before**
```md
Companion to: `ops/unresolved-decisions-brief-wave26.md` (primary decision-call route) and `ops/decision-queue-wave25.md` (analysis backlog).
Routing note (Wave 28): supporting one-screen response form; primary decision-call route remains `ops/unresolved-decisions-brief-wave26.md`.
```
**After**
```md
Companion to: `ops/decision-quickfill-card-wave32.md` (primary decision-call route) and `ops/decision-queue-wave25.md` (analysis backlog).
Routing note (Wave 38): supporting one-screen response form; primary decision-call route is `ops/decision-quickfill-card-wave32.md`.
```

### 4) `ops/decision-queue-wave25.md`
**Before**
```md
Routing note (Wave 27): supporting decision analysis queue; **primary decision-call route is `ops/unresolved-decisions-brief-wave26.md`**.
```
**After**
```md
Routing note (Wave 38): supporting decision analysis queue; **primary decision-call route is `ops/decision-quickfill-card-wave32.md`; this queue remains supporting analysis.**
```

### 5) `ops/reviewer-question-bank-top50-v1.md`
**Before**
```md
Companion to: `ops/unresolved-decisions-brief-wave26.md` (primary decision-call route) and `ops/decision-queue-wave25.md` (prioritized decision ordering).
```
**After**
```md
Companion to: `ops/decision-quickfill-card-wave32.md` (primary decision-call route) and `ops/decision-queue-wave25.md` (prioritized decision ordering).
```

## Dependency outcome
- Removed active primary-route dependency on legacy wave26 doc in all Step 1 target files.
- Removed active decision-route references to legacy wave28/wave29 tracker/sheet from the Step 1 route map surface.
- No workflow logic body edits beyond routing/header/note declarations.
