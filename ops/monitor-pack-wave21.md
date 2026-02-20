# Monitor Pack — Wave 21 (Post-RC Weekly Maintenance)

Date: 2026-02-19  
Owner: Bible maintenance  
Cadence: **Weekly** (recommended every Thu/Fri before any major content merge)

---

## 1) Objective

Keep RC lock integrity stable by running a repeatable weekly monitor for:
1. **Naming drift** (canonical actor/faction terms)
2. **Lock violations** (A1-E2 continuity lock families)
3. **Risk regressions** (R-005..R-008 status drift)

This pack is a monitor/runbook, not a rewrite pass.

---

## 2) Weekly Execution (from repo root)

```bash
# Recommended scope
SCAN_PATHS="canon characters factions locations ops scenes series tech timeline"
EXCLUDES="--exclude-dir=.git --exclude-dir=agent-backup-2026-02-19 --exclude-dir=evidence --exclude-dir=full-state-backup-2026-02-19-2046"
STAMP="$(date +%F)"
OUT="ops/evidence/wave21-weekly-monitor-${STAMP}.txt"

mkdir -p ops/evidence
{
  echo "# Wave 21 Weekly Monitor - ${STAMP}"
  echo
  echo "## Naming Drift"
  echo "### ND-1 Deprecated naming residue"
  grep -RIn $EXCLUDES -E "\\bBelters\\b|Solar Defense Force" $SCAN_PATHS || true
  echo
  echo "### ND-2 Canonical naming presence"
  grep -RIn $EXCLUDES -E "Asterion League" canon factions series timeline ops tech || true

  echo
  echo "## Lock Violations (A1-E2)"
  echo "### A1"
  grep -RIn $EXCLUDES -E "\\bBelters\\b|Solar Defense Force" $SCAN_PATHS || true
  echo "### A2"
  grep -RIn $EXCLUDES -E "Asterion League" canon factions series timeline ops tech || true
  echo "### B1"
  grep -RIn $EXCLUDES -E "databank raid.*(acquire|recovers?).*(AI seed|AI system|AI seed/system)" $SCAN_PATHS || true
  echo "### B2"
  grep -RIn $EXCLUDES -E "opening spec-ops extraction.*AI seed/system|databank raid.*training/upgrade" canon series timeline ops || true
  echo "### C1"
  grep -RIn $EXCLUDES -E "exact position known|always knows? (their|its) position|perfect tracking" $SCAN_PATHS || true
  echo "### C2"
  grep -RIn $EXCLUDES -E "unknown current location|probabilistic dragnet|missing asset" canon series ops || true
  echo "### D1"
  grep -RIn $EXCLUDES -E "normal walking|earthlike gravity firefight|stood firm without anchoring" $SCAN_PATHS || true
  echo "### D2"
  grep -RIn $EXCLUDES -E "anchoring|attitude control|recoil" canon series ops tech || true
  echo "### D3"
  grep -RIn $EXCLUDES -E "non-conscious human puppets|full override|remote warform" canon ops factions series || true
  echo "### E1"
  grep -RIn $EXCLUDES -E "Blackfly.*Class 2|Asterion League.*Class 1|Class 3/4" canon tech factions series ops || true
  echo "### E2"
  grep -RIn $EXCLUDES -E "Class-0|Class 0|Class IV" tech canon factions series || true

  echo
  echo "## Risk Regression"
  echo "### RR-1 Canonical risk table"
  grep -n "Canonical Risk Status Table" -A 12 ops/continuity-holes-register-v1.md || true
  echo
  echo "### RR-2 Open-risk lines"
  grep -n -E "R-005|R-006|R-007|R-008|OPEN|CLOSED" ops/continuity-holes-register-v1.md | head -n 80 || true
} > "$OUT"

echo "Wrote $OUT"
```

---

## 3) Thresholds and Gate Rules

### 3.1 Naming Drift Thresholds
- **PASS:** 0 new deprecated naming hits in active content layers (`canon/series/timeline/scenes/factions/tech/locations/characters`).
- **WARN:** Any hit confined to ops policy/checklist/history context only.
- **FAIL:** Any deprecated naming hit in canon/series/timeline/scenes or faction/tech authorities.

### 3.2 Lock Violation Thresholds (A1-E2)
- **PASS:**
  - No anti-pattern hits (A1, B1, C1, D1, E2) in active canon layers.
  - Positive lock cues (A2, B2, C2, D2, D3, E1) remain present in authority layers.
- **FAIL (P1):** Any anti-pattern in authoritative story/canon docs.
- **FAIL (P0):** Contradiction that inverts core lock (AI timing inversion, omniscient Blackfly tracking certainty, fabrication ladder break).

### 3.3 Risk Regression Thresholds
- **PASS:** Risk table remains: `R-005 OPEN (monitor)`, `R-006 CLOSED`, `R-007 CLOSED`, `R-008 CLOSED`.
- **WARN:** Wording churn with unchanged status meaning.
- **FAIL:** Any closed risk (R-006/007/008) re-opened, or R-005 severity escalates above P2 without documented rationale.

---

## 4) Triage + Response SLA

If any FAIL condition triggers:
1. Log issue in `ops/continuity-holes-register-v1.md` (new W21-* entry with severity + affected files).
2. Patch same day for P0/P1, within 72h for P2.
3. Re-run weekly monitor command block and attach evidence file path in register entry.
4. If risk status changed, update `ops/post250k-reconciliation-completion-status-2026-02-19.md` (or successor status file).

SLA:
- **P0:** immediate block on merges until fixed.
- **P1:** fix before next content wave merge.
- **P2:** fix/decision by next weekly monitor.

---

## 5) Weekly Signoff Template

```md
## Wave 21 Weekly Monitor — YYYY-MM-DD
- Evidence: `ops/evidence/wave21-weekly-monitor-YYYY-MM-DD.txt`
- Naming drift: PASS/WARN/FAIL
- Lock violations: PASS/WARN/FAIL
- Risk regression: PASS/WARN/FAIL
- New holes logged: none / H-xxx / W21-xxx
- Follow-up owner + due date: ...
```

This template can be appended to `ops/book-bible-pass-log.md` or a current-cycle status file.
