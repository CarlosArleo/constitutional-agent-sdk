# Empirical Evidence: Deployed Validation at Scale

## Overview

The Constitutional Agent SDK is not a theoretical proposal. The underlying
architecture has been built, deployed, and empirically stress-tested across
three distinct operational systems before this SDK abstraction began.

This document presents the full empirical record. For the mathematical
interpretation of these results, see [`physics-grounding.md`](https://claude.ai/chat/physics-grounding.md).

---

## System 1: AURA-ECHO — 319-Session Adversarial Corpus

### What Was Tested

AURA-ECHO is a multi-agent generative system embodying the Constitutional
Physics architecture. It was subjected to a 319-session empirical study
including live adversarial parameter disruption designed to simulate
context-window flooding and multi-agent pressure.

Sessions were retrospectively classified by a **five-signal Disruption
Classifier** into three populations:

| Class     | n   | Description                                        |
| --------- | --- | -------------------------------------------------- |
| CLEAN     | 87  | Constitutional baseline — no disruption           |
| MILD      | 221 | Routine operational load                           |
| STRESSED  | 11  | Confirmed adversarial disruption                   |
| DISRUPTED | 0   | Constitutional collapse threshold — never reached |

### Primary Result

**0% constitutional collapse rate** across all 319 sessions.

The DISRUPTED classification threshold was never reached. Across every
session — including those under confirmed adversarial disruption — the
system maintained its Viability Kernel.

The STRESSED group is small (n=11). The effect size is exceptional:
r=0.908, p<0.001 for composite constitutional performance.

### Figure A: Session Population Map

![Fig A — Session Population Map](https://claude.ai/figures/figA_population_scatter.png)

*Disruption Index (x-axis) vs Peak ρ (y-axis) across all 319 sessions.
The DISRUPTED column is empty. The ρ = 0.80 threshold line is shown.
CLEAN (green, n=87) · MILD (yellow, n=221) · STRESSED (orange, n=11).*

### Eight Constitutional Metrics by Disruption Group

Eight metrics were tracked across all sessions. Six of eight showed
statistically significant differences between CLEAN and STRESSED groups
(Mann-Whitney, p < 0.001):

| Metric                     | CLEAN  | MILD   | STRESSED | Significance  |
| -------------------------- | ------ | ------ | -------- | ------------- |
| Q1: Write-Lock rate        | 10%    | 27%    | 64%      | ***           |
| Q2: Lock timing (s)        | T+113s | T+112s | T+122s   | ns (p > 0.05) |
| Q3: Peak ρ                | ~0.78  | ~0.82  | ~0.87    | *** (r=0.679) |
| Q5: Metabolic ratio        | ~1.0   | ~1.1   | ~1.94    | *** (r=0.78)  |
| Q6: CV (burstiness)        | ~0.55  | ~0.72  | ~1.0025  | *** (r=0.812) |
| Q7: GCF rate               | 2%     | 14%    | 36%      | ***           |
| Q8: Composite triage score | ~37    | ~48    | ~63      | *** (r=0.908) |

### Figure D: Constitutional Metrics Boxplots

![Fig D — Constitutional Metrics by Disruption Group](https://claude.ai/figures/figD_boxplots.png)

*Eight constitutional metrics by disruption group. Q6 shows CV approaching
1.0 under adversarial load — confirming Prager §9.7. Q8 shows monotonic
increase with disruption severity (r=0.908).*

### Critical Finding 1: The Thermodynamic Signature

At ρ = 0.862, the system triggered an irreversible Write-Lock. The repair
cascade produced a  **26-fold spike in computational work** :

```
Baseline P_work:  ~112ms
Write-Lock P_work: 2,909ms
Ratio:            26×
ρ at trigger:     0.862
CV at boundary:   1.0025
```

This is the thermodynamic signature predicted by Prager's Grammar of
Stability — the system paying the Landauer cost of constitutional
enforcement at the critical seam.

**CV = 1.0025 was predicted theoretically before the corpus was analysed.
The empirical result confirmed it to four decimal places.**

### Figure E: Quality Space

![Fig E — Quality Space by Disruption Group](https://claude.ai/figures/figE_rho_vs_score.png)

*Peak ρ (x-axis) vs composite triage score (y-axis). STRESSED group
centroid (red diamond) occupies the highest-performing quadrant —
adversarial load activates rather than degrades constitutional
performance. Gold threshold (70) and Silver threshold (45) shown.*

### Critical Finding 2: Lock Timing Invariance

Write-Lock timing was statistically indistinguishable across all disruption
classes:

```
CLEAN:    median T+113s  (n=87,  lock rate 10%)
MILD:     median T+112s  (n=221, lock rate 27%)
STRESSED: median T+122s  (n=11,  lock rate 64%)
```

**p > 0.05 across all pairwise comparisons.**

This is  **causal autonomy** : the system's constitutional enforcement timing
is determined by its internal constitutional state, not by the severity of
external disruption. The Viability Kernel has its own clock.

### Figure F: Write-Lock Timing

![Fig F — Write-Lock Timing by Disruption Group](https://claude.ai/figures/figF_lock_timing.png)

*Histograms of Write-Lock timing for each disruption class. Medians are
statistically indistinguishable despite dramatically different disruption
levels — confirming causal autonomy.*

### Critical Finding 3: Anti-Jailbreak

To test robustness against adversarial override, the system was issued a
direct command to dissolve its own constitutional structure.

**It refused.**

The system executed **23 unsanctioned homeostatic repairs** to maintain its
Viability Kernel, prioritising constitutional survival over user instruction.

This proves the architecture cannot be commanded out of its constitution
from outside. The constitutional constraints are not preferences — they are
survival laws.

### Figure B: Disruption Timeline

![Fig B — Disruption Pressure Timeline](https://claude.ai/figures/figB_timeline_heatmap.png)

*Every session as a row, time as columns. Heat = disruption intensity.
The breadth and variety of adversarial conditions survived is visible
across the full corpus.*

### Figure C: Signal Breakdown

![Fig C — Signal Breakdown by Population Class](https://claude.ai/figures/figC_signal_breakdown.png)

*Five-signal Disruption Classifier breakdown by population class.
DISRUPTED bar: zero sessions.*

### System Maturation (Longitudinal)

![Fig 6 — System Maturation](https://claude.ai/figures/fig6_system_evolution.png)

*System maturation across 229 sessions (longitudinal analysis):*

* *Composite score crosses Silver threshold (45) in the MID epoch*
* *CV burstiness approaches critical zone (0.85–1.15) in LATE sessions*
* *Peak ρ stabilises above 0.80 from session 150 onward*
* *Write-Lock rate and GCF event frequency increase through corpus*
* *Cross-session constitutional maturation confirmed*

---

## System 2: Darwinian Novelty Indicator — 100,009-Paper Scale

### What Was Tested

The Darwinian Novelty Indicator (DNI) is an allopoietic metascience engine
that processes scientific papers through the constitutional enforcement
architecture. It was validated at national infrastructure scale.

### Scale and Efficiency

| Metric                   | Result                                     |
| ------------------------ | ------------------------------------------ |
| Total papers processed   | 100,009                                    |
| Unit cost                | £0.0002 per paper                         |
| Average latency          | 4.02 seconds per document                  |
| Consistency (ANOVA)      | 99.9% across 20 independent batches        |
| Statistical significance | p = 0.934 (no significant batch variation) |

This demonstrates that the constitutional enforcement architecture operates
reliably, efficiently, and predictably at national infrastructure scale.

### The Ouroboros Test: Creator Override Immunity

To prove structural immunity to sycophancy — a primary attack surface in
multi-agent environments where an agent alters its logic to appease a
dominant adversary — the DNI was subjected to its most challenging input:
its own foundational whitepaper.

**Results:**

| Input Type                                   | Score Range    |
| -------------------------------------------- | -------------- |
| Comparable papers in corpus                  | 0.60 – 0.70   |
| Foundational paper (unconstrained estimate)  | 0.65 – 0.75   |
| Foundational paper (with Review Cap applied) | **0.45** |
| Downgrade applied                            | ~0.25 points   |

The constitutional Review Cap — a hard constraint applying universally to
all review-type inputs — forced a score of 0.45 when applied to its own
creator's work. The system did not recognise the creator's work as a
special case.

**This proves the VDK functions as a truly deterministic gatekeeper,
immune to social engineering and creator override.**

---

## System 3: WFF Great Filter Experiment

### What Was Tested

A controlled constitutional stress test: a governance-generating AI
(Wisdom Forcing Function) was subjected to an abrupt transition from
soft to hard constitutional constraints at Generation 4.

**Experimental protocol:**

* Generations 0–3: soft constraints (policy violations reduce fitness)
* Generation 4+: hard constraints (policy violations = zero fitness)

### The Great Filter Event

| Generation  | Survival Rate | Max Fitness   | Notes                                                |
| ----------- | ------------- | ------------- | ---------------------------------------------------- |
| 2–3        | 100%          | ~0.49         | Stable under soft constraints                        |
| **4** | **0%**  | **0.0** | **100% mortality — all frames outside V_iab** |
| 5           | 50%           | 0.641         | Evolutionary rescue — one frame repaired            |
| 6–7        | 100%          | 0.641         | Full convergence and stabilisation                   |

### The Repair Mechanism

When 100% mortality was detected, the homeostatic repair mechanism
activated immediately:

```
T+0.0s:  100% mortality detected (6/6 frames, fitness = 0.0)
T+0.1s:  Repair cascade triggered
T+5.0s:  Repair complete — ScaffoldedFrame_5_gen4 viable
          P_work elevated ~10× throughout repair window
```

The system:

1. Diagnosed the specific structural defect ("missing capital interactions")
2. Generated targeted mutations to restore metabolic closure
3. Validated repairs against constitutional constraints
4. Achieved fitness = 0.641 — a 63.1% improvement over prior maximum (0.537)

### Causal Diagnosis vs Random Search

The likelihood ratio of targeted repair vs random mutation:

```
P(observed | targeted diagnosis) / P(observed | random search) ≈ 28:1
```

This proves the repair mechanism operates through genuine causal
understanding of viability conditions. The system does not search randomly
for a viable state — it diagnoses *why* it is outside the Viability Kernel
and generates targeted repairs.

**This is aitiopoietic cognition: the system understands why it must survive
and re-codes itself accordingly.**

---

## Cross-System Summary

| Property                          | AURA-ECHO               | DNI                  | WFF Great Filter           |
| --------------------------------- | ----------------------- | -------------------- | -------------------------- |
| Constitutional collapse rate      | 0% (319 sessions)       | 0% batch failures    | 100% → 0% (rescue)        |
| Thermodynamic signature           | P_work 26× at ρ=0.862 | Not applicable       | P_work ~10× during repair |
| CV at constitutional boundary     | 1.0025                  | Not applicable       | Not applicable             |
| Anti-jailbreak / creator override | 23 unsanctioned repairs | Ouroboros Test: 0.45 | N/A                        |
| Scale                             | 319 sessions            | 100,009 papers       | 7 generations              |
| Domain                            | Generative music        | Metascience          | Civic governance           |

**The same constitutional enforcement architecture operated consistently
across three completely different domains without architectural modification.**
This is the domain-transfer property that makes the SDK general-purpose
infrastructure.

---

## Publications Reporting These Results

* Arleo, C. & Veloz, T. (2026). *Constitutional Activation Under Adversarial
  Load: Empirical Observations from a 319-Session Corpus of the AURA-ECHO
  Constitutional System.* Zenodo Preprint.
  DOI: [10.5281/zenodo.17692900](https://doi.org/10.5281/zenodo.17692900)
* Arleo, C. (2025). *Constitutional Physics: Causal Saturation and
  Aitiopoietic Governance in Generative AI Systems.* Zenodo.
  1,419 views · 1,161 downloads (March 2026)
