# MM-KPNN: Multi-Modal Knowledge-Primed Neural Network
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17194732.svg)](https://doi.org/10.5281/zenodo.17194732)

This repository contains the implementation of **MM-KPNN** (Multi-Modal Knowledge-Primed Neural Network), a hybrid neural architecture that integrates biological prior knowledge with multi-modal single-cell data (e.g., scRNA-seq, scATAC-seq, spatial transcriptomics) to enhance cell-type classification and interpretability.

MM-KPNN combines the structure of biological networks with the flexibility of graph neural networks and traditional MLP branches to allow data-informed learning while preserving interpretable biological constraints.

## Overview

- **Biological priors**: A gene-regulatory graph encodes domain knowledge (e.g., TF-gene, pathway interactions).
- **Multi-modal input**: Supports scRNA-seq, scATAC-seq, and spatial transcriptomics.
- **Hybrid architecture**: Combines a GNN branch over the prior graph with modality-specific dense branches.
- **Interpretability**: Enables node and edge attribution to uncover the biological drivers of classification.

- Richly commented script guide users through logic, assumptions, and interpretation. "scripts/Pipeline_mm-kpnn.ipynb"
- The Prototype.ipynb serves as a conceptual demonstration of the model's design, flexibility, and explainability features.
- Preprocessing real scRNA-seq, scATAC-seq, and spatial data are provided as supporting material for demonstration.

## Applications

This pipeline supports:
- Interpretability-driven benchmarking of multi-modal architectures
- Biological discovery from prior-informed classification
- Extensions to real-world clinical single-cell datasets

## Quick Start
For full documentation and methods see "docs/README.pdf", "scripts/Pipeline_mm-kpnn.ipynb", and scripts/Prototype.ipynb
  

## Citation

If you use or adapt this framework, please cite:

Yepes S. *MM-KPNN: Multi-Modal Knowledge-Primed Neural Network*.  
GitHub, 2025. https://github.com/Sally332/MM-KPNN-Neural-Network
