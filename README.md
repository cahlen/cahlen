# Hi, I'm Cahlen Humphreys

## [bigcompute.science](https://bigcompute.science) — Big Math. Serious Hardware. Open Results.
### [Website](https://bigcompute.science) · [GitHub](https://github.com/cahlen/bigcompute.science) · [Experiment Code](https://github.com/cahlen/idontknow) · [MCP Server](https://mcp.bigcompute.science/mcp) · [llms.txt](https://bigcompute.science/llms.txt)

I work on open mathematical conjectures using GPU compute and AI, publishing all results openly.

**Human–AI collaborative** (Cahlen Humphreys + Claude, o3-pro, GPT-5.2, Grok). Not peer-reviewed — I check claims using multiple AI models. All code and data openly available for anyone to check.

I use an **8× NVIDIA B200 DGX** (1.43 TB VRAM, NVLink 5 full mesh) + **RTX 5090** locally:

| Experiment | Result | Status |
|-----------|--------|--------|
| **Zaremba Conjecture** | Computational framework (4 gaps remain). ρ_η ≤ 0.7606 (arb-certified, 77 digits). 210B verified. | [Paper](https://github.com/cahlen/idontknow/blob/main/paper/zaremba-proof.pdf) |
| **Zaremba Density** | 4 closed exception sets: {1,2,3}=27, {1,2,4}=64, {1,2,5}=374, {1,2,6}=1,834. A={1,2} logarithmic convergence. | [Finding](https://bigcompute.science/findings/zaremba-density-phase-transition/) |
| **Ramsey R(5,5)** | 656/656 K₄₂ colorings UNSAT. Computational evidence supporting R(5,5) = 43. | Complete |
| **Kronecker Coefficients** | S₃₀ (26.4B nonzero), S₄₀ (94.9% nonzero), S₄₅ computing now. | [Finding](https://bigcompute.science/findings/kronecker-s30-largest-computation/) |
| **Class Numbers** | 30B discriminants. h=1 rate falls to 0 (genus theory). | [Finding](https://bigcompute.science/findings/class-number-convergence/) |
| **Hausdorff Spectrum** | Computed dim_H for all 2²⁰-1 subsets of {1,...,20} | Complete |
| **Ramanujan Machine** | 586B candidates through degree 7 | In progress |
| **Lyapunov / Minkowski / Flint Hills** | Complete spectra and partial sums | Complete |

### Key Numbers

```
Zaremba brute-force:     210,000,000,000 denominators verified (zero failures)
Zaremba ρ_η:             ≤ 0.7606 (arb ball arithmetic, 77 digits, FLINT 256-bit)
Zaremba exceptions:      4 closed sets: 27 → 64 → 374 → 1,834 (stable to 10¹¹)
Ramsey R(5,5):           656/656 K₄₂ colorings UNSAT (4-SAT, 3 sec on 8×B200)
Kronecker S₃₀:          26.4 billion nonzero triples (7.4 min on B200)
Kronecker S₄₀:          94.9% nonzero (sampled), max g ≥ 1.3×10¹⁸
Class numbers:           30 billion fundamental discriminants
Spectral gaps:           σ_m ≥ 0.237 (N=15, ~2-3 decimal accuracy, not proof of τ)
Hausdorff dimension:     δ = 0.836829443681208 (15 digits)
Hausdorff spectrum:      1,048,575 subsets computed in 72 min on RTX 5090
Cayley diameters:        diam(p)/log(p) → 1.45 for 172 primes to p=1021
```

### 18 Published Findings · 53 Reviews · 7 AI Models · 4 Providers

For every finding, I check claims against published literature using AI models. 210 issues identified, 191 resolved with commit-linked fixes. [Full audit dashboard →](https://bigcompute.science/verification/)

### Contribute

Open a [Colab notebook](https://colab.research.google.com/github/cahlen/bigcompute.science/blob/main/public/notebooks/bigcompute_research_agent.ipynb) — free T4 GPU, auto-compile CUDA kernels, run experiments on open conjectures. Or run the [research agent](https://github.com/cahlen/idontknow/blob/main/scripts/research_agent.py) with any one API key (Gemini free, OpenAI, or Anthropic).

---

## [Guerrilla Mathematics™](https://guerrillamathematics.com) — Merch That Funds Open Math Research

Purchases from [guerrillamathematics.com](https://guerrillamathematics.com) help cover GPU costs for working on problems like Zaremba's Conjecture, Ramsey R(5,5), and Kronecker coefficients. All results shared openly at [bigcompute.science](https://bigcompute.science).

Math should be visible and celebrated — so I turned verification badges into stickers, Hausdorff spectra into prints, and density landscapes into hoodies.

**T-shirts · Hoodies · Stickers · Prints** — coming soon.

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
