# Fabrication Systems Architecture (Coherence Pass 1)

Status: **Canon-aligned systems reference**  
Continuity links: `tech/fabricator-classes.md`, `tech/operational-logistics.md`, `factions/factions-doctrine-ledger-v1.md`.

---

## Purpose in Setting
In *Stewards of Progress*, strategic dominance is governed by **throughput authority**: who can reliably convert feedstock, energy, and trusted templates into deployable capability under latency, sabotage, and political stress.

Fabrication is therefore not just industry; it is sovereignty infrastructure.

---

## 1) Core Stack

### 1.1 Feedstock Intake
- Ore, scrap, polymer waste, and reclaimed structural composites enter assay/sorting loops.
- Battlefield salvage is valuable but contamination-prone.

**Constraints**
- Isotopic impurity and nanite residue can silently poison high-stress components.
- Water/hydrogen balance limits sustained output in dry theaters.

### 1.2 Energy Envelope
- Fusion generation enables high baseline power, but local stability is still fragile.
- Power spikes, thermal limits, and coolant loss cause throughput collapse before feedstock exhaustion.

### 1.3 Design Authority Layer (DAL)
- Controls template lineage, signing, release policy, and legal accountability.
- Operationally, DAL is the bridge between politics and machines.

**Key mechanisms**
- Template provenance registry.
- Quorum-gated release keys.
- Safety envelopes and forensic trace markers.

### 1.4 Execution Layer
- Macro-additive structures (hulls, habitat shells, armor frames).
- Electronics fabrication (within class limits).
- Precision machining and molecular synthesis where authorized.

### 1.5 Validation/Hardening
- Stress testing, EMI hardening, material scans, destructive sampling.
- Under crisis tempo, factions that bypass this gain short-term surge and long-term collapse risk.

---

## 2) Canon Class Coupling

Fabrication classes are fixed to canon definitions:

- **Class 4:** heavy industrial backbone.
- **Class 3:** general electronics tier.
- **Class 2:** strategic precision (advanced chips, molecular meds, superconductive components).
- **Class 1:** AGI bottleneck fabrication.

Important: class label describes capability/governance tier, not facility size. A small facility may still be class-gated by template authority.

---

## 3) Control Concepts

### Throughput Sovereignty
A polity is only truly sovereign if it controls enough class access + DAL authority to arm and repair itself without hostile keyholders.

### Blue Delay
Time from approved design to fieldable lot.
- < 6h: tactical adaptation possible.
- > 48h: doctrine calcifies; adversary can out-cycle you.

### Ghost Capacity
Dormant lines and covert queue reserves that can be activated for strategic surprise.

---

## 4) Earth-Belt Implication Layer

- Belt can sustain wide autonomy with Class 4/3 ecosystems.
- Earth retains leverage by controlling Class 2 distribution and concealing Class 1 reality.
- As comm latency grows, Earth control shifts from direct behavioral steering to queue pressure, sanctions, and narrative shaping.

---

## 5) Recurring Vulnerabilities

| Attack surface | Immediate effect | Delayed effect | Typical countermeasure |
|---|---|---|---|
| DAL key compromise | Unauthorized production | Fleet-wide latent defects | Quorum rotation + segmented signing |
| Feedstock contamination | Scrap spikes | fatigue-failure cascades | Multi-stage assay + quarantine loops |
| Grid/coolant disruption | Throughput halt | thermal hardware damage | segmented microgrids + reserve sinks |
| Queue spoofing | Priority starvation | political legitimacy fracture | authenticated scheduling + independent audit |
| Validation bypass | rapid output surge | combat reliability collapse | randomized destructive testing |

---

## 6) Story-Use Rules

1. No fabrication miracle without feedstock, power, and queue source.
2. Any major output jump must show corresponding governance permission (or breach).
3. Sabotage should have technical signatures and downstream consequences.
4. Production success in one area should create cost or scarcity elsewhere.