# Decision Signoff Tracker — Wave 28

Date: 2026-02-20  
Companion to: `ops/decision-ballot-pack-wave27.md` | Supersedes: `ops/unresolved-decisions-brief-wave26.md`
Routing note (Wave 30): supporting decision execution tracker; primary decision-call route remains `ops/unresolved-decisions-brief-wave26.md` until explicit final signoff closure.

Purpose: execution tracker for Wave 27 decision signoff items with explicit status, ownership, due-by dates, and impact tiers.

## Status legend
- **open** = pending signoff
- **decided** = explicitly approved/rejected
- **deferred** = intentionally postponed with revisit date

## Tracker

| Decision ID | Decision | Current default (Wave 27 ballot) | Status | Owner | Due-by | Impact tier | Notes / Evidence |
|---|---|---|---|---|---|---|---|
| D-01 (RC1 baseline) | Approve RC1 now or hold pending evidence freshness? | **HOLD** until Wave21 Critical checks are evidence-backed PASS + weekly monitor fresh | open | Chris (final signoff) | 2026-02-22 | Critical | `ops/reviewer-checklist-wave21.md`; `ops/evidence/wave21-weekly-monitor-YYYY-MM-DD.txt`; RC1 notes/changelog/rollback docs |
| D-02 (R-005 policy) | Keep monitor-only or schedule closure pass? | **Scheduled closure pass** + keep weekly sentinel until closure | open | Chris + Ops workflow owner | 2026-02-23 | High | `ops/continuity-holes-register-v1.md`; `ops/r005-regression-sentinel-wave25.md`; `ops/r005-gate-check-wave24.md`; lint checklist |
| D-03 (next cycle mode) | Stabilization-first or expansion-first? | **Stabilization-first** | open | Chris | 2026-02-21 | High | Strategy log 2026-02-20 entries; contradiction hunt and dedupe outputs |
| D-04 (signoff depth) | 60-min only, 1-day only, or two-stage? | **Two-stage** (60-min triage, 1-day only if Critical uncertainty remains) | open | Chris | 2026-02-21 | Medium | Reading guides + Wave21 checklist |
| D-05 (provisional promotion policy) | Ad hoc promotion or explicit criteria gate? | **Explicit criteria gate** (lock scan pass + validation + authority citation) | open | Chris + Canon gate owner | 2026-02-24 | High | Executive summary, handoff brief, lock matrix, domain validation checklists |
| D-06 (anti-dup governance) | Optional novelty/compression check or mandatory blocker? | **Mandatory pre-merge blocker** for high-volume commits | open | Chris + Merge gate owner | 2026-02-24 | High | Reconciliation completion status, dedupe map, final snapshot, executive summary |
| D-07 (question-bank policy) | Full Top-50 each cycle or phase-targeted subset? | **Phase-targeted subset** with LOCKED/REVISE/DEFER tracking | open | Chris + Review ops owner | 2026-02-25 | Medium | Top-50 bank, handoff brief, start-here review path |

## Update protocol
For each decision, update this tracker using one of:
- `Status: decided` + record selected option and decision date
- `Status: deferred` + record defer reason + next review date
- `Status: open` only while awaiting explicit signoff

## Quick signoff capture format
- `D-01: <GO/HOLD> | status=<decided/deferred> | owner=<name> | due=<YYYY-MM-DD>`
- `D-02: <Scheduled closure/Monitor-only> | status=<...>`
- `D-03: <Stabilization/Expansion> | status=<...>`
- `D-04: <Two-stage/60-min/1-day> | status=<...>`
- `D-05: <Explicit criteria/Ad hoc> | status=<...>`
- `D-06: <Mandatory/Optional> | status=<...>`
- `D-07: <Targeted subset/Full Top-50> | status=<...>`
