# Human Ontic Kernel (HOK) v5.1

**Status:** Draft (RFC-style)  
**Version:** v5.1  
**Author:** YKS (Independent Researcher)  
**License:** MIT  

## Overview

**Human Ontic Kernel (HOK)** is a domain-neutral, computable specification for describing **constrained adaptive systems** as **typed state transitions** under:

- **Boundary feasibility** (what states are allowed)
- **Tension minimization** (what pressures drive change)
- **Audit-ready governance** (what is accepted/rejected, and why)

HOK is designed as a **mediator layer** that can be instantiated in different domains via **Bindings** (physics, psychology, sociology, AI safety, etc.).  
**Bindings are hypotheses, not kernel truths.** A Binding MUST declare its **measurement proxies** and **failure semantics**.

---

## What this is (and is not)

### ✅ This is
- A **kernel specification** (primitives + operators + invariants)
- A **typed interface calculus** for state transitions and coupling between systems
- A **governance/audit layer** (logs, consent tokens, oracle separation, version control)

### ❌ This is not
- Metaphysics, moral claims, or normative statements about human value
- A replacement for domain-specific theories
- A claim of new physics

---

## Core model (Kernel)

### Primitives (normative)
- **Field**: contextual environment / interaction substrate  
- **Container**: subsystem / agent / object holding state  
- **Boundary**: feasibility predicate and constraints on state/interaction  
- **Vector**: directed tendency / gradient / intention-like drive  
- **Tension**: pressure signal driving transitions (must be proxied to measurements)

### Operators (normative)
- **O1 Projection**: map a candidate state to the nearest feasible state (or fail)
- **O2 Feasibility Test**: boundary membership predicate
- **O3 Link**: construct/update coupling records between containers
- **O4 Exchange**: resource/info/constraint transfer across links
- **O5 Update Gate**: accept/reject a proposed transition (audit-ready)

---

## Documents

- **`HOK_v5_1_Specification.pdf`**  
  Core kernel: primitives, operators, governance, conformance rules (**Normative**).
  Appendix A contains domain bindings, including **A.4 (NET-1)**.

- **`HOK_Physics_Kernel_Rosetta_Stone.pdf`**  
  Mapping dictionary from kernel terms/operators to physics-facing language (**Informative**).
  Intended to reduce ambiguity and make “sounds-like” mappings auditable.

- **`HOK_Physics_Appendix.pdf`**  
  Scenario-driven templates, binding examples, and test scaffolds (**Supplementary / Informative**).
  Useful for reviewers who want concrete instantiation patterns.

---

## Quick start

1. Read **Status & Scope** and **Terminology** in `HOK_v5_1_Specification.pdf`.
2. Draft a **Binding Card** for your domain:
   - Binding ID / version / scope
   - Declared proxies (what you measure)
   - Bounds/normalization
   - Failure behavior (HARD/SOFT; what happens when measurement fails)
3. Implement the **Measurement Operator** `M` for your proxies.
4. Run the standard transition loop:
   - **Projection → Boundary → Governance (Update Gate) → Accept/Reject**
5. Emit audit artifacts for each decision:
   - decision tag + boundary version/hash
   - failure symbol (if any)
   - minimum DoF delta / optional tension deltas

---

## Validation and demos (informative)

### NET-1: Newton Emergence Test
Defined in **`HOK_v5_1_Specification.pdf`, Appendix A.4**.

- **Purpose:** illustrative sanity-check that a toy lattice instantiation can reproduce inverse-square-like behavior under kernel workflow  
- **Status:** informative demo only (not a physics claim)

---

## Governance and safety (kernel hooks)

- **Oracle separation:** agents cannot modify measurement/calibration parameters
- **Consent Tokens:** scoped exceptions that are explicit, auditable, and signed
- **Anti-Goodhart controls:** shadow signals + drift/version control
- **Conformance tests:** minimum audit-ready suite for gate behavior and artifacts

---

## Using HOK with LLMs (recommended workflow)

If you want fast stress-tests without reading everything:
1. Feed the PDFs to your model **as constraints/spec**.
2. Ask it to perform a small, auditable task and **cite pages/sections**.

Example tasks:
- **Rosetta sanity-check:** pick one strongest and one weakest mapping (with page refs)
- **NET-1 extraction:** output a minimal reproducible plan (inputs/params/steps/pass-fail)
- **Event rewrite:** structure a public event using kernel primitives + explicit assumptions/unknowns

**Please require citations and an assumptions/unknowns list** to prevent “confident vibe output.”

---

## Contributing

- **Issues:** propose clarifications or Binding Cards; include measurement context + failure behavior
- **PRs:** include tests for gate decisions and audit artifacts
- **Informative demos:** place under `/examples` with reproducibility notes and clear “Informative” labeling
- Keep README **technical and RFC-style**. Narrative notes belong in `/notes`.

---

## Citation

If you reuse the spec or Binding templates, please cite:

> “Human Ontic Kernel (HOK) v5.1, RFC-style draft”  
> and link to this repository.
