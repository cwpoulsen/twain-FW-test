# Doc-Map Dedupe — Wave 24

Companion to: `ops/start-here-review-path.md` (primary route), `ops/archive-index-wave20.md` (catalog), and `ops/decision-queue-wave25.md` (human decisions).

Date: 2026-02-20  
Scope: authority/index/guide overlap reduction across review-routing docs.  
Constraint: **CANON LOCKS unchanged** (no canon-domain edits).

## 1) Strategy-control alignment (latest-first execution)
Latest strategy entry (`2026-02-20T01:12-05:00`) requires:
1. contradiction-hunting + compression over net-new prose,
2. reduced index/briefing churn,
3. explicit keep/merge/archive recommendations per run.

This pass addresses that by defining one deduplicated doc-map and tightening role boundaries between existing guides.

---

## 2) Deduplicated authority doc-map (single routing view)
Use this as the default routing stack (top-to-bottom):

1. **`ops/start-here-review-path.md`** — **Primary entrypoint** (ordered reading route).
2. **`ops/executive-summary-wave20.md`** — **Decision snapshot** (status, locks, active risks, near-term decisions).
3. **`ops/handoff-briefing-wave23.md`** — **Action queue** (what to decide next + 30-minute execution plan).
4. **`ops/archive-index-wave20.md`** — **Repository catalog** (domain-by-domain lookup, lower-frequency use).
5. **`ops/final-snapshot-status-wave19.md`** — **Historical baseline** (pre-W20 reference state only).

Operational rule:
- For current decisions, prefer docs 1-3.
- Use doc 4 only for broad lookup.
- Use doc 5 only for historical reconstruction/delta checks.

---

## 3) Overlap analysis and disposition

| Doc | Current value | Main overlap | Recommendation |
|---|---|---|---|
| `ops/start-here-review-path.md` | Fast practical reading path | overlaps with reading guides + handoff top-files | **KEEP (primary route)**; keep concise and link to dedupe map |
| `ops/executive-summary-wave20.md` | Best high-level status/risk summary | partial overlap with handoff status section | **KEEP (decision snapshot)**; avoid duplicating long file lists |
| `ops/handoff-briefing-wave23.md` | Concrete next decisions + steps | repeats status/orientation already in executive/start-here | **KEEP (action-oriented)**; trim future repeats of orientation prose |
| `ops/archive-index-wave20.md` | Full domain map, useful lookup index | overlaps with start-here and reading guides for onboarding | **KEEP (catalog)** but not a first-read gate |
| `ops/final-snapshot-status-wave19.md` | Historical commit/risk/corpus baseline | stale if treated as current status | **KEEP as historical snapshot**; explicitly mark baseline-only usage |
| `ops/reading-guide-60min-quick-review-v1.md` | Time-boxed onboarding | overlaps with start-here orientation | **MERGE role into start-here over time** (retain file for now) |
| `ops/reading-guide-1day-deep-review-v1.md` | Deep review sequence | overlaps with archive-index + start-here + optional dives | **MERGE role into start-here optional section** (retain for now) |
| `ops/release-candidate-index-pack-wave17-v1.md` | Legacy RC packet index | overlaps with newer wave20+ routing docs | **ARCHIVE-ONLY (historical)** |
| `ops/final-review-pack-wave17-for-chris.md` | Legacy signoff packet | superseded by newer handoff/reviewer/checklist docs | **ARCHIVE-ONLY (historical)** |

---

## 4) Low-risk tightening applied in this wave

1. Added cross-link in `ops/start-here-review-path.md` to this dedupe map so readers can resolve guide/index ambiguity quickly.
2. Added cross-link in `ops/archive-index-wave20.md` pointing to this dedupe map for role boundaries.

No canon lock docs changed. No authority semantics changed.

---

## 5) Keep / Merge / Archive policy (next passes)

### Keep (active)
- `ops/start-here-review-path.md`
- `ops/executive-summary-wave20.md`
- `ops/handoff-briefing-wave23.md`
- `ops/archive-index-wave20.md`

### Merge (planned, not executed in this pass)
- Fold key value of both reading guides into:
  - start-here (time-box callouts), and
  - handoff (decision-focused short path).
- After merge verification, convert reading guides to short stubs pointing to start-here.

### Archive (historical reference)
- `ops/final-snapshot-status-wave19.md` (baseline)
- `ops/release-candidate-index-pack-wave17-v1.md`
- `ops/final-review-pack-wave17-for-chris.md`

---

## 6) Notes for next operator
- If churn continues, enforce a single-doc ownership rule:
  - route ownership = `start-here`
  - status ownership = `executive-summary`
  - action ownership = `handoff-briefing`
  - catalog ownership = `archive-index`
- Reject new guide/index docs unless they replace one of the above roles.