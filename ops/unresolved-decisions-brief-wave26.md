# Unresolved Decisions Brief — Wave 26

Companion to: `ops/decision-queue-wave25.md` (analysis backlog), `ops/reviewer-checklist-wave21.md` (gate criteria), and `ops/handoff-briefing-wave23.md` (execution context).

Date: 2026-02-20  
Source queue: `ops/decision-queue-wave25.md`  
Purpose: fast human-answer brief (consolidation-only cycle step 2).

Routing note (Wave 27): **Primary route for decision calls.**

## Decision summary (answer-ready)

| Decision ID | Question | Options | Recommended default | Consequence of delay | Required evidence links |
|---|---|---|---|---|---|
| D-01 (RC1) | Approve RC1 baseline now or hold? | 1) **GO** now 2) **HOLD/NO-GO** pending fixes | **GO only if all Wave21 Critical checks are evidence-backed PASS and weekly monitor is fresh; else HOLD with fail log + owner/date.** | Baseline ambiguity, repeated re-review loops, accidental drift before anchor. | `ops/reviewer-checklist-wave21.md`; `ops/evidence/wave21-weekly-monitor-YYYY-MM-DD.txt`; `ops/rc1-release-notes-wave22.md`; `ops/rc1-changelog-slice-recent-waves-wave22.md`; `ops/rc1-rollback-instructions-wave22.md` |
| D-02 (R-005) | Keep R-005 as monitor-only, or schedule closure pass? | 1) Monitor-only 2) **Scheduled closure pass with checkpoint date** | **Schedule closure pass** and keep weekly monitor until closure criteria met. | Template conformance drift can return silently; recurring lint debt and later contradiction risk. | `ops/continuity-holes-register-v1.md`; `ops/r005-regression-sentinel-wave25.md`; `ops/r005-gate-check-wave24.md`; `ops/packet-doc-lint-checklist-v1.md`; `ops/evidence/` (latest sentinel/monitor artifacts) |
| D-03 (Wave mode) | Next cycle should be stabilization or expansion? | 1) **Stabilization-first** 2) Expansion-first | **Stabilization-first** (contradiction hunt + compression + R-005 closure), then bounded expansion under acceptance tests. | Meta-doc churn, duplicate prose, lower quality-per-wave from over-automation. | `ops/strategy-control-log.md` (2026-02-20 entries); `ops/contradiction-hunt-wave24.md`; `ops/doc-map-dedupe-wave24.md`; `ops/decision-queue-wave25.md` |
| D-04 (Signoff depth) | For this cycle, use 60-min fast signoff or 1-day deep signoff? | 1) 60-min only 2) 1-day only 3) **Two-stage** | **Two-stage:** 60-min gate triage first; run 1-day deep only if any Critical/near-Critical uncertainty remains. | Too shallow risks false confidence; too deep without trigger adds avoidable delay. | `ops/reading-guide-60min-quick-review-v1.md`; `ops/reading-guide-1day-deep-review-v1.md`; `ops/reviewer-checklist-wave21.md` |
| D-05 (Provisional promotion) | What policy governs promotion from provisional reservoir content into canon authority docs? | 1) Ad hoc promotion 2) **Explicit promotion criteria gate** | **Lock explicit criteria now:** lock scan pass + timeline/mechanism validation + authority citation before promotion. | Authority-layer contamination and future continuity ambiguity. | `ops/executive-summary-wave20.md`; `ops/handoff-briefing-wave23.md`; `ops/continuity-lock-check-matrix-v1.md`; `ops/domain-validation-checklists-v1.md` |
| D-06 (Anti-dup governance) | Should pre-merge novelty/compression gate be mandatory? | 1) Optional advisory 2) **Mandatory merge blocker for high-volume commits** | **Mandatory gate** for high-volume commits; failures block merge until corrected. | Reintroduction of duplication seams, readability drop, hidden contradiction risk. | `ops/post250k-reconciliation-completion-status-2026-02-19.md`; `ops/doc-map-dedupe-wave24.md`; `ops/final-snapshot-status-wave19.md`; `ops/executive-summary-wave20.md` |
| D-07 (Question-bank policy) | Run Top-50 every cycle, or phase-targeted subset? | 1) Full Top-50 every cycle 2) **Phase-targeted subset with status tracking** | **Targeted subset by phase** (Canon+Arc 0s → Character/Faction → Tech), with LOCKED/REVISE/DEFER tracking. | Reviewer fatigue, uneven usage, weaker decision traceability. | `ops/reviewer-question-bank-top50-v1.md`; `ops/handoff-briefing-wave23.md`; `ops/start-here-review-path.md` |

## Fast answer format for Chris

Use this one-line response template per decision:

- `D-01: GO` or `D-01: HOLD (reason, owner, date)`
- `D-02: Scheduled closure` or `D-02: Monitor-only`
- `D-03: Stabilization` or `D-03: Expansion`
- `D-04: Two-stage` / `60-min only` / `1-day only`
- `D-05: Explicit criteria` or `Ad hoc`
- `D-06: Mandatory gate` or `Optional`
- `D-07: Targeted subset` or `Full Top-50`

## Suggested default bundle (if approving in one pass)

`D-01 HOLD-until-evidence-fresh; D-02 Scheduled closure; D-03 Stabilization; D-04 Two-stage; D-05 Explicit criteria; D-06 Mandatory gate; D-07 Targeted subset`.
