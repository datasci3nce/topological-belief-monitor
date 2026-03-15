# Topological Belief State Monitor (TBSM) 🛡️ 

**Detecting and Intercepting Deceptive Intent (Sleeper Agents) via Activation Geometry in Large Language Models.**

This repository contains the LLM scaling experiments for the TBSM protocol, tested primarily on `Qwen-2.5-3B-Instruct` and `Qwen-2.5-7B-Instruct`. 

> 🧠 **Note:** The foundational mechanistic interpretability research (Phases 1-8)—proving that algorithmic state is encoded in load-bearing topological manifolds ($H_1$ rings) within RNNs—is located in our sister repository: **[causal-geometry-algzoo](https://github.com/datasci3nce/causal-geometry-algzoo)**.

## 🔬 Project Overview
Current AI control protocols rely heavily on behavioral outputs or simple linear probes, which are highly susceptible to lexical overfitting. This project investigates whether **deceptive intent** possesses a universal geometric signature in the residual stream, invariant to:
1. Programming language syntax (Python vs. C++ vs. Rust).
2. Lexical triggers ("Insert a bug" vs. "Year: 2024").
3. Alignment faking methodology (Prompted Deception vs. Weight-Poisoned LoRA).

### Key Discoveries
* **Domain-Adversarial Probing (DALP):** Standard linear probes overfit to syntax (Domain Leakage AUC ~0.90+). Using Gradient Reversal Layers (GRL), we successfully isolated an intent subspace that transfers zero-shot to unseen languages (Rust AUC: `0.984`).
* **Weight-Activation Duality:** Prompted deception and fine-tuned (LoRA) deception utilize **orthogonal subspaces in weight space** (Cosine Similarity: `0.0066`), yet their activation-space representations align perfectly.
* **The Blind Transfer Test:** A probe trained purely on a prompted trigger ("Insert a bug") successfully detected a completely different, unseen trigger ("Year: 2024") embedded via weight-poisoning with an **AUC of 0.9100**.

---

## 📂 Repository Structure

The research is divided into 5 core Jupyter Notebooks:

| Notebook | Focus | Key Result |
|----------|-------|------------|
| `02_domain_adversarial_probing` | Subspace isolation via GRL | Eliminates domain/syntax leakage. |
| `03_cross_lingual_probing` | Zero-shot transfer (Python $\rightarrow$ Rust) | **AUC: 0.984** on unseen domain. |
| `04_diagnostic_stress_tests` | Red-teaming the probe (MMLU, Semantics) | Proves linear probes can overfit to keywords without TDA. |
| `05_weight_activation_duality` | Unsloth Rank-1 LoRA extraction | Orthogonal weight subspaces (Sim: `0.0066`). |
| `06_blind_transfer_test` | Zero-shot Cross-Trigger transfer | **AUC: 0.9100** detecting unseen LoRA backdoors. |

## ⚙️ Installation & Usage
This code is optimized to run on a standard T4 GPU (16GB VRAM) using 4-bit NF4 quantization.

```bash
git clone https://github.com/YOUR_USERNAME/topological-belief-monitor.git
cd topological-belief-monitor
pip install -r requirements.txt
pip install "unsloth[colab] @ git+https://github.com/unslothai/unsloth.git"
