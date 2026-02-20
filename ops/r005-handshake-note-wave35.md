# R-005 Operator Handshake Note — Wave 35

Metadata: wave=35 | doc=r005-handshake-note | owner=weekly-watchdog-operator | generated=2026-02-20
Companion to: `ops/r005-weekly-cron-brief-wave34.md`, `ops/r005-next-run-kit-wave30.md`, `ops/r005-escalation-card-wave31.md`, `ops/r005-watchdog-run-2026-02-20-wave28.md`.

## Use This At Start of Next Weekly Run

1. Confirm cadence window from weekly brief (`ops/r005-weekly-cron-brief-wave34.md`): next target is one week after 2026-02-20 (target 2026-02-27).
2. Execute the command block from `ops/r005-next-run-kit-wave30.md` and write evidence to:
   - `ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt`
3. Record ST-1..ST-4 results in a new run doc from template:
   - `ops/r005-watchdog-template-wave27.md` → `ops/r005-watchdog-run-YYYY-MM-DD-waveNN.md`
4. If any gate drops from PASS, apply `ops/r005-escalation-card-wave31.md` immediately (declare escalation, freeze affected packet-touching scope, patch failing condition(s), rerun, attach evidence).

## Latest Evidence Pointers (operator quick links)

- Current execution anchor: `ops/evidence/wave28-r005-watchdog-run-2026-02-20.txt`
- Current run record: `ops/r005-watchdog-run-2026-02-20-wave28.md`
- Stability trend support: `ops/evidence/wave26-r005-stability-delta-2026-02-20.txt`
- Prior sentinel evidence: `ops/evidence/wave25-r005-regression-sentinel-2026-02-20.txt`
- Prior gate-check evidence: `ops/evidence/wave24-r005-gate-check-2026-02-20.txt`
- Consolidated historical index: `ops/evidence/evidence-index-wave23.md`

## Exact Weekly Reporting Snippets

Use exactly one of the following in the run doc summary section.

- **If PASS then report:**
  - `R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST-1 PASS / ST-2 PASS / ST-3 PASS / ST-4 PASS, trend: Stable or Improved, escalation: not triggered, evidence: ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt, posture: R-005 OPEN (monitor).`

- **If WARN then report:**
  - `R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST gate(s) WARN [list gates], impacted files: [list], trend: Regressed, escalation: triggered, evidence: ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt, continuity-hole: [ID], owner: [name], due: [YYYY-MM-DD], recheck: planned.`

- **If FAIL then report:**
  - `R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST gate(s) FAIL [list gates], impacted files: [list], trend: Regressed, escalation: triggered, merge path: frozen for affected packet-touching scope, evidence: ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt, continuity-hole: [ID], owner: [name], due: [YYYY-MM-DD], rerun required for escalation-cleared status.`

## Escalation Reminder (from card, no reinterpretation)

- Trigger: any PASS → WARN/FAIL on ST-1/ST-2/ST-3/ST-4.
- Same-cycle actions: declare, freeze affected scope, hole entry, patch failing condition(s), rerun with fresh evidence.
- Recovery close only when ST-1..ST-4 all PASS and run doc explicitly states escalation cleared.

## Handshake Close

Before ending the run, verify all four are present and aligned:
1. New run doc (`ops/r005-watchdog-run-YYYY-MM-DD-waveNN.md`)
2. Evidence artifact (`ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt`)
3. Updated status pointers in active monitor docs
4. One-line PASS/WARN/FAIL report snippet pasted verbatim
