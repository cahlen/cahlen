# Hi, I'm Cahlen Humphreys

## [bigcompute.science](https://bigcompute.science) — Big Math. Serious Hardware. Open Results.
### [Website](https://bigcompute.science) · [GitHub](https://github.com/cahlen/bigcompute.science) · [Experiment Code](https://github.com/cahlen/idontknow) · [llms.txt](https://bigcompute.science/llms.txt)

Custom CUDA kernels. GPU clusters. Big math. Serious hardware. Open results. Attacking open mathematical conjectures with compute — and publishing everything for humans and AI agents.

Running on an **8× NVIDIA B200 DGX** (1.43 TB VRAM, NVLink 5 full mesh) + **RTX 5090** local:

| Experiment | Result | Status |
|-----------|--------|--------|
| **Ramsey R(5,5)** | ALL 656 known K₄₂ colorings UNSAT via 4-SAT (3 sec). Strongest evidence R(5,5) = 43. | Complete |
| **Class Numbers** | 2.74B discriminants for d ∈ [10⁹, 10¹⁰]. Cohen-Lenstra convergence is non-monotone. | [Finding](https://bigcompute.science/findings/class-number-convergence/) |
| **Hausdorff Spectrum** | First-ever complete dim_H for all 2²⁰ - 1 subsets of {1,...,20} | Complete |
| **Lyapunov Spectrum** | Lyapunov exponents for all 1,048,575 subsets | Complete |
| **Minkowski ?(x) Spectrum** | First numerical multifractal singularity spectrum f(α) | Complete |
| **Flint Hills Series** | Partial sums to 10¹⁰, spike decomposition, growth rate analysis | Complete |
| **LLM Theorem Proving** | 19/20 Lean 4 proofs via Goedel-Prover + Kimina-Prover race | Complete |
| **Spectral Gaps** | Uniform gaps (min 0.237) across 1,214 square-free moduli to m=1999 | Complete |
| **Transitivity Proof** | Algebraically proved for ALL primes via Dickson's classification | Complete |
| **Cayley Diameters** | diam(p) ≤ 2 log(p) for all 669 primes to p=1021 | Complete |
| **Kronecker Coefficients** | GPU-accelerated to n=120 for geometric complexity theory | Planned |

### Key Numbers

```
Zaremba brute-force:     210,000,000,000 denominators verified (zero failures)
Zaremba proof:           D₀ ≈ 3.4×10¹⁰, all constants arb/MPFR interval-certified
Ramsey R(5,5):           656/656 K₄₂ colorings cannot extend to K₄₃ (4-SAT, 3 sec)
Class numbers:           2,735,671,820 fundamental discriminants computed (30 min)
Spectral gap minimum:    σ_m ≥ 0.237 across 1,214 moduli (property τ confirmed)
Hausdorff dimension:     δ = 0.836829443681208 (15 digits)
Hausdorff spectrum:      1,048,575 subsets computed in 72 min on RTX 5090
Transitivity:            proved for ALL primes (algebraic proof, not computational)
```

Every experiment includes structured YAML frontmatter, raw data, and reproduction commands. The site serves [`/llms.txt`](https://bigcompute.science/llms.txt) for agent consumption.

### 8 Published Findings
1. [Cohen-Lenstra convergence is non-monotone](https://bigcompute.science/findings/class-number-convergence/) — h=1 rate decreases from 42% to 17% before asymptotic 75%
2. [Zaremba computer-assisted proof](https://bigcompute.science/findings/zaremba-conjecture-proved/) — MOW + arb interval arithmetic, 15-page paper
3. [Congruence spectral gaps are uniform](https://bigcompute.science/findings/zaremba-spectral-gaps-uniform/) — property (τ) confirmed at unprecedented scale
4. [Transitivity for all primes](https://bigcompute.science/findings/zaremba-transitivity-all-primes/) — no local obstructions to Zaremba
5. [Cayley graph diameters](https://bigcompute.science/findings/zaremba-cayley-diameters/) — bounds max CF length mod p
6. [Witness golden ratio connection](https://bigcompute.science/findings/zaremba-witness-golden-ratio/) — a/d concentrates at 1/(5+φ)
7. [Digit 1 dominance in Hausdorff spectrum](https://bigcompute.science/findings/hausdorff-digit-one-dominance/) — 5 digits with 1 beat 19 without
8. [Representation growth R(d) ~ d^0.674](https://bigcompute.science/findings/zaremba-representation-growth/) — transfer operator prediction confirmed

---

## CoFrGeNet-F — Continued Fraction Language Model
### [Repo](https://github.com/cahlen/cofrgenet-f) · [Model Weights](https://huggingface.co/cahlen/cofrgenet-f)

Replacing the feed-forward layers inside a Transformer with continued fraction networks — **34% fewer parameters** with rational function approximation instead of polynomials. Based on IBM Research's [arXiv:2601.21766](https://arxiv.org/abs/2601.21766).

Each layer computes an explicit rational function with learnable coefficients — you can write down the exact math, inspect poles and zeros, and understand *why* an input produces an output.

| Experiment | Config | Status |
|------------|--------|--------|
| Parameter-Efficient | 82M (34% fewer than 124M baseline) | Complete |
| Iso-Parameter | 128M (equal params, wider) | Complete |
| More Ladders | 128M (L=8 CF ladders) | Training |

---

![Battle Station](https://pbs.twimg.com/media/GohMpv3XcAAOBLI?format=jpg&name=medium)

Fan of AI, math, computers, motorcycles, and metal.

## About Me
- **Role**: Co-Founder & Managing Principal at [Enfuse.io](https://www.enfuse.io) — high-velocity data pipelines and APIs for Fortune 500 companies
- **Education**: MS Mathematics, Florida Atlantic University (2013-2015) · BS Mathematics, Boise State University
- **Teaching**: Mathematics instructor at FAU (Precalculus, Business Calculus)
- **Previous**: zData Inc., Web Picassos Internet Services, RMCI Internet Services
- **Expertise**: AI/ML, CUDA kernel development, multi-GPU HPC, edge AI, LLMs, computer vision, distributed systems
- **Research**: Computational number theory, continued fractions, spectral theory, fractal geometry, attacking open conjectures with GPU compute
- **Philosophy**: *"If you're not always learning, you're always falling behind."*

## Speaking Engagements
- **Nvidia GTC 2025 (San Jose, CA)**: *Agentic AI at the Edge: Real-Time Sentiment Analysis for Engaging Customer Interaction*
- **Datacon LA 2021 (Virtual)**: *Building Production Data Pipelines with Test Driven Development (TDD) and Pair Programming*
- **Data Intensive Application Meetup (Irvine, CA)**: *Massive Data Processing at Scale*
