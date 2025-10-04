# MM-KPNN: Multimodal Knowledge-Primed Neural Network for Interpretable Integration of Single-Cell Data

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17194732.svg)](https://doi.org/10.5281/zenodo.17194732)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#)
[![Reproducible](https://img.shields.io/badge/reproducible-yes-blue.svg)](#)
[![Pipeline](https://img.shields.io/badge/pipeline-end--to--end-brightgreen.svg)](#)

**A reproducible framework for interpretable multimodal learning in single-cell biology**

---

## Abstract

**MM-KPNN** is an interpretable multimodal deep-learning framework that integrates **scRNA-seq**, **scATAC-seq**, and **spatial transcriptomics** data through biologically constrained neural architectures. Building upon existing multimodal models, MM-KPNN introduces **pathway- and transcription-factor-aware connectivity** within the network topology, enabling transparent interpretation of how molecular programs and regulatory networks drive predictions. This repository generalizes the original single-cell prototype into a **reproducible benchmarking platform for multimodal integration and explainability**, supporting expansion to real datasets, regulatory priors, and biological validation.

---

## Key Features

- **Biologically Grounded Architecture**  
  Decoder constrained by **pathway** and **TF nodes**, linking latent representations to biologically interpretable output logits.

- **Cross-Modality Integration**  
  Jointly models **gene expression**, **chromatin accessibility**, and **spatial features** within a unified multimodal graph framework.

- **Mechanistic Interpretability**  
  Produces **pathway- and regulator-level attributions**, including node and edge relevance via *gradient × input*, *integrated gradients*, and *GNNExplainer*-compatible modules.

- **Reproducible Infrastructure**  
  Implements standardized data handling, model training, and evaluation pipelines ready for **HPC or cloud environments**.

---

## Methods Overview

The core framework is implemented in:

- `scripts/Pipeline_mm-kpnn.ipynb` – complete MM-KPNN training and evaluation pipeline  
- `scripts/Prototype.ipynb` – compact version for experimentation or adaptation

**Model Architecture**

1. **Encoder:** modality-specific encoders (RNA, ATAC, spatial) projecting inputs to a shared latent representation.  
2. **Knowledge-Constrained Decoder:** biologically structured layers mapping latent features to **Reactome/KEGG pathways**, then to **TFs** and **genes**.  
3. **Attribution Module:** computes node- and edge-level relevance using *gradient × input*, *integrated gradients*, and *GNNExplainer* methods.  
4. **Evaluation Suite:** includes benchmarking tools for interpretability fidelity, modality alignment, and biological consistency.

---

## Executable Documentation and Design Transparency

The notebooks in this repository are written to maximize **clarity and interpretability**, not just execution.  
Each pipeline includes detailed in-line documentation explaining the **scientific rationale, assumptions, and decisions** behind each step — from data preprocessing to model interpretation.

Key design principles:
- **Transparent logic** – Each analytical step links computational choices to biological motivation.  
- **Integrated results** – Figures, metrics, and outputs are embedded directly in the workflow to ensure interpretability.  
- **Modular organization** – Code follows the structure of the stepwise guide in `docs/README.pdf`, enabling selective reuse or adaptation.  

This approach transforms the repository into **a reproducible and interpretable record of model reasoning**, adding scientific value beyond conventional scripts.

---

## Results and Biological Insight

MM-KPNN demonstrates how biologically informed architectures can achieve **accurate, interpretable, and transferable** multimodal integration across diverse single-cell datasets.

**Model performance and interpretability outcomes include:**
- **Multimodal alignment** – joint RNA–ATAC embeddings preserve cell-type topology and improve separation by molecular identity.  
- **Pathway-level attribution** – interpretable activation patterns reveal dominant signaling and regulatory programs (e.g., TGF-β, WNT, and interferon responses).  
- **Regulatory driver identification** – edge- and node-level attributions highlight key transcription factors and regulatory connections shaping cell-type predictions.  
- **Cross-dataset robustness** – embeddings and attributions remain stable across random seeds, feature subsets, and batch-corrected inputs.  
- **Explainability benchmarking** – results include quantitative metrics for attribution fidelity and overlap with curated pathway databases.

All analyses are fully reproducible through the main pipeline notebooks, which integrate quantitative metrics, visualizations, and interpretive commentary at each step.

---

## Benchmarking and Expansion

The framework has been validated across multiple datasets, showing consistent multimodal alignment, robust interpretability metrics, and reproducible feature attributions. It is designed for **scalability and extension**, supporting additional modalities (e.g., methylation or spatial data) and integration of **regulatory priors** to expand biological interpretability. The repository also includes concise guidance for **parameter tuning and graph adaptation** to facilitate deployment across datasets and experimental contexts.

---

## Quick Start

For full documentation and methods, see:  
- `docs/README.pdf`  
- `scripts/Pipeline_mm-kpnn.ipynb`  
- `scripts/Prototype.ipynb`

---

## Reproducibility and Citation

Each release of this repository is archived and citable via Zenodo DOI.

> Yepes, S. *et al.* “MM-KPNN: Interpretable Multimodal Neural Networks for Single-Cell Integration.” GitHub Repository, 2025.  
> DOI: [10.5281/zenodo.17194732](https://doi.org/10.5281/zenodo.17194732)
