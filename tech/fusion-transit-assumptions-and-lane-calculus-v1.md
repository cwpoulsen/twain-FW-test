# Fusion Transit Assumptions + Core-Lane Trajectory Calculus v2

Status: **Quantitative continuity lock for route timing, burn-mode choice, and command-latency realism**  
Authority links: `tech/technical-architecture-v1.md`, `tech/interplanetary-transit-and-comms-envelope-v1.md`, `timeline/master-timeline-sequence-v1.md`, `ops/timeline-policy.md`.

---

## 1) Locked Assumptions (2055 fleet envelope)

| Parameter | Symbol | Locked planning value | Notes |
|---|---:|---:|---|
| Standard gravity | \(g_0\) | 9.81 m/s^2 | Reference constant |
| Effective exhaust velocity (campaign median) | \(v_e\) | 260,000 m/s | Military torch median; lower cargo drives exist |
| Lower/upper exhaust sanity band | \(v_e\) | 120,000 to 450,000 m/s | Use for margin checks |
| Patrol-convoy acceleration | \(a_A\) | 0.005 g0 | Fuel-first, low signature doctrine |
| Standard military acceleration | \(a_B\) | 0.010 g0 | Default redeployment profile |
| Rapid strike acceleration | \(a_C\) | 0.015 g0 | High maintenance and fuel burden |
| Patrol burn duration (per leg) | \(\tau_A\) | 4 days | accel + flip + decel |
| Standard burn duration (per leg) | \(\tau_B\) | 5 days | accel + flip + decel |
| Rapid burn duration (per leg) | \(\tau_C\) | 7 days | accel + flip + decel |

**Interpretation lock:** for AU-scale lanes, ships do **burn-coast-burn** with fixed-duration thrust windows; full brachistochrone across entire lane is an ideal lower bound, not routine doctrine.

---

## 2) Transfer Modes + Equations

### 2.1 Mode M1 — Full brachistochrone lower bound (rare)
Used only as hard lower-bound estimate when propellant/thermal budget is hand-waved impossible in normal ops.

\[
 t_{M1} = 2\sqrt{\frac{d}{a}}, \qquad v_{peak} = \sqrt{ad}
\]

### 2.2 Mode M2 — Symmetric burn-coast-burn (campaign default)
Burn \(\tau\) at acceleration \(a\), coast, then burn \(\tau\) to brake.

\[
 v_c = a\tau
\]
\[
 d_b = a\tau^2 \quad (\text{distance covered by both burn legs})
\]

If \(d > d_b\):
\[
 t_{M2} = 2\tau + \frac{d-d_b}{v_c}
\]

If \(d \le d_b\):
\[
 t_{M2} = 2\sqrt{\frac{d}{a}} \quad (\text{short-lane triangular profile})
\]

### 2.3 Comms floor (cannot be bypassed)
\[
 t_{light} = \frac{d}{c}
\]

### 2.4 Propellant sanity check (must be stated for hard burns)
\[
 \Delta v \approx 2a\tau, \qquad \frac{m_0}{m_f} = e^{\Delta v/v_e}
\]

---

## 3) Example Calculation (Earth -> Ceres, median geometry)

Assume:
- \(d = 2.77\,AU = 4.143 \times 10^{11}\,m\)
- Standard profile \(a_B = 0.01g_0 = 0.0981\,m/s^2\), \(\tau_B=5\) days \(=432,000\,s\)

1) Cruise velocity:
\[
 v_c = a\tau = 0.0981\times432000 = 42,379\,m/s \approx 42.4\,km/s
\]

2) Burn distance:
\[
 d_b = a\tau^2 = 0.0981\times(432000)^2 = 1.831\times10^{10}\,m \approx 0.122\,AU
\]

3) Coast distance:
\[
 d_c = d-d_b = 3.960\times10^{11}\,m
\]

4) Transit time:
\[
 t = 2\tau + \frac{d_c}{v_c}
= 864000 + \frac{3.960\times10^{11}}{42379}
= 1.0207\times10^7\,s
\approx 118.1\,days
\]

5) Propellant sanity for this profile:
\[
 \Delta v \approx 2a\tau = 84.8\,km/s
\]
At \(v_e=260\,km/s\),
\[
 m_0/m_f = e^{84.8/260} \approx 1.39
\]
(plausible with reserves; at \(v_e=120\,km/s\), ratio ~2.03 and logistics burden jumps.)

---

## 4) Core-Lane Geometry Bands (locked for planning)

| Lane | Min distance | Max distance |
|---|---:|---:|
| Earth-Moon | 384,400 km | 405,000 km |
| Earth-Mars | 0.52 AU | 2.52 AU |
| Earth-Ceres | 1.77 AU | 3.77 AU |
| Mars-Ceres | 1.25 AU | 4.29 AU |
| Ceres-Jovian lanes (to Jovian system approach nets) | 2.20 AU | 6.00 AU |
| Belt intra-lanes (industrial habitat mesh) | 0.12 AU | 1.20 AU |

(1 AU = 149,597,870 km)

---

## 5) Core-Lane Flight-Time Table (Mode M2: burn-coast-burn default)

| Route | Patrol convoy BC-A (0.005g, 4d+4d burns) | Standard transit BC-B (0.01g, 5d+5d burns) | Rapid strike BC-C (0.015g, 7d+7d burns) | One-way light-time |
|---|---:|---:|---:|---:|
| Earth-Moon | 2.0–2.1 d | 1.4–1.5 d | 1.2 d | ~1.3–1.4 s |
| Earth-Mars | 57.1–261.4 d | 26.2–108.0 d | 17.1–56.0 d | 4.3–21.0 min |
| Earth-Ceres | 184.8–389.1 d | 77.3–159.0 d | 41.4–80.3 d | 14.7–31.4 min |
| Mars-Ceres | 131.7–442.2 d | 56.1–180.3 d | 31.3–90.5 d | 10.4–35.7 min |
| Ceres-Jovian lanes | 228.7–616.8 d | 94.9–250.1 d | 49.8–123.7 d | 18.3–49.9 min |
| Belt intra-lanes | 16.3–126.6 d | 9.9–54.0 d | 8.1–30.3 d | 1.0–10.0 min |

---

## 6) Belt Intra-Lane Detail (named sub-routes)

| Intra-Belt lane | Geometry band | BC-A | BC-B | BC-C |
|---|---:|---:|---:|---:|
| Ceres <-> Vesta industrial stream | 0.35–1.20 AU | 39.7–126.6 d | 19.3–54.0 d | 13.8–30.3 d |
| Ceres <-> Pallas arbitration lane | 0.12–0.90 AU | 16.3–95.9 d | 9.9–41.8 d | 8.1–24.5 d |
| Vesta <-> Pallas smuggling arc | 0.25–1.40 AU | 29.5–147.0 d | 15.2–62.2 d | 11.7–34.2 d |

---

## 7) Tactical Implications (continuity hooks)

1. **Geometry dominates strategy:** the same route can vary by 2–4x in duration; campaign plans must state geometry condition (favorable, median, unfavorable).
2. **Rapid strike is expensive:** BC-C profiles consume propellant margin and create mandatory maintenance debt; repeated BC-C use must degrade later options.
3. **Earth command lag is structural:** Earth->Ceres and Ceres->Jovian operations cannot be tightly micromanaged in real time.
4. **Interception windows are predictable:** burn-coast-burn legs create vulnerable coast phases; ambush doctrine targets mid-course vector commitment.
5. **Belt politics follow transit reality:** coalition cohesion degrades when intra-lane reinforcement times exceed local stockpile endurance.
6. **Narrative pacing rule:** any major redeployment beat must include lane, burn class, mode, and elapsed time in chapter-level chronology.

---

## 8) Writer Enforcement Checklist

For every transit scene, specify:
- Route + geometry assumption (min/median/max-like placement)
- Burn class (BC-A/B/C)
- Transfer mode (M2 by default; M1 only as explicit lower bound)
- Stated elapsed travel days
- Comms delay implications on command decisions
- Operational cost paid (fuel, maintenance, crew fatigue, or missed opportunity)

If these are absent, scene is under-specified for canon continuity.
