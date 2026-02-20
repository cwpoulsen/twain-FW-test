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
   - Resolution: rewrote faction references to canonical actor set: Steward Directorate, Consensus Operations Complex, EDF Command, Belt Municipal Compacts, Asterion League, Predatory Belt Actors.

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

---

## 2026-02-19 — Rewrite Pass 2 (Consequence Pass) + Curveball Canon Lock

### Objective
Integrate user-issued canon changes while preserving consequence discipline: (1) raid box now contains new AI seed/system, (2) named Belt anti-Consensus faction with Class 1 breakthrough, (3) Blackfly Class 2 fabricator lock, (4) long arc extended to ~10 books with slow reconquest, (5) quantified fusion/transit assumptions with equations + travel-time tables.

### Canon Locks Added
1. **Databank raid payload elevation**
   - `scenes/databank-raid-ashes-in-the-box-v1.md` and `timeline/master-timeline-sequence-v1.md` now explicitly lock the box as a new AI seed/system artifact.
   - Consequence: box custody now drives multi-faction strategic behavior beyond Book 1.

2. **Named anti-Consensus Belt faction + Class 1 creation**
   - Proper-name lock: **Asterion League** (with Asterion Concord as flagship technical wing).
   - Updated in `factions/major-factions.md`, `factions/factions-doctrine-ledger-v1.md`, `factions/doctrine-and-command.md`, `canon/canon-ledger-v2.md`, and timeline sequence events.
   - Consequence: Earth monopoly certainty over Class 1 is broken; deterrence/escalation logic shifts from suppression to replication-control conflict.

3. **Blackfly Class 2 fabricator lock**
   - Added to `tech/fabricator-classes.md`, `canon/canon-ledger-v2.md`, and timeline entry `0200`.
   - Consequence: squad transitions from pure fugitive cell to strategically targeted fabrication actor.

4. **Long-arc extension to ~10 books**
   - `series/book-and-series-arc-scaffolds-v1.md` and `series/series-architecture-v2.md` now include Books 5–10 reconquest/reintegration spine.
   - `timeline/master-timeline-sequence-v1.md` adds long-horizon reconquest arc window.

5. **Hard-SF propulsion/travel quantification**
   - New file: `tech/fusion-transit-assumptions-and-lane-calculus-v1.md` with assumptions table, equations, lane distances, transfer-time table, and continuity usage rules.
   - Linked via `tech/technical-architecture-v1.md` and `ops/timeline-policy.md`.

### Continuity Conflicts Fixed
- Removed inconsistent faction naming drift by standardizing on **Asterion League** references.
- Rebuilt `timeline/master-timeline-sequence-v1.md` to eliminate duplicate sequence IDs and conflicting long-arc entries.
- Re-pointed canonical transport references to existing quantitative transit file.

### Files Added
- `tech/fusion-transit-assumptions-and-lane-calculus-v1.md`

### Files Updated
- `canon/canon-ledger-v2.md`
- `scenes/databank-raid-ashes-in-the-box-v1.md`
- `factions/major-factions.md`
- `factions/factions-doctrine-ledger-v1.md`
- `factions/doctrine-and-command.md`
- `tech/fabricator-classes.md`
- `tech/technical-architecture-v1.md`
- `series/book-and-series-arc-scaffolds-v1.md`
- `series/series-architecture-v2.md`
- `timeline/master-timeline-sequence-v1.md`
- `ops/timeline-policy.md`
- `ops/book-bible-pass-log.md`

---

## 2026-02-19 — Rewrite Pass 3 (Voice/Tone Pass, Wave 5)

### Objective
Replace generic phrasing with specific military-sci-fi diction across high-impact canon/series/tech/factions/characters documents while preserving locked causality, class constraints, and previously patched canon.

### Voice/Tone Strategy Applied
- Swapped abstract governance language for concrete control mechanics (queues, signatures, chokepoints, after-action narrative control).
- Increased operational texture (duty-cycle repair tempo, soft blockade dynamics, burn-window costs, deconfliction constraints).
- Tightened character/faction phrasing toward doctrine-and-consequence framing rather than broad descriptors.
- Preserved all hard locks: AI-seed box, Asterion League Class 1 breakthrough, Blackfly Class 2 constraint, no-FTL/transit envelope, long-arc (~10 books) escalation logic.

### Files Updated
- `canon/canon-ledger-v2.md`
- `series/series-architecture-v2.md`
- `tech/fabricator-classes.md`
- `tech/interplanetary-transit-and-comms-envelope-v1.md`
- `factions/doctrine-and-command.md`
- `factions/factions-doctrine-ledger-v1.md`
- `characters/core-squad-depth-pack-v1.md`
- `ops/book-bible-pass-log.md`

### Rationale Notes
- **Canon ledger:** reinforced regime-control specificity without altering authority structure or causality chain order.
- **Series architecture:** increased tonal sharpness in thesis/constraints while keeping anti-miracle and consequence laws intact.
- **Fabricator taxonomy:** converted neutral technical prose into theater-relevant stakes language; class definitions unchanged.
- **Transit/comms envelope:** maintained equations/tables exactly; improved operational wording for continuity enforcement.
- **Faction doctrine docs:** shifted from generic institutional phrasing to command-friction language tied to battlefield outcomes.
- **Core squad depth pack:** tuned role descriptors and shared emotional engine to sound like field-unit doctrine under coercive command conditions.

### Net Outcome
Pass 3 voice profile now reads more like an operational war-bible: specific, textured, and consequence-aware, with no canon drift introduced.
