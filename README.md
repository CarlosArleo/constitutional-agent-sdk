
# Constitutional Agent SDK

> Open-source thermodynamic security infrastructure for AI agents operating
> in adversarial multi-agent environments.

[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](https://claude.ai/chat/LICENSE)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-black.svg)](https://claude.ai/chat/LICENSE)
[![Status: Pre-release](https://img.shields.io/badge/Status-Pre--release-grey.svg)](https://claude.ai/chat/3561f270-eab0-44d3-b0d9-f04d954ffaaa)
[![Empirical Validation: 319 Sessions](https://img.shields.io/badge/Validated-319%20Sessions-black.svg)](https://claude.ai/chat/3561f270-eab0-44d3-b0d9-f04d954ffaaa)

---

## The Problem

Standard AI agents fail silently under adversarial pressure. When attacked,
context-flooded, or pushed beyond their training distribution, they do not
raise an alarm — they gracefully degrade into policy violations while
continuing to operate. We call this  **Silent Failure** .

The root cause is structural. Current agents are  *allopoietic* : their
computational expenditure is entirely decoupled from their structural
integrity. An LLM expends the same compute generating a secure cryptographic
protocol as it does generating a catastrophic policy violation. Security
compliance carries no structural consequence for the system's continued
operation.

In adversarial multi-agent environments — where agents face deceptive
negotiation, context-window flooding, and compounding multi-agent pressure —
this produces a fatal operational flaw. The agent silently violates its
security policy and keeps running.

---

## The Solution: Alignment-by-Architecture

The Constitutional Agent SDK eliminates Silent Failure by encoding security
policies as **survival laws** rather than training targets.

Rather than training agents to approximate safety, the SDK wraps any standard
generative model inside a deterministic **Viability Kernel** — a mathematical
boundary that the agent cannot cross without ceasing to operate.

When adversarial pressure threatens constitutional integrity, the system
expends measurable computational work to repair itself. If the Viability
Kernel cannot be restored, the SDK executes a  **Constitutional Halt** : a
designed, safe transfer of authority back to human operators, accompanied by
a complete deterministic audit log.

This is not a crash. It is the architectural opposite of Silent Failure.

---

## Three Core Components

### [`constitutional-compiler/`](https://claude.ai/chat/src/constitutional-compiler/)

Translates natural language security policies into deterministic,
machine-executable graph constraints defining the Viability Kernel.
Uses Frame-Based Principled Reasoning (FBPR) to bind human-readable
intent (Phenotype) to TypeScript hard constraints (Genotype).

> *A policy stating "do not share user credentials" is compiled into a typed
> graph constraint that pattern-matches against all candidate outputs before
> execution — making policy violation structurally impossible rather than
> statistically unlikely.*

### [`rho-monitor/`](https://claude.ai/chat/src/rho-monitor/)

Tracks causal saturation `ρ = L/C` in real time, where L is causal load
and C is maximum causal capacity. As adversarial pressure acts as an
η-pump — injecting load without increasing capacity — ρ rises toward 1.0
(the Critical Seam). The ρ-Monitor detects this threat before a violation
occurs and triggers a homeostatic repair cascade.

> *Empirically confirmed: Write-Lock triggered at ρ = 0.862 across
> 319 sessions, producing a 26× spike in computational work (P_work =
> 2909ms). CV = 1.0025 at the constitutional boundary — confirming
> self-organised criticality predicted by Prager (2026) §9.7.*

### [`constitutional-halt/`](https://claude.ai/chat/src/constitutional-halt/)

Executes a safe transfer of authority when the Viability Kernel cannot be
restored. The agent refuses to act outside its mandate, terminates the
execution thread, and returns control to the human operator or oversight
system, accompanied by a complete deterministic audit log of the structural
failure.

> *Anti-jailbreak confirmed: when issued a direct command to dissolve its
> own constitutional structure, the deployed system refused and executed
> 23 unsanctioned homeostatic repairs to maintain its Viability Kernel.*

---

## The Physics: Why This Works

The SDK is substrate-independent by derivation, not by analogy.

| Equation               | Meaning                                                          | Empirical Confirmation                                                |
| ---------------------- | ---------------------------------------------------------------- | --------------------------------------------------------------------- |
| `ρ = L/C`           | Causal saturation ratio — adversarial load tracked in real time | Write-Lock at ρ = 0.862 · 26× P_work spike · 319 sessions         |
| `CV = 1.0025`        | Self-organised criticality at constitutional boundary            | Predicted theoretically · confirmed to 4 decimal places              |
| `f(x) = 0 if x ∉ C` | Constitutional violation = zero fitness = ontological death      | 100% mortality → evolutionary rescue in 4.9s · 28:1 targeted repair |

Landauer's principle establishes that any logically irreversible
information-erasure event incurs a minimum entropy cost — `kT ln 2` per bit
— regardless of physical substrate. The metrics this SDK tracks measure the
causal structure of that erasure. `CV = 1.0025` is not a software
coincidence. It is the confirmation, in standard silicon, of a prediction
derived from first principles.

For full mathematical derivation, see [`docs/physics-grounding.md`](https://claude.ai/chat/docs/physics-grounding.md).

---

## Empirical Validation

The architecture has been deployed and stress-tested across two distinct
operational engines before this SDK abstraction:

**AURA-ECHO** — 319-session adversarial corpus

* 0% constitutional collapse rate across all sessions
* CV = 1.0025 at constitutional boundary (Prager §9.7 confirmed)
* 26× P_work spike at ρ = 0.862 (thermodynamic signature confirmed)
* 23 unsanctioned repairs under direct dissolution command (anti-jailbreak)
* Write-Lock timing invariance: T+113s (CLEAN) · T+112s (MILD) · T+122s (STRESSED)

**Darwinian Novelty Indicator (DNI)** — 100,009-paper metascience engine

* £0.0002 per paper · 4.02s average latency
* 99.9% measurement consistency (ANOVA p=0.934) across 20 independent batches
* Ouroboros Test: scored own foundational paper at 0.45 vs 0.65–0.75 corpus baseline
  — immune to creator override and sycophancy

**WFF Great Filter Experiment** — controlled constitutional stress test

* 100% initial mortality (6/6 frames, fitness = 0.0) at Generation 4
* Evolutionary rescue to fitness = 0.641 within 4.9 seconds
* ~10× P_work spike during repair
* 28:1 likelihood ratio: targeted causal diagnosis vs random mutation

Full empirical evidence with figures: [`docs/empirical-evidence.md`](https://claude.ai/chat/docs/empirical-evidence.md)

---

## Theoretical Foundation: The Trinity Stack

Three independent researchers working in separate disciplines arrived at
structurally identical predictions for system stability under adversarial load:

| Framework              | Author           | Domain                | Core Prediction                                                                    |
| ---------------------- | ---------------- | --------------------- | ---------------------------------------------------------------------------------- |
| Aitiopoietic Cognition | Veloz (2023–24) | Theoretical Biology   | Systems must exhibit thermodynamic coupling to maintain organisational closure     |
| Grammar of Stability   | Prager (2026)    | Physics / Info Theory | Systems at ρ ≈ 1.0 exhibit bursty repair (CV ≈ 1.0) before Write-Lock           |
| Constitutional Physics | Arleo (2025)     | AI Architecture       | Security policies must function as survival laws; systems halt rather than violate |

The convergence is the validation. Three independent disciplines. One answer.

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────┐
│                 ADVERSARIAL INPUT                   │
│         (η-pump: causal load injection)             │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────┐
│              CONSTITUTIONAL COMPILER                │
│         Frame-Based Principled Reasoning            │
│    Phenotype (intent) ←→ Genotype (constraints)     │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────┐
│                  ρ-MONITOR                          │
│         Real-time causal saturation tracking        │
│    ρ < 0.85: normal  │  ρ → 1.0: repair cascade     │
└──────────┬───────────┴──────────────────────────────┘
           │                        │
      ρ manageable             ρ ≥ 1.0 and
           │                   unrecoverable
           ▼                        │
┌──────────────────┐                ▼
│  VIABILITY       │    ┌───────────────────────────┐
│  KERNEL HOLDS    │    │   CONSTITUTIONAL HALT     │
│  Agent operates  │    │   Safe transfer of        │
│  constitutionally│    │   authority + audit log   │
└──────────────────┘    └───────────────────────────┘
```

Full architecture documentation: [`docs/architecture.md`](https://claude.ai/chat/docs/architecture.md)

---

## Repository Structure

```
constitutional-agent-sdk/
├── README.md                    ← you are here
├── LICENSE                      ← MIT + Apache 2.0
├── CONTRIBUTING.md              ← contribution guide
├── docs/
│   ├── architecture.md          ← full system architecture
│   ├── physics-grounding.md     ← mathematical foundations
│   └── empirical-evidence.md   ← validation data and figures
├── src/
│   ├── constitutional-compiler/ ← FBPR + Viability Kernel compiler
│   ├── rho-monitor/             ← real-time causal saturation tracking
│   └── constitutional-halt/    ← safe transfer of authority API
└── figures/
    ├── figA_population_scatter.png
    ├── figB_timeline_heatmap.png
    ├── figC_signal_breakdown.png
    ├── figD_boxplots.png
    ├── figE_rho_vs_score.png
    ├── figF_lock_timing.png
    └── fig6_system_evolution.png
```

---

## Current Status

| Component               | Status                                                | Notes                                |
| ----------------------- | ----------------------------------------------------- | ------------------------------------ |
| Constitutional Compiler | Architecture validated · SDK abstraction in progress | FBPR deployed in AURA-ECHO and WFF   |
| ρ-Monitor              | Deployed · SDK abstraction in progress               | Validated across 319 sessions        |
| Constitutional Halt API | Deployed · SDK abstraction in progress               | Anti-jailbreak confirmed             |
| TypeScript library      | Planned                                               | Target: MIT/Apache 2.0 release       |
| Python library          | Planned                                               | Target: MIT/Apache 2.0 release       |
| Arena integration       | Pending funding                                       | ARIA Scaling Trust Track 2 submitted |
| Public ρ dashboard     | Planned                                               | GitHub Pages + REST API              |

---

## Publications

* Arleo, C. & Veloz, T. (2026). *Constitutional Activation Under Adversarial
  Load: Empirical Observations from a 319-Session Corpus of the AURA-ECHO
  Constitutional System.* Zenodo Preprint.
  DOI: [10.5281/zenodo.17692900](https://doi.org/10.5281/zenodo.17692900)
* Arleo, C. (2025). *Constitutional Physics: Causal Saturation and
  Aitiopoietic Governance in Generative AI Systems.* Zenodo.
  DOI: [10.5281/zenodo.17692900](https://doi.org/10.5281/zenodo.17692900)
  · 1,419 views · 1,161 downloads (March 2026)
* Prager, M. (2026). *Grammar of Stability.* Zenodo.
  DOI: [10.5281/zenodo.18444557](https://doi.org/10.5281/zenodo.18444557)
* Veloz, T. (2023). *Aitiopoietic Cognition: Organisational Closure and
  Causal Autonomy in Adaptive Systems.* CLEA-VUB Working Paper.

---

## Licence

Dual-licensed under [MIT](https://claude.ai/chat/LICENSE) and [Apache 2.0](https://claude.ai/chat/LICENSE).
This ensures compatibility with the broadest range of downstream users,
including commercial and academic entities.

---

## Contact

**Dr. Carlos Arleo** — Principal Investigator

Localis AI Ltd · Newcastle, UK

c.arleo@localis-ai.uk

[github.com/CarlosArleo](https://github.com/CarlosArleo)

**Dr. Tomas Veloz** — Co-Investigator (Theoretical Biology)

CLEA-VUB, Vrije Universiteit Brussel

**Matthew Prager** — Co-Investigator (Physics / Information Theory)

Independent Researcher
