# Wave 41 Blocker Fix Report — Decision Resolution Sheet (Wave 29)

Date: 2026-02-20
Target file: `ops/decision-resolution-sheet-wave29.md`
Scope executed: routing note + impacted file lists D-01..D-07 rewired to active W32/W33/W36 decision surfaces; legacy Wave26/Wave28 active-update dependencies removed.

## Exact substitutions applied

1) Routing note rewired

- Old:
`Routing note (Wave 30): primary resolution sheet for Wave27–29 decision outcomes; upstream rationale remains in \`ops/unresolved-decisions-brief-wave26.md\` and \`ops/decision-queue-wave25.md\`.`
- New:
`Routing note (Wave 41 patch): keep this sheet as historical Wave27–29 resolution context; active-live decision routing is now through \`ops/decision-quickfill-card-wave32.md\`, \`ops/decision-finalization-queue-wave33.md\`, and \`ops/decision-capture-sheet-wave36.md\` (with \`ops/decision-queue-wave25.md\` retained as upstream rationale context).`

2) Common D-01..D-07 impacted-list dependency swap (legacy decision surfaces → active decision surfaces)

- Old fragment:
`\`ops/decision-ballot-pack-wave27.md\`; \`ops/decision-signoff-tracker-wave28.md\`; \`ops/unresolved-decisions-brief-wave26.md\`;`
- New fragment:
`\`ops/decision-ballot-pack-wave27.md\`; \`ops/decision-quickfill-card-wave32.md\`; \`ops/decision-finalization-queue-wave33.md\`; \`ops/decision-capture-sheet-wave36.md\`;`

3) D-02 R-005 impacted-list swap (remove Wave28 run dependency)

- Old fragment:
`\`ops/r005-watchdog-template-wave27.md\`; \`ops/r005-watchdog-run-2026-02-20-wave28.md\`; \`ops/r005-gate-check-wave24.md\`;`
- New fragment:
`\`ops/r005-watchdog-template-wave27.md\`; \`ops/r005-health-checkpoint-wave33.md\`; \`ops/r005-gate-check-wave24.md\`;`

4) D-03 next-cycle impacted-list swap (remove Wave28 routing dependency)

- Old tail fragment:
`\`ops/decision-queue-wave25.md\`; \`ops/routing-consolidation-wave28.md\``
- New tail fragment:
`\`ops/decision-queue-wave25.md\``

(Active W32/W33/W36 decision surfaces are already included earlier in the D-03 impacted list via substitution #2.)

5) D-03 post-substitution normalization

- Removed duplicate repeated trio introduced by overlapping text replacement:
`\`ops/decision-quickfill-card-wave32.md\`; \`ops/decision-finalization-queue-wave33.md\`; \`ops/decision-capture-sheet-wave36.md\``

## Constraints check

- `Supersedes:` metadata line left unchanged.
- Historical context references retained where not part of active-update dependency paths.
- Active impacted routing now points to Wave32/Wave33/Wave36 decision surfaces across D-01..D-07.
