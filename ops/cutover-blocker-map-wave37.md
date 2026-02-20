# Cutover Blocker Map — Wave 37 (Planning)

Date: 2026-02-20  
Metadata: wave=37 | doc=cutover-blocker-map | scope=wave36-cutover-readiness-blockers | mode=planning-only | canon-locks=unchanged
Companion to: `ops/archive-cutover-readiness-wave36.md`, `ops/routing-reduction-proposal-wave33.md`, `ops/routing-cutover-checklist-wave34.md`, `ops/strategy-control-log.md` (latest entry first)

## Strategy-control first check
Latest strategy entry applied first: `2026-02-20T01:23-05:00` (decision-first cadence, consolidation-only, prefer merge/annotate over net-new sprawl).

## Legacy docs in scope (proposed archive targets)
- `ops/unresolved-decisions-brief-wave26.md`
- `ops/decision-signoff-tracker-wave28.md`
- `ops/decision-resolution-sheet-wave29.md`
- `ops/decision-answers-template-wave31.md`

## Blocker map (active-route dependency refs)

### Critical blockers (must patch before archive move)

| File | Exact lines with active dependency | Why this blocks cutover | Safe patch recommendation (planning-level, exact target) |
|---|---|---|---|
| `ops/start-here-review-path.md` | L13 (`Decision calls (primary): wave26`) | Declares wave26 as current primary route. | Replace L13 with: `- **Decision calls (primary):** \`ops/decision-quickfill-card-wave32.md\`` and optionally append `(summary context: \`ops/decision-ready-packet-wave30.md\`)`. |
| `ops/route-map-single-page-wave31.md` | L33 (`Primary: wave26`), L38 (wave28 support), L39 (wave29 support) | Keeps all three legacy docs in current DECISIONS route section. | In DECISIONS section, set primary to W32; replace support list entries L38-L39 with W30/W33/W36 decision surfaces. |
| `ops/decision-ballot-pack-wave27.md` | L4-L5 (primary decision-call route remains wave26) | Still routes users to legacy primary decision surface. | Change both lines to supporting-only language: `Companion to: \`ops/decision-quickfill-card-wave32.md\` ...` and `Routing note: supporting one-screen response form; primary decision-call route is \`ops/decision-quickfill-card-wave32.md\`.` |
| `ops/decision-queue-wave25.md` | L5 (primary decision-call route is wave26) | Explicit active-route pointer to archive candidate. | Replace with: `Routing note ... primary decision-call route is \`ops/decision-quickfill-card-wave32.md\`; this queue remains supporting analysis.` |
| `ops/reviewer-question-bank-top50-v1.md` | L3 (companion says wave26 primary route) | Keeps question-bank usage chained to legacy primary route. | Update companion line to point to W32 as primary decision-call route, with wave26 downgraded to optional historical rationale (or removed). |
| `ops/decision-ready-packet-wave30.md` | L11-L17 (`Impact files` include wave28 + wave26 across all decisions) | Active execution packet still instructs updates to legacy files. | In all D-01..D-07 impact lists, replace `wave28` with `ops/decision-finalization-queue-wave33.md` and remove `wave26` from active impact targets. Keep historical mention only in note if needed. |
| `ops/decision-chat-prompt-pack-wave35.md` | L45 (D-01 update map includes wave28), L56 (post-apply update wave28) | Runtime update instructions still write into legacy tracker. | Replace wave28 targets with `ops/decision-finalization-queue-wave33.md`; ensure final step writes only to W32/W33/W36-era active docs. |
| `ops/decision-signoff-script-wave34.md` | L35, L46 (update wave28 status) | Signoff flow still depends on legacy execution tracker. | Replace wave28 with `ops/decision-finalization-queue-wave33.md` in impacted files table and fast-processing mirror step. |
| `ops/decision-finalization-queue-wave33.md` | L15 (D-01 follow-up targets wave28) | Queue still points D-01 follow-up to legacy tracker. | Replace D-01 follow-up target `wave28` with `ops/decision-capture-sheet-wave36.md` (capture state) or W33 self-status + W32 selected fields, per desired single-source workflow. |
| `ops/decision-capture-sheet-wave36.md` | L22 (D-01 auto-update includes wave28) | Latest capture sheet still emits writes to legacy tracker. | Replace D-01 auto-update list with: `ops/decision-quickfill-card-wave32.md`; `ops/decision-finalization-queue-wave33.md`; `ops/monitor-pack-wave21.md`; `ops/rc1-release-notes-wave22.md`. |

### Secondary blockers (non-active but should be normalized in same patch wave)

| File | Line(s) | Note | Safe recommendation |
|---|---|---|---|
| `ops/decision-signoff-script-wave34.md` | L5 (`Supersedes: wave31`) | Historical/supersession metadata, not an active route dependency by itself. | Keep as-is unless metadata policy now requires explicit `legacy` tag. |
| `ops/decision-finalization-queue-wave33.md` | L5 (`Supersedes: wave31`) | Historical metadata only. | Keep as-is. |
| `ops/decision-ready-packet-wave30.md` | L5 (`Supersedes: wave29, wave28`) | Historical metadata only. | Keep as-is; do not rewrite supersession provenance. |

## Safe patch bundle recommendation (ordered)
1. **Route declaration patch** (no workflow logic changes):
   - `ops/start-here-review-path.md`
   - `ops/route-map-single-page-wave31.md`
   - `ops/decision-ballot-pack-wave27.md`
   - `ops/decision-queue-wave25.md`
   - `ops/reviewer-question-bank-top50-v1.md`
2. **Execution map patch** (update-target rewiring):
   - `ops/decision-ready-packet-wave30.md`
   - `ops/decision-signoff-script-wave34.md`
   - `ops/decision-chat-prompt-pack-wave35.md`
   - `ops/decision-finalization-queue-wave33.md`
   - `ops/decision-capture-sheet-wave36.md`
3. **Post-patch verification gate** (must pass before move):
   ```bash
   grep -nE "primary decision-call route|Decision calls \(primary\)|decision-signoff-tracker-wave28\.md|decision-resolution-sheet-wave29\.md|decision-answers-template-wave31\.md|unresolved-decisions-brief-wave26\.md" ops/*.md
   ```
   Expected PASS condition for live cutover: no active-routing or auto-update instructions point to wave26/28/29/31; remaining hits are only archive/history/cutover docs.

## Archive move readiness decision (post-patch)
- If critical blockers above are patched and grep gate passes, Wave36 cutover blocker class reduces from **NOT READY** to **READY FOR CONTROLLED MOVE** for:
  - `ops/decision-signoff-tracker-wave28.md`
  - `ops/decision-resolution-sheet-wave29.md`
  - `ops/decision-answers-template-wave31.md`
  - `ops/unresolved-decisions-brief-wave26.md`

## Contradiction / continuity note
- Canon locks: unchanged.
- This document is planning-level only; no canonical, timeline, or policy semantics changed.
