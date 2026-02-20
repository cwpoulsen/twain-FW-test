# Continuity Guard Grep Recipes v1

Purpose: fast, repeatable scans for lock drift before/after any major content wave.

Run from repo root:

```bash
# 0) Suggested scope (exclude git + backups)
SCAN_PATHS="canon characters factions locations ops scenes series tech timeline"
EXCLUDES="--exclude-dir=.git --exclude-dir=ops/agent-backup-2026-02-19"
```

## A. Naming + Identity Locks

```bash
# A1. Deprecated faction naming residue
grep -RIn $EXCLUDES -E "\bBelters\b|Solar Defense Force" $SCAN_PATHS

# A2. Required proper-name lock presence
grep -RIn $EXCLUDES -E "Asterion League" canon factions series timeline ops tech
```

## B. Causality Locks

```bash
# B1. AI acquisition timing (should be opening spec-op, not databank first acquisition)
grep -RIn $EXCLUDES -E "databank raid.*(acquire|recovers?).*(AI seed|AI system|AI seed/system)" $SCAN_PATHS

# B2. Positive lock phrase checks
grep -RIn $EXCLUDES -E "opening spec-ops extraction.*AI seed/system|databank raid.*training/upgrade" canon series timeline ops
```

## C. Pursuit / Knowledge Bounds

```bash
# C1. Forbidden certainty framing
grep -RIn $EXCLUDES -E "exact position known|always knows? (their|its) position|perfect tracking" $SCAN_PATHS

# C2. Required bounded pursuit framing
grep -RIn $EXCLUDES -E "unknown current location|probabilistic dragnet|missing asset" canon series ops
```

## D. Physics + Warform Locks

```bash
# D1. Low-g realism anti-pattern cues
grep -RIn $EXCLUDES -E "normal walking|earthlike gravity firefight|stood firm without anchoring" $SCAN_PATHS

# D2. Required low-g lock cues
grep -RIn $EXCLUDES -E "anchoring|attitude control|recoil" canon series ops tech

# D3. Warform agency lock cues
grep -RIn $EXCLUDES -E "non-conscious human puppets|full override|remote warform" canon ops factions series
```

## E. Fabrication Ladder Locks

```bash
# E1. Fabrication lock presence
grep -RIn $EXCLUDES -E "Blackfly.*Class 2|Asterion League.*Class 1|Class 3/4" canon tech factions series ops

# E2. Taxonomy drift hints
grep -RIn $EXCLUDES -E "Class-0|Class 0|Class IV" tech canon factions series
```

## Triage Rule
- Hits in policy/checklist/history files can be valid.
- Hits in canon/series/timeline/scenes are presumed violations until reviewed.
- Any confirmed violation must be logged in `ops/continuity-holes-register-v1.md` with severity + patch note.
