# Stewards of Progress — Governor Module Autonomy Bands v1

Status: **Locked-SOFT operational constraint table**  
Purpose: define allowed marine autonomy by mission state without hand-wavy overrides.

Cross-refs:
- Canon ledger: `canon/canon-ledger-v2.md` (§8)
- Continuity patch: `canon/continuity-patch-wave3-v1.md`
- Technical architecture: `tech/technical-architecture-v1.md`

---

## 1) Control-State Bands

| Band | Mission State | Allowed Autonomy | Hard Prohibitions | Typical Enforcement |
|---|---|---|---|---|
| **G0 Compliance Idle** | Transit / garrison / staging | Routine tactical discretion; self-preservation allowed | Desertion prep, cryptographic tamper, unsanctioned external intel exchange | Warning cascade -> mobility dampening |
| **G1 Active Ops** | Authorized combat mission | Local maneuver and target sequencing within ROE | Refusal of mission objective, chain-of-command spoofing | Neuro-pain spike + actuator lock windows |
| **G2 Priority Override** | Command-critical operation | Narrow objective optimization only | Objective abandonment, protected-target violation exceptions | Motor inhibition + cognition suppression bursts |
| **G3 Counter-Defection** | Suspected disobedience/flight | Minimal autonomy; mostly execution under constraint | Route deviation, unapproved docking, comm blackout creation | Full-lock posture + armed escort beaconing |
| **G4 Terminal Sanction** | Confirmed hard breach | No meaningful autonomy | Any resistance | Lethal enforcement path (hard kill) |

---

## 2) Trigger Logic (Narrative-Usable)

| Trigger Type | Typical Band Escalation | Notes |
|---|---|---|
| Missed command acknowledgment beyond latency allowance | G0 -> G1 | Must include comm-latency context |
| Repeated route divergence with no hazard declaration | G1 -> G2 | Requires route telemetry evidence |
| Verified tamper attempt on governor bus | Any -> G3 immediately | No warning required |
| Refusal at lethal command checkpoint | G2/G3 -> G4 | Requires dual-signature or authenticated emergency doctrine token |

---

## 3) Autonomy Envelope Constraints

1. Module constrains **classes of forbidden action**, not every movement decision.
2. Marines can improvise tactics inside band limits, especially under comm delays.
3. Escalation to G4 must leave audit artifacts (time stamp, authority signature, local telemetry digest).
4. Repeated high-band operation creates measurable neurocognitive degradation risk in 30–90 day windows.

---

## 4) Scene Header Add-On (required for governor-relevant scenes)

- `governor_band_at_scene_start:`
- `band_change_events:`
- `authority_token_source:`
- `audit_artifact_location:`

If absent, governor-module behavior is continuity-incomplete.
