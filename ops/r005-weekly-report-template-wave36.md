# R-005 Weekly User-Facing Report Template — Wave 36

Metadata: wave=36 | doc=r005-weekly-report-template | scope=R-005 weekly status message | generated=2026-02-20

Companion to: `ops/r005-weekly-cron-brief-wave34.md`, `ops/r005-watchdog-template-wave27.md`, `ops/r005-watchdog-run-2026-02-20-wave28.md`, `ops/r005-escalation-card-wave31.md`.

Use this as the concise external update message after each weekly watchdog run.

## Naming references (current)
- Run file pattern: `ops/r005-watchdog-run-YYYY-MM-DD-waveNN.md`
- Evidence file pattern (current active): `ops/evidence/waveNN-r005-watchdog-run-YYYY-MM-DD.txt`
- If older/alternate convention appears, preserve existing file names and link exactly as written.

## PASS variant
`R-005 Weekly Update ({{date}}): PASS. ST-1/2/3/4 all PASS; trend {{Stable|Improved}}; escalation not triggered. Latest run: ops/r005-watchdog-run-{{date}}-wave{{NN}}. Evidence: ops/evidence/wave{{NN}}-r005-watchdog-run-{{date}}.txt. Risk posture remains R-005 OPEN (monitor).`

## WARN variant
`R-005 Weekly Update ({{date}}): WARN. Gate issue(s): {{list ST gates}}; trend Regressed; escalation triggered. Impacted file(s): {{paths}}. Latest run: ops/r005-watchdog-run-{{date}}-wave{{NN}}. Evidence: ops/evidence/wave{{NN}}-r005-watchdog-run-{{date}}.txt. Remediation owner/due: {{owner, due date}}; recheck scheduled {{date}}.`

## FAIL variant
`R-005 Weekly Update ({{date}}): FAIL. Critical gate failure(s): {{list ST gates}}; trend Regressed; escalation triggered; merge path blocked for affected packet-touching scope pending clean rerun. Latest run: ops/r005-watchdog-run-{{date}}-wave{{NN}}. Evidence: ops/evidence/wave{{NN}}-r005-watchdog-run-{{date}}.txt. Recovery owner/due: {{owner, due date}}; unblock requires full ST-1/2/3/4 PASS rerun with linked evidence.`

## Fill checklist (before sending)
- Replace all placeholders (`{{...}}`).
- Ensure run/evidence links match actual created files.
- Keep wording concise; do not add lore/canon content.
