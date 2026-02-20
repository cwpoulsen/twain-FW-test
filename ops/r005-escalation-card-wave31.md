# R-005 Escalation Card — Wave 31

Companion to: `ops/r005-next-run-kit-wave30.md` and `ops/r005-watchdog-rollup-wave29.md`

Purpose: immediate operator response when any ST gate degrades from PASS.

## Trigger (escalate immediately)
- Any ST gate changes from **PASS → WARN/FAIL** in a watchdog run (`ST-1`, `ST-2`, `ST-3`, or `ST-4`).
- Treat as active `R-005 OPEN (monitor)` regression until recheck returns full PASS.

## Immediate Actions (same cycle)
1. **Declare escalation** in the active run doc with failing gate(s) and impacted file(s).
2. **Freeze packet-touching merge path** for affected scope until remediation evidence is captured.
3. **Classify severity + create/update hole entry** in `ops/continuity-holes-register-v1.md` (owner + due date + recheck plan).
4. **Patch only the failing condition(s)** (template block, required field coverage/order, or ST-4 drift language).
5. **Rerun ST checks** and publish fresh evidence artifact under `ops/evidence/`.

## Evidence Commands (repo root)
```bash
# Primary run block (from next-run kit)
STAMP="$(date +%F)"
OUT="ops/evidence/r005-weekly-watchdog-${STAMP}.txt"
bash -lc 'source /dev/stdin' <<'EOF'
PACKET_DOCS=(
  "series/scene-packets-books1-4-v1.md"
  "series/scene-packets-books5-7-bridge-v1.md"
  "series/scene-packets-books8-10-endgame-bridge-v1.md"
)
mkdir -p ops/evidence
{
  echo "# R-005 Weekly Watchdog - ${STAMP}"
  echo "## ST-1"
  for f in "${PACKET_DOCS[@]}"; do
    grep -q "^## Scene Packet Template Lock (R-005)" "$f" && echo "PASS $f" || echo "FAIL $f"
  done
  echo "## ST-2"
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
  echo "## ST-3"
  for f in "${PACKET_DOCS[@]}"; do
    awk '/^### Packet /{if(in&&fail==0){for(i=1;i<=8;i++)if(pos[i]==0){print "FAIL "file" :: "pkt" missing field #"i;fail=1}
      for(i=2;i<=8;i++)if(pos[i]&&pos[i-1]&&pos[i]<pos[i-1]){print "FAIL "file" :: "pkt" out-of-order field #"i;fail=1}}
      in=1;pkt=$0;for(i=1;i<=8;i++)pos[i]=0;next}
      in{ln=NR;if($0~/^\*\*(Mission seed|Mission-chain anchor):\*\*/)pos[1]=ln;else if($0~/^\*\*Objective:\*\*/)pos[2]=ln;
      else if($0~/^\*\*Conflict:\*\*/)pos[3]=ln;else if($0~/^\*\*Tactical geometry:\*\*/)pos[4]=ln;else if($0~/^\*\*Reality gate row:\*\*/)pos[5]=ln;
      else if($0~/^\*\*Emotional turn:\*\*/)pos[6]=ln;else if($0~/^\*\*Consequence ledger:\*\*/)pos[7]=ln;else if($0~/^\*\*Continuity refs:\*\*/)pos[8]=ln}
      END{if(in&&fail==0){for(i=1;i<=8;i++)if(pos[i]==0){print "FAIL "file" :: "pkt" missing field #"i;fail=1}
      for(i=2;i<=8;i++)if(pos[i]&&pos[i-1]&&pos[i]<pos[i-1]){print "FAIL "file" :: "pkt" out-of-order field #"i;fail=1}}
      if(fail==0)print "PASS order-check: "file}' file="$f" "$f"
  done
  echo "## ST-4"
  echo "Run manual anti-pattern lint per ops/packet-doc-lint-checklist-v1.md"
} > "$OUT"
echo "Wrote $OUT"
EOF
```

## Owners
- **Watchdog Operator (run owner):** declares escalation, executes reruns, posts evidence path.
- **Packet Doc Owner(s):** applies structural/content patch for failing gate.
- **Continuity Lead:** validates hole-log entry quality and approves merge unblock when exit criteria are met.

## Recovery Exit Criteria (close escalation)
All must be true:
- ST-1, ST-2, ST-3, ST-4 are **PASS** on rerun evidence.
- Continuity-hole record includes: root cause, fix summary, owner, due date met, and recheck artifact path.
- Run doc includes trend disposition vs prior run (Stable/Improved/Regressed) and explicit “escalation cleared”.
- Affected packet-touching merge path is explicitly unblocked by continuity lead.

## Operator Links
- Wave 30 next-run kit: `ops/r005-next-run-kit-wave30.md`
- Wave 29 rollup: `ops/r005-watchdog-rollup-wave29.md`
- Execution template: `ops/r005-watchdog-template-wave27.md`
