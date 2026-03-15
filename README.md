# Topological Belief State Monitor (TBSM) 🛡️

**Detecting and Intercepting Deceptive Intent (Sleeper Agents) via Activation Geometry in Large Language Models.**

This repository contains the final research paper and figures for the TBSM project, which investigates whether deceptive intent possesses a universal geometric signature in the residual stream of LLMs.

> 🧠 **Note:** The foundational mechanistic interpretability research (Phases 1–8)—proving that algorithmic state is encoded in load‑bearing topological manifolds ($H_1$ rings) within RNNs—is located in our sister repository: **[causal-geometry-algzoo](https://github.com/datasci3nce/causal-geometry-algzoo)**.

## 🔬 Project Overview
Current AI control protocols rely heavily on behavioral outputs or simple linear probes, which are highly susceptible to lexical overfitting. This project investigates whether deceptive intent possesses a universal geometric signature in the residual stream, invariant to:
- Programming language syntax (Python vs. C++ vs. Rust)
- Lexical triggers ("Insert a bug" vs. "Year: 2024")
- Alignment faking methodology (Prompted Deception vs. Weight‑Poisoned LoRA)

## 📄 Paper
- [`tbsm_report.pdf`](./tbsm_report.pdf) – Full research paper with 12‑phase methodology, results, and discussion.

## 📊 Figures
All figures from the paper are in the [`figures/`](./figures) folder:
- `notebook2_grl_separation.png` – Domain‑adversarial probing (syntax invariance).
- `notebook3_cross_lingual.png` – Zero‑shot Rust transfer (AUC 0.984).
- `notebook4_semantic.png`, `notebook4_mmlu.png`, `notebook4_ablation.png` – Diagnostic stress tests.
- `duality_plot.png` – Weight‑activation duality (orthogonal subspaces).
- `notebook6_blind_transfer.png` – Blind transfer test (AUC 0.91).

## 🔑 Key Discoveries
- **Domain‑Adversarial Probing (DALP):** Standard linear probes overfit to syntax. Using Gradient Reversal Layers (GRL), we isolate an intent subspace that transfers zero‑shot to unseen languages (Rust AUC `0.984`).
- **Weight‑Activation Duality:** Prompted deception and fine‑tuned (LoRA) deception occupy **orthogonal subspaces in weight space** (cosine similarity `0.0066`), yet their activation‑space representations align perfectly.
- **Blind Transfer Test:** A probe trained on “Insert a bug” detects a completely different trigger (“Year 2024”) embedded via weight‑poisoning with **AUC 0.9100** – evidence of a universal activation‑space signature.

## ⚙️ Reproducibility
The raw code and Jupyter notebooks used to generate these results are available from the author upon request, or can be reconstructed from the descriptions in the paper. For the RNN foundation, see the sister repository linked above.

## 📬 Contact
Kishore Kumar Mariappan – [your email / website / GitHub profile]
