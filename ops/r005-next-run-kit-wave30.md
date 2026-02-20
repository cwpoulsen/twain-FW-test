# R-005 Next-Run Kit — Wave 30

Companion to: `ops/r005-watchdog-template-wave27.md` and `ops/r005-watchdog-rollup-wave29.md`

Purpose: fast, low-friction run kit for the next weekly R-005 watchdog cycle.

---

## Minimal Checklist (operator)

- [ ] Duplicate/fill `ops/r005-watchdog-template-wave27.md` as the new run doc (date-stamped filename).
- [ ] Set run metadata (date, owner, prior-run reference, evidence path).
- [ ] Run ST-1..ST-4 command block below from repo root.
- [ ] Confirm ST-1..ST-3 are PASS and ST-4 notes are recorded.
- [ ] Compare against prior run and set trend: Stable / Improved / Regressed.
- [ ] If any WARN/FAIL, apply escalation flow from rollup + template (hole ID, owner, due date, recheck evidence).
- [ ] Keep risk posture as `R-005 OPEN (monitor)` unless explicitly closed by approved decision.
- [ ] Paste one-line summary into the run doc.

---

## Copy/Paste Command Block (weekly watchdog)

```bash
# R-005 weekly watchdog quick run (repo root)
STAMP="$(date +%F)"
OUT="ops/evidence/r005-weekly-watchdog-${STAMP}.txt"

PACKET_DOCS=(
  "series/scene-packets-books1-4-v1.md"
  "series/scene-packets-books5-7-bridge-v1.md"
  "series/scene-packets-books8-10-endgame-bridge-v1.md"
)

mkdir -p ops/evidence
{
  echo "# R-005 Weekly Watchdog - ${STAMP}"
  echo

  echo "## ST-1 Template-lock block present"
  for f in "${PACKET_DOCS[@]}"; do
    if grep -q "^## Scene Packet Template Lock (R-005)" "$f"; then
      echo "PASS template-lock block: $f"
    else
      echo "FAIL template-lock block missing: $f"
    fi
  done

  echo
  echo "## ST-2 Required field coverage counts"
  for f in "${PACKET_DOCS[@]}"; do
    packets=$(grep -c '^### Packet ' "$f" || true)
    mission=$(grep -Ec '^\*\*(Mission seed|Mission-chain anchor):\*\*' "$f" || true)
    objective=$(grep -Ec '^\*\*Objective:\*\*' "$f" || true)
    conflict=$(grep -Ec '^\*\*Conflict:\*\*' "$f" || true)
    tactical=$(grep -Ec '^\*\*Tactical geometry:\*\*' "$f" || true)
    reality=$(grep -Ec '^\*\*Reality gate row:\*\*' "$f" || true)
    emotional=$(grep -Ec '^\*\*Emotional turn:\*\*' "$f" || true)
    consequence=$(grep -Ec '^\*\*Consequence ledger:\*\*' "$f" || true)
    refs=$(grep -Ec '^\*\*Continuity refs:\*\*' "$f" || true)

    printf "%s | packets=%s mission=%s objective=%s conflict=%s tactical=%s reality=%s emotional=%s consequence=%s refs=%s\n" \
      "$f" "$packets" "$mission" "$objective" "$conflict" "$tactical" "$reality" "$emotional" "$consequence" "$refs"
  done

  echo
  echo "## ST-3 Required field order"
  for f in "${PACKET_DOCS[@]}"; do
    awk '
    /^### Packet / {
      if (in_packet && fail==0) {
        for (i=1;i<=8;i++) if (pos[i]==0) { print "FAIL " file " :: " packet " missing field #" i; fail=1 }
        for (i=2;i<=8;i++) if (pos[i] && pos[i-1] && pos[i] < pos[i-1]) { print "FAIL " file " :: " packet " out-of-order field #" i; fail=1 }
      }
      in_packet=1
      packet=$0
      for (i=1;i<=8;i++) pos[i]=0
      next
    }
    in_packet {
      ln=NR
      if ($0 ~ /^\*\*(Mission seed|Mission-chain anchor):\*\*/) pos[1]=ln
      else if ($0 ~ /^\*\*Objective:\*\*/) pos[2]=ln
      else if ($0 ~ /^\*\*Conflict:\*\*/) pos[3]=ln
      else if ($0 ~ /^\*\*Tactical geometry:\*\*/) pos[4]=ln
      else if ($0 ~ /^\*\*Reality gate row:\*\*/) pos[5]=ln
      else if ($0 ~ /^\*\*Emotional turn:\*\*/) pos[6]=ln
      else if ($0 ~ /^\*\*Consequence ledger:\*\*/) pos[7]=ln
      else if ($0 ~ /^\*\*Continuity refs:\*\*/) pos[8]=ln
    }
    END {
      if (in_packet && fail==0) {
        for (i=1;i<=8;i++) if (pos[i]==0) { print "FAIL " file " :: " packet " missing field #" i; fail=1 }
        for (i=2;i<=8;i++) if (pos[i] && pos[i-1] && pos[i] < pos[i-1]) { print "FAIL " file " :: " packet " out-of-order field #" i; fail=1 }
      }
      if (fail==0) print "PASS order-check: " file
    }' file="$f" "$f"
  done

  echo
  echo "## ST-4 Manual lint reminder"
  echo "Run lightweight packet lint checklist: ops/packet-doc-lint-checklist-v1.md"
} > "$OUT"

echo "Wrote $OUT"
```

---

## Quick Link Set (for operator use)

- Run template: `ops/r005-watchdog-template-wave27.md`
- Trend rollup: `ops/r005-watchdog-rollup-wave29.md`
- Last executed run: `ops/r005-watchdog-run-2026-02-20-wave28.md`
- Lint checklist: `ops/packet-doc-lint-checklist-v1.md`
- Evidence directory: `ops/evidence/`

## One-Line Summary Stub

`R-005 weekly watchdog (YYYY-MM-DD, owner: ___): ST-1 __ / ST-2 __ / ST-3 __ / ST-4 __, trend: ___, escalation: ___, evidence: ops/evidence/r005-weekly-watchdog-YYYY-MM-DD.txt`