# Decision Capture Sheet — Wave 36

Date: 2026-02-20  
Companion to: `ops/decision-chat-prompt-pack-wave35.md`, `ops/decision-quickfill-card-wave32.md`, `ops/decision-finalization-queue-wave33.md`, `ops/strategy-control-log.md` (latest entry first)  
Supersedes: `ops/decision-chat-prompt-pack-wave35.md`

Purpose: final compact capture for immediate human reply processing (D-01..D-07), with strict tokens, optional rationale, and auto-update targets.

## Reply format (single line)

`D-03=<token>|<H/M/L>|<optional rationale>; D-04=<token>|<H/M/L>|<optional rationale>; D-01=<token>|<H/M/L>|<optional rationale>; D-02=<token>|<H/M/L>|<optional rationale>; D-05=<token>|<H/M/L>|<optional rationale>; D-06=<token>|<H/M/L>|<optional rationale>; D-07=<token>|<H/M/L>|<optional rationale>`

- Confidence: `H` / `M` / `L`
- Optional rationale: short free text, or leave blank after final `|`

## Token + auto-update map

| ID | Allowed tokens | Auto-update target files |
|---|---|---|
| D-03 | `StabilizationFirst` \| `ExpansionFirst` | `ops/decision-quickfill-card-wave32.md`; `ops/strategy-control-log.md`; `ops/decision-queue-wave25.md`; `ops/routing-consolidation-wave28.md` |
| D-04 | `TwoStage` \| `60MinOnly` \| `1DayOnly` | `ops/decision-quickfill-card-wave32.md`; `ops/start-here-review-path.md`; `ops/reading-guide-60min-quick-review-v1.md`; `ops/reviewer-checklist-wave21.md` |
| D-01 | `HOLD` \| `GO` | `ops/decision-quickfill-card-wave32.md`; `ops/decision-signoff-tracker-wave28.md`; `ops/monitor-pack-wave21.md`; `ops/rc1-release-notes-wave22.md` |
| D-02 | `ScheduledClosure+Sentinel` \| `MonitorOnly` | `ops/decision-quickfill-card-wave32.md`; `ops/r005-regression-sentinel-wave25.md`; `ops/r005-watchdog-run-2026-02-20-wave28.md`; `ops/packet-doc-lint-checklist-v1.md` |
| D-05 | `ExplicitCriteriaGate` \| `AdHocPromotion` | `ops/decision-quickfill-card-wave32.md`; `ops/continuity-lock-check-matrix-v1.md`; `ops/domain-validation-checklists-v1.md`; `ops/canon-policy.md` |
| D-06 | `MandatoryBlocker` \| `OptionalCheck` | `ops/decision-quickfill-card-wave32.md`; `ops/workflow-v2.md`; `ops/doc-map-dedupe-wave24.md`; `ops/final-snapshot-status-wave19.md` |
| D-07 | `PhaseTargetedSubset` \| `FullTop50` | `ops/decision-quickfill-card-wave32.md`; `ops/reviewer-question-bank-top50-v1.md`; `ops/handoff-briefing-wave23.md`; `ops/reading-guide-1day-deep-review-v1.md` |

## Parse/apply rules (compact)

1. Require all keys: `D-03,D-04,D-01,D-02,D-05,D-06,D-07` in one message.
2. Validate token and confidence per key before writes.
3. Apply updates in listed order; skip only invalid keys.
4. Batch commit if all seven valid; otherwise commit validated subset with note.
