# Mission Requirements & Launch Service Definition
## P-Class Sounding Rocket Program — Document MRLD-001, Rev 0.1
*Confidential — Internal Working Document*

---

## 1. Executive Summary

This document establishes the mission-level requirements for a commercial P-class sounding rocket launch service targeting the scientific, academic, and avionics-testing communities. The service is designed around an in-house-developed solid rocket motor (SRM) producing approximately 25,000 Newton-seconds of total impulse, enabling suborbital flights to 8–15 km apogee with recoverable payloads in the 0.5–3 kg class.

The reference mission is the Cosmic Research Bondar vehicle (Spain, 2021): 131 mm diameter, 33 kg liftoff mass, Cesaroni 21,062 Ns O-class motor, 7,800 m apogee at Mach 1.7. This program targets a 19% increase in total impulse over Bondar while adding a standardized payload interface and full recovery capability.

---

## 2. Mission Concept

### 2.1 Value Proposition

Provide affordable, reliable, repeatable suborbital access at the P-class impulse level to customers who require a controlled high-dynamic, high-altitude, or microgravity flight environment — without the cost, lead time, or complexity of larger sounding rocket programs.

**Target flight envelope:**
- Apogee: 8–15 km (altitude-configurable by payload mass)
- Max velocity: Mach 1.5–2.0
- Peak acceleration: 10–20 G (motor-burn phase)
- Microgravity window: 30–90 seconds (coast phase, apogee-centered)
- Total flight time: 3–8 minutes (launch to recovery touchdown)

### 2.2 Customer Segments

| Segment | Primary Need | Example Missions |
|---|---|---|
| University research groups | Affordable suborbital access, microgravity experiments | Fluid dynamics, biological samples, crystal growth |
| Avionics developers | Controlled in-flight validation environment | IMU/GPS systems, attitude determination, RF links |
| Sensor manufacturers | At-altitude calibration and qualification | Atmospheric sensors, radiation detectors, MEMS |
| Space startup ecosystem | Low-cost hardware flight heritage | CubeSat components, reaction wheels, power systems |
| Defense/government research | Sounding capability without bureaucratic complexity | Atmospheric characterization, telemetry testing |

### 2.3 Competitive Landscape

The service occupies the gap between commercial high-power rocketry (N-class, <5 km, unrecovered payloads) and large sounding rocket programs (Terrier-Orion class, 100+ km, $500K+ per flight). No widely available commercial service currently occupies the 8–15 km recoverable payload niche at this price point.

---

## 3. Key Performance Parameters (KPPs)

These are the non-negotiable, top-level parameters that define mission success. All vehicle and motor design decisions flow from these.

| ID | Parameter | Threshold (min acceptable) | Objective (design target) | Rationale |
|---|---|---|---|---|
| KPP-01 | Total Impulse | 22,000 Ns | 25,000 Ns | P-class capability; margin over Bondar reference |
| KPP-02 | Apogee (1 kg payload) | 8 km | 12 km | Stratospheric access; meaningful microgravity window |
| KPP-03 | Payload mass | 0.5 kg | 3 kg | Useful scientific instrument mass |
| KPP-04 | Payload recovery | Required | Required | Payload and data must be returned intact |
| KPP-05 | Mission reliability | 85% | 95% | Commercial service viability |
| KPP-06 | Launch cadence | 4 flights/year | 12 flights/year | Revenue model viability |
| KPP-07 | Payload G-limit (axial) | < 20 G peak | < 15 G peak | Protects sensitive instruments |

---

## 4. Mission-Level Requirements

### 4.1 Propulsion (MRL-1xx)

**MRL-101** — The propulsion system shall deliver a total impulse of no less than 22,000 Ns and no greater than 40,960 Ns (P-class upper bound).

**MRL-102** — The motor shall produce a thrust profile compatible with stable flight from the launch rail; minimum thrust-to-weight ratio at liftoff shall be ≥ 5:1.

**MRL-103** — The motor shall be designed for static test verification prior to any flight article use. No flight motor configuration shall fly without a successful static fire of the same grain design.

**MRL-104** — The propellant grain design shall achieve a substantially neutral (±15% of mean) thrust profile to avoid excessive peak G-loading on the payload.

**MRL-105** — The motor case shall incorporate a pressure relief or structural fuse mechanism to prevent catastrophic uncontained failure in overpressurization scenarios.

**MRL-106** — Motor design shall target a minimum safety factor of 4.0 on chamber pressure burst limit relative to nominal operating pressure (NOP).

**MRL-107** — The motor shall be re-loadable or replaceable between flights with a turnaround time of ≤ 2 weeks at the operator level.

### 4.2 Payload Interface (MRL-2xx)

**MRL-201** — The vehicle shall provide a standardized payload bay with a minimum usable internal diameter of 90 mm and minimum usable length of 200 mm.

**MRL-202** — The payload interface shall be a defined mechanical standard (bolt pattern, alignment features) published to customers as a Payload User's Guide (PUG).

**MRL-203** — The payload bay shall experience no more than 20 G of axial acceleration and no more than 5 G of lateral acceleration during the powered phase.

**MRL-204** — The payload bay shall maintain a temperature between -10°C and +50°C throughout the flight envelope.

**MRL-205** — The payload shall be electrically isolated from the vehicle structure. A payload power interface (regulated 5V and 12V, minimum 10W each) shall be available as an optional service.

**MRL-206** — A 1 Hz GPS-derived position and vehicle state (altitude, velocity, acceleration vector) data stream shall be available to the payload via a defined serial interface (RS-232 or CAN bus, TBD).

**MRL-207** — The vehicle shall provide a minimum microgravity quality of < 0.01 G (RMS, 3-axis) for a duration of no less than 30 seconds during the coast phase, for a 1 kg payload configuration.

**MRL-208** — The payload module shall be the recovered element. Payload must survive recovery loads not exceeding 15 G during parachute deployment.

### 4.3 Vehicle & Systems (MRL-3xx)

**MRL-301** — The vehicle shall be passively aerodynamically stable (positive static margin ≥ 1 caliber) throughout the powered flight phase without active control.

**MRL-302** — The vehicle shall carry a dual-event recovery system (drogue + main parachute) with independent deployment triggers on separate flight computers.

**MRL-303** — All vehicle sections shall be recovered or shall be designed to limit kinetic energy at ground impact to ≤ 75 J for any unrecovered section (per FAA Advisory Circular equivalent).

**MRL-304** — The vehicle shall carry a real-time GPS telemetry downlink at minimum 1 Hz update rate, with ground-readable altitude, velocity, and vehicle health data, from launch through landing.

**MRL-305** — The vehicle shall incorporate a flight termination capability (FTS) if required by range authority. FTS design shall comply with applicable range safety documentation.

**MRL-306** — Vehicle dry mass (excluding motor and payload) shall not exceed 15 kg in the baseline configuration.

### 4.4 Operations (MRL-4xx)

**MRL-401** — The launch system (vehicle + ground support) shall be operable by a crew of no more than 6 personnel.

**MRL-402** — Total time from vehicle arrival at launch site to launch-ready state shall not exceed 8 hours.

**MRL-403** — The ground support equipment (GSE) shall be transportable in a standard cargo van or equivalent without specialized transport permits.

**MRL-404** — The vehicle shall support launch holds of up to 4 hours after entering terminal countdown without requiring re-servicing of any system (excluding motor igniter continuity check).

**MRL-405** — Payload integration (customer payload installation into bay) shall be accomplished in ≤ 2 hours by customer personnel following the PUG, without specialized tooling.

### 4.5 Safety & Regulatory (MRL-5xx)

**MRL-501** — All propellant handling, storage, and transport shall comply with applicable federal, state, and local regulations in the launch jurisdiction (ATF, DOT 49 CFR, and applicable state fire codes).

**MRL-502** — The program shall obtain and maintain all required licenses and permits prior to any propellant manufacturing or static fire activity, including but not limited to: ATF Federal Explosives License (if applicable), FAA Part 101 waiver (or equivalent), and range authority approvals.

**MRL-503** — A formal Hazard Analysis and Risk Assessment (HARA) shall be completed and reviewed before the first static test and before the first flight.

**MRL-504** — The motor design shall be validated through a minimum of 3 successful static fires at full scale before flight certification.

**MRL-505** — No personnel shall be within the minimum safe distance during motor static fire or launch. Minimum safe distance shall be calculated per FAA and/or NFPA 1127 methodology.

### 4.6 Business & Service Level (MRL-6xx)

**MRL-601** — Target price per flight (standard 1 kg payload, no telemetry processing) shall be < $15,000 USD at program maturity (≥ 10 flights flown).

**MRL-602** — Customer lead time from contract signature to launch shall be ≤ 6 months in steady-state operations.

**MRL-603** — A Payload User's Guide shall be published and maintained, defining all payload interfaces, environments, and customer responsibilities.

**MRL-604** — Post-flight, the customer shall receive: recovered payload, raw telemetry data, and a flight summary report within 30 days of landing.

---

## 5. Operational Concept (CONOPS)

### 5.1 Mission Flow

```
Customer engagement → Payload definition → PUG review → Contract
    ↓
Motor fabrication & grain casting → Static test campaign (3 firings min)
    ↓
Motor certification → Vehicle fabrication & integration
    ↓
Payload delivery & integration (T-48 hrs) → Pre-launch checkout
    ↓
Launch campaign (T-8 hr to T-0) → Powered flight (6–10 sec)
    ↓
Coast phase / payload operations (30–90 sec microgravity)
    ↓
Apogee → Dual deployment recovery → Splashdown/touchdown
    ↓
Payload recovery → Data processing → Customer report
```

### 5.2 Development Phases

**Phase 0 — Foundation (Months 1–6)**
- Propellant trade study finalization (this document)
- Motor design (grain geometry, nozzle, casing)
- Regulatory filing initiation (ATF/FAA)
- Static test stand design and build

**Phase 1 — Motor Development (Months 6–18)**
- Sub-scale static tests (50% propellant mass)
- Full-scale static test campaign (3 minimum)
- Motor certification

**Phase 2 — Vehicle Development (Months 12–24)**
- Vehicle design (parallel with Phase 1)
- Subsystem testing (recovery, avionics, telemetry)
- Integrated vehicle static fire (motor in vehicle on stand)

**Phase 3 — Flight Certification (Months 18–30)**
- First flight (instrumented, no customer payload)
- Envelope expansion flights
- Commercial launch license / range authority approval

**Phase 4 — Commercial Operations (Month 30+)**
- First customer flight
- Cadence build to 12 flights/year

---

## 6. Propellant Trade Study

### 6.1 Candidates Evaluated

Four solid propellant families were evaluated for the 25,000 Ns target at P-class scale:

1. **APCP — AP/HTPB** (ammonium perchlorate / hydroxyl-terminated polybutadiene)
2. **APCP — AP/PBAN** (ammonium perchlorate / polybutadiene acrylonitrile)
3. **KNSB** (potassium nitrate / sorbitol, 65/35 by mass)
4. **KNDX** (potassium nitrate / dextrose, 65/35 by mass)

A hybrid motor (N₂O/HTPB) was considered and excluded from detailed analysis due to the fundamental system complexity difference (pressurized oxidizer tank, injector, flow control) being incompatible with the program's SRM development goal.

### 6.2 Key Performance Calculations

For total impulse I_t = 25,000 Ns and propellant mass m_p = I_t / (I_sp × g₀):

| Propellant | I_sp (s) | Propellant mass (kg) | Flame temp (K) | NOP (MPa) |
|---|---|---|---|---|
| AP/HTPB | 210–230 | **11.4–12.5** | 3,000–3,300 | 3.5–7.0 |
| AP/PBAN | 200–220 | 11.9–13.1 | 3,100–3,400 | 4.0–7.5 |
| KNSB | 125–132 | **19.4–20.8** | 1,600–1,720 | 2.0–5.0 |
| KNDX | 120–128 | 20.1–21.6 | 1,590–1,680 | 2.0–4.5 |

The propellant mass delta between APCP and KN-based propellants is ~8 kg — a significant vehicle design driver. With typical propellant densities (APCP ~1,700 kg/m³, KNSB ~1,840 kg/m³), the grain volume difference is approximately 3.5–4.5 liters, translating to roughly 200–350 mm of additional motor length at 131 mm casing diameter.

### 6.3 Regulatory Analysis (United States)

**AP/HTPB and AP/PBAN:**
- Ammonium perchlorate classified as an oxidizer and explosive precursor
- Manufacturing APCP requires ATF **Federal Explosives Manufacturing License (FEL)**
- Storage requires licensed magazine
- Transport regulated under DOT 49 CFR Part 173 (Division 1.3 or 1.4 depending on formulation)
- Application to first static fire: minimum 6–12 months from regulatory filing
- NAR/Tripoli experimental certification also required for flight
- **Path is achievable but adds significant lead time and overhead to Phase 0–1**

**KNSB and KNDX:**
- Potassium nitrate is a common oxidizer (fertilizer, food preservative) — not controlled
- Sorbitol/dextrose are food-grade sugars — not controlled
- The *mixture* (KN-sugar propellant) has received ATF letter determinations as **not a low explosive** in multiple cases when properly characterized
- Does not require FEL in most US jurisdictions (verify with current ATF guidance)
- Classified as a Division 4.1 flammable solid for transport — far lighter regulatory burden
- Storage under NFPA 1 / local fire code (consult AHJ)
- **Can proceed to static test within weeks of program start**

### 6.4 Manufacturing Assessment

**AP/HTPB:**
- Requires vacuum mixer (to eliminate voids) — capital cost $5,000–$20,000 for P-class batch sizes
- Pot life of ~4–8 hours after mixing; timing-critical casting operation
- AP is respiratory/skin hazard — requires PPE and ventilated/filtered facility
- Cure: 24–72 hours at 50–60°C in a controlled oven
- Grain bonding to case liner is critical — bond failure is a common failure mode
- Significant formulation expertise required (oxidizer particle size distribution, plasticizer ratios, burn rate modifier loading)
- Commercial propellant suppliers exist (could outsource casting as interim measure)

**KNSB:**
- Melt-cast process: heat to ~105°C, pour into mold, cool — straightforward
- No vacuum mixing required
- Equipment: hot plate/oven, stainless steel pots, simple molds — capital cost < $500
- Safety: moderate fire hazard during processing (open flame prohibited); non-toxic
- Hygroscopic — requires humidity-controlled storage and moisture-sealed grain packaging
- Well-documented at all scales on Nakka's site; strong amateur heritage up to L/M class
- Grain geometries (BATES, hollow cylinder) are simple and reliable
- **Highest manufacturability score of all candidates**

**KNDX:**
- Similar to KNSB; slightly faster burn rate (higher Kn sensitivity)
- More brittle grain — higher cracking risk, especially at P-class segment lengths
- Less preferred than KNSB for large grains

**AP/PBAN:**
- Higher processing temperature than HTPB systems
- Shuttle heritage but extremely challenging at amateur scale
- Not recommended for in-house development without industrial infrastructure

### 6.5 Weighted Trade Matrix

Criteria weighted by importance to the program's mission (commercial service development):

| Criterion | Weight | AP/HTPB | AP/PBAN | KNSB | KNDX |
|---|---|---|---|---|---|
| Specific impulse (vehicle efficiency) | 20% | 5 | 5 | 2 | 2 |
| Propellant mass efficiency (vehicle sizing) | 15% | 5 | 5 | 2 | 2 |
| Manufacturing simplicity | 20% | 2 | 1 | 5 | 4 |
| Regulatory burden | 20% | 2 | 1 | 5 | 5 |
| Material cost | 10% | 3 | 2 | 5 | 5 |
| Safety / handling | 10% | 3 | 2 | 4 | 4 |
| Heritage at ≥ L-class scale | 5% | 5 | 3 | 3 | 2 |
| **Weighted Score** | | **3.40** | **2.90** | **3.65** | **3.45** |

*Scoring: 1 = poor, 3 = adequate, 5 = excellent*

### 6.6 Recommendation: Dual-Track Strategy

Neither a pure KNSB nor a pure APCP approach is optimal for this program at this stage. The recommended strategy is a **two-track development path**:

**Track A — KNSB Development Motor (Months 0–18)**
Use KNSB to develop and validate the motor casing, nozzle, grain geometry, Kn profile, and static test infrastructure. KNSB enables rapid iteration (weeks per cycle, not months), very low regulatory friction, and low per-test cost. All structural, thermal, and ballistic design work transfers directly to the APCP flight motor.

**Track B — APCP Regulatory & Development Path (Months 3–24)**
Initiate ATF FEL application, facility design, and APCP formulation development in parallel. By the time the KNSB development motor is fully characterized, the regulatory path should be clear and the APCP manufacturing capability coming online.

**Target End State:**
The flight-certified commercial product is an **AP/HTPB motor**. KNSB is a development and testing tool, not the commercial propellant. This gives the program the regulatory simplicity needed to start fast, while targeting the performance and vehicle efficiency the commercial service requires.

**If APCP regulatory path proves infeasible** (e.g., jurisdiction-specific restrictions, facility cost), KNSB remains a viable — if penalized on vehicle mass — fallback for the commercial service, consistent with the operational analogy of Nakka's own L-class Liberty motor program.

---

## 7. Open Questions & Next Steps

| Item | Owner | Target |
|---|---|---|
| Confirm launch jurisdiction and applicable regulatory framework (FAA, ATF, state AHJ) | Program Lead | Month 1 |
| Initiate ATF pre-application inquiry (letter of determination for KNSB; FEL scope for APCP) | Program Lead / Legal | Month 2 |
| Select KNSB formulation and obtain Nakka burn rate data for design | Propulsion | Month 1 |
| Begin motor sizing: grain geometry, Kn profile, chamber pressure model | Propulsion | Month 2 |
| Define launch site options and range authority requirements | Operations | Month 3 |
| Develop Payload User's Guide (draft) for customer engagement | Systems | Month 4 |
| Begin static test stand conceptual design | Structures | Month 3 |

---

*Document MRLD-001 Rev 0.1 — Working Draft. Subject to revision as design matures.*
*Next review: following propellant selection confirmation and initial grain design.*
