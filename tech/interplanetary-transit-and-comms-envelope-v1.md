# Stewards of Progress — Interplanetary Transit, Fusion Performance & Comms Envelope v2

Status: **Quantitative continuity lock (2055+ theater)**  
Authority: `canon/canon-ledger-v2.md` (§6, §7), `timeline/master-timeline-sequence-v1.md`

Cross-refs:
- `tech/technical-architecture-v1.md`
- `ops/timeline-policy.md`

---

## 1) Physical Assumptions (Locked)

### 1.1 Propulsion model assumptions

| Parameter | Assumption Band | Notes |
|---|---:|---|
| Fusion core thermal-to-jet efficiency, \(\eta_t\) | 0.32–0.48 | Includes reactor + power-conversion + nozzle losses |
| Effective propulsive efficiency, \(\eta_p\) | 0.55–0.72 | Beam/plume + control losses |
| Net mission efficiency, \(\eta = \eta_t\eta_p\) | 0.18–0.35 | Use 0.26 default for planning |
| Exhaust velocity, \(v_e\) | 120–450 km/s | Lower band cargo drives, upper band military torch modes |
| Specific impulse, \(I_{sp}=v_e/g_0\) | ~12,000–46,000 s | Not atmosphere-capable |
| Sustained accel envelopes | 0.005 g to 0.12 g | By burn class, hull and crew limits |

### 1.2 Core equations used in continuity checks

1. **Rocket equation**  
\[\Delta v = v_e \ln\left(\frac{m_0}{m_f}\right)\]

2. **Propulsive power relation** (idealized kinetic jet power)  
\[P_{jet} = \frac{1}{2}\dot{m}v_e^2, \quad P_{reactor} = \frac{P_{jet}}{\eta}\]

3. **Constant-accel half-flip-half-decel estimate** (first-pass transit lower bound)  
\[t_{min} \approx 2\sqrt{\frac{d}{a}}\]

4. **Average transfer planning rule**  
Real mission time = \(t_{min}\) + orbital phasing margin + traffic/stealth/thermal constraints.

---

## 2) Burn Classes and Thrust Profiles

| Burn Class | Sustained Accel | Typical Use | Crew/Hardware Cost |
|---|---:|---|---|
| BC-A Economy | 0.005–0.015 g | Freight, covert drift | Low fatigue, high schedule variance |
| BC-B Balanced | 0.02–0.05 g | Standard military transit | Moderate maintenance burden |
| BC-C Hard Military | 0.06–0.12 g | Time-critical operations | Significant thermal + structural debt |
| BC-D Emergency | 0.13–0.20 g (short windows) | Survival/intercept denial | Major post-burn downtime mandatory |

**Lock:** BC-D is burst-only; cannot be narrative default.

---

## 3) Transfer Trajectories and Travel Times (Key Lanes)

Ranges include favorable/unfavorable geometry, phasing, and operational constraints.

| Lane | Distance basis (AU, variable) | BC-A | BC-B | BC-C | BC-D burst-assisted |
|---|---|---:|---:|---:|---:|
| Earth orbit -> Luna corridor | 0.0026 AU local | 2.5–4.5 d | 1.7–3.0 d | 1.1–2.0 d | 0.8–1.4 d |
| Earth orbit -> Mars transfer | 0.38–2.68 AU geometry span | 85–150 d | 60–110 d | 42–80 d | 33–62 d |
| Earth orbit -> Ceres arc | 1.6–3.9 AU geometry span | 145–240 d | 104–180 d | 75–130 d | 60–102 d |
| Mars high orbit -> Ceres | 0.8–3.4 AU | 58–105 d | 41–76 d | 30–55 d | 24–44 d |
| Ceres -> Vesta/Pallas industrial lanes | 0.35–1.2 AU | 17–36 d | 12–25 d | 8–18 d | 6–14 d |
| Ceres -> inner-belt habitat mesh | 0.12–0.7 AU | 7–20 d | 5–14 d | 3.5–9.5 d | 2.5–7 d |

### 3.1 Trajectory doctrine tags
- **Hohmann-like economy arcs:** BC-A dominant; max payload and stealth.
- **Semi-brachistochrone military arcs:** BC-B/BC-C with strict thermal accounting.
- **Broken-thrust evasive arcs:** segmented burns to defeat pursuit prediction; adds travel-time penalty.

---

## 4) Communication Latency Envelope

| Communication Lane | One-Way Typical | One-Way Worst | Round-Trip Typical | Round-Trip Worst |
|---|---:|---:|---:|---:|
| Earth <-> Luna | 1.3–2.7 s | 4 s | 3–6 s | 8 s |
| Earth <-> Mars | 4–12 min | 22 min | 8–24 min | 44 min |
| Earth <-> Ceres | 14–27 min | 38 min | 28–54 min | 76 min |
| Mars <-> Ceres | 6–15 min | 24 min | 12–30 min | 48 min |
| Ceres <-> inner Belt | 45–180 s | 5 min | 1.5–6 min | 10 min |

---

## 5) Continuity Enforcement Rules

1. Any scene with transit must declare lane + burn class + stated elapsed days.
2. If timing is faster than BC-D lower bound, scene is invalid unless a retcon note is logged.
3. High-thrust scenes must show downstream cost (maintenance delay, med strain, fuel austerity).
4. Earth cannot provide real-time tactical command to Mars/Belt theaters.
5. Fabricator logistics timelines must include transit reality (Class 2 lots and Class 1 precursors do not teleport).

---

## 6) Quick Assumptions Table for Writers

| Use case | Default value |
|---|---:|
| Planning efficiency \(\eta\) | 0.26 |
| Military exhaust velocity \(v_e\) | 260 km/s |
| Balanced accel assumption | 0.035 g |
| Hard military accel assumption | 0.085 g |
| Emergency burst cap | 0.18 g (minutes to hours, not days) |

Use these defaults unless a scene explicitly justifies deviation.
