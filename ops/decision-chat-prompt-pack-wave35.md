# Decision Chat Prompt Pack — Wave 35

Date: 2026-02-20  
Companion to: `ops/decision-signoff-script-wave34.md`, `ops/decision-quickfill-card-wave32.md`, `ops/decision-finalization-queue-wave33.md`, `ops/strategy-control-log.md` (2026-02-20T01:23-05:00 decision-first cadence)  
Supersedes: `ops/decision-signoff-script-wave34.md`

Purpose: one-message decision capture pack for Chris (D-01..D-07), with strict answer format and direct per-answer file update routing.

## Chat-ready prompt (send as-is)

Reply in one message using this exact pattern:

`D-03=<choice>|<H/M/L>; D-04=<choice>|<H/M/L>; D-01=<choice>|<H/M/L>; D-02=<choice>|<H/M/L>; D-05=<choice>|<H/M/L>; D-06=<choice>|<H/M/L>; D-07=<choice>|<H/M/L>`

Use only these choices:
- D-03 (Next cycle mode): `StabilizationFirst` or `ExpansionFirst`
- D-04 (Signoff depth): `TwoStage` or `60MinOnly` or `1DayOnly`
- D-01 (RC1 baseline): `HOLD` or `GO`
- D-02 (R-005 policy): `ScheduledClosure+Sentinel` or `MonitorOnly`
- D-05 (Provisional→Authority promotion): `ExplicitCriteriaGate` or `AdHocPromotion`
- D-06 (Anti-dup governance): `MandatoryBlocker` or `OptionalCheck`
- D-07 (Question-bank policy): `PhaseTargetedSubset` or `FullTop50`

Confidence must be `H`, `M`, or `L`.

Example:
`D-03=StabilizationFirst|H; D-04=TwoStage|M; D-01=HOLD|H; D-02=ScheduledClosure+Sentinel|H; D-05=ExplicitCriteriaGate|H; D-06=MandatoryBlocker|H; D-07=PhaseTargetedSubset|M`

## Compact question order (decision-first cadence)

1. D-03 Next cycle mode
2. D-04 Signoff depth
3. D-01 RC1 baseline
4. D-02 R-005 policy
5. D-05 Provisional→Authority promotion
6. D-06 Anti-dup governance
7. D-07 Question-bank policy

## Per-answer update map (immediate routing)

| Order | Decision | Update this canonical capture first | Then update these impacted files |
|---:|---|---|---|
| 1 | D-03 | `ops/decision-quickfill-card-wave32.md` (`selected`, `confidence`) | `ops/strategy-control-log.md`; `ops/decision-queue-wave25.md`; `ops/routing-consolidation-wave28.md` |
| 2 | D-04 | `ops/decision-quickfill-card-wave32.md` | `ops/start-here-review-path.md`; `ops/reading-guide-60min-quick-review-v1.md`; `ops/reviewer-checklist-wave21.md` |
| 3 | D-01 | `ops/decision-quickfill-card-wave32.md` | `ops/decision-finalization-queue-wave33.md`; `ops/monitor-pack-wave21.md`; `ops/rc1-release-notes-wave22.md` |
| 4 | D-02 | `ops/decision-quickfill-card-wave32.md` | `ops/r005-regression-sentinel-wave25.md`; `ops/r005-health-checkpoint-wave33.md`; `ops/packet-doc-lint-checklist-v1.md` |
| 5 | D-05 | `ops/decision-quickfill-card-wave32.md` | `ops/continuity-lock-check-matrix-v1.md`; `ops/domain-validation-checklists-v1.md`; `ops/canon-policy.md` |
| 6 | D-06 | `ops/decision-quickfill-card-wave32.md` | `ops/workflow-v2.md`; `ops/doc-map-dedupe-wave24.md`; `ops/final-snapshot-status-wave19.md` |
| 7 | D-07 | `ops/decision-quickfill-card-wave32.md` | `ops/reviewer-question-bank-top50-v1.md`; `ops/handoff-briefing-wave23.md`; `ops/reading-guide-1day-deep-review-v1.md` |

## Processing rules

1. Accept only responses that use all seven keys (`D-03, D-04, D-01, D-02, D-05, D-06, D-07`) in one message.
2. Validate each choice token against the allowed list before writing files.
3. After each valid decision: update quickfill row + route mapped files above.
4. After all seven are applied: update `ops/decision-capture-sheet-wave36.md` and `ops/decision-finalization-queue-wave33.md` to resolved status.
5. Commit as one batch when all seven parse cleanly; otherwise commit partial blocks only for fully validated decisions.
