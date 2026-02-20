# Strategy Control Log

Purpose: Keep a living strategy record for the autonomous bible-build pipeline.
Rule: Before spawning any new subagent wave, read the latest entries in this file and apply them to prompts/task design.

---

## 2026-02-19T19:23-05:00 — Strategy Baseline v1

### Objective State
- Build toward 250,000+ words without quality collapse.
- Maintain continuity under rapid parallel expansion.
- Integrate new canon injections fast (AI seed, Asterion League, fab ladder, 10-book arc, fusion/transit realism).

### What Is Working
1. **Parallel wave model** (3 focused runs per wave) is producing fast coverage.
2. **Early continuity ops layer** prevented drift from becoming unmanageable.
3. **Explicit pass structure** (coherence, consequence, tone) is improving quality over time.
4. **Commit-gated integration** keeps the repo auditable and recoverable.

### What Is Not Working / Risks
1. **Throughput > depth risk:** rapid generation can create polished-but-thin sections.
2. **Terminology drift risk:** faction/class names can fork when prompts are broad.
3. **Math-realism fragility:** propulsion/trajectory assumptions can desync across docs.
4. **Voice inconsistency:** sections written by different runs can feel stylistically uneven.

### Strategy Pivots (Apply Immediately)
1. **Prompt with lock headers:** every new run starts with current canon lock bullets.
2. **Use authority anchors:** each run names source-of-truth docs to obey first.
3. **Demand cross-links:** all new docs must cite affected canon/timeline refs.
4. **Require contradiction check section** in each run’s output summary.
5. **Alternate expansion and rewrite waves** to prevent debt buildup.

### Next-Cycle Plan
- Wave focus: naming propagation + quantified transit tables + tone pass.
- Then: scene packs tied to mission bank + pass 4 specificity/novelty + pass 5 clarity/compression.

### Operator Checklist Before Spawning New Subagents
- [ ] Read latest 2 entries in this file
- [ ] Include canon locks in prompt
- [ ] Include authority files to reference
- [ ] Require continuity-impact notes in output
- [ ] Require commit + word count + files list
