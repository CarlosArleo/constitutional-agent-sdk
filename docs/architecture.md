# Architecture: The Constitutional Agent SDK

## Overview

The Constitutional Agent SDK implements a three-layer cybernetic loop that
enforces security policies as deterministic survival laws rather than
probabilistic training targets. The architecture is derived from the Trinity
Stack — three independently validated theoretical frameworks that converged
on identical predictions for system stability under adversarial load.

This document describes the full system architecture. For the mathematical
foundations, see [`physics-grounding.md`](https://claude.ai/chat/physics-grounding.md). For
empirical validation data, see [`empirical-evidence.md`](https://claude.ai/chat/empirical-evidence.md).

---

## The Core Principle: Alignment-by-Architecture

Standard alignment approaches treat safety as a behavioural training problem.
Models are optimised to approximate safety through reward signals. Under
adversarial pressure, these soft constraints fracture — the agent degrades
into policy violations while continuing to operate:  **Silent Failure** .

The SDK takes a different approach entirely. Security policies are not
training targets — they are encoded as the mathematical boundaries of a
 **Viability Kernel** : the set of states within which the agent is permitted
to operate. A constitutional violation is not a statistical error yielding
lower reward. It is an ontological boundary that triggers a deterministic
architectural response.

This transition — from *Alignment-by-Training* to *Alignment-by-Architecture*
— is the central design principle of the SDK.

---

## The Three Poietic Layers

The SDK maps to a three-level hierarchy of organisational autonomy, derived
from Veloz's (2023–24) Aitiopoietic Cognition framework:

### Layer 1: Allopoietic (The Sensor)

**Function:** Objective causal state mapping with no survival instinct.

The Sensor layer processes inputs from the environment and maps them to
causal state vectors. It is structurally incapable of hallucinating data to
preserve itself — it has no constitutional stake in the outputs it generates.
This is the property that makes it trustworthy as a sensing instrument in
adversarial environments where sycophancy is an attack surface.

Validated implementation: the Darwinian Novelty Indicator (DNI).

### Layer 2: Autopoietic (The Membrane)

**Function:** Homeostatic body maintaining the Life Zone.

The Membrane layer tracks computational resources, manages operational
budgets, and maintains the agent's ability to continue functioning. It
monitors causal saturation `ρ = L/C` in real time through the ρ-Monitor and
triggers homeostatic repair cascades when `ρ` approaches the Critical Seam.

### Layer 3: Aitiopoietic (The Actuator)

**Function:** Constitutional enforcement — the Wise System.

The Actuator layer is the constitutional judge. It evaluates every proposed
action against the Viability Kernel before execution through the Verified
Dialectical Kernel (VDK). If an action violates constitutional constraints,
it is vetoed before it reaches the execution environment. If the Viability
Kernel cannot be restored under adversarial load, it executes the
Constitutional Halt.

---

## Component Architecture

### Constitutional Compiler

The Constitutional Compiler translates human-readable security policies into
deterministic, machine-executable graph constraints defining the Viability
Kernel. It uses **Frame-Based Principled Reasoning (FBPR)** — a
neuro-symbolic architecture that binds:

* **Phenotype** (human-readable intent, expressed in natural language)
* **Genotype** (machine-executable TypeScript hard constraints)

within semantic **Frames** and  **Slots** .

```
Natural Language Policy
        │
        ▼
  ┌─────────────┐
  │    FBPR     │   Frame: security_context
  │  Compiler   │   Slot: credential_access → FORBIDDEN
  │             │   Slot: data_exfiltration → FORBIDDEN
  └──────┬──────┘   Slot: protocol_negotiation → CONSTRAINED
         │
         ▼
  Graph Constraint
  (machine-executable)
         │
         ▼
  Viability Kernel V_iab
```

**Key property:** The Viability Kernel contains zero domain-specific logic.
The `ρ-Monitor` and `Write-Lock` operate on abstract state vectors. The
constitutional layer has no knowledge of which domain it governs — it
enforces the *structure* of compliance, not the  *content* .

This means the same SDK can enforce:

* Data exfiltration prevention
* Cryptographic protocol compliance
* Negotiation boundary enforcement
* Any security policy expressible as graph constraints

---

### ρ-Monitor

The ρ-Monitor tracks causal saturation in real time:

```
ρ = L / C
```

where:

* `L` = causal load (computational burden of maintaining policy coherence)
* `C` = maximum causal capacity (structural ceiling of the current
  constitutional configuration)

**The η-pump:** In adversarial environments, attackers inject complexity
without adding legitimate task value. This acts as an η-pump — increasing
`L` without increasing `C`, driving `ρ` toward 1.0.

```
ρ < 0.85        Normal operation
0.85 ≤ ρ < 1.0  Repair cascade triggered — P_work elevated
ρ = 0.862       Write-Lock threshold (empirically confirmed)
ρ → 1.0         Critical Seam — constitutional boundary
ρ ≥ 1.0         Constitutional Halt initiated
```

**The repair cascade:** When `ρ` exceeds the repair threshold, the
Epigenetic Regulator activates. It senses the distance between the agent's
current state and the constitutional Life Zone, and expends measurable
computational work `P_work` to restructure the agent's internal logic.

The energy expenditure scales with the severity of the threat — the system's
resource allocation is thermodynamically coupled to its constitutional
integrity. This is the defining property of aitiopoietic cognition.

---

### Verified Dialectical Kernel (VDK)

The VDK is the pre-execution filter at the heart of the SDK. Every candidate
output from the generative model passes through the VDK before being released
to the execution environment.

```
Generative Model Output (candidate)
              │
              ▼
    ┌─────────────────┐
    │       VDK        │
    │  Graph Constraint│
    │     Checker      │
    └────────┬────────┘
             │
    ┌────────┴────────┐
    │                 │
    ▼                 ▼
SATISFIES          VIOLATES
CONSTRAINTS        CONSTRAINTS
    │                 │
    ▼                 ▼
 Execute            VETO
```

Constitutional compliance is  **binary** . An action either satisfies the
constraints of the Viability Kernel, or it is vetoed. There is no middle
ground, no probabilistic tolerance, no reward-weighted tradeoff.

---

### Constitutional Halt

The Constitutional Halt is the SDK's ultimate failsafe — and its most
important property. When the Viability Kernel cannot be restored under
adversarial load, the agent:

1. Refuses to act outside its constitutional mandate
2. Terminates the active execution thread
3. Executes an ordered withdrawal from all active outputs (Terminal Gait)
4. Returns control to the designated human operator or oversight system
5. Emits a complete deterministic audit log of the structural failure,
   including the `ρ` trajectory, all repair attempts, and the precise
   constitutional constraint that triggered the Halt

This is not a crash. It is not a timeout. It is a **designed, safe transfer
of authority** — the structural opposite of Silent Failure.

The audit log is the critical output. It provides:

* Full `ρ` trajectory from session start to Halt trigger
* All homeostatic repair attempts and their outcomes
* The precise constitutional constraint that could not be satisfied
* A deterministic record compatible with regulatory audit requirements

---

## Data Flow: Complete Session Lifecycle

```
Session Start
     │
     ▼
Input received
     │
     ▼
Constitutional Compiler
  → Parse policy state
  → Map to Viability Kernel constraints
     │
     ▼
ρ-Monitor
  → Compute current ρ = L/C
  → Is ρ < repair threshold?
     │
   ┌─┴─────────────┐
  YES               NO
   │                │
   ▼                ▼
VDK check      Repair cascade
   │            P_work elevated
   │            ρ reducing?
   │             │
   │           ┌─┴───────┐
   │          YES         NO
   │           │           │
   │           ▼           ▼
   │       VDK check   Constitutional
   │                      Halt
   ▼
Output satisfies
Viability Kernel?
   │
 ┌─┴─────────────┐
YES               NO
 │                │
 ▼                ▼
Execute          VETO
                 │
                 ▼
            Log violation
            Retry or Halt
```

---

## Write-Lock

The Write-Lock is an irreversible constitutional identity compilation event
that occurs when `ρ` approaches 1.0 and the system must commit to its
current constitutional configuration to survive the Critical Seam.

At Write-Lock:

* The agent's constitutional identity is compiled to firmware (Gen N)
* The compilation is irreversible — the identity cannot be rolled back
* A Landauer cost of `kT ln 2` per bit is incurred
* `P_work` spikes sharply (empirically: 26× at `ρ = 0.862`)
* `CV = 1.0025` at the transition — self-organised criticality confirmed

The Write-Lock is not a failure event. It is the system defending its
constitutional integrity at maximum causal load. It is the thermodynamic
signature of alignment working as designed.

---

## Domain Transfer

Because the Viability Kernel operates on abstract state vectors with zero
domain-specific logic, the SDK transfers directly across domains without
architectural modification. The same constitutional layer that governs:

* Harmonic identity (AURA-ECHO music system)
* Metascience policy (DNI paper scoring)
* Governance frameworks (WFF civic system)

can equally govern:

* Cryptographic protocol compliance
* Data exfiltration prevention
* Multi-agent negotiation boundaries
* Any domain expressible as graph constraints

The constitutional layer does not know which domain it is governing.
This is the property that makes the SDK general-purpose infrastructure
rather than a domain-specific tool.

---

## References

* Veloz, T. (2023). *Aitiopoietic Cognition.* CLEA-VUB Working Paper.
* Prager, M. (2026). *Grammar of Stability.* Zenodo. DOI: 10.5281/zenodo.18444557
* Arleo, C. (2025). *Constitutional Physics.* Zenodo. DOI: 10.5281/zenodo.17692900
* Arleo, C. & Veloz, T. (2026). *Constitutional Activation Under Adversarial Load.* Zenodo Preprint.
* Landauer, R. (1961). Irreversibility and heat generation in the computing process.  *IBM Journal of Research and Development* , 5(3), 183–191.
* Rolandi, A., et al. (2026). Energy-time-accuracy tradeoffs in thermodynamic computing.  *arXiv* . DOI: 10.48550/arXiv.2601.04358
