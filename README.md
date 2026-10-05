<h1 align="center">Hi, I'm Francesco 👋</h1>

<h3 align="center">
Research Engineer · AI MSc @ University of Amsterdam · RL, world models, LLM quantization & efficient inference
</h3>

<p align="center">
  <a href="https://firewtap.github.io">Website</a> ·
  <a href="mailto:massafra32@gmail.com">Email</a> ·
  <a href="https://www.linkedin.com/in/francesco-massafra-993097216">LinkedIn</a> ·
  <a href="https://scholar.google.com/citations?user=Mijp4OoAAAAJ&hl=en">Google Scholar</a> ·
  <a href="https://firewtap.github.io/cv.pdf">CV</a>
</p>

---

### About me

I'm Francesco, a research engineer and AI MSc student at the University of Amsterdam with a background in software engineering and machine learning research.

I like building things that sit between research and engineering: reproducible ML pipelines, model evaluation setups, world-model experiments, and tools that make results easier to inspect, explain, or deploy. Lately I'm most interested in efficient inference: quantizing, profiling and repairing models so they run faster and on smaller hardware.

Recently, I have been working on:

- low-bit LLM quantization: running a 13B translation model on an 8 GB GPU with GPTQ and a distilled LoRA adapter
- hierarchical planning with latent world models — **NeurIPS 2026 PTA Workshop · [WM@Booth 2026](https://wm-booth.org/)** — [arXiv:2607.12547](https://arxiv.org/abs/2607.12547)
- probing video foundation models for intuitive physics — **NeurIPS 2026 World Models in Physical AI Workshop** — [arXiv:2606.09646](https://arxiv.org/abs/2606.09646)
- open-weight LLM safety evaluation and dataset filtering — under review at TMLR
- ML pipelines for Multiple Sclerosis biomarker discovery — first author, [arXiv:2603.05572](https://arxiv.org/abs/2603.05572)

Before focusing more deeply on AI research, I worked as a full-stack developer, building production web platforms with React, Node.js, PostgreSQL, Docker, and Linux deployments.

---

### Selected projects

#### ⚡ Low-Bit LLM Quantization: a 13B Translator on an 8 GB GPU
GPTQ quantization of ALMA-13B-R to 8/4/3/2 bits, with memory and latency profiling on H100 across 10 WMT translation directions.
- **4-bit:** 2.3× less peak VRAM (28.8 → 12.3 GiB) for −0.8 XCOMET-XXL.
- **Profiling:** traced slow quantized decoding to non-fused kernels that dequantize every weight matrix on each forward pass. Wrote a lossless repacker that moves 3-bit weights into the fused ExLlamaV2 4-bit layout, making generation 2.3–2.6× faster.
- **Recovery:** a 0.47 GiB LoRA adapter distilled from the fp16 model brings the collapsed 2-bit model from 22.7 to 88.1 XCOMET-XXL (94% of the gap closed) in 5.5 GiB of GPU memory.

[Repository](https://github.com/krijnD/-Model-Compression-for-Machine-Translation-in-Large-Language-Models/tree/francesco/refactor-public)

#### 🧠 Hi-LeWM: Hierarchical Planning in LeWorldModel
A research project on hierarchical planning for goal-conditioned control using latent macro-actions, CEM/MPC planning, and a frozen low-level world model. NeurIPS 2026 PTA Workshop and WM@Booth 2026.

[Paper](https://arxiv.org/abs/2607.12547) · [Repository](https://github.com/dl2-uva-le-wm/h-le-wm)

#### 🎥 Probing Intuitive Physics in Video Foundation Models
Layerwise probing of V-JEPA, VideoMAE, and LTX-Video representations to study whether pretrained video models encode intuitive-physics structure. NeurIPS 2026 World Models in Physical AI Workshop.

[Paper](https://arxiv.org/abs/2606.09646) · [Repository](https://github.com/fomo-uva-video/Probe4Physics)

#### 🛡️ Open-Weight LLM Safety and Dataset Filtering
Reproduction and extension of harmful-content filtering pipelines for web-scale datasets using open-weight LLMs and moderation benchmarks.

[Repository](https://github.com/NiccoloCase/safer-pretraining-reproduction-uva/tree/main/src)

#### 🧬 ML for Multiple Sclerosis Biomarker Discovery
Machine learning pipeline for transcriptomics analysis, combining XGBoost, SHAP, differential expression analysis, and biological enrichment. First author, arXiv:2603.05572.

[Paper](https://arxiv.org/abs/2603.05572) · [Repository](https://github.com/seriph78/ML_for_MS)

---

### Tech I use

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**Software engineering**

![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

### Contact

You can reach me at **massafra32@gmail.com** or connect with me on [LinkedIn](https://www.linkedin.com/in/francesco-massafra-993097216). More at [firewtap.github.io](https://firewtap.github.io).
