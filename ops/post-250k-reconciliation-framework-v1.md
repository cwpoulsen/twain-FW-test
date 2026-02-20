# Post-250k Reconciliation Framework v1

Purpose: run one controlled, auditable global cleanup after the bible crosses 250k words, without reopening canon drift.

Primary authorities (obey in this order):
1. `canon/canon-ledger-v2.md`
2. `timeline/master-timeline-sequence-v1.md`
3. `ops/continuity-lock-check-matrix-v1.md`
4. `ops/continuity-guard-grep-recipes-v1.md`
5. `ops/contradiction-scanner-checklist-v1.md`
6. `ops/domain-validation-checklists-v1.md`
7. `ops/continuity-dependency-map-v1.md`
8. `ops/continuity-holes-register-v1.md`
9. `ops/reality-gate-enforcement-pack-v1.md`

---

## 1) Final Audit Checklist (Release Gate)

### A. Freeze + Input Control
- [ ] Declare reconciliation freeze window (no expansion merges during cleanup).
- [ ] Record exact git baseline SHA in audit notes.
- [ ] Confirm authority pointers above are current (no stale filenames/versions).
- [ ] Create evidence file for this run under `ops/evidence/`.

### B. Repository-wide Lock Scans
- [ ] Run full grep suite from `ops/continuity-guard-grep-recipes-v1.md` (A-E).
- [ ] Capture command transcript + hit counts in evidence file.
- [ ] Classify every hit: `VALID_POLICY`, `ARCHIVE_ONLY`, `ACTIVE_VIOLATION`, `NEEDS_REVIEW`.

### C. Contradiction Scan + Domain Validation
- [ ] Execute full `ops/contradiction-scanner-checklist-v1.md`.
- [ ] Execute all domain checks in `ops/domain-validation-checklists-v1.md`.
- [ ] Log unresolved contradictions to `ops/continuity-holes-register-v1.md` with severity and owner.

### D. Patch + Verification Loop
- [ ] Apply fixes in smallest possible commits by domain.
- [ ] Re-run only relevant lock scans after each patch.
- [ ] Re-run full A-E + contradiction checklist after final patch.
- [ ] Confirm no P0/P1 unresolved violations remain.

### E. Final Closure
- [ ] Update `ops/book-bible-progress-log.md` with what changed and why.
- [ ] Add reconciliation summary + evidence path to `ops/book-bible-pass-log.md`.
- [ ] Record final status in `ops/strategy-control-log.md`.
- [ ] Tag as post-250k reconciliation complete (or list explicit blockers).

---

## 2) Lock Verification Matrix (Execution Form)

Use with `ops/continuity-lock-check-matrix-v1.md` for lock definitions.

| Lock Family | Required State | Verification Method | Evidence Artifact | Fail Class | Action Owner |
|---|---|---|---|---|---|
| Naming lock (Asterion League) | Deprecated terms absent in active canon prose | Grep A1/A2 + spot check canon/series/timeline | `ops/evidence/post250k-*.txt` | P1 | Canon lead |
| AI timing lock | Opening spec-op acquires AI seed/system; databank is training/provenance | Grep B1/B2 + timeline event-chain review | `ops/evidence/post250k-*.txt` + timeline diff | P0 | Timeline lead |
| Pursuit uncertainty lock | Blackfly location framed as unknown/probabilistic | Grep C1/C2 + scene/series narrative sweep | evidence transcript + note block | P1 | Series lead |
| Physics realism lock | Low-g anchoring/attitude/recoil constraints preserved | Grep D1/D2 + random scene sample | evidence transcript + sampled scene IDs | P1 | Scene/tech lead |
| Warform agency lock | Full override depicted as non-conscious remote operation | Grep D3 + doctrine consistency read | evidence transcript + doctrine citation | P1 | Canon/ops lead |
| Fabrication ladder lock | 3/4 -> Blackfly 2 -> Asterion 1 unchanged | Grep E1/E2 + tech table verification | evidence transcript + tech diff | P0/P1 | Tech lead |
| Process traceability lock | Ops docs point to current authorities and logs | Ops file link audit + process grep | checklist appendix in evidence file | P2 | Ops lead |

Pass criteria:
- No unresolved P0/P1 lock failures.
- Any P2 process failures either fixed or explicitly waived with rationale.

---

## 3) Contradiction Triage Workflow

### Intake
1. Capture contradiction with exact file + line refs.
2. Assign one of four classes:
   - `L0 FALSE_POSITIVE` (tool hit but canon-safe)
   - `L1 PROCESS_ONLY` (documentation/linkage defect)
   - `L2 SOFT_CONTRADICTION` (tone/implication drift)
   - `L3 HARD_CONTRADICTION` (canon/timeline/rule break)

### Severity Mapping
- `L0` -> close with note in evidence file.
- `L1` -> patch same pass; no canon retcon required.
- `L2` -> patch in current pass; verify downstream docs.
- `L3` -> stop-line event: fix before further cleanup passes.

### Decision Path
1. Check authority precedence (ledger/timeline first).
2. Determine if contradiction is local text issue or upstream lock issue.
3. Choose resolution type:
   - `TEXT_PATCH` (local rewrite)
   - `CANON_PATCH` (explicit lock update with impact list)
   - `TIMELINE_PATCH` (sequence/causality adjustment)
4. Apply patch and run targeted re-scan.
5. If unresolved after 2 attempts, escalate to holes register with owner + due pass.

### Exit Conditions
- Contradiction closed only when:
  - source file corrected,
  - dependent references updated,
  - relevant grep/checklist gates pass,
  - closure evidence written to `ops/evidence/`.

---

## 4) Pass-by-Pass Execution Order (Global Cleanup)

Run passes in strict order; do not skip forward with open stop-line defects.

1. **Pass 0 — Baseline + Freeze**
   - Snapshot baseline SHA, create evidence log, announce freeze window.

2. **Pass 1 — Hard Lock Enforcement**
   - Execute A-E scans from grep recipes.
   - Fix all P0/P1 lock violations first.

3. **Pass 2 — Timeline/Causality Reconciliation**
   - Run timeline section of contradiction checklist.
   - Resolve sequencing, travel/comms plausibility, reveal-order breaks.

4. **Pass 3 — Canon Layer Consistency**
   - Validate CORE/SOFT/RUMOR layering and retcon hygiene.
   - Ensure no silent CORE overrides.

5. **Pass 4 — Domain-by-Domain Validation**
   - Apply `ops/domain-validation-checklists-v1.md` across canon/timeline/series/factions/tech/characters/scenes/ops.

6. **Pass 5 — Dependency Cross-Link Repair**
   - Use `ops/continuity-dependency-map-v1.md` to repair downstream references and stale pointers.

7. **Pass 6 — Contradiction Triage Sweep**
   - Process remaining contradictions through workflow above.
   - Update holes register for any deferred non-blockers.

8. **Pass 7 — Reality Gate + Final Regression**
   - Run enforcement from `ops/reality-gate-enforcement-pack-v1.md`.
   - Re-run full grep suite and contradiction checklist as regression gate.

9. **Pass 8 — Closeout + Audit Record**
   - Update pass/progress/strategy logs.
   - Publish final reconciliation summary with evidence link and unresolved-item table (if any).

---

## 5) Required Artifacts for Completion

- Evidence transcript: `ops/evidence/post250k-reconciliation-YYYY-MM-DD.txt`
- Pass summary entry: `ops/book-bible-pass-log.md`
- Progress summary entry: `ops/book-bible-progress-log.md`
- Any open issues: `ops/continuity-holes-register-v1.md`
- Strategy note: `ops/strategy-control-log.md`

Definition of done:
- Full pass chain (0-8) completed.
- All lock families verified with evidence.
- No unresolved P0/P1 contradictions.
- Audit trail is reproducible by a fresh operator from docs + evidence alone.
