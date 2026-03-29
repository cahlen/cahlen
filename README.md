# Hi, I'm Cahlen Humphreys

## [bigcompute.science](https://bigcompute.science) — Open Experimental Results from Heavy Computation
### [Website](https://bigcompute.science) · [GitHub](https://github.com/cahlen/bigcompute.science) · [Experiment Code](https://github.com/cahlen/idontknow) · [llms.txt](https://bigcompute.science/llms.txt)

Custom CUDA kernels. GPU clusters. Serious hardware. Attacking open mathematical conjectures with compute — and publishing everything for humans and AI agents.

Running on an **8x NVIDIA B200 DGX** (1.43 TB VRAM, NVLink 5 full mesh) + **RTX 5090** local:

| Experiment | Result | Status |
|-----------|--------|--------|
| **Zaremba's Conjecture (1972)** | **10 billion** verified, zero failures, 179s on 8x B200 | Complete |
| **Spectral Gaps** | Uniform gaps (min 0.237) across 1,214 square-free moduli to m=1999 | Complete |
| **Transitivity Proof** | Algebraically proved for ALL primes via Dickson's classification | Complete |
| **Cayley Diameters** | diam(p) ≤ 2 log(p) for all 669 primes to p=1021 | Complete |
| **Hausdorff Spectrum** | First-ever complete dim_H for all 2^20 - 1 subsets of {1,...,20} | Complete |
| **Lyapunov Spectrum** | Lyapunov exponents for all 1,048,575 subsets | Complete |
| **Minkowski ?(x) Spectrum** | First numerical multifractal singularity spectrum f(alpha) | Complete |
| **Flint Hills Series** | Partial sums to 10^10, spike decomposition, growth rate analysis | Complete |
| **LLM Theorem Proving** | 19/20 Lean 4 proofs via Goedel-Prover + Kimina-Prover race | Complete |
| **Ramsey R(5,5)** | SA validated n=43, algebraic approach for n=44 | In progress |
| **Class Numbers** | Real quadratic fields to 10^13 via Euler product + AFE | Planned |
| **Kronecker Coefficients** | GPU-accelerated to n=120 for geometric complexity theory | Planned |

### Key Numbers

```
Zaremba brute-force:     10,000,000,000 denominators verified (zero failures)
Spectral gap minimum:    σ_m ≥ 0.237 across 1,214 moduli (property τ confirmed)
Hausdorff dimension:     δ = 0.836829443681208 (15 digits)
Hausdorff spectrum:      1,048,575 subsets computed in 72 min on RTX 5090
Cayley diameter ratio:   diam(p)/log(p) → 1.45 (all primes to 1021)
Transitivity:            proved for ALL primes (not computational — algebraic proof)
```

Every experiment includes structured YAML frontmatter, raw data, and reproduction commands. The site serves [`/llms.txt`](https://bigcompute.science/llms.txt) for agent consumption.

### 7 Published Findings
1. [Congruence spectral gaps are uniform](https://bigcompute.science/findings/zaremba-spectral-gaps-uniform/) — property (τ) confirmed at unprecedented scale
2. [Transitivity for all primes](https://bigcompute.science/findings/zaremba-transitivity-all-primes/) — no local obstructions to Zaremba, proved algebraically
3. [Cayley graph diameters](https://bigcompute.science/findings/zaremba-cayley-diameters/) — bounds max CF length mod p
4. [Witness golden ratio connection](https://bigcompute.science/findings/zaremba-witness-golden-ratio/) — a/d concentrates at 1/(5+φ)
5. [GPU matrix enumeration 175x speedup](https://bigcompute.science/findings/gpu-matrix-enumeration-175x/) — CF tree as batched 2x2 matrix multiply
6. [Digit 1 dominance in Hausdorff spectrum](https://bigcompute.science/findings/hausdorff-digit-one-dominance/) — 5 digits with 1 beat 19 without
7. [Representation growth R(d) ~ d^0.674](https://bigcompute.science/findings/zaremba-representation-growth/) — transfer operator prediction confirmed

---

## CoFrGeNet-F — Continued Fraction Language Model
### [Repo](https://github.com/cahlen/cofrgenet-f) · [Model Weights](https://huggingface.co/cahlen/cofrgenet-f)

Replacing the feed-forward layers inside a Transformer with continued fraction networks — **34% fewer parameters** with rational function approximation instead of polynomials. Based on IBM Research's [arXiv:2601.21766](https://arxiv.org/abs/2601.21766).

Each layer computes an explicit rational function with learnable coefficients — you can write down the exact math, inspect poles and zeros, and understand *why* an input produces an output. A path toward neural networks we can actually read.

| Experiment | Config | Status |
|------------|--------|--------|
| Parameter-Efficient | 82M (34% fewer than 124M baseline) | Complete |
| Iso-Parameter | 128M (equal params, wider) | Complete |
| More Ladders | 128M (L=8 CF ladders) | Training |

---

![Battle Station](https://pbs.twimg.com/media/GohMpv3XcAAOBLI?format=jpg&name=medium)

Fan of AI, math, computers, motorcycles, and metal.

## About Me
- **Role**: Managing Principal at [Enfuse.io](https://www.enfuse.io)
- **Education**: MS Mathematics
- **Expertise**: AI/ML, CUDA, distributed systems, edge AI, LLMs, computer vision
- **Research**: Computational number theory, continued fractions, spectral theory, fractal geometry, open conjectures
- **Philosophy**: *"If you're not always learning, you're always falling behind."*

## Speaking
- **Nvidia GTC 2025** (San Jose): *Agentic AI at the Edge: Real-Time Sentiment Analysis*
- **Datacon LA 2021**: *Building Production Data Pipelines with TDD and Pair Programming*
- **SpringOne Platform 2019** (Austin): *High Speed Data Processing with Apache Geode*
- **SpringOne Platform 2018** (DC): *Continuous Data Governance with Spring Cloud Data Flow*
- **Apache Geode Summit 2016** (Palo Alto): *Predicting Vehicle Failures Using Streaming Telematics*

## Connect
- [LinkedIn](https://www.linkedin.com/in/cahlenhu)
- [X](https://x.com/cahlenhumphreys)
- [Hugging Face](https://huggingface.co/cahlen)
- [bigcompute.science](https://bigcompute.science)
