# Fusion Transit Assumptions + Lane Calculus v1

Status: **Quantitative continuity lock for travel-time realism**  
Authority links: `tech/technical-architecture-v1.md`, `timeline/master-timeline-sequence-v1.md`, `ops/timeline-policy.md`.

---

## 1) Core Assumptions (2055 fleet baseline)

| Parameter | Symbol | Baseline | Notes |
|---|---:|---:|---|
| Standard gravity | g0 | 9.81 m/s^2 | Reference constant |
| Fusion drive electrical conversion efficiency | eta_e | 0.35 | Thermal->electric equivalent chain |
| Jet coupling efficiency | eta_j | 0.55 | Electric/plasma power to directed exhaust |
| Net propulsive efficiency | eta_p=eta_e*eta_j | 0.1925 | Used in thrust-power estimates |
| Effective exhaust velocity (fleet median) | v_e | 120,000 m/s | Isp ~ 12,200 s equivalent |
| Patrol acceleration envelope | a_p | 0.003 g0 | Fuel-conservative |
| Military transit envelope | a_m | 0.010 g0 | Common rapid redeployment |
| Sprint envelope (short-duration) | a_s | 0.020 g0 | Crew + fuel costly |

---

## 2) Working Equations

1. **Power-to-thrust estimate (fusion-electric approximation):**  
   F ≈ (2 * eta_p * P) / v_e

2. **Brachistochrone-style half-burn transfer (accelerate/flip/decelerate):**  
   t_total = 2 * sqrt(d / a)

3. **Peak midpoint velocity in half-burn profile:**  
   v_peak = sqrt(a * d)

4. **One-way light-time (comms floor):**  
   t_light = d / c

5. **Rocket equation check for propellant sanity:**  
   delta_v = v_e * ln(m0/mf)

Use Eq.2 only when propellant and thermal margins support continuous half-burn profile.

---

## 3) Key Lane Distances (Reference Ranges)

| Lane | Min distance | Max distance |
|---|---:|---:|
| Earth-Luna | 384,400 km | 405,000 km |
| Earth-Mars | 0.52 AU | 2.52 AU |
| Earth-Ceres | 1.77 AU | 3.77 AU |
| Mars-Ceres | 1.25 AU | 4.29 AU |
| Earth-Jupiter system | 4.20 AU | 6.20 AU |

(1 AU = 149,597,870 km)

---

## 4) Transfer-Time Table (Half-Burn Idealization)

| Lane distance | t @ 0.003g | t @ 0.010g | t @ 0.020g | One-way light-time |
|---:|---:|---:|---:|---:|
| 0.52 AU | 37.5 d | 20.5 d | 14.5 d | 4.3 min |
| 1.00 AU | 52.3 d | 28.6 d | 20.2 d | 8.3 min |
| 1.77 AU | 69.6 d | 38.1 d | 26.9 d | 14.7 min |
| 2.52 AU | 83.0 d | 45.5 d | 32.2 d | 20.9 min |
| 3.77 AU | 101.5 d | 55.6 d | 39.3 d | 31.3 min |
| 6.20 AU | 130.4 d | 71.4 d | 50.5 d | 51.6 min |

Real missions are typically longer due to coast phases, traffic deconfliction, thermal throttling, and tactical rerouting.

---

## 5) Continuity Use Rules

1. Scene travel must choose a lane distance + acceleration envelope; no “arrives next chapter” shortcuts.
2. Emergency sprints consume future options (heat, maintenance debt, propellant margin).
3. Command plans must include comm-delay consequences using light-time table.
4. If plotted timing violates this sheet, either revise timeline or log explicit exception with cost.
