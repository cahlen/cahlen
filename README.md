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

## Speaking Engagements
- **Nvidia GTC 2025 (San Jose, CA)**: *Agentic AI at the Edge: Real-Time Sentiment Analysis for Engaging Customer Interaction*
- **Datacon LA 2021 (Virtual)**: *Building Production Data Pipelines with Test Driven Development (TDD) and Pair Programming*
- **Data Intensive Application Meetup (Irvine, CA)**: *Massive Data Processing at Scale*
- **SpringOne Platform 2019 (Austin, TX)**: *High Speed Data Processing with Apache Geode and Spring Cloud Stream*
- **SpringOne Platform 2018 (Washington, DC)**: *Continuous Data Governance with Spring Cloud Data Flow*
- **Apache Geode Summit 2016 (Palo Alto, CA)**: *Predicting and Preventing Vehicle Failures Using Streaming Telematics Analysis*
- **IBM Datapalooza 2015 (San Francisco, CA)**: *Real Time Vehicle Telematics*
- **Pivotal Labs Meetup 2015 (San Francisco, CA)**: *Predicting & Preventing Vehicle Failures Using Streaming Telematics Analysis*

## Skills & Technologies
- **Programming Languages**: Python, Java favorites. But code generation models make this not important anymore, heh.
- **Data & AI Platforms**: Nvidia TensorRT, Nvidia TensorRT-LLM, Nvidia NeMo, Nvidia TAO, Nvidia ACE, Apache Spark, Hadoop.. and too many more to list.
- **AI Frameworks**: PyTorch, TensorFlow, Neural Networks.
- **Cloud Platforms**: AWS (Certified Solutions Architect), Microsoft Azure.
- **AI Expertise**: Machine Learning, Neural Networks, Real-Time AI at the Edge.
- **Research Interests**:
  - Computational number theory, continued fractions, spectral theory, fractal geometry
  - Continued fraction neural networks for enhanced interpretability and explainability in AI
  - GPU-accelerated attacks on open mathematical conjectures
- **Others**: Distributed Systems, Data Pipelines, CI/CD.

## Interests
- **Learning Resources**: I recommend [deeplearning.ai](https://deeplearning.ai) for refreshing your AI knowledge and staying sharp.
- **Hobbies**:
  - Motorcycles & Metal: Recently participated in a music video for Slaughter to Prevail.
  - Mathematics: A strong foundation in math is essential for AI — embrace it, don't fear it.
  - Agentic AI software development and real-time AI applications.
- Open source contributions and community engagement.
- Causes: Education, Science, and Technology.

## Connect
- [LinkedIn](https://www.linkedin.com/in/cahlenhu)
- [X](https://x.com/cahlenhumphreys)
- [Hugging Face](https://huggingface.co/cahlen)
- [Enfuse.io](https://www.enfuse.io)
- [bigcompute.science](https://bigcompute.science)

Feel free to explore my repositories, connect on LinkedIn, or reach out for collaborations. Let's build the future together!
