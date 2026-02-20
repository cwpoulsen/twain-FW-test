# Book Bible Pass Log

## 2026-02-19 — Rewrite Pass 1 (Coherence Pass)

### Objective
Run coherence-focused rewrite across core docs to remove terminology conflicts, align faction/tech doctrine with locked canon, and tighten cross-file authority without reducing setting depth.

### High-Impact Contradictions Resolved
1. **Fabricator class-number drift**
   - Problem: some tech docs used Class-0→IV ladder while canon lock uses Class 4→1.
   - Resolution: normalized all class semantics to Class 4/3/2/1; retained prior useful topology detail as deployment-form language rather than class labels.

2. **Faction identity drift**
   - Problem: several faction docs referenced alternate bloc names (CIS/DHE/etc.) incompatible with Steward/Consensus/Earth-Belt canon.
   - Resolution: rewrote faction references to canonical actor set: Steward Directorate, Consensus Operations Complex, EDF Command, Belt Municipal Compacts, Belt Autonomist Fronts, Predatory Belt Actors.

3. **Authority ambiguity across early discovery docs**
   - Problem: draft-era worldbuilding doc could be interpreted as equal authority to locked files.
   - Resolution: added explicit supersession/authority map in series discovery doc and crosslinks from canon/timeline/character files.

### Files Edited
- `tech/fabricator-classes.md` (major rewrite)
- `tech/fabrication-systems.md` (major rewrite)
- `factions/major-factions.md` (major rewrite)
- `factions/doctrine-and-command.md` (major rewrite)
- `series/worldbuilding-core-pack-v1.md` (authority/supersession annotation)
- `canon/canon-ledger-v2.md` (coherence-pass reference anchor)
- `timeline/master-timeline-sequence-v1.md` (class/faction nomenclature alignment note)
- `characters/core-squad-depth-pack-v1.md` (timeline index continuity note)

### Rationale Pattern Used
- Prefer **relabel + structural clarification** over content deletion.
- Preserve tactical/story utility details by moving them into canon-compatible categories.
- Add explicit file authority hierarchy to prevent future contradiction reintroduction.

### Net Coherence Outcome
- Terminology and actor model now match locked canon across the six requested domains (canon/tech/factions/series/timeline/characters).
- Cross-file references should now be safer for downstream scene generation and additional passes.
