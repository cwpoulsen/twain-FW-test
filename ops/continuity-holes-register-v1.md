# Continuity Holes Register v1 (Wave 2)

Status: active continuity audit ledger  
Owner: bible maintenance pass  
Last updated: 2026-02-19

Cross-refs:
- Dependency map: `ops/continuity-dependency-map-v1.md`
- Scanner checklist: `ops/contradiction-scanner-checklist-v1.md`
- Canon patch set: `canon/continuity-patch-wave2-v1.md`
- Master timeline authority: `timeline/master-timeline-sequence-v1.md`

---

## Severity Key
- **P0:** breaks causality or core arc readability now
- **P1:** high drift risk across books if unresolved
- **P2:** quality/clarity gap; does not yet break canon

---

## Hole Ledger

| Hole ID | Severity | Type | Problem Statement | Affected Docs | Resolution Status |
|---|---|---|---|---|---|
| H-001 | P0 | Sequence contradiction | Book 1 scaffold placed databank corruption reveal before betrayal confirmation, while locked timeline had betrayal/escape before databank raid event. | `series/book-and-series-arc-scaffolds-v1.md`, `timeline/master-timeline-sequence-v1.md`, `timeline/character-arc-turning-points-v1.md` | **FIXED** via canon chronology lock + scaffold retune |
| H-002 | P0 | Character-arc timing conflict | Valerie brother thread timing conflicted between Book 1 late-turn cues and Book 2 reveal architecture. | `characters/core-squad-depth-pack-v1.md`, `series/book-and-series-arc-scaffolds-v1.md`, `timeline/character-arc-turning-points-v1.md`, `characters/valerie-brother-reveal-blueprint-v1.md` | **FIXED** by defining Book 1 = signal seed only; Book 2 = pre-reveal and full reveal |
| H-003 | P1 | Mechanism gap | Unknown intervention during Blackfly escape lacked hard comms/latency/corridor mechanism, risking “plot magic.” | `timeline/master-timeline-sequence-v1.md`, `canon/continuity-patch-wave2-v1.md`, `tech/technical-architecture-v1.md` | **FIXED (SOFT->LOCKED-SOFT)** corridor-window mechanism + delayed packet model |
| H-004 | P1 | Identity chain ambiguity | Unknown helper identity and trust chain lacked rules, risking arbitrary rescue repetition. | `canon/continuity-patch-wave2-v1.md`, future scenes | **PARTIAL** helper remains intentionally unnamed; use-of-intervention now constrained by rule set |
| H-005 | P2 | Evidence chain fragility | “Shadow truth ledger” existed conceptually but lacked canon-level audit requirements for admissible proof. | `timeline/character-arc-turning-points-v1.md`, `canon/continuity-patch-wave2-v1.md` | **FIXED** via evidence continuity requirements |

---

## Fixed-in-Wave2 Summary
1. Book 1 chronology is now unambiguous: betrayal/escape first, databank raid later under free-team conditions.
2. Valerie brother continuity now clean: seed in Book 1, pressure + reveal in Book 2.
3. Intervention mechanics constrained by comms windows and pre-positioned exploit work, not omniscient realtime control.
4. Evidence continuity now requires chain-of-custody metadata and mirrored logs before major information-war beats.

---

## Remaining Risks (next pass)
1. **R-001 (P1):** Need explicit travel-time matrix by lane and burn class to prevent tactical teleport effects.
2. **R-002 (P1):** Need governor-module firmware constraints table (allowed autonomy bands per mission state).
3. **R-003 (P2):** Need standardized scene header schema enforcing sequence index + local timestamp + comms latency note.
4. **R-004 (P2):** Need recurring antagonist adaptation cadence table (Kite counter-evolution per major contact).
