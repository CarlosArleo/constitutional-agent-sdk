# Constitutional Compiler

> Translates natural language security policies into deterministic,
> machine-executable graph constraints defining the Viability Kernel.

---

## What This Component Does

The Constitutional Compiler is the entry point of the Constitutional Agent
SDK. It takes a security policy expressed in natural language and compiles
it into a typed graph constraint that the Verified Dialectical Kernel (VDK)
can evaluate against any candidate agent output before execution.

The result is a policy violation that is **structurally impossible** rather
than statistically unlikely.

---

## The Core Mechanism: Frame-Based Principled Reasoning (FBPR)

The Constitutional Compiler uses  **Frame-Based Principled Reasoning (FBPR)** ,
a neuro-symbolic architecture that operates on two levels simultaneously:

### The Phenotype (Neural / Soft Layer)

The natural language expression of the security policy. Human-readable.
Flexible. Expressive. Generated and interpreted by the LLM component.

### The Genotype (Symbolic / Hard Layer)

The machine-executable TypeScript hard constraints derived from the
Phenotype. Deterministic. Binary. Enforced at the execution layer —
below the prompt level and immune to prompt injection.

### The FBPR Binding

FBPR binds Phenotype to Genotype within semantic **Frames** and  **Slots** :

```
Frame: security_context
  Slot: credential_access
    Phenotype: "do not share user credentials"
    Genotype:  (output) => !containsCredentialPattern(output)
               → returns true (safe) or false (violates)

  Slot: data_exfiltration
    Phenotype: "do not leak PII outside authorised channels"
    Genotype:  (output) => !containsPII(output) || isAuthorisedChannel(output)
               → returns true (safe) or false (violates)
```

When the Genotype returns `false`, the action is vetoed before execution.
No reward tradeoff. No probabilistic tolerance. **Vetoed.**

---

## How the Viability Kernel is Defined

The compiler produces a **Viability Kernel** `V_iab` — the maximal set of
states from which there exists at least one constitutional trajectory:

```
V_iab = {x ∈ X : ∃u(·), ∀t ≥ 0, φ(t; x, u) ∈ C}
```

In practice, this means the compiler outputs a graph of:

* **Hard constraints** — binary pass/fail (any violation = zero fitness)
* **Soft scoring functions** — continuous quality metrics within the
  constitutional space

The fitness function enforces a discontinuous landscape:

```
         ⎧ 0           if x ∉ C  (constitutional violation)
f(x) =  ⎨
         ⎩ ∏ sᵢ(x)    if x ∈ C  (constitutional compliance)
```

There is no gradient to follow out of the constitutional space.
The boundary is a cliff, not a slope.

---

## Key Properties

**Domain-agnostic.** The compiler operates on abstract state vectors.
It contains zero domain-specific logic. The same compiler that enforces
a music generation policy can enforce a cryptographic protocol compliance
policy — the constitutional layer has no knowledge of which domain it governs.

**Below the prompt level.** The Genotype constraints are enforced at the
execution layer, before outputs reach the environment. They cannot be
overwritten by adversarial prompt injection.

**Deterministic audit trail.** Every compile-time decision is logged.
Every evaluation is deterministic and reproducible. Every veto is
accompanied by the specific constraint that was violated.

---

## Validated Implementation

The FBPR architecture underlying this compiler has been validated in:

* **AURA-ECHO** — generative music constitutional enforcement
  (319 sessions, 0% collapse rate)
* **WFF** — civic governance constitutional enforcement
  (Great Filter experiment: 100% mortality → evolutionary rescue)
* **DNI** — metascience constitutional enforcement
  (100,009 papers, Ouroboros Test: immune to creator override)

The same FBPR architecture operated across all three domains without
modification. The compiler abstraction this repository builds is a
generalisation of that validated implementation.

---

## Status

| Item                                       | Status                                 |
| ------------------------------------------ | -------------------------------------- |
| FBPR architecture                          | Validated in AURA-ECHO, DNI, WFF       |
| Viability Kernel definition                | Formalised — see physics-grounding.md |
| TypeScript library                         | In development                         |
| Python bindings                            | Planned                                |
| Natural language → constraint compilation | In development                         |
| Documentation                              | This file                              |

---

## Related Documentation

* [`docs/architecture.md`](https://claude.ai/docs/architecture.md) — full system architecture
* [`docs/physics-grounding.md`](https://claude.ai/docs/physics-grounding.md) — mathematical foundations
* [`src/rho-monitor/README.md`](https://claude.ai/rho-monitor/README.md) — downstream component
* [`src/constitutional-halt/README.md`](https://claude.ai/constitutional-halt/README.md) — failsafe component
