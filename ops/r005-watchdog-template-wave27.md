# R-005 Weekly Watchdog Template — Wave 27

Companion to: `ops/r005-stability-delta-wave26.md` and `ops/monitor-pack-wave21.md`.
Routing note (Wave 30): **Primary route for recurring R-005 watchdog runs.**

## R-005 Status Banner (Wave 32)
- **Current state:** `R-005 OPEN (monitor)`; latest executed watchdog snapshot is `ST-1 PASS / ST-2 PASS / ST-3 PASS / ST-4 PASS`, trend **Stable**, escalation **not triggered**.
- **Latest evidence pointer:** `ops/evidence/wave28-r005-watchdog-run-2026-02-20.txt`
- **Latest run record:** `ops/r005-watchdog-run-2026-02-20-wave28.md`
- **Banner maintenance rule:** update this banner on each new watchdog run; keep gate criteria/process logic below unchanged.

Use this lightweight template for recurring weekly R-005 checks.

---

## Run Metadata
- **Run date (YYYY-MM-DD):**
- **Run owner:**
- **Evidence artifact path:** `ops/evidence/...`
- **Prior run reference:**
- **Scope checked:**
  - `series/scene-packets-books1-4-v1.md`
  - `series/scene-packets-books5-7-bridge-v1.md`
  - `series/scene-packets-books8-10-endgame-bridge-v1.md`

## ST-1..ST-4 Current Status
- **ST-1 (template-lock block present):** PASS / WARN / FAIL
- **ST-2 (required field coverage counts):** PASS / WARN / FAIL
- **ST-3 (required field order):** PASS / WARN / FAIL
- **ST-4 (lightweight packet lint):** PASS / WARN / FAIL

## Trend vs Prior Run
- **Prior snapshot:** ST-1 __ / ST-2 __ / ST-3 __ / ST-4 __
- **Current snapshot:** ST-1 __ / ST-2 __ / ST-3 __ / ST-4 __
- **Trend call:** Stable / Improved / Regressed
- **Delta notes (only changed items):**
  - 

## Escalation Actions (only if any WARN/FAIL)
- **Escalation triggered?** yes / no
- **Trigger(s):** ST-1 / ST-2 / ST-3 / ST-4 / other
- **Immediate action taken:**
- **Continuity hole entry:** `ops/continuity-holes-register-v1.md` (ID: ___)
- **Owner + due date for remediation:**
- **Recheck evidence path:** `ops/evidence/...`

## Weekly Disposition
- **Overall R-005 watchdog status:** PASS / WARN / FAIL
- **Merge gate impact:** none / caution / block
- **Notes for next run (max 3 bullets):**
  - 
  - 
  - 

---

### Copy/Paste One-Line Summary
`R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST-1 __ / ST-2 __ / ST-3 __ / ST-4 __, trend: ___, escalation: ___, evidence: ops/evidence/...`