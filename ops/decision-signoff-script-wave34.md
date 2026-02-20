# Decision Signoff Script — Wave 34

Date: 2026-02-20  
Companion to: `ops/decision-quickfill-card-wave32.md`, `ops/decision-finalization-queue-wave33.md`, `ops/strategy-control-log.md` (2026-02-20T01:23-05:00 decision-first cadence)  
Supersedes: `ops/decision-answers-template-wave31.md`

Purpose: chat-fast signoff script Chris can answer in one message (D-01..D-07), directly mappable to quickfill + finalization queue + commit targets.

## Expected response format (copy/paste)

Use one line:

`D-01=<choice>|<H/M/L>; D-02=<choice>|<H/M/L>; D-03=<choice>|<H/M/L>; D-04=<choice>|<H/M/L>; D-05=<choice>|<H/M/L>; D-06=<choice>|<H/M/L>; D-07=<choice>|<H/M/L>`

Example:

`D-01=HOLD|H; D-02=ScheduledClosure+Sentinel|H; D-03=StabilizationFirst|H; D-04=TwoStage|M; D-05=ExplicitCriteriaGate|H; D-06=MandatoryBlocker|H; D-07=PhaseTargetedSubset|M`

## Chat script (ask/answer order = finalization queue order)

1. **D-03 Next cycle mode** — choose `StabilizationFirst` or `ExpansionFirst`
2. **D-04 Signoff depth** — choose `TwoStage`, `60MinOnly`, or `1DayOnly`
3. **D-01 RC1 baseline** — choose `HOLD` or `GO`
4. **D-02 R-005 policy** — choose `ScheduledClosure+Sentinel` or `MonitorOnly`
5. **D-05 Provisional→Authority promotion** — choose `ExplicitCriteriaGate` or `AdHocPromotion`
6. **D-06 Anti-dup governance** — choose `MandatoryBlocker` or `OptionalCheck`
7. **D-07 Question-bank policy** — choose `PhaseTargetedSubset` or `FullTop50`

## Decision mapping: quickfill + queue + impacted files

| Decision | Quickfill line | Queue order | Impacted files to update after signoff |
|---|---|---:|---|
| D-03 | D-03 Next cycle mode | 1 | `ops/strategy-control-log.md`; `ops/decision-queue-wave25.md`; `ops/routing-consolidation-wave28.md` |
| D-04 | D-04 Signoff depth | 2 | `ops/start-here-review-path.md`; `ops/reading-guide-60min-quick-review-v1.md`; `ops/reviewer-checklist-wave21.md` |
| D-01 | D-01 RC1 baseline | 3 | `ops/decision-finalization-queue-wave33.md`; `ops/monitor-pack-wave21.md`; `ops/rc1-release-notes-wave22.md` |
| D-02 | D-02 R-005 policy | 4 | `ops/r005-regression-sentinel-wave25.md`; `ops/r005-watchdog-run-2026-02-20-wave28.md`; `ops/packet-doc-lint-checklist-v1.md` |
| D-05 | D-05 Provisional→Authority promotion | 5 | `ops/continuity-lock-check-matrix-v1.md`; `ops/domain-validation-checklists-v1.md`; `ops/canon-policy.md` |
| D-06 | D-06 Anti-dup governance | 6 | `ops/workflow-v2.md`; `ops/doc-map-dedupe-wave24.md`; `ops/final-snapshot-status-wave19.md` |
| D-07 | D-07 Question-bank policy | 7 | `ops/reviewer-question-bank-top50-v1.md`; `ops/handoff-briefing-wave23.md`; `ops/reading-guide-1day-deep-review-v1.md` |

## Fast processing rule

- If Chris replies in the expected one-line format, treat all seven decisions as captured in one pass.
- Immediately mirror selections into:
  1. `ops/decision-quickfill-card-wave32.md` (`selected=` fields)
  2. `ops/decision-capture-sheet-wave36.md` (captured decision tokens/confidence)
  3. `ops/decision-finalization-queue-wave33.md` (mark resolved/remaining)
- Commit after each resolved queue block (or full batch if all seven are resolved cleanly).