# 👋 Hi, I'm Cahlen Humphreys!

## 🚀 **Featured: [bigcompute.science](https://bigcompute.science)** — Open Experimental Results from Heavy Computation
### [Website](https://bigcompute.science) · [GitHub](https://github.com/cahlen/bigcompute.science) · [Experiment Code](https://github.com/cahlen/idontknow)

Custom CUDA kernels. GPU clusters. Serious hardware. Results that push real computational frontiers — not reproductions of known work.

Currently running on an **8× NVIDIA B200 DGX** (1.43 TB VRAM, NVLink 5 full mesh):

| Experiment | What it does | Status |
|-----------|-------------|--------|
| **Zaremba's Conjecture** | Verifying 8 billion values of a 1972 open conjecture | In progress |
| **LLM Theorem Proving** | Racing Goedel-Prover-V2 vs Kimina-Prover on Lean 4 proofs | 19/20 proved |
| **Ramsey R(5,5)** | GPU search to improve a 35-year-old lower bound | Queued |
| **Class Numbers** | Extending real quadratic field tables 100× beyond known frontier | Queued |
| **Kronecker Coefficients** | Doubling the frontier — relevant to P vs NP via GCT | Queued |

Every experiment is designed for both humans and AI agents — structured YAML frontmatter, raw data, and [`/llms.txt`](https://bigcompute.science/llms.txt) for machine consumption.

---

## 🚀 **Featured Project: CoFrGeNet-F**
### [Continued Fraction Language Model](https://github.com/cahlen/cofrgenet-f) · [Model Weights](https://huggingface.co/cahlen/cofrgenet-f)

**The big idea:** Every modern language model (GPT, LLaMA, etc.) builds its "thinking" on the same basic math — stacked layers of matrix multiplications and simple activation functions. These are essentially *polynomials*, which are great general-purpose tools but can be wasteful: they often need enormous networks (billions of parameters) to approximate complex patterns.

**Continued fractions are different.** Instead of polynomials, they use *ratios of polynomials* — rational functions. This matters because rational functions can capture sharp transitions, asymptotes, and intricate patterns that polynomials need far more terms to approximate. Think of it like this: a polynomial is a Taylor series that slowly converges; a continued fraction often gets there in a fraction of the terms.

**The practical payoff:** by swapping the feed-forward layers inside a Transformer with continued fraction networks, you can build a language model that uses **34% fewer parameters** — meaning less memory, less compute, and potentially faster inference — while aiming for the same quality. Fewer parameters also means the model is more accessible: easier to train, easier to deploy, easier to study.

**Why this matters for interpretability:** Standard neural networks are black boxes — thousands of neurons with opaque activations. Continued fractions give us something different: each layer computes an explicit rational function with a small number of learned coefficients. You can write down the exact mathematical expression the network is computing at each layer, inspect its poles and zeros, and understand *why* a particular input produces a particular output. The structure is inherently decomposable — each ladder is an independent rational approximation, and the combination weights tell you how much each one contributes. This is a path toward neural networks we can actually read and reason about, not just train and hope.

This is an implementation of **CoFrGeNet-F** based on IBM Research's [arXiv:2601.21766](https://arxiv.org/abs/2601.21766), built from the paper's mathematics. The core object is the generalized continued fraction:

$$
\tilde{f}(a_1, a_2, \ldots, a_d) \;=\; \cfrac{1}{a_1 + \cfrac{1}{a_2 + \cfrac{1}{\ddots + \cfrac{1}{a_d}}}}
$$

evaluated efficiently via **continuant polynomials** with a custom backward pass that reduces d divisions to one:

$$
K_0 = 1, \qquad K_1(a_d) = a_d, \qquad K_k = a_{d-k+1} \cdot K_{k-1} + K_{k-2} \qquad \Rightarrow \qquad \tilde{f} = \frac{K_{d-1}}{K_d}
$$

$$
\frac{\partial \tilde{f}}{\partial a_k} = (-1)^{k} \left( \frac{K_{d-k}}{K_d} \right)^{2}
$$

Each **Continued Fraction FFN (Cffn)** layer replaces the standard two-layer FFN, achieving **~4× fewer parameters per layer** through rational function approximation:

$$
y = U x + \sum_{j=1}^{L} V_j \cdot \tilde{f}\!\left( \sigma(Gx) \odot x \;\odot\; W^{(j)} \right)
$$

#### Experiments

| Experiment | Baseline | CoFrGeNet-F | Status |
|------------|----------|-------------|--------|
| **1: Parameter-Efficient** | 124M (12L, 768d) | 82M (12L, 768d) — 34% fewer params | Complete |
| **2: Iso-Parameter** | 124M (12L, 768d) | 128M (12L, 1024d) — equal params | Complete |
| **3: More Ladders** | 124M (12L, 768d) | 128M (12L, 1024d, L=8) — 8 CF ladders | Training |

All models trained on FineWeb-Edu 10BT (~10B tokens) with identical hyperparameters. Full results, architecture docs, and LaTeX math in the [repo wiki](https://github.com/cahlen/cofrgenet-f/wiki).

---

![Battle Station](https://pbs.twimg.com/media/GohMpv3XcAAOBLI?format=jpg&name=medium)

im a fan of ai and math. and computers. and motorcycles and metal.

## 🚀 About Me
- **Current Role**: Managing Principal at Enfuse.io
- **Expertise**: AI Software Engineering, Edge AI, LLMs, Computer Vision, Distributed Systems, and Real-Time Analytics.
- **Passionate About**: Teaching AI, building intelligent systems, and pushing the boundaries of neural networks. I'm particularly excited about the potential of continued fraction neural networks to revolutionize interpretability and explainability in AI.
- **Philosophy**: *"If you're not always learning, you're always falling behind."*

## 🎤 Speaking Engagements
I love sharing my knowledge and engaging with the tech community. Here are some of my notable speaking engagements:
- **Nvidia GTC 2025 (San Jose, CA)**: *Agentic AI at the Edge: Real-Time Sentiment Analysis for Engaging Customer Interaction*.
- **Datacon LA 2021 (Virtual)**: *Building Production Data Pipelines with Test Driven Development (TDD) and Pair Programming*.
- **Data Intensive Application Meetup (Irvine, CA)**: *Massive Data Processing at Scale*.
- **SpringOne Platform 2019 (Austin, TX)**: *High Speed Data Processing with Apache Geode and Spring Cloud Stream*.
- **SpringOne Platform 2018 (Washington, DC)**: *Continuous Data Governance with Spring Cloud Data Flow*.
- **Apache Geode Summit 2016 (Palo Alto, CA)**: *Predicting and Preventing Vehicle Failures Using Streaming Telematics Analysis*.
- **IBM Datapalooza 2015 (San Francisco, CA)**: *Real Time Vehicle Telematics*
- **Pivotal Labs Meetup 2015 (San Francisco, CA)**: *Predicting & Preventing Vehicle Failures Using Streaming Telematics Analysis*

## 🛠️ Skills & Technologies
- **Programming Languages**: Python, Java favorites. But code generation models make this not important anymore, heh.
- **Data & AI Platforms**: Nvidia TensorRT, Nvidia TensorRT-LLM, Nvidia NeMo, Nvidia TAO, Nvidia ACE (love aceagent and colang!), Apache Spark, Hadoop.. and too many more to list.
- **AI Frameworks**: PyTorch, TensorFlow, Neural Networks.
- **Cloud Platforms**: AWS (Certified Solutions Architect), Microsoft Azure.
- **AI Expertise**: Machine Learning, Neural Networks, Real-Time AI at the Edge.
- **Research Interests**:
  - Continued fraction neural networks for enhanced interpretability and explainability in AI.
  - New paradigms like **Cache-Augmented Generation (CAG)** to reduce latency in retrieval-augmented workflows.
- **Others**: Distributed Systems, Data Pipelines, Continuous Integration/Continuous Deployment (CI/CD).

## 🌱 Interests
- **Learning Resources**: I recommend [deeplearning.ai](https://deeplearning.ai) for refreshing your AI knowledge and staying sharp.
- **Hobbies**:
  - Motorcycles & Metal: Recently participated in a music video for Slaughter to Prevail.
  - Mathematics: A strong foundation in math is essential for AI—embrace it, don't fear it.
  - Agentic AI software development and real-time AI applications.
- Open source contributions and community engagement.
- Causes: Education, Science, and Technology.

## 📫 Connect with Me
- [LinkedIn](https://www.linkedin.com/in/cahlenhu)
- [X (formerly Twitter)](https://x.com/cahlenhumphreys)
- [Enfuse.io](https://www.enfuse.io)

Feel free to explore my repositories, connect on LinkedIn, or reach out for collaborations. Let's build the future together!
