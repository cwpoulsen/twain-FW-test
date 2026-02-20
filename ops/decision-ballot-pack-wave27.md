# Decision Ballot Pack — Wave 27

Date: 2026-02-20  
Companion to: `ops/unresolved-decisions-brief-wave26.md` (primary decision-call route) and `ops/decision-queue-wave25.md` (analysis backlog).
Routing note (Wave 28): supporting one-screen response form; primary decision-call route remains `ops/unresolved-decisions-brief-wave26.md`.

**How to answer:** keep checked default, or switch to an alternative box.

## Ballot (one-screen)

- **D-01 RC1 baseline**
  - [ ] GO now
  - [x] HOLD until Wave21 Critical checks are evidence-backed PASS + weekly monitor is fresh
  - Evidence: `ops/reviewer-checklist-wave21.md`, `ops/evidence/wave21-weekly-monitor-YYYY-MM-DD.txt`, `ops/rc1-release-notes-wave22.md`, `ops/rc1-changelog-slice-recent-waves-wave22.md`, `ops/rc1-rollback-instructions-wave22.md`

- **D-02 R-005 policy**
  - [ ] Monitor-only
  - [x] Scheduled closure pass (set checkpoint date) + keep weekly sentinel until closure
  - Evidence: `ops/continuity-holes-register-v1.md`, `ops/r005-regression-sentinel-wave25.md`, `ops/r005-gate-check-wave24.md`, `ops/packet-doc-lint-checklist-v1.md`, `ops/evidence/`

- **D-03 Next cycle mode**
  - [x] Stabilization-first (contradiction hunt + compression + R-005 closure)
  - [ ] Expansion-first
  - Evidence: `ops/strategy-control-log.md` (2026-02-20 entries), `ops/contradiction-hunt-wave24.md`, `ops/doc-map-dedupe-wave24.md`, `ops/decision-queue-wave25.md`

- **D-04 Signoff depth this cycle**
  - [ ] 60-min only
  - [ ] 1-day only
  - [x] Two-stage (60-min triage, then 1-day only if Critical uncertainty remains)
  - Evidence: `ops/reading-guide-60min-quick-review-v1.md`, `ops/reading-guide-1day-deep-review-v1.md`, `ops/reviewer-checklist-wave21.md`

- **D-05 Provisional → authority promotion policy**
  - [ ] Ad hoc promotion
  - [x] Explicit criteria gate (lock scan pass + timeline/mechanism validation + authority citation)
  - Evidence: `ops/executive-summary-wave20.md`, `ops/handoff-briefing-wave23.md`, `ops/continuity-lock-check-matrix-v1.md`, `ops/domain-validation-checklists-v1.md`

- **D-06 Anti-dup governance**
  - [ ] Optional advisory novelty/compression check
  - [x] Mandatory pre-merge blocker for high-volume commits
  - Evidence: `ops/post250k-reconciliation-completion-status-2026-02-19.md`, `ops/doc-map-dedupe-wave24.md`, `ops/final-snapshot-status-wave19.md`, `ops/executive-summary-wave20.md`

- **D-07 Question-bank policy**
  - [ ] Full Top-50 every cycle
  - [x] Phase-targeted subset with LOCKED/REVISE/DEFER tracking
  - Evidence: `ops/reviewer-question-bank-top50-v1.md`, `ops/handoff-briefing-wave23.md`, `ops/start-here-review-path.md`

## Quick reply line (copy/edit)

`D-01 HOLD; D-02 Scheduled closure (date: ____); D-03 Stabilization; D-04 Two-stage; D-05 Explicit criteria; D-06 Mandatory gate; D-07 Targeted subset.`
