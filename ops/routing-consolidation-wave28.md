# Routing Consolidation — Wave 28

Date: 2026-02-20  
Companion to: `ops/doc-routing-prune-wave27.md` (primary-route lock), `ops/supersession-finalize-wave26.md` (metadata/supersession controls), and `ops/start-here-review-path.md` (active review entrypoint).  
Routing note (Wave 30): supporting consolidation summary; primary review entry routes remain in `ops/start-here-review-path.md`.  
Input strategy control: `ops/strategy-control-log.md` latest entry (2026-02-20T01:23-05:00) reviewed first.  
Scope: low-risk routing consolidation pass across review docs touched in Waves 24–27.  
Constraint: **No canon changes** (ops-layer routing/metadata text only).

## What was consolidated
- Ensured each targeted review doc has:
  1) an explicit metadata line (`Companion to:`), and
  2) a clear routing-role note (primary vs supporting route).
- Removed routing ambiguity by clarifying that decision-call primary route is `ops/decision-quickfill-card-wave32.md` (with `ops/decision-ready-packet-wave30.md` as summary context).
- Replaced one conflicting routing signal in Wave 27 ballot doc (`Supersedes` claim) with supporting-route language.

## Changed files (Wave 28 pass)
1. `ops/doc-map-dedupe-wave24.md`
   - Added Wave 28 routing-role note (supporting dedupe/governance map; primary routes remain in `ops/start-here-review-path.md`).
2. `ops/doc-merge-plan-wave25.md`
   - Added `Companion to:` metadata line.
   - Added Wave 28 routing-role note (supporting merge/archive plan).
3. `ops/supersession-finalize-wave26.md`
   - Added `Companion to:` metadata line.
   - Added Wave 28 routing-role note (supporting supersession control log).
4. `ops/decision-ballot-pack-wave27.md`
   - Replaced `Supersedes: ops/unresolved-decisions-brief-wave26.md` with companion/reference metadata.
   - Added Wave 28 routing-role note clarifying ballot is supporting one-screen response form.

## Docs reviewed (no edit required)
- `ops/decision-queue-wave25.md` (already clear supporting-route note + metadata)
- `ops/decision-quickfill-card-wave32.md` (current primary decision-call route + metadata)
- `ops/doc-routing-prune-wave27.md` (already clear routing lock + metadata)

## Keep / Merge / Archive recommendations

### Keep (active)
- `ops/start-here-review-path.md` (primary review routing owner)
- `ops/decision-quickfill-card-wave32.md` (primary decision-call route)
- `ops/doc-map-dedupe-wave24.md` (dedupe/ownership governance)
- `ops/doc-merge-plan-wave25.md` (merge/archive execution plan)
- `ops/supersession-finalize-wave26.md` (annotation control history)
- `ops/doc-routing-prune-wave27.md` (primary-route lock record)

### Merge (recommended)
- Keep `ops/decision-ballot-pack-wave27.md` as a supporting one-screen ballot alongside `ops/decision-quickfill-card-wave32.md`; avoid creating a legacy-primary dependency.
- Optionally merge overlapping route-governance notes from:
  - `ops/doc-map-dedupe-wave24.md`
  - `ops/doc-merge-plan-wave25.md`
  - `ops/supersession-finalize-wave26.md`
  into one maintained routing-governance owner doc, with the others reduced to historical stubs.

### Archive (not now; future after merge)
- No immediate archive action in this pass.
- After merge validation, archive superseded full-body planning docs to `ops/archive/review-routing-legacy/` with pointer stubs retained at original paths.

## Risk / continuity check
- Canon/domain content edited: **none**.
- Policy logic changes: **none**.
- Routing/metadata only: **yes**.
- Net effect: reduced review-route ambiguity, lower duplication risk in decision-routing docs.
