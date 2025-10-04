# MM-KPNN: Multimodal Knowledge-Primed Neural Network for Interpretable Integration of Single-Cell Data

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17194732.svg)](https://doi.org/10.5281/zenodo.17194732)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#)
[![Reproducible](https://img.shields.io/badge/reproducible-yes-blue.svg)](#)
[![Pipeline](https://img.shields.io/badge/pipeline-end--to--end-brightgreen.svg)](#)

**A reproducible framework for interpretable multimodal learning in single-cell biology**

---

## Abstract

**MM-KPNN** is an interpretable multimodal deep learning framework that integrates **scRNA-seq** and **scATAC-seq** data through biologically constrained neural architectures.  

Unlike conventional black-box models, MM-KPNN embeds **pathway and transcription factor (TF) priors** directly into the network topology, allowing transparent interpretation of how molecular programs and regulatory networks drive predictions.  
This repository generalizes the original prototype into a **benchmarking platform for multimodal reproducibility and explainability** in single-cell omics.

---

## Key Features

- **Biologically Grounded Architecture**  
  Decoder constrained by **pathway** and **TF nodes**, connecting latent multimodal embeddings to known molecular mechanisms.

- **Cross-Modality Integration**  
  Jointly models **gene expression** and **chromatin accessibility** profiles from the same cells using biologically meaningful links.

- **Mechanistic Interpretability**  
  Generates **pathway- and regulator-level attributions** that can be visualized, benchmarked, and compared across datasets or conditions.

- **Reproducible Infrastructure**  
  Includes standardized preprocessing, training, and evaluation pipelines designed for integration into **HPC or cloud environments**.

---

## Methods Overview

The MM-KPNN framework combines:

1. **Encoder:** modality-specific encoders (e.g., for RNA and ATAC) followed by a shared latent layer.  
2. **Knowledge-Constrained Decoder:** a biologically structured layer mapping latent features to known **Reactome or KEGG pathways**, and then to **transcription factors (TFs)** or **genes**.  
3. **Attribution Module:** computes node- and edge-level relevance using **gradient × input** and **integrated gradients** methods.  
4. **Evaluation Suite:** includes benchmarking tools for interpretability fidelity, modality alignment, and biological consistency.

---

## Results and Example Output

Example analyses include:

- Modality alignment accuracy (RNA–ATAC embedding concordance)  
- Pathway attribution maps highlighting active signaling programs  
- TF–target relevance heatmaps per cell type or cluster  

Example figure scripts are located in `notebooks/figures/`.

---

## Benchmarking and Extension

| Benchmark | Reference Dataset | Comparison | Metric | Result |
|------------|------------------|-------------|---------|---------|
| Multimodal integration | 10x PBMC Multiome | Seurat WNN | Silhouette score | +12% |
| Interpretability fidelity | Simulated cell states | TabNet / DeepLift | Pathway overlap | 0.81 |
| Reproducibility | Multi-seed training | Internal | Feature attribution consistency | 0.92 |

**Future extensions:**
- Integration of **methylation** and **spatial** modalities  
- Support for **explainability benchmarking** across biological contexts  

---
## Quick Start
For full documentation and methods see "docs/README.pdf", "scripts/Pipeline_mm-kpnn.ipynb", and scripts/Prototype.ipynb

---

## Reproducibility and Citation

Each release of this repository is archived and citable via Zenodo DOI.

> Yepes, S. *et al.* “MM-KPNN: Interpretable Multimodal Neural Networks for Single-Cell Integration.” GitHub Repository, 2025.  
> DOI: [10.5281/zenodo.17194732](https://doi.org/10.5281/zenodo.17194732)

