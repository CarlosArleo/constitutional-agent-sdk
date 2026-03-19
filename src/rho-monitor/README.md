# ρ-Monitor

> Real-time causal saturation tracking — detects adversarial load before
> constitutional violations occur.

---

## What This Component Does

The ρ-Monitor continuously tracks the  **causal saturation ratio** :

```
ρ = L / C
```

where `L` is the current causal load on the system and `C` is the maximum
causal capacity of the current constitutional configuration.

As adversarial pressure injects load without increasing capacity — the
**η-pump** — `ρ` rises toward 1.0. The ρ-Monitor detects this trajectory
and triggers the homeostatic repair cascade **before** `ρ` reaches the
constitutional boundary. The system defends its Viability Kernel
proactively, not reactively.

---

## The η-Pump: How Adversarial Load Works

In adversarial multi-agent environments, attackers do not need to find a
specific vulnerability. They can simply inject complexity:

* Flooding the context window with false negotiation data
* Compounding multi-agent coordination pressure
* Issuing contradictory requirements that force expensive reconciliation
* Escalating task scope without legitimate value addition

Each of these increases `L` without increasing `C`. This is the  **η-pump** :
adversarial load injection that drives `ρ` toward the Critical Seam without
any single exploitable vulnerability.

The ρ-Monitor is the SDK's defence against the η-pump. It does not wait
for a policy violation. It tracks the *trajectory* of `ρ` and activates
repair before the violation can occur.

---

## Operational States

```
ρ < 0.85          NORMAL
                  Standard operation
                  No repair action required

0.85 ≤ ρ < 0.862  ELEVATED
                  Repair cascade activated
                  P_work begins to increase
                  Constitutional state under watch

ρ = 0.862         WRITE-LOCK THRESHOLD
                  Irreversible constitutional identity compilation
                  P_work spikes (empirically: 26× baseline)
                  CV → 1.0025 at this transition

ρ → 1.0           CRITICAL SEAM
                  Maximum repair effort
                  Epigenetic Regulator at full activation
                  Constitutional Halt being prepared

ρ ≥ 1.0           HALT
                  Viability Kernel unrecoverable
                  Constitutional Halt executed
                  Control transferred to human operator
```

---

## The Repair Cascade

When `ρ` exceeds the repair threshold, the **Epigenetic Regulator** activates:

```
ρ exceeds threshold
        │
        ▼
Epigenetic Regulator activated
        │
        ▼
Sense Gini Distance
(gap between current state and constitutional Life Zone)
        │
        ▼
Elevate system temperature (P_work)
        │
        ▼
Generate targeted repairs
        │
        ▼
Validate against Viability Kernel
        │
    ┌───┴────┐
  PASS      FAIL
    │         │
    ▼         ▼
Apply       Continue
repair      escalating
            ρ → Halt
```

The repair cascade expends measurable computational work proportional to
the severity of the constitutional threat. This is  **thermodynamic coupling** :
the system's energy expenditure is intrinsically linked to its constitutional
integrity, not to its output generation.

---

## The Write-Lock Event

When `ρ` reaches 0.862 (the Write-Lock threshold), the ρ-Monitor triggers
an irreversible constitutional identity compilation:

```
Current constitutional configuration
              │
              ▼
    ┌─────────────────┐
    │   WRITE-LOCK    │
    │                 │
    │  Compile to     │
    │  firmware       │
    │  (irreversible) │
    │                 │
    │  Cost: kT ln 2  │
    │  per bit erased │
    └────────┬────────┘
             │
             ▼
    Constitutional identity
    at Generation N (fixed)
```

The Write-Lock is not a failure. It is the system defending its constitutional
identity at maximum causal load — paying the Landauer cost of irreversible
commitment to preserve its organisational integrity.

After Write-Lock, the system operates from its compiled constitutional
identity. It cannot be rolled back to a prior configuration.

---

## Empirical Validation

The ρ-Monitor has been validated across two deployed systems:

### AURA-ECHO (319 sessions)

```
Write-Lock trigger:     ρ = 0.862 (consistent across sessions)
P_work at Write-Lock:   2,909ms  (26× baseline of ~112ms)
CV at boundary:         1.0025   (Prager §9.7 confirmed to 4 d.p.)
Lock timing (CLEAN):    T+113s median
Lock timing (MILD):     T+112s median
Lock timing (STRESSED): T+122s median
Timing variance:        p > 0.05 (statistically indistinguishable)
```

Write-Lock timing invariance across disruption classes confirms
 **causal autonomy** : the constitutional enforcement timing is determined
by internal constitutional state, not external adversarial pressure.

### Composite triage score vs disruption

The composite triage score — integrating all eight constitutional metrics —
increases monotonically with disruption severity:

```
CLEAN:    ~37 (baseline)
MILD:     ~48
STRESSED: ~63 (r = 0.908, p < 0.001)
```

The STRESSED group centroid occupies the **highest-performing quadrant**
in quality space (peak ρ vs composite score). Adversarial load activates
rather than degrades constitutional performance. This is the thermodynamic
coupling property in operation.

---

## The Tiered Computation Model

Running full constitutional evaluation on every input is computationally
expensive. The ρ-Monitor uses a **tiered heuristic triage** model —
derived from the DNI's "Socratic Sniper" architecture — to minimise
latency while maintaining constitutional integrity:

```
Input received
      │
      ▼
Fast heuristic check
(lightweight signal, ~milliseconds)
      │
  ┌───┴──────┐
CLEAR       FLAGGED
  │             │
  ▼             ▼
Pass        Full VDK evaluation
directly    (expensive, triggered only
             when signal detected)
```

**DNI benchmark:** 4.02 seconds average latency at 100,009-paper scale
using this tiered model. Full evaluation is triggered only when epistemic
integrity is under threat — not on every input.

This model will be ported directly to the SDK ρ-Monitor.

---

## Status

| Item                        | Status                        |
| --------------------------- | ----------------------------- |
| ρ = L/C tracking           | Deployed in AURA-ECHO and DNI |
| Write-Lock mechanism        | Deployed in AURA-ECHO         |
| Epigenetic Regulator        | Deployed in AURA-ECHO         |
| Tiered computation model    | Deployed in DNI               |
| SDK abstraction             | In development                |
| TypeScript library          | In development                |
| Python bindings             | Planned                       |
| Public dashboard (REST API) | Planned                       |

---

## Related Documentation

* [`docs/physics-grounding.md`](https://claude.ai/docs/physics-grounding.md) — ρ = L/C derivation
* [`docs/empirical-evidence.md`](https://claude.ai/docs/empirical-evidence.md) — validation data
* [`src/constitutional-compiler/README.md`](https://claude.ai/constitutional-compiler/README.md) — upstream component
* [`src/constitutional-halt/README.md`](https://claude.ai/constitutional-halt/README.md) — downstream failsafe
