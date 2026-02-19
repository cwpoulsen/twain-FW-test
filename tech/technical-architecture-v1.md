# Stewards of Progress — Technical Architecture v1

Status: **Hard-SF systems baseline (2055)**  
Purpose: constrain plot decisions through explicit engineering and logistics rules.

---

## 1) Propulsion and Transit

## 1.1 Propulsion stack
- **Chemical launch systems:** required for all atmospheric ascent/descent in meaningful gravity wells.
- **Fusion drives:** primary inter-orbital and interplanetary propulsion once clear of atmosphere.

## 1.2 Fusion drive envelope (soft numeric baseline)
- Operational acceleration profile usually constrained by crew survivability and fuel economy, not theoretical peak.
- Typical military cruise doctrine:
  - acceleration burn window,
  - flip-and-decelerate profile,
  - reserve margins for evasive vectoring.
- Water feedstock cracking and reaction-mass management are central mission constraints.

## 1.3 Consequences
- Launch windows and transfer trajectories are strategic assets.
- Vessels that burn hard for schedule lose contingency options.
- Transit time asymmetry creates command ambiguity and brittle synchronization.

---

## 2) Communications and Control-Latency

## 2.1 Backbone model
- Interplanetary comms rely on relay mesh + directional laser links + delay-tolerant packet routing.
- No instantaneous synchronization across Earth–Belt theater.

## 2.2 Governance consequence
- Consensus cognitive-shaping fidelity degrades with latency and intermittent connectivity.
- Earth command often acts on stale state estimates when engaging Belt crises.

## 2.3 Operational consequence
- Tactical units must execute with mission-command autonomy despite authoritarian doctrine.
- “Real-time omniscience” is propaganda myth; fog of war is structural.

---

## 3) Fabrication Infrastructure

## 3.1 Class map (locked)
- Class 4: heavy industrial parts and bulk structures.
- Class 3: mainstream electronics.
- Class 2: advanced chips, molecular medicine, superconductive strategic components.
- Class 1: AGI-capable quantum compute chip fabric (black-tier secrecy).

## 3.2 Manufacturing geopolitics
- Belt can sustain broad infrastructure with Class 3/4 ecosystems.
- Belt cannot fully sovereignize high-end computation/biomedical stacks without Class 2 access.
- Earth cannot sustain industrial scale without Belt extraction throughput.

## 3.3 Failure modes for story
- Sabotage of calibration libraries can silently poison fab outputs.
- Feedstock purity variance can force cascading quality defects.
- Firmware lockouts are often more decisive than physical plant destruction.

---

## 4) Military Systems (EDF Marine Context)

## 4.1 Governor module architecture (core behavior)
- Marines carry embedded compliance governor.
- Module enforces hard limits on refusal/disobedience pathways.
- Hard-kill response exists for boundary breach.

## 4.2 Practical envelope
- Module does not micromanage every action; it constrains disallowed classes of behavior.
- Units retain local initiative necessary for survival in high-latency combat.
- This creates moral dissonance: tactical freedom inside strategic enslavement.

## 4.3 Powered armor constraints
- Armor provides force multiplication but is not invulnerability.
- AP munitions, exploit payloads, and system-level sabotage can neutralize armor advantages rapidly.
- Degraded armor radically increases casualty risk and psychological collapse probability.

---

## 5) Habitat and Ship Systems

## 5.1 Belt habitat baseline
- Mixed architecture: spin-gravity drums, anchored industrial stations, modular tunnel/rock habitats.
- Radiation shielding quality varies by wealth and mission criticality.

## 5.2 Life support economics
- Air, water, thermal control, and seal integrity are currency-equivalent assets.
- Conflict targeting life support is strategically effective but politically catastrophic.

## 5.3 Ship maintenance reality
- Maintenance debt is unavoidable; field repairs are doctrine, not exception.
- Crews who can merge mechanical improvisation with software adaptation survive disproportionally.

---

## 6) Medical Stratification

## 6.1 Public tier
- Broad access to baseline molecularly fabricated medicines for common disease/injury management.

## 6.2 Restricted tier
- Performance enhancement, accelerated healing, and longevity interventions exist but are heavily rationed by status/access control.

## 6.3 Social consequences
- Elite longevity compounds political continuity and suppresses leadership turnover.
- Trauma medicine inequity shapes loyalty, resentment, and black-market demand.

---

## 7) Security and Cyber Reality

## 7.1 Consensus-era weakness pattern
- Many systems prioritize compliance reporting optics over resilient segmentation.
- Centralized trust roots create high-value exploit chains.

## 7.2 Tactical exploit doctrine
- Attacks on identity/authentication layers often outperform brute-force hardware attacks.
- Legacy compatibility systems are frequent breach points.

## 7.3 Narrative discipline
- Hacking events must include setup cost, access path, and side effects.
- No “magic terminal solves everything” beats.

---

## 8) Hard Constraints Checklist for Any Scene

1. Where is the ship/habitat physically, and what delta-v/fuel state applies?  
2. What comm latency applies to command updates?  
3. Which fabrication class can actually produce required parts?  
4. What life-support and maintenance debt limits current options?  
5. What governor-module boundaries shape marine choices?  
6. What technical side effect follows the chosen workaround?

If a scene cannot answer these, it is under-specified.
