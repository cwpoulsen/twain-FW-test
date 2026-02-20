# Wave 38 Execution Map Rewire Report

Date: 2026-02-20  
Scope: Safe patch bundle **step 2** from `ops/cutover-blocker-map-wave37.md` (execution map/update-target rewiring only).  
Canon locks: unchanged.

## Files touched (step 2 only)

1. `ops/decision-ready-packet-wave30.md`
2. `ops/decision-signoff-script-wave34.md`
3. `ops/decision-chat-prompt-pack-wave35.md`
4. `ops/decision-finalization-queue-wave33.md`
5. `ops/decision-capture-sheet-wave36.md`

## Exact substitutions

### 1) `ops/decision-ready-packet-wave30.md`
- For D-01..D-07 Impact files:
  - Replaced every instance of:
    - `ops/decision-signoff-tracker-wave28.md`
  - With:
    - `ops/decision-finalization-queue-wave33.md`
- Removed every instance of:
  - `ops/unresolved-decisions-brief-wave26.md`

Rationale: moves active impact targets off legacy Wave26/Wave28 decision surfaces and onto active Wave33 queue.

### 2) `ops/decision-signoff-script-wave34.md`
- In Decision mapping table, D-01 impacted files:
  - Replaced:
    - `ops/decision-signoff-tracker-wave28.md`
  - With:
    - `ops/decision-finalization-queue-wave33.md`
- In Fast processing rule mirror step:
  - Replaced:
    - `ops/decision-signoff-tracker-wave28.md` (status updates)
  - With:
    - `ops/decision-capture-sheet-wave36.md` (captured decision tokens/confidence)

Rationale: keeps signoff script aligned to active W33 execution queue and W36 capture surface.

### 3) `ops/decision-chat-prompt-pack-wave35.md`
- In Per-answer update map, D-01 row:
  - Replaced:
    - `ops/decision-signoff-tracker-wave28.md`
  - With:
    - `ops/decision-finalization-queue-wave33.md`
- In Processing rules (post-apply resolution step):
  - Replaced:
    - `update ops/decision-signoff-tracker-wave28.md and ops/decision-finalization-queue-wave33.md`
  - With:
    - `update ops/decision-capture-sheet-wave36.md and ops/decision-finalization-queue-wave33.md`

Rationale: removes legacy Wave28 tracker writes from runtime prompt flow; routes closure to W36+W33.

### 4) `ops/decision-finalization-queue-wave33.md`
- In Queue Order, D-01 immediate follow-up commit targets:
  - Replaced:
    - `ops/decision-signoff-tracker-wave28.md`
  - With:
    - `ops/decision-capture-sheet-wave36.md`

Rationale: queue follow-up now points to current capture layer (W36) instead of legacy tracker.

### 5) `ops/decision-capture-sheet-wave36.md`
- In Token + auto-update map, D-01 auto-update targets:
  - Replaced:
    - `ops/decision-signoff-tracker-wave28.md`
  - With:
    - `ops/decision-finalization-queue-wave33.md`

Rationale: latest capture sheet no longer emits writes to legacy Wave28 tracker; uses active Wave33 queue.

## Continuity/lock note
- No canon/timeline/policy semantics changed.
- Supersedes metadata entries were left unchanged by design.
