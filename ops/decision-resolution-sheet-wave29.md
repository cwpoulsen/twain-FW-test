# Decision Resolution Sheet — Wave 29

Date: 2026-02-20  
Companion to: `ops/decision-signoff-tracker-wave28.md` and `ops/decision-ballot-pack-wave27.md`  
Supersedes: `ops/unresolved-decisions-brief-wave26.md` (decision-call surface for items D-01..D-07)
Routing note (Wave 30): primary resolution sheet for Wave27–29 decision outcomes; upstream rationale remains in `ops/unresolved-decisions-brief-wave26.md` and `ops/decision-queue-wave25.md`.

Purpose: single-sheet resolution view for Wave 27/28 decision items with recommended call, fallback path, deadline, and exact files that would require updates if the decision changes from the recommended default.

## Resolution table

| Decision ID | Final recommendation | Fallback | Decision deadline | Exact file(s) impacted if changed |
|---|---|---|---|---|
| D-01 (RC1 baseline) | **HOLD** RC1 until Wave21 Critical checks are evidence-backed PASS and weekly monitor is fresh. | GO now (promote RC1 immediately). | 2026-02-22 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/monitor-pack-wave21.md`; `ops/reviewer-checklist-wave21.md`; `ops/rc1-release-notes-wave22.md`; `ops/rc1-changelog-slice-recent-waves-wave22.md`; `ops/rc1-rollback-instructions-wave22.md` |
| D-02 (R-005 policy) | **Scheduled closure pass** with checkpoint date, while keeping weekly sentinel active until closure. | Monitor-only (no scheduled closure pass). | 2026-02-23 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/continuity-holes-register-v1.md`; `ops/r005-regression-sentinel-wave25.md`; `ops/r005-watchdog-template-wave27.md`; `ops/r005-watchdog-run-2026-02-20-wave28.md`; `ops/r005-gate-check-wave24.md`; `ops/packet-doc-lint-checklist-v1.md` |
| D-03 (next cycle mode) | **Stabilization-first** (contradiction hunt + compression + R-005 closure). | Expansion-first. | 2026-02-21 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/strategy-control-log.md`; `ops/contradiction-hunt-wave24.md`; `ops/doc-map-dedupe-wave24.md`; `ops/decision-queue-wave25.md`; `ops/routing-consolidation-wave28.md` |
| D-04 (signoff depth) | **Two-stage** review (60-min triage, then 1-day deep review only if Critical uncertainty remains). | Single-pass mode (60-min only or 1-day only). | 2026-02-21 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/reading-guide-60min-quick-review-v1.md`; `ops/reading-guide-1day-deep-review-v1.md`; `ops/reviewer-checklist-wave21.md`; `ops/start-here-review-path.md` |
| D-05 (provisional → authority promotion policy) | **Explicit criteria gate** (lock scan pass + timeline/mechanism validation + authority citation). | Ad hoc promotion. | 2026-02-24 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/continuity-lock-check-matrix-v1.md`; `ops/domain-validation-checklists-v1.md`; `ops/executive-summary-wave20.md`; `ops/handoff-briefing-wave23.md`; `ops/canon-policy.md`; `ops/timeline-policy.md` |
| D-06 (anti-dup governance) | **Mandatory pre-merge blocker** for high-volume commits (novelty/compression check required). | Optional advisory check. | 2026-02-24 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/post250k-reconciliation-completion-status-2026-02-19.md`; `ops/doc-map-dedupe-wave24.md`; `ops/final-snapshot-status-wave19.md`; `ops/executive-summary-wave20.md`; `ops/workflow-v2.md`; `ops/workflow.md` |
| D-07 (question-bank policy) | **Phase-targeted subset** with explicit LOCKED/REVISE/DEFER tracking. | Full Top-50 every cycle. | 2026-02-25 | `ops/decision-ballot-pack-wave27.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/unresolved-decisions-brief-wave26.md`; `ops/reviewer-question-bank-top50-v1.md`; `ops/handoff-briefing-wave23.md`; `ops/start-here-review-path.md`; `ops/reading-guide-60min-quick-review-v1.md`; `ops/reading-guide-1day-deep-review-v1.md` |

## Notes
- Recommendations mirror the checked defaults in `ops/decision-ballot-pack-wave27.md` and due-by dates in `ops/decision-signoff-tracker-wave28.md`.
- "Impacted if changed" is scoped to direct decision-routing, policy/gate, and execution-surface docs that encode the current defaults.
