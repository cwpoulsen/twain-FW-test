# R-005 Weekly Cron Brief — Wave 34

Metadata: wave=34 | doc=r005-weekly-cron-brief | cadence=weekly | generated=2026-02-20

Companion to: `ops/r005-watchdog-template-wave27.md`, `ops/r005-watchdog-rollup-wave29.md`, `ops/r005-escalation-card-wave31.md`, `ops/r005-next-run-kit-wave30.md`.

## Run Cadence (when to run)
- Run **once per week** on the recurring watchdog slot.
- Anchor to the prior executed run date in `ops/r005-watchdog-run-YYYY-MM-DD-waveNN.md`.
- Current planning anchor from Wave 33: next target window is **one week after 2026-02-20** (i.e., 2026-02-27).

## Required File Updates (what to update)
1. Create/update the weekly run record from template:
   - `ops/r005-watchdog-template-wave27.md` → new dated run doc `ops/r005-watchdog-run-YYYY-MM-DD-waveNN.md`
2. Update status banners/pointers in active monitor docs (state/snapshot/trend/escalation + latest evidence/run links).
3. If trend or status changes, reflect it in rollup context:
   - `ops/r005-watchdog-rollup-wave29.md` (or successor rollup file).
4. If any gate degrades, execute and document escalation via:
   - `ops/r005-escalation-card-wave31.md`.

## Evidence Naming Convention
- Evidence artifact path:
  - `ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt`
- Keep one evidence artifact per weekly run, referenced in the run record and banner pointers.

## Weekly Report Rules (PASS/WARN/FAIL)
- **PASS**
  - Report ST snapshot (`ST-1..ST-4` all PASS), trend call (usually Stable/Improved), escalation `not triggered`, and evidence path.
  - Keep risk posture labeled: `R-005 OPEN (monitor)` unless explicitly closed by approved decision.
- **WARN**
  - Report failing gate(s), impacted file(s), trend `Regressed`, escalation `triggered`, and evidence path.
  - Open/update continuity hole entry with owner + due date + recheck plan.
- **FAIL**
  - Same as WARN, plus merge-path freeze for affected packet-touching scope until rerun returns full PASS.
  - Publish rerun evidence and explicit escalation-cleared statement only after exit criteria are met.

## Quick Operator Links
- Template/run format: `ops/r005-watchdog-template-wave27.md`
- Trend/trigger context: `ops/r005-watchdog-rollup-wave29.md`
- Escalation procedure: `ops/r005-escalation-card-wave31.md`
- Command checklist: `ops/r005-next-run-kit-wave30.md`

## One-Line Weekly Output Stub
`R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST-1 __ / ST-2 __ / ST-3 __ / ST-4 __, trend: ___, escalation: ___, evidence: ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt`
