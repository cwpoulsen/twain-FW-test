# Decision Queue — Wave 25

Companion to: `ops/handoff-briefing-wave23.md` (execution sequencing) and `ops/doc-map-dedupe-wave24.md` (keep/merge/archive context).

Routing note (Wave 27): supporting decision analysis queue; **primary decision-call route is `ops/unresolved-decisions-brief-wave26.md`**.

Date: 2026-02-20  
Scope source docs: `ops/reviewer-checklist-wave21.md`, `ops/reviewer-question-bank-top50-v1.md`, `ops/handoff-briefing-wave23.md`, `ops/executive-summary-wave20.md`, `ops/continuity-holes-register-v1.md`  
Strategy alignment: latest `ops/strategy-control-log.md` entry (2026-02-20T01:12-05:00) — prioritize decision enablement, contradiction-hunt/compression, and keep/merge/archive outcomes.

Canon locks preserved in this queue: AI first-scene seed timing; Asterion naming; Class 4/3/2/1 ladder (Blackfly Class 2, Asterion fragile Class 1); post-defection free-operator framing; realism constraints.

---

## Priority Decision Queue (highest impact first)

| Order | Pending human decision | Why this is high-impact now | Impact if delayed | Recommendation |
|---|---|---|---|---|
| 1 | **RC1 decision:** tag now vs hold (`rc1-wave22`) | This is the release gate controlling whether current stable state becomes an explicit baseline. It unlocks all downstream planning and prevents ambiguous “almost-approved” state. | Ongoing ambiguity, repeated re-review cycles, and higher chance of accidental drift before baseline is anchored. | **Decide within this pass.** Default: **GO** only if Wave 21 Critical checklist items have evidence-backed PASS and weekly monitor evidence is fresh; otherwise **HOLD/NO-GO** with explicit fail log + fix owner/date. |
| 2 | **R-005 path:** monitor-only vs scheduled closure pass | `R-005` is the only open canonical risk (P2 monitor). Leaving it indefinite risks template conformance regression in scene packets. | Silent quality drift, recurring lint debt, and future contradiction risk masked by format inconsistency. | **Choose scheduled closure pass** (preferred) with a dated checkpoint; keep weekly monitor until closure criteria are met. |
| 3 | **Next wave mode:** stabilization vs expansion | Multiple docs recommend avoiding broad net-new prose until review decisions land. This governs scope, risk, and review efficiency for Wave 25+. | Meta-doc churn, duplicate prose, and reduced marginal quality from over-automation. | **Stabilization-first** (contradiction hunt + compression + R-005 closure), then expansion only under bounded acceptance tests. |
| 4 | **Signoff depth mode:** 60-min fast signoff vs 1-day deep signoff | Determines review confidence level before RC promotion and next writing wave. | Either premature confidence (too shallow) or unnecessary delay (too deep) without explicit rationale. | **Two-stage:** run 60-min now for gate triage, then 1-day deep only if any Critical/near-Critical uncertainty remains. |
| 5 | **Promotion policy for provisional reservoir content** | Executive summary flags unresolved governance for what can graduate from provisional packs into canon authority docs. | Future continuity confusion and authority-layer contamination from unvetted ideation text. | **Lock explicit promotion criteria now** (required validations: lock scan pass + timeline/mechanism check + authority citation). |
| 6 | **Anti-duplication governance:** mandatory pre-merge novelty/compression gate | Historical W11/W15 duplication seams show this is a recurring process risk even when lock scans pass. | Reintroduction of repetitive sections, lower readability, and hidden contradiction risk. | **Adopt mandatory pre-merge duplication/compression check** for high-volume commits; treat failures as merge blockers until corrected. |
| 7 | **Question-bank execution policy:** full Top-50 each cycle vs targeted subset | Top-50 is high-value but can become throughput drag if applied indiscriminately. | Review fatigue, inconsistent usage, and weaker decision traceability. | **Use targeted subset by phase**: Canon+Arc 0s first, then Character/Faction, then Tech; require LOCKED/REVISE/DEFER tracking per selected question set. |

---

## Recommended decision sequence (operational)

1. **RC1 GO/NO-GO call** (Decision 1)  
2. **R-005 closure policy + date** (Decision 2)  
3. **Wave mode selection (stabilize vs expand)** (Decision 3)  
4. **Signoff depth protocol for this cycle** (Decision 4)  
5. **Promotion criteria for provisional content** (Decision 5)  
6. **Pre-merge anti-dup gate policy** (Decision 6)  
7. **Question-bank usage cadence** (Decision 7)

Rationale for order: 1-3 set release and production posture; 4 sets review depth; 5-7 harden process against known drift channels.

---

## Minimum evidence bundle to close top decisions

- Completed `ops/reviewer-checklist-wave21.md` with evidence refs for every Critical item.  
- Fresh weekly monitor artifact in `ops/evidence/wave21-weekly-monitor-YYYY-MM-DD.txt`.  
- Explicit R-005 status update in `ops/continuity-holes-register-v1.md` after decision (monitor-only or closure-scheduled).  
- Short decision log note in handoff/update doc recording final calls and dates.

---

## Keep / Merge / Archive recommendations for overlapping decision docs

| Doc | Primary role | Overlap | Recommendation |
|---|---|---|---|
| `ops/reviewer-checklist-wave21.md` | Final go/no-go gate with Critical criteria | Overlaps with handoff decision section and question bank intent | **KEEP (authoritative gate form).** Do not duplicate gate criteria elsewhere. |
| `ops/reviewer-question-bank-top50-v1.md` | Strategic forcing questions to drive high-leverage decisions | Overlaps with executive “next decisions” and checklist diagnostics | **KEEP, but MERGE usage guidance into handoff/start-here.** Keep bank as reference library, not first-step checklist. |
| `ops/handoff-briefing-wave23.md` | Immediate action queue and operator next steps | Repeats project status also in executive summary | **KEEP (action owner doc), trim repeated status text over time.** |
| `ops/executive-summary-wave20.md` | Snapshot status/risk + decision framing | Overlaps with handoff status and continuity register risk table | **KEEP (status authority).** Avoid action-task duplication here. |
| `ops/continuity-holes-register-v1.md` | Canonical risk ledger and closure state | Status snippets echoed in executive/handoff docs | **KEEP (single source of risk truth).** Other docs should only reference, not restate tables in full. |

### Consolidation policy (recommended)

- **Decision authority stack:**
  1) continuity/risk truth = `continuity-holes-register`  
  2) release decision gate = `reviewer-checklist`  
  3) strategic framing = `executive-summary`  
  4) immediate operator actions = `handoff-briefing`  
  5) deep prompts = `question-bank`

- **Merge target:** add a short “how to use Top-50 question bank this cycle” block in `handoff-briefing` (or `start-here`), instead of repeating decision questions in multiple docs.
- **Archive:** no immediate archive required among these five active decision docs; they are complementary once role boundaries above are enforced.