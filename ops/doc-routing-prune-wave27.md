# Doc Routing Prune — Wave 27

Date: 2026-02-20
Companion to: `ops/doc-map-dedupe-wave24.md` (routing/ownership dedupe), `ops/supersession-finalize-wave26.md` (merge/supersession control), `ops/strategy-control-log.md` (latest cycle pivots).

## Objective
Prune routing ambiguity across review docs by making exactly one primary entry route obvious for each review intent:
- quick review
- deep review
- decision calls
- evidence audit

## Primary route lock (now explicit)
- **Quick review (primary):** `ops/reading-guide-60min-quick-review-v1.md`
- **Deep review (primary):** `ops/reading-guide-1day-deep-review-v1.md`
- **Decision calls (primary):** `ops/unresolved-decisions-brief-wave26.md`
- **Evidence audit (primary):** `ops/evidence/evidence-index-wave23.md`

These are now listed directly in `ops/start-here-review-path.md` under a dedicated Wave 27 routing lock section.

## Files patched (headers/notes only)
1. `ops/start-here-review-path.md`
   - Added Wave 27 "Primary Review Routes" section with one primary doc per review intent.
2. `ops/reading-guide-60min-quick-review-v1.md`
   - Added `Companion to` metadata line.
   - Added routing note marking this as primary for quick review.
3. `ops/reading-guide-1day-deep-review-v1.md`
   - Added `Companion to` metadata line.
   - Added routing note marking this as primary for deep review.
4. `ops/decision-queue-wave25.md`
   - Added routing note clarifying this is supporting analysis (not primary decision-call entry).
5. `ops/unresolved-decisions-brief-wave26.md`
   - Added `Companion to` metadata line.
   - Added routing note marking this as primary for decision calls.
6. `ops/evidence/evidence-index-wave23.md`
   - Added `Companion to` metadata line.
   - Added routing note marking this as primary for evidence audit.
7. `ops/reviewer-question-bank-top50-v1.md`
   - Added `Companion to` metadata line.
   - Added routing note clarifying supporting role after primary decision-call route.

## Metadata compliance update
For all touched docs lacking explicit metadata, added `Companion to:` lines to satisfy Wave 25+ proliferation-control rule.

## Risk/impact
- Scope intentionally low-risk: no canon, policy logic, or checklist criteria changed.
- Changes are navigational only (headers/notes), focused on reducing reviewer path ambiguity.

## Recommended follow-up
- During next review cycle, validate reduced route confusion by checking whether reviewer handoff references converge on the four Wave 27 primary routes above.
