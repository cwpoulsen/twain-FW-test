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

---

## 2026-02-19 — Rewrite Pass 4 (Specificity/Novelty Pass, Wave 6)

### Objective
Replace generic worldbuilding language with concrete, distinctive, causally-grounded detail in high-impact canon/factions/tech/series/characters docs, while preserving all locked canon constraints and taxonomy.

### Canon-Lock Preservation Check (pre-edit guardrails)
- Preserved: AI seed payload in liberated box (no alterations to payload ontology).
- Preserved: **Asterion League** naming and Belt-side Class 1 capability.
- Preserved: **Blackfly** constrained Class 2 capability.
- Preserved: ~10-book reconquest arc (Books 5–10 continuity intact).
- Preserved: fusion/transit realism constraints (M2 default, no FTL, burn/comms/fuel consequences retained).

### Files Updated (Pass 4)
- `canon/earth-consensus-daily-life-and-legal-architecture-v1.md`
- `factions/doctrine-and-command.md`
- `tech/fusion-transit-assumptions-and-lane-calculus-v1.md`
- `series/series-architecture-v2.md`
- `characters/core-squad-depth-pack-v1.md`
- `ops/book-bible-pass-log.md`

### Rationale Pattern Used
1. **Numerical concretization:** replaced abstract claims ("standardized", "delays", "expensive") with plausible ranges, windows, and operational thresholds.
2. **Mechanism-first causality:** tied social or strategic outcomes to explicit mechanisms (queue bands, signature authority, maintenance debt, reserve floors).
3. **Distinctive institutional texture:** introduced setting-specific process artifacts (objective packets, two-key mission unlocks, reserve SLAs) instead of generic dystopian phrasing.
4. **Character operational fingerprints:** converted personality-level tactical patterns into repeatable, scene-usable behaviors under pressure.

### Before/After Examples
1. **Canon (daily life controls)**
   - Before: "Units are climate-stable, clean, and highly standardized."
   - After: "Most MCC blocks are 18-floor slabs with 42m² family units... corridor cameras every 12 meters..." 
   - Effect: turns ambiance into an enforceable surveillance-and-gathering constraint.

2. **Factions (command mechanics)**
   - Before: "Class-2 access decisions act as coercive diplomacy."
   - After: "Class-2 queue tickets... grant 72-hour priority to allies, push rivals into 30-60 day slip bands."
   - Effect: makes coercion measurable and plot-drivable.

3. **Tech (transit consequences)**
   - Before: "Rapid strike is expensive... creates mandatory maintenance debt."
   - After: "each BC-C leg typically burns ~1.3-1.6x BC-B propellant... forces 18-36 hours dockside maintenance..."
   - Effect: converts hand-wave cost into concrete campaign tempo constraints.

4. **Series (escalation specificity)**
   - Before: "Internal Steward factions split over Consensus succession strategy."
   - After: named bloc split (Continuity / Reconciliation / Security) with incompatible succession doctrines.
   - Effect: enables causally distinct political maneuvers instead of abstract "elite fracture" beats.

5. **Characters (tactical behavior)**
   - Before: "Stabilize immediate casualties."
   - After: "tourniquet/airway/pressure integrity in first 90 seconds..."
   - Effect: gives consistent action grammar for scene-level authenticity.

### Contradiction Check (Pass 4)
- **Fabricator taxonomy drift:** none detected (Class 4/3/2/1 unchanged).
- **Faction naming drift:** none detected (Asterion League naming preserved).
- **AI payload drift:** none detected (still AI seed/system in box).
- **Arc horizon drift:** none detected (10-book reconquest framing retained).
- **Transit realism drift:** none detected (M2 default + comm-light constraints preserved; added costs are refinements, not model changes).

### Net Outcome
Pass 4 increases uniqueness and causal precision without changing locked strategic facts. Documents now provide clearer scene-building hooks (numbers, thresholds, procedural artifacts, and decision costs) and reduce recurrence of generic "control-state" language.

---

## 2026-02-19 — Rewrite Pass 5 (Clarity/Compression, Wave 7)

### Objective
Tighten high-impact docs by removing repetition, sharpening ambiguous phrasing, and propagating lock language for: post-EDF free-operator status, AI acquisition/databank split, Asterion League naming, staged Class2->Class1 fabrication path, 10-book reconquest, unknown-position Blackfly after nuke masking, warform doctrine, and small-body anchoring physics.

### Files Updated
- `canon/canon-ledger-v2.md`
- `canon/continuity-patch-wave3-v1.md`
- `series/series-architecture-v2.md`
- `series/reconquest-institutional-integration-matrix-v1.md`
- `tech/technical-architecture-v1.md`
- `factions/freed-voider-bands-dossier-v1.md`
- `characters/character-interaction-pressure-tests-v1.md`
- `ops/book-bible-pass-log.md`

### Rationale Pattern Used
1. **Compression by lock bundles:** replaced repeated 7-bullet continuity blocks with one-line hard-assumption bundles where docs already had full authority references.
2. **Ambiguity removal:** standardized pursuit phrasing to “missing asset, unknown current position, probabilistic dragnet.”
3. **Causality correction:** fixed acquisition sequence drift by splitting AI first-acquisition (opening spec-op) from databank training/provenance value.
4. **Mechanics enforcement language:** inserted direct warform and small-body physics phrasing in tech/series/canon control points.

### Before/After Examples
1. **Acquisition wording fix**
   - Before: “Databank raid recovers a new AI seed/system.”
   - After: “Blackfly acquires a new AI seed/system in the opening spec-ops extraction; databank raid later supplies training/upgrade data.”

2. **Continuity-note compression**
   - Before: repeated 7-bullet lock sections in multiple docs.
   - After: single compressed “Continuity Lock Bundle” paragraph with same constraints and less boilerplate.

3. **Watchlist clarity**
   - Before: contradiction list numbering/order drift (6/7/8 out of order) and mixed phrasing.
   - After: ordered list 1-8 with explicit failure conditions and patch actions.

### Contradiction Check (Pass 5)
- **Post-EDF status drift:** patched; core crew now explicitly permanent free operators after Blackfly theft.
- **AI acquisition timing drift:** patched in canon ledger + continuity patch + series architecture.
- **Faction naming drift:** no new drift; Asterion League naming preserved.
- **Class path drift:** clarified as staged Class3/4 -> Blackfly Class2 -> Asterion Class1; no taxonomy changes.
- **Arc horizon drift:** no drift; 10-book reconquest framing preserved.
- **Pursuit omniscience drift:** patched to unknown-position probabilistic dragnet language.
- **Warform agency drift:** patched; full override treated as non-conscious remote control.
- **Small-body physics drift:** patched with explicit anchoring/attitude-control requirements.

### Word Impact (edited docs)
- `canon/canon-ledger-v2.md`: 991 -> 1073 (**+82**)
- `canon/continuity-patch-wave3-v1.md`: 301 -> 327 (**+26**)
- `series/series-architecture-v2.md`: 1523 -> 1546 (**+23**)
- `series/reconquest-institutional-integration-matrix-v1.md`: 1252 -> 1164 (**-88**)
- `tech/technical-architecture-v1.md`: 1084 -> 1143 (**+59**)
- `factions/freed-voider-bands-dossier-v1.md`: 771 -> 692 (**-79**)
- `characters/character-interaction-pressure-tests-v1.md`: 2641 -> 2523 (**-118**)

**Net across edited canon/series/tech/factions/characters docs:** **-95 words** (clarity gain via compression despite lock-propagation additions).

---

## 2026-02-19 — Targeted Weak-Section Refinement (Specificity/Voice/Coherence Debt, Wave 9)

### Objective
Identify and upgrade the weakest eight docs (highest placeholder density, generic diction, or coherence debt) without taxonomy drift or canon-lock breakage.

### Strategy + Lock Guidance Applied
- Applied Strategy Control Log latest entries: lock-header discipline, authority anchors, contradiction-check requirement, and FVB destabilizer integration.
- Preserved locked assumptions:
  - AI-seed/system acquisition split (opening extraction vs later databank provenance/training value)
  - Asterion League naming + Belt-side Class 1 breakthrough
  - Blackfly constrained Class 2 role
  - 10-book reconquest gradient (no one-battle resolution)
  - no-FTL/fusion-transit consequence discipline
  - unknown-position probabilistic dragnet framing
  - FVB treated as persistent agency-bearing destabilizer ecology

### Weakest 8 Docs Refined
1. `characters/marko-branik-character-bible-v1.md`
2. `characters/lindsay-veil-character-bible-v1.md`
3. `characters/isaac-beckham-character-bible-v1.md`
4. `locations/strategic-theater-atlas-v1.md`
5. `series/books1-4-mission-bank-integration-notes-v1.md`
6. `series/antagonist-learning-loops-and-escalation-branches-books1-4-v1.md`
7. `timeline/books1-10-strategic-reconquest-map-v1.md`
8. `factions/major-factions.md`

### Rationale Pattern Used
1. **Placeholder -> operational behavior:** replaced TBD-heavy framing with scene-usable action fingerprints and failure modes.
2. **Abstract -> mechanism:** converted broad claims into concrete enforcement mechanics (queue warfare, cadence, custody, branch triggers).
3. **Voice sharpening:** shifted phrasing toward war-bible diction (timing, signatures, survivability, coercive process).
4. **Coherence anchoring:** added explicit authority cross-refs and contradiction triggers in-doc.

### Before/After Examples
1. **Character specificity (Marko)**
   - Before: “Open Placeholders (TBD) … specific loadout/weakness/arc target.”
   - After: explicit mechanical-veto authority, stress triggers, scene fingerprints, and Books 1–4 arc spine.
   - Effect: removes template feel; increases deployable scene consistency.

2. **Character voice clarity (Veil)**
   - Before: broad “dreamy shield-maiden mind” + unresolved shield placeholder.
   - After: dual-register voice model, time-band decision horizons, concrete stress-recovery behavior.
   - Effect: preserves concept while grounding in tactical procedure.

3. **Mission integration coherence**
   - Before: generic seed-selection guidance.
   - After: rejection tests for canon breaks (miracle wins, omniscience, FVB episodic misuse, zero-cost success).
   - Effect: lowers downstream continuity debt during scene drafting.

4. **Timeline arc precision (Books 1–10 map)**
   - Before: single “primary arc function” line per book.
   - After: added dominant campaign-cost column, contradiction triggers, and class-path continuity language.
   - Effect: strengthens causality and prevents reconquest hand-waving.

### Contradiction-Check Summary
- **Fabricator taxonomy drift (Class 4/3/2/1):** none introduced.
- **Faction naming drift (Asterion League):** none introduced.
- **AI-seed acquisition/databank timing split:** preserved.
- **Arc horizon drift (10-book reconquest):** preserved.
- **Transit realism/no-FTL envelope drift:** preserved.
- **Pursuit omniscience drift:** guarded against (probabilistic dragnet language retained).
- **FVB handling drift:** improved (persistent ecology + recruitment-funnel logic propagated).

### Net Outcome
The selected eight docs now read as operationally specific and voice-consistent while staying inside locked canon taxonomy and continuity constraints.

---

## 2026-02-19 — Rewrite Pass 6 (Voice Unification Wave 10, Top-12 High-Impact Docs)

### Objective
Unify narrator voice and command-language cadence across the twelve highest-impact canon/series/factions/tech/timeline/character authority docs while preserving all canon locks and authority anchors.

### Top-12 Documents Unified
1. `canon/canon-ledger-v2.md`
2. `canon/continuity-patch-wave3-v1.md`
3. `series/series-architecture-v2.md`
4. `series/book-and-series-arc-scaffolds-v1.md`
5. `factions/factions-doctrine-ledger-v1.md`
6. `factions/doctrine-and-command.md`
7. `tech/technical-architecture-v1.md`
8. `tech/fabricator-classes.md`
9. `tech/interplanetary-transit-and-comms-envelope-v1.md`
10. `timeline/master-timeline-sequence-v1.md`
11. `timeline/books1-10-strategic-reconquest-map-v1.md`
12. `characters/core-squad-depth-pack-v1.md`

### Voice/Style Unification Pattern Applied
1. **Common authority preamble:** inserted `Voice & Authority Lock (Wave 10)` section in each target doc.
2. **Nomenclature lock:** standardized canonical actor set in each file preamble:
   - Steward Directorate
   - Consensus Operations Complex
   - Earth Defense Fleet (EDF)
   - Belt Municipal Compacts
   - Asterion League
3. **Cadence lock:** explicit mechanism -> decision -> cost writing rule to reduce multi-author tonal seams.
4. **Consequence lock:** explicit prohibition on miracle throughput, realtime deep-theater Earth command, and zero-cost victories.

### Concrete Examples
1. **Authority naming alignment**
   - Before (`canon/canon-ledger-v2.md`): “Real authority = Stewards of Earth ...”
   - After: “Real authority = Steward Directorate (\"Stewards of Earth\" in internal shorthand) ...”
   - Effect: keeps in-world shorthand while anchoring the canonical institution name used across docs.

2. **Military institution naming alignment**
   - Before (`factions/factions-doctrine-ledger-v1.md`): “Earth Defense Force (EDF) Command Apparatus”
   - After: “Earth Defense Fleet (EDF) Command Apparatus”
   - Effect: removes Force/Fleet oscillation and prevents faction-level terminology drift.

3. **Cross-domain cadence normalization**
   - Added the same consequence-forward cadence rule to canon, series, factions, tech, timeline, and character docs.
   - Effect: docs now read with one command-brief rhythm instead of mixed academic/template/prose registers.

### Contradiction-Check Summary (Post-Edit)
- **Fabricator taxonomy (Class 4/3/2/1):** unchanged.
- **AI-seed acquisition split (opening extraction vs databank training/provenance):** unchanged.
- **Asterion League naming + Belt Class 1 breakthrough:** preserved.
- **Blackfly Class 2 lock:** preserved.
- **10-book reconquest arc:** preserved.
- **No-FTL / transit-latency constraints:** preserved.
- **Unknown-position probabilistic dragnet framing:** preserved.
- **Warform non-conscious override framing + small-body anchoring realism:** preserved.

### Net Outcome
Top-12 authority docs now share a single military-space-opera command voice with consistent nomenclature and consequence-forward cadence, reducing multi-author seams without canon drift.
