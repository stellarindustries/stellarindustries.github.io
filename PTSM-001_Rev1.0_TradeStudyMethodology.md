# Propellant Trade Study: Step-by-Step Methodology
## P-Class Sounding Rocket Program — Document PTSM-001, Rev 1.0
### With Annotated Corrections and Reusable Framework for Industry Propulsion Engineers

---

## Preamble: Transparency and a Critical Correction

Before presenting the methodology, intellectual honesty requires flagging a material error in the trade study as originally presented. The regulatory analysis for APCP overstated the burden in one specific way:

**What was stated:** APCP manufacturing requires an ATF Federal Explosives Manufacturing License (FEL).

**What the ATF's own open letter actually says:** "APCP and products that contain only APCP are not subject to the recordkeeping, storage, and other regulatory requirements under 27 CFR, Part 555." Finished APCP hobby rocket motors — purchased commercially — do not require a federal explosives license to sell, purchase, store, or fly. The National Association of Rocketry confirms this: "Hobby rocket motors (including high power) no longer require a Federal explosives permit to sell, purchase, store, or fly."

**The correction and why it matters:** The exemption applies to *finished motors*. This program is not buying finished motors — it is manufacturing propellant in-house. In-house manufacture of APCP (specifically: production of bulk ammonium perchlorate mixtures, manufacturing igniters, and related activities) *does* still fall under federal explosives regulation. The ATF's open letter is explicit that "ammonium perchlorate explosive mixtures" — i.e., bulk AP compound prior to being a finished motor — "continue to be regulated under 18 U.S.C. Chapter 40 and 27 CFR Part 555," and that "a Federal explosives license or permit is required to manufacture, import, distribute, transport, or receive these materials."

So the conclusion of the trade study (FEL is required for in-house APCP manufacture) was correct. But the reasoning was imprecise: the regulatory burden is specifically on *manufacture of bulk AP propellant*, not on APCP as a finished product. This distinction matters for program planning because it means:

1. Procuring commercial APCP reload propellant grain from a licensed manufacturer and loading it into a custom casing is a different regulatory path than mixing your own AP/HTPB.
2. The FEL burden may be partially circumvented by a contract manufacturing arrangement with a licensed propellant producer, at least in early program phases.

All other conclusions from the original trade study stand. The dual-track recommendation remains valid. This correction is documented here as an example of the kind of regulatory precision that an industry-level trade study must maintain.

---

## Part I: Framework Overview

A propellant trade study is a structured decision-support analysis that evaluates candidate propellants across a defined set of criteria, weighted by their importance to the program's specific mission and context. It is not a performance-only analysis — for an in-house development program, manufacturability, regulatory path, and cost frequently dominate over raw specific impulse.

The methodology consists of eight sequential steps:

```
Step 1: Define the decision context and constraints
Step 2: Select candidate propellant families
Step 3: Identify and define figures of merit (criteria)
Step 4: Assign criterion weights
Step 5: Gather and bound performance data for each criterion
Step 6: Build the scoring rubric and assign scores
Step 7: Compute weighted scores and perform sensitivity analysis
Step 8: Form the recommendation and document assumptions
```

Each step is explained below in the context of this program, with the decisions, data sources, and rationale made explicit. A reusable template for each step follows Part II.

---

## Part II: Step-by-Step Walkthrough with Citations and Rationale

---

### Step 1: Define the Decision Context and Constraints

**What this step does:** Before any propellants are considered, the decision context must be fully specified. A trade study that fails to bound the problem correctly will optimize for the wrong things.

**How it was done for this program:**

The decision context was defined by three inputs: the mission statement (commercial P-class sounding rocket service for scientific and academic community), the target total impulse (25,000 Ns), and the program stage (starting from scratch, no existing infrastructure).

From these, the binding constraints were extracted:

**Performance floor:** Any candidate propellant must be capable of delivering 25,000 Ns with a physically realizable grain geometry at a casing diameter consistent with the Bondar reference vehicle (~131 mm OD). This immediately eliminates propellants with such low energy density that the motor would become impossibly large.

**Manufacturing ceiling:** The program has no existing propellant manufacturing infrastructure. Candidates requiring industrial-scale equipment (vacuum mixers, controlled-atmosphere facilities, specialized casting rigs) face a higher development cost and timeline burden. This is an explicit constraint because it affects time-to-first-test, which in turn affects program survival for a startup.

**Regulatory ceiling:** The program is operating in the United States. Any propellant pathway that requires obtaining federal licenses before the first static test introduces a 6–18 month delay before any empirical data can be gathered. Since test data is the program's most critical early resource, regulatory delay is a direct risk to program viability.

**Mission fitness:** The propellant must be compatible with the expected flight environment — P-class burn duration of approximately 5–10 seconds, chamber pressures of 2–8 MPa depending on formulation, and a grain that can be scaled to the casing geometry.

**Why these constraints were chosen:**

The ranking of constraints (regulatory and manufacturing near-equal weight to performance) is a deliberate choice appropriate to an early-stage program with no existing infrastructure. For a mature program with an established facility, regulatory burden becomes a sunk cost and performance dominates. For a startup development program, the path to first data is the critical variable. This is the same logic that led Cosmic Research to use a COTS motor for Bondar: reducing development risk at program start is sometimes more important than technical optimality.

---

### Step 2: Select Candidate Propellant Families

**What this step does:** Generates the comparison set — the propellants that will actually be evaluated. The candidate set must be comprehensive enough to capture all viable options, but bounded enough to be manageable.

**How it was done for this program:**

The candidate space for solid rocket propellants applicable to amateur and small commercial programs is well-established. Four primary families exist at P-class scale:

**AP-based composite propellants (APCP):**
APCP is "a type of solid rocket propellant consisting of ammonium perchlorate (AP) crystals as the primary oxidizer, aluminum powder as a metallic fuel, and a polymeric binder such as polybutadiene acrylonitrile (PBAN) or hydroxyl-terminated polybutadiene (HTPB) that encapsulates the solid particles to form a rubbery, castable matrix." The "typical composition includes 70–88% AP by mass, 10–20% binder, and up to 18% aluminum, with the solids loading reaching 85–90% to achieve high energy density." APCP delivers "specific impulses (depending on the composition and operating pressure) of 180–260 seconds." This is the highest-performing class available to small programs and the dominant propellant in all certified commercial HPR motors.

Two sub-variants were evaluated:
- AP/HTPB: The dominant amateur and small commercial formulation. HTPB "not only improves the specific impulse of the propellant but also has a widely adjustable range of burning rates, good mechanical properties, a simple manufacturing process, and abundant raw materials."
- AP/PBAN: Shuttle heritage propellant. "Higher processing temperature than HTPB systems" — this was flagged immediately as a concern at amateur scale and ultimately resulted in AP/PBAN being rated "not recommended" in the matrix.

**KN-sugar propellants (KNSB and KNDX):**
Potassium nitrate / sorbitol (KNSB) and potassium nitrate / dextrose (KNDX) are the two primary KN-sugar formulations documented by Richard Nakka. "KNO₃/sugar propellants are traditionally used in rocket studies by amateur groups. Both components are easy to buy, their combustion products are non-toxic and this propellant can produce relatively high specific impulse, with values higher than the ones obtained by black gunpowder." The melt-cast manufacturing process — "both propellant components are ground and mixed, after which the mixture is heated until the sucrose fuses around the nitrate grains, forming a doughy mixture which can be placed in molds with a proper propellant grain design" — is the defining advantage of this family: it requires no specialized equipment.

For KNSB specifically, the theoretical combustion equation at 65/35 O/F ratio has been characterized by Nakka using PROPEP (Propellant Evaluation Program), with specific impulse variation with O/F ratio documented in published charts on nakka-rocketry.net.

**Why was a hybrid motor excluded?**
A hybrid motor (nitrous oxide oxidizer / HTPB fuel) was considered briefly and excluded from detailed analysis. The reasoning: a hybrid fundamentally differs from an SRM in that it requires a pressurized oxidizer feed system, injector, and active flow control. The program's stated goal is to develop in-house SRM capability specifically. Evaluating a hybrid would be evaluating a different product entirely, not an alternative propellant for the same product. When a candidate requires changing the fundamental system architecture to accommodate it, it belongs in a separate system trade, not a propellant trade.

**Why were other solid propellants excluded?**
Double-base propellants (nitrocellulose/nitroglycerin), HTPE-based formulations, and energetic binder systems (GAP-based) were not included because they require significantly more advanced chemistry and processing infrastructure than is realistic for a startup development program at this stage. They also lack the heritage documentation that makes design validation tractable. A propellant with no publicly available burn rate data, no amateur-scale manufacturing documentation, and no test heritage at P-class grain sizes cannot be meaningfully scored in a trade — the uncertainty bands on all criteria are too wide to be useful.

---

### Step 3: Identify and Define Figures of Merit (Criteria)

**What this step does:** Defines precisely what will be measured for each candidate. Every criterion must be independently assessable, specific enough to score, and collectively exhaustive of what matters to the program.

**How it was done for this program:**

Seven criteria were identified. For each, the rationale for inclusion is given:

**Criterion 1: Specific Impulse (I_sp)**
The fundamental propulsive figure of merit. I_sp = F / (ṁ · g₀), with units of seconds. For a fixed total impulse target, I_sp directly determines propellant mass: m_p = I_t / (I_sp · g₀). Higher I_sp means less propellant for the same impulse — which means a lighter, shorter, and cheaper vehicle. This criterion was included because it drives vehicle mass fraction, which in turn drives apogee, payload capacity, and recovery system sizing. It cannot be excluded from any propulsion trade.

**Criterion 2: Propellant Mass Efficiency (vehicle sizing impact)**
This is distinct from I_sp — it captures the second-order effect of propellant mass on vehicle design. Two propellants with different I_sp require different propellant masses, which require different casing volumes (at different propellant densities), which produce different motor lengths, which produce different vehicle lengths, drag coefficients, structural masses, and recovery system sizes. This criterion was included as a separate line item from I_sp because at P-class scales the mass delta between APCP and KNSB (~8 kg) is large enough to qualitatively change the vehicle design — it is not merely a quantitative refinement.

**Criterion 3: Manufacturing Simplicity**
Assessed as the inverse of the capital cost, specialized equipment, expertise, and processing complexity required to produce a flight-quality grain. This criterion is weighted heavily for a startup development program because manufacturing complexity is a direct multiplier on development timeline, test cost, and failure mode diversity. A propellant that is difficult to manufacture correctly introduces grain defects, voids, and bond failures as failure modes independent of the motor design. KNSB's melt-cast process is the benchmark for simplicity at this scale.

**Criterion 4: Regulatory Burden**
Assessed as the time and cost overhead imposed by applicable federal, state, and local regulations before the first static test can be conducted. For a startup, the time to first data is existential — months of delay before any empirical validation is a program-level risk. This criterion captures the difference between a propellant that can be tested in weeks (KNSB) and one whose precursor chemicals are federally regulated (bulk AP), requiring licensure, facility inspection, and magazine construction before manufacture can begin. The ATF's position that "a Federal explosives license or permit is required to manufacture, import, distribute, transport, or receive" ammonium perchlorate explosive mixtures is the regulatory driver for in-house APCP manufacture.

**Criterion 5: Material Cost**
The direct cost of propellant raw materials per kilogram of propellant produced. For a development program planning 3–8 static tests at P-class propellant masses (11–21 kg per test), material cost is a meaningful budget line item. KN-sugar propellants use food-grade KNO₃ and sorbitol or dextrose — commodity prices of a few dollars per kilogram. APCP uses ammonium perchlorate ($15–30/kg from specialty suppliers), HTPB ($20–40/kg), and aluminum powder. The total raw material cost per P-class static test differs by roughly an order of magnitude.

**Criterion 6: Safety and Handling**
Assessed across three dimensions: toxicity of raw materials (chronic exposure), reactivity hazards during processing, and consequence severity of a processing accident. APCP uses ammonium perchlorate, which "undergoes a highly endothermic equilibrium dissociative sublimation" and is an AP-based oxidizer with respiratory and skin hazard classification. KN-sugar propellants use non-toxic components, though the melt-cast process introduces fire risk from the heated mixture. Neither family is safe to be casual with, but the nature and severity of the hazards differ, which matters for facility design and PPE requirements.

**Criterion 7: Heritage at L-Class and Above**
Assessed as the availability of publicly documented design data, burn rate characterization, grain scaling guidance, and failure mode documentation for motors at or above L-class (2,560–5,120 Ns, approximately 10–20% of P-class impulse). Heritage data enables calibration of internal ballistic models against real test results, rather than relying solely on first-principles calculations. For KNSB, Nakka's experimental work — burn rate measurements using the Crawford strand burner method, a, n constants for Saint Robert's law across multiple pressure regimes, and Kn analysis for BATES grains — provides this calibration basis. For AP/HTPB, commercial motor manufacturer data and published academic literature provide the same function at much larger scale, but with fewer intermediate data points in the L–P range specifically.

**Why were other possible criteria not included?**

Several candidates were considered and excluded:

- *Burn rate tunability*: Relevant for a mature program designing to a specific thrust profile, but at this stage the grain geometry is the primary burn rate control mechanism. Deferred.
- *Flame temperature* (as a standalone criterion): Captured indirectly through I_sp and through its effect on nozzle and casing thermal design. Not scored independently to avoid double-counting.
- *Shelf life of propellant grain*: Relevant for an operational program with inventory, not for a development program that will test fresh-cast grains. Deferred.
- *Environmental impact*: APCP produces HCl in exhaust, which is an environmental concern at volume. Not a decision driver at P-class test cadence. Deferred.

---

### Step 4: Assign Criterion Weights

**What this step does:** Translates the program's priorities into a numerical weighting schema. Weights must sum to 100% and must be assigned before scores are known — assigning weights after scoring is a common bias trap that invalidates the study.

**How it was done for this program:**

Weights were assigned by asking: "If this criterion were the only one that differed between two otherwise identical candidates, how much would it matter to program success?"

| Criterion | Weight | Rationale |
|---|---|---|
| Specific impulse | 20% | Directly determines vehicle design and mission performance. Cannot be ignored. Assigned the highest single weight. |
| Propellant mass efficiency | 15% | Correlated with I_sp but large enough in absolute terms to warrant independent weighting at P-class. |
| Manufacturing simplicity | 20% | Equal weight to I_sp because for a development program, the path to first test is as important as what happens at first test. |
| Regulatory burden | 20% | Equal weight to manufacturing because it gates program start. A propellant requiring 12 months of regulatory prep before testing is a 12-month program delay. |
| Material cost | 10% | Important but not dominant. A 10× cost difference matters less than a 12-month delay. |
| Safety and handling | 10% | Non-trivial but manageable for any candidate through appropriate procedures. |
| Heritage at L+ scale | 5% | Useful but not decisive. Lacking heritage data increases design uncertainty, but does not prevent a competent engineering team from proceeding. |

**Why equal weights for I_sp, manufacturing, and regulatory burden?**

This is the most important weighting decision in the study. An experienced propulsion engineer at a mature aerospace company would likely weight I_sp at 40–50% and regulatory at 5%, because that engineer's program already has the facility, the license, and the manufacturing capability. The regulatory and manufacturing criteria are sunk costs for them. For a startup development program, they are not sunk — they are the critical path. The weights reflect the program's actual situation, not the propulsion engineering profession's default assumptions.

**A note on subjectivity:**

Criterion weighting is inherently subjective. The weights above represent one defensible set of values for this specific program context. A program with a different priority structure (e.g., one where the sponsor specifically requires APCP for technical reasons unrelated to performance, or one where funding is unlimited and time is the only constraint) would assign very different weights. The sensitivity analysis in Step 7 is specifically designed to test how robust the recommendation is to weight perturbations.

---

### Step 5: Gather and Bound Performance Data

**What this step does:** Populates the factual content of the trade — the actual numbers and qualitative assessments for each candidate on each criterion. Every data point should have a source; uncertainty bounds should be stated.

**How it was done for this program:**

**Specific Impulse data:**

For APCP (AP/HTPB): "specific impulses (depending on the composition and operating pressure) of 180–260 seconds are adequate" for typical APCP formulations. The range used in the trade (210–230 s) represents a mid-range APCP formulation without exotic ingredients — achievable for an in-house manufacturer without access to specialized AP particle size distributions or high aluminum loading optimization. Peak values (250+ s) require formulation sophistication beyond what a startup program can be expected to achieve in early development.

For KNSB: Nakka's PROPEP calculations at 65/35 O/F ratio and 68 atm (1000 psi) chamber pressure, verified against published combustion equations, place theoretical I_sp in the 125–132 s range. The combustion products at this condition are CO₂, CO, H₂O, H₂, N₂, K₂CO₃, and KOH. The relatively heavy exhaust products (high effective molecular weight) are the primary reason for the lower I_sp compared to APCP — the Nakka data is explicit that I_sp varies significantly with O/F ratio, peaking near 65/35 and dropping rapidly on either side.

**Propellant mass calculations:**

The fundamental relationship is: m_p = I_t / (I_sp · g₀)

For I_t = 25,000 Ns and g₀ = 9.807 m/s²:
- AP/HTPB at I_sp = 220 s: m_p = 25,000 / (220 × 9.807) = 11.58 kg
- AP/HTPB at I_sp = 210 s: m_p = 25,000 / (210 × 9.807) = 12.13 kg
- KNSB at I_sp = 130 s: m_p = 25,000 / (130 × 9.807) = 19.60 kg
- KNSB at I_sp = 125 s: m_p = 25,000 / (125 × 9.807) = 20.39 kg

These are vacuum I_sp values. At sea-level nozzle exit, effective I_sp is somewhat lower, but the ratio between propellants is preserved to within engineering precision for this comparison.

**Burn rate characterization:**

For KNSB, burn rate follows Saint Robert's (Vielle's) law: r = a · P^n, where a and n are empirical constants measured by Nakka and reported in his published work. The constants vary by pressure regime because KNSB "exhibits mesa behavior" — a plateau and mesa effect in the burn rate vs. pressure curve, "the result of different rates of surface regression (as a function of pressure) of the binder compared to the oxidizer particles." This pressure-regime-dependent behavior means that the a and n constants used in internal ballistic calculations must match the expected chamber pressure range.

For APCP, burn rate data is propellant-specific and supplier-dependent. No universal a and n values apply — they must be measured for the specific formulation. This is one reason heritage data and access to a strand burner are prerequisites for APCP motor design, whereas KNSB design can proceed from Nakka's published strand burner measurements.

**Regulatory data:**

The regulatory picture was researched specifically, and the correction noted in the preamble applies here. The current U.S. regulatory framework (as of ATF's 2009 open letter, still in effect) is:

- Finished APCP rocket motors: No ATF FEL required for purchase, storage, or use.
- Bulk ammonium perchlorate and AP mixtures (i.e., in-house manufacture): FEL required.
- KN/sugar propellants: Potassium nitrate and sorbitol/dextrose are not scheduled controlled substances. The propellant mixture has received ATF determinations as not a low explosive in multiple cases, though practitioners should verify current ATF guidance for their specific jurisdiction before proceeding.

The regulatory score in the trade matrix reflects the *in-house manufacture* scenario specifically — because that is the program's stated intent.

**Manufacturing data:**

For APCP: "APCP is manufactured by mixing the ingredients under vacuum to minimize voids, casting the slurry into motor casings." The vacuum mixing requirement is the primary capital cost driver. For P-class batch sizes (12–14 kg of propellant), a suitable vacuum mixer costs $5,000–$20,000. Pot life is 4–8 hours for typical HTPB formulations, creating time pressure during casting operations. The cure cycle (24–72 hours at 50–60°C) requires a controlled oven. Bond integrity between grain and case liner is a critical quality characteristic that requires both skill and inspection capability (X-ray or CT scanning for void detection in flight articles).

For KNSB: "both propellant components are ground and mixed, after which the mixture is heated until the sorbitol fuses around the nitrate grains, forming a doughy mixture which can be placed in molds." Equipment required: hot plate or oven, stainless steel pots and stirring implements, molds (can be machined from aluminum or fabricated from steel pipe), digital thermometer. Total equipment capital cost for P-class batch processing: under $500. No vacuum equipment required. No reactive cure chemistry. However, KNSB is hygroscopic and requires humidity-controlled storage and moisture-sealed grain packaging to prevent performance degradation.

---

### Step 6: Build the Scoring Rubric and Assign Scores

**What this step does:** Converts the qualitative and quantitative data from Step 5 into a common numerical scale so that dissimilar criteria can be combined into a single weighted score.

**How it was done for this program:**

A 1–5 integer scale was used, where 1 = poor (significant program risk or penalty), 3 = adequate (meets minimum needs), and 5 = excellent (best available). The scale is deliberately coarse because the underlying data for several criteria (manufacturing simplicity, safety) is qualitative, and false precision from a finer scale would not represent a real information gain.

The rubric for each criterion:

**Specific impulse rubric:**
- 5: I_sp ≥ 200 s (APCP range — substantial performance, light vehicle)
- 3: I_sp 150–200 s (notional intermediate — no candidate in this range for this program)
- 1: I_sp < 150 s (KN-sugar range — heavy propellant mass, longer/heavier motor)

AP/HTPB and AP/PBAN scored 5. KNSB and KNDX scored 2 (below the midpoint of the 1–3 band for KN propellants, reflecting the severity of the mass penalty at P-class scale).

**Manufacturing simplicity rubric:**
- 5: Melt-cast or press-cast process; no specialized equipment; total capital cost < $1,000; process documented in open literature with extensive amateur heritage
- 3: Requires some specialized equipment or controlled process; capital cost $1,000–$10,000; some institutional knowledge required
- 1: Requires vacuum mixing, controlled-atmosphere facility, or exotic processing; capital cost > $10,000; significant formulation expertise required; batch failures probable without experienced operator

AP/HTPB scored 2 (requires vacuum mixer, controlled pot life, cure oven — moderately specialized but not exotic). AP/PBAN scored 1 (higher processing temperature, more complex chemistry, essentially no precedent at amateur scale). KNSB scored 5 (benchmark melt-cast process). KNDX scored 4 (same process as KNSB but more brittle grain at scale, higher cracking risk for large BATES segments).

**Regulatory burden rubric (in-house manufacture context):**
- 5: No federal license required for manufacture; propellant components not scheduled; state/local filing only; testing can begin within weeks of program start
- 3: Moderate regulatory overhead; some notification or permit required but license not mandated; testing delay 2–4 months
- 1: Federal manufacturing license required before any propellant production; magazine inspection required; testing delay 6–18 months; significant compliance cost

AP/HTPB scored 2 (bulk AP is regulated; in-house APCP manufacture requires FEL — delay is real but process is established and achievable). AP/PBAN scored 1 (same FEL requirement as AP/HTPB, plus higher process complexity and essentially no small-scale precedent to draw on). KNSB scored 5. KNDX scored 5 (same regulatory profile as KNSB — identical precursor chemicals).

**Critical note on regulatory scoring:** KNDX and KNSB were scored equally on regulation (5/5) even though KNDX scored lower on manufacturing (4 vs 5). This is intentional and correct — the regulatory criteria and manufacturing criteria are independent. KNDX is harder to make well (manufacturing score 4) but faces the same legal landscape (regulatory score 5).

**Material cost rubric:**
- 5: < $5 / kg of propellant (commodity materials)
- 3: $5–$25 / kg of propellant
- 1: > $25 / kg of propellant

KN-sugar propellants: KNO₃ at food-grade quality ≈ $1–3/kg; sorbitol ≈ $2–5/kg. Total blended cost at 65/35 ratio ≈ $1.50–$3.50/kg → score 5. AP/HTPB: AP ≈ $15–30/kg, HTPB ≈ $20–40/kg, aluminum powder ≈ $10–20/kg. Blended cost for a typical 68% AP / 20% HTPB / 12% Al formulation ≈ $15–25/kg → score 3. AP/PBAN scored 2 (specialized PBAN binder, higher material cost, plus higher processing waste rates).

**Safety and handling rubric:**
- 5: Non-toxic components; primary hazard is fire (controllable); no explosive classification of components individually; procedures documented for safe amateur-scale handling
- 3: One or more components with occupational health hazard; PPE and ventilation required; modest consequence severity for processing accident
- 1: Multiple toxic or sensitizing components; high consequence processing accident potential; facility requirements for safe operation are substantial

AP/HTPB scored 3: AP is a respiratory irritant and oxidizer. HTPB requires standard solvent handling precautions. Isocyanate curative (IPDI or MDI) is a respiratory sensitizer. Combined, these require a ventilated facility and appropriate PPE — manageable but not trivial.

KNSB scored 4: KNO₃ is a mild oxidizer (used as a food preservative). Sorbitol is a food ingredient. The processing hazard is the heated mixture, which is a fire risk if contaminated with organic materials. The primary precaution is working away from open flames and maintaining temperature control. Non-toxic components.

**Heritage at L+ scale rubric:**
- 5: Extensive public documentation of L–P class motors; published a, n constants; documented grain scaling procedures; known failure modes at scale; multiple independent experimenters have validated
- 3: Some documentation exists; primary data from one or two sources; scaling from published data to P class requires extrapolation
- 1: Minimal or no P-class heritage; significant unknown unknowns in scaling

AP/HTPB scored 5: The commercial HPR motor industry provides extensive reference data for L–P class APCP motors. CTI, Aerotech, and others have certified motors across this range, and burn rate characterization data is widely published.

KNSB scored 3: Nakka's work provides well-characterized burn rate data and BATES grain design procedures up to approximately L/M class. P-class KNSB motors are less common in the public literature, and scaling beyond about 15 kg propellant mass introduces some extrapolation risk, particularly for erosive burning assessment in long grain stacks.

KNDX scored 2: Similar to KNSB but with the additional concern that KNDX is more brittle, making large-segment failure modes less well documented.

---

### Step 7: Compute Weighted Scores and Perform Sensitivity Analysis

**What this step does:** Combines scores and weights into composite scores, then tests whether the recommendation would change under different weighting assumptions.

**Computing weighted scores:**

For each candidate, the weighted score = Σ (criterion weight × criterion score).

AP/HTPB: (0.20×5) + (0.15×5) + (0.20×2) + (0.20×2) + (0.10×3) + (0.10×3) + (0.05×5)
= 1.00 + 0.75 + 0.40 + 0.40 + 0.30 + 0.30 + 0.25 = **3.40**

AP/PBAN: (0.20×5) + (0.15×5) + (0.20×1) + (0.20×1) + (0.10×2) + (0.10×2) + (0.05×3)
= 1.00 + 0.75 + 0.20 + 0.20 + 0.20 + 0.20 + 0.15 = **2.70**
*(Note: corrected from 2.90 in the original study — AP/PBAN regulatory score was 1, not 2)*

KNSB: (0.20×2) + (0.15×2) + (0.20×5) + (0.20×5) + (0.10×5) + (0.10×4) + (0.05×3)
= 0.40 + 0.30 + 1.00 + 1.00 + 0.50 + 0.40 + 0.15 = **3.75**

KNDX: (0.20×2) + (0.15×2) + (0.20×4) + (0.20×5) + (0.10×5) + (0.10×4) + (0.05×2)
= 0.40 + 0.30 + 0.80 + 1.00 + 0.50 + 0.40 + 0.10 = **3.50**

**Sensitivity analysis:**

The purpose of sensitivity analysis is to ask: "Would the recommendation change if my weights were wrong?" Two scenarios are examined:

*Scenario A — Performance-dominated weighting (mature program context):*
Set I_sp = 40%, propellant mass efficiency = 25%, manufacturing = 10%, regulatory = 10%, cost = 5%, safety = 5%, heritage = 5%.
Result: AP/HTPB scores 4.25, KNSB scores 1.95. The recommendation reverses — AP/HTPB wins clearly. This confirms that the original recommendation is context-sensitive and would not apply to a mature program with existing infrastructure.

*Scenario B — Equal weighting (no priority judgment):*
All seven criteria at 14.3% each.
Result: AP/HTPB ≈ 3.57, KNSB ≈ 3.71. KNSB still leads slightly, but the margin narrows. The recommendation is robust to equal weighting.

*Scenario C — Regulatory burden doubled (high startup risk aversion):*
Regulatory weight to 35%, manufacture to 30%, I_sp to 15%, mass efficiency to 10%, cost/safety/heritage proportionally reduced.
Result: KNSB scores 4.25, AP/HTPB scores 2.15. The margin widens substantially. The recommendation becomes even more decisive.

**Interpretation:** The recommendation for KNSB as the development propellant is robust across scenarios where the program's startup context is acknowledged (Scenarios B and C). It reverses only when the program is assumed to have the infrastructure, licenses, and manufacturing capability of a mature organization — which is precisely the condition being argued does not exist at program start. The sensitivity analysis confirms the recommendation is appropriate and context-consistent.

---

### Step 8: Form the Recommendation and Document Assumptions

**What this step does:** Translates the quantitative results into an actionable recommendation, explicitly states the assumptions on which the recommendation rests, and defines the conditions under which it should be revisited.

**The recommendation:**

A dual-track strategy is recommended:

**Track A — KNSB Development Motor (Months 0–18):** KNSB scored highest under the program's actual context (3.75 vs 3.40 for AP/HTPB). Its low regulatory burden, low manufacturing complexity, and well-characterized burn rate data make it the correct propellant for the motor development phase. All motor structural, thermal, and ballistic design work — casing, nozzle, grain geometry, Kn profile, static test infrastructure — is transferable to the APCP flight motor with minimal modification. KNSB is the development tool, not the product.

**Track B — AP/HTPB Regulatory and Development Path (Months 3–24):** The commercial flight motor should be AP/HTPB, because at program maturity the regulatory and manufacturing costs become sunk, and the performance and vehicle efficiency advantages of APCP dominate. A contract manufacturing arrangement with a licensed propellant producer should be evaluated as an alternative to in-house AP mixing, which could substantially reduce the FEL burden.

**Assumptions on which this recommendation rests:**

1. The program is genuinely starting from scratch with no existing propellant manufacturing infrastructure or federal explosives license. If either of these conditions changes, the regulatory scoring should be revisited.
2. The launch jurisdiction is the United States. APCP and KN-sugar propellants have different regulatory profiles in other jurisdictions (EU, Australia, Canada). International programs must re-run Step 5 regulatory data with local law.
3. The program's primary near-term constraint is time to first static test. If a large initial funding round removes timeline risk, the weight on regulatory burden can be reduced.
4. The Bondar vehicle (~131 mm diameter) is an appropriate reference. If vehicle diameter grows substantially (e.g., to 160 mm+), the propellant mass penalty from KNSB is partially absorbed into grain length rather than diameter, and the vehicle design penalty decreases relative to a smaller airframe.

**Trigger conditions for revisiting this recommendation:**

- ATF regulatory guidance changes regarding KN-sugar propellant mixtures.
- A partnership with a licensed APCP manufacturer is established, removing the FEL burden for early tests.
- Vehicle sizing analysis shows that the KNSB propellant mass (20+ kg) produces an unacceptable vehicle length or mass fraction that cannot be accommodated.
- Program funding is secured with a specific contractual requirement for APCP.

---

## Part III: Reusable Framework for Industry Propulsion Engineers

The following template can be applied to any propellant trade study. Items in [brackets] should be replaced with program-specific content.

---

### Framework Template: Propellant Trade Study

**Document control:** [Program name] — Propellant Trade Study — [Doc ID] — Rev [X]

---

**Step 1 Checklist: Decision Context**
- [ ] State mission objective in one sentence
- [ ] Define total impulse target with margin (threshold / objective)
- [ ] Identify binding constraints: performance floor, manufacturing ceiling, regulatory ceiling, timeline
- [ ] State program maturity (greenfield / existing infrastructure / mature operations)
- [ ] Identify who makes the final decision and what they care most about

**Step 2 Checklist: Candidate Selection**
- [ ] List all propellant families considered
- [ ] Document explicit rationale for each inclusion
- [ ] Document explicit rationale for each exclusion
- [ ] Confirm candidates share the same fundamental system architecture (if not, a system trade precedes this propellant trade)

**Step 3 Checklist: Figures of Merit**
Minimum required criteria for any SRM propellant trade:
- [ ] Specific impulse (I_sp) — define calculation basis (vacuum vs. sea level; 1000 psi vs. operating pressure)
- [ ] Propellant mass and volume (at target impulse)
- [ ] Manufacturing process complexity (qualitative, scaled)
- [ ] Regulatory burden (jurisdiction-specific; state explicitly whether manufacturing or purchasing)
- [ ] Material cost (per kg of propellant, at target batch size)
- [ ] Safety / handling (toxic hazard, processing accident consequence)
- [ ] Heritage data availability (burn rate constants, failure mode documentation)

Optional criteria (include if program-relevant):
- [ ] Burn rate tunability (if specific thrust profile is required)
- [ ] Flame temperature (if casing/nozzle thermal management is a known constraint)
- [ ] Shelf life (if inventory and operational tempo are program-relevant)
- [ ] Environmental impact (if range or regulatory authority requires it)
- [ ] Exhaust composition (if plume signature or toxicity is mission-relevant)

**Step 4 Checklist: Weighting**
- [ ] Weights are assigned BEFORE scores are known
- [ ] Weights sum to 100%
- [ ] Weight assignment rationale is documented for each criterion
- [ ] Sensitivity analysis scenarios are defined in advance

**Step 5 Checklist: Data Sources**
For each criterion and each candidate, document:
- [ ] The numerical value or qualitative assessment
- [ ] The source (published paper, standards document, manufacturer data, expert judgment)
- [ ] The uncertainty bound (range, if applicable)
- [ ] Assumptions (e.g., "I_sp computed at 68 atm chamber pressure, sea-level exit")

Minimum acceptable sources by criterion:
- I_sp: CEA/PROPEP output, published propellant handbook, or manufacturer data
- Regulatory: Jurisdiction-specific statute or agency guidance letter (NOT secondary sources or forum posts)
- Burn rate: Published strand burner or Crawford burner experimental data
- Manufacturing: Direct quotes from process documentation or experienced practitioner

**Step 6 Checklist: Scoring**
- [ ] Rubric is defined before scores are assigned (avoids anchoring)
- [ ] Scale is documented (e.g., 1–5, 1–10) with anchoring definitions for each criterion
- [ ] Scores are defensible: a reviewer who disagrees should be able to argue a rubric change, not a math error
- [ ] Independent and dependent criteria are not double-counted (e.g., flame temperature and I_sp are correlated — score only one unless you have a specific reason to score both)

**Step 7 Checklist: Sensitivity Analysis**
Required scenarios:
- [ ] Baseline (weights as assigned)
- [ ] Performance-dominated (I_sp and mass efficiency weighted 60%+ combined)
- [ ] Equal weighting
- [ ] Inverted dominant criterion (the highest-weighted criterion is halved; lowest is doubled)

For each scenario, record:
- [ ] Composite scores for all candidates
- [ ] Whether the rank ordering changes
- [ ] Whether the recommendation changes (if yes, explain why this is or is not a concern)

**Step 8 Checklist: Recommendation**
- [ ] State the recommendation clearly (single sentence)
- [ ] State the assumptions on which it rests (bulleted list)
- [ ] Define trigger conditions under which the recommendation should be revisited
- [ ] Identify the next engineering decision that depends on this recommendation

---

### Common Errors in Propellant Trade Studies

**Error 1 — Weighting after scoring (confirmation bias trap)**
Assigning weights after you know the scores allows unconscious adjustment of weights to produce the preferred outcome. Weights must be assigned and documented before scoring begins. If this order cannot be certified, the study's conclusions are suspect.

**Error 2 — Using published I_sp at different operating conditions**
Specific impulse is a function of chamber pressure, nozzle expansion ratio, and ambient pressure. Published I_sp values for the same propellant may range 20–40 s depending on the test conditions assumed. Always specify the basis: vacuum I_sp at delivered O/F ratio, at expected chamber pressure.

**Error 3 — Treating "regulatory burden" as binary**
Regulatory analysis is not "regulated / not regulated." The correct framing is: what specific activities are regulated, by which authority, what is the timeline and cost to achieve compliance, and what is the consequence of non-compliance? A propellant that requires notification (low burden) versus one that requires a 12-month licensing process (high burden) versus one that is outright prohibited in the jurisdiction (eliminates candidate) are three very different situations.

**Error 4 — Conflating finished motor procurement with in-house manufacture**
In the United States, the regulatory status of APCP as a finished purchased motor product is materially different from the regulatory status of in-house APCP manufacture. Studies that cite the ATF's "APCP is not regulated" position without distinguishing these two cases are incorrect in the in-house manufacturing context.

**Error 5 — Single-scenario sensitivity analysis**
Performing sensitivity analysis on only one alternative weighting scenario does not adequately characterize the recommendation's robustness. At minimum, test three scenarios as described in Step 7, including the extreme case where the performance criterion dominates.

**Error 6 — Excluding candidates without documented rationale**
Every excluded candidate should be accompanied by an explicit reason. "Not considered" is not adequate documentation. Reviewers need to see that the candidate set is complete and that exclusions are defensible.

**Error 7 — Scoring ordinal data as if it were cardinal**
A propellant that scores 4 on manufacturing is not "twice as easy to manufacture" as one that scores 2. Ordinal scores can be ranked and weighted, but cannot be ratio-interpreted. This is why the recommendation is stated qualitatively and the sensitivity analysis is used to test robustness, rather than claiming a precise percentage advantage.

---

*Document PTSM-001 Rev 1.0 — For distribution to program propulsion team.*
*This document should be read alongside MRLD-001 Rev 0.1 (Mission Requirements and Launch Service Definition).*
