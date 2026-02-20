# Operational Logistics of Fabrication War

## Premise
In this setting, logistics is not merely moving ammunition; it is maintaining **conversion flow** (feedstock -> energy -> validated template -> deployable system). Armies fail when any one of these four flows desynchronizes.

Linked docs: [Fabrication Systems Architecture](./fabrication-systems.md), [Fabricator Class Taxonomy](./fabricator-classes.md), [Faction Failure Modes](../factions/failure-modes-and-escalation.md).

Lock note: uses canonical class ladder **Class 4 -> Class 3 -> Class 2 -> Class 1**.

---

## The Four-Flow Model

### A. Matter Flow
- Ore, salvage, organics, and rare isotopes from extraction zones.
- Measured in **combat-equivalent mass-hours** (CEMh), not raw tonnage.
- Salvage quality grading determines usable yield; battlefield contamination can cut yield by 30–60%.

### B. Energy Flow
- Continuous power quality is more critical than peak wattage.
- Brownouts corrupt long-cycle builds and induce microfractures.
- Energy rationing politics often trigger civilian unrest before frontline collapse.

### C. Authority Flow
- Signed templates, release keys, legal waivers, and doctrine updates.
- Delay here causes units to fight with outdated fits while enemy iterates.
- Over-centralized authority creates brittle command latency.

### D. Distribution Flow
- Delivery of completed systems + spare modules to operating units.
- Vulnerable to route interdiction and load-priority corruption.
- Last 100 km is often autonomous and therefore hack-susceptible.

---

## Throughput Math Used by Planners

### Tactical Replacement Interval (TRI)
Average hours required to restore a formation to 85% combat readiness after major contact.

### Fabrication Attrition Differential (FAD)
Difference between losses per day and replacement-equivalent output per day.
- Positive FAD: force shrinks regardless of tactical wins.
- Negative FAD: force can absorb setbacks and maintain initiative.

### Validation Debt Index (VDI)
Accumulated unverified output percentage.
- VDI > 18% correlates with sudden failure cascades during extreme maneuver operations.

---

## Logistics Echelons

### Echelon 1: Contact Zone
- Class 4 stitchers and scavenger drones.
- Objective: keep squads operational through short-cycle repairs.
- Typical failure: poisoned salvage entering local feedstock.

### Echelon 2: Mobile Sustainment Belt
- Class 3 forge carriers plus convoyed power/coolant.
- Objective: restore battalion/brigade combat systems.
- Typical failure: ambush and signal spoofing on autonomous convoys.

### Echelon 3: Theater Industrial Core
- Class 2 bastion fabs with rail/orbital links.
- Objective: maintain campaign-level replacement and upgrade tempo.
- Typical failure: labor strikes + cyber queue poisoning.

### Echelon 4: Strategic Mobility Layer
- Class 2 strategic seedyards and deep-route transport.
- Objective: reinforce or evacuate theaters.
- Typical failure: transfer bottleneck and orbital denial.

### Echelon 5: Sovereign Regeneration Layer
- Class 1 genesis stacks.
- Objective: regenerate national war capacity after major damage.
- Typical failure: legitimacy fracture in release-key governance.

---

## Common Constraint Regimes

1. **Coolant Poverty Regime**
   - Tropical/low-water worlds hit thermal ceilings first.
   - Leads to rotating shutdown schedules and black-market coolant theft.

2. **Rare-Earth Denial Regime**
   - Guidance/sensor quality collapses despite high gross output.
   - Armies compensate with volume fire and lower-precision doctrine.

3. **Authority Fragmentation Regime**
   - Competing regional commanders issue incompatible templates.
   - Friendly systems lose interoperability over 2–4 weeks.

4. **Transit Attrition Regime**
   - Logistics routes lose >20% volume en route.
   - Forces local cannibalization, accelerating mechanical decay.

---

## Anti-Logistics Warfare Patterns
- **Queue Flooding:** Fake high-priority repair tickets delay genuine critical builds.
- **Spec Drift Attacks:** Subtle changes to fasteners/seals causing delayed failure.
- **Convoy Echo Spoofing:** Autonomous trucks diverted into kill boxes.
- **Credential Harvesting:** Capture of release officers to force CRK approvals.

Countermeasures are doctrinally distributed across factions; see [Doctrine & Command](../factions/doctrine-and-command.md).

---

## Civil-Military Coupling
Fabrication wars erase the old rear/front distinction. Civilian industry is continuously converted, then partially restored.

**Political implications**
- Civilian deprivation windows longer than 21 days produce support collapse in democracies.
- Authoritarian systems can sustain longer deprivation but face sabotage and silent work slowdowns.
- Corporate polities maintain service continuity but lose legitimacy quickly if contract protections fail.

---

## Campaign End Conditions (Logistics-Based)
A theater is effectively lost when two or more of the following persist >14 days:
- TRI exceeds 96 hours.
- FAD remains positive across three consecutive operational cycles.
- VDI exceeds 20% and rising.
- Distribution flow drops below 65% of planned demand.

At this point, tactical brilliance cannot compensate for structural throughput failure.
