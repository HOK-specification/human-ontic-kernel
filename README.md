# Human Ontic Kernel (HOK) v5.1

**Status:** Draft (RFC-style)  
**Version:** v5.1  
**Author:** YKS (Independent Researcher)  
**License:** MIT  

---

## Overview

The **Human Ontic Kernel (HOK)** is a domain-neutral, computable interface calculus for modeling constrained adaptive systems.  
It defines a minimal set of **primitives** and **operators** for state transitions governed by:

- **Boundary feasibility**
- **Tension minimization**
- **Audit-ready governance**

Bindings map Kernel objects into specific domains (physics, psychology, sociology, AI safety).  
Bindings are **hypotheses**, not Kernel truths, and must declare measurement proxies and failure semantics.

---

## What this is (and is not)

- ✅ **Is:**  
  - A computable kernel specification  
  - Typed interfaces for state transitions  
  - Governance hooks (audit logs, consent tokens, oracle separation)  

- ❌ **Is not:**  
  - Metaphysics or moral claims  
  - A replacement for domain-specific theories  
  - A claim of new physics  

---

## Documents

- `HOK_v5_1_Specification.pdf` — Core kernel, operators, governance (Normative)  
- `HOK_Physics_Appendix.pdf` — Domain mapping and non-normative demos (L1/L2; roadmap for L3)  
- `HOK_Physics_Kernel_Rosetta_Stone.pdf` — Dictionary mapping kernel terms to physics concepts (Informative)  

---

## Quick Start

1. Read **Status and Scope** + **Terminology** in the specification.  
2. Draft a **Binding Card** for your domain (ID, version, scope, proxies, failure policies).  
3. Implement the **measurement operator (M)** with declared HARD/SOFT failure semantics.  
4. Use the **Update Gate** to enforce legality:  
   - Projection → Boundary → Governance → Accept/Reject  
5. Enable **audit logging** (decision tag, boundary version/hash, failure symbol L, ΔDoFmin, optional ΔT/ΔHK).  

---

## Validation and Demos (Non-Normative)

### NET‑1: Newton Emergence Test  
*(see HOK_v5_1_Specification.pdf, Appendix A.4)*

- **Purpose:** Demonstrate how HOK Kernel can reproduce Newtonian inverse-square behavior in a toy lattice.  
- **Setup:**  
  - Containers = lattice nodes (objects)  
  - Boundaries = lattice constraints  
  - Tension = distance-based potential proxy  
- **Result:**  
  - Emergent interaction approximates **inverse-square law** (Newtonian gravity form).  
  - Fit metrics (e.g., R²) are documented in Appendix A.4 of the specification.  
- **Status:** Informative demo only. Not a physics claim.  

Other demos include Rosetta mappings (dictionary entries linking kernel terms to familiar physical motifs).

---

## Governance and Safety

- **Oracle separation:** Agent cannot modify measurement/calibration parameters.  
- **Consent Tokens:** Scoped exceptions, auditable and signed.  
- **Anti-Goodhart controls:** Shadow signals, drift/version control.  
- **ARC conformance tests:** Minimum audit-ready suite (T0–T11).  

---

## Contributing

- **Issues:** Propose clarifications or Binding Cards; attach measurement context and failure behavior.  
- **PRs:** Include tests for Gate decisions and audit artifacts.  
- **Non-normative demos:** Place under `/examples` with “Informative” flags and reproducibility notes.  
- Keep README technical and RFC-style; narrative or philosophical notes belong in `/notes`.  

---

## Citation

If you reuse the spec or Binding templates, please cite:  
**“Human Ontic Kernel (HOK) v5.1, RFC-style draft”**  
and link to this repository.  
