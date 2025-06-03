# MM-KPNN Neural Networks

## 1. Overview
This guide walks you through a simplified, step-by-step implementation of the Multi-Modal Knowledge-Primed Neural Network (MM-KPNN) using PyTorch-Geometric. It covers:

- Loading and preprocessing input graphs (e.g., gene–TF networks, multimodal data)  
- Building the MM-KPNN architecture with biological context  
- Training and evaluating the model on example data  
- Generating performance comparisons and visualizations (e.g., loss curves, accuracy metrics)  
- Integrating external prior graphs as separate edge sets  
All code is in a single Jupyter Notebook (`Pipeline_mm-kpnn.ipynb`) with line-by-line comments to explain the math and logic of the process
---

## 2. Dependencies
To run and view this notebook, you’ll need:

1. **Python ≥ 3.8**  
2. **Jupyter Notebook** (install via `pip install notebook`)  
3. **PyTorch ≥ 1.10** (CPU or GPU build)  
4. **PyTorch-Geometric** (compatible version for your PyTorch build; e.g., `torch-geometric==2.1.0`)  
5. **Additional Python packages**:  
numpy, pandas, scikit-learn, matplotlib, seaborn
6. **Optional**:  
- **NetworkX** (for graph inspection)  
- **plotly** (for interactive visualizations)  

## Quick Start
Launch Jupyter Notebook

Run each cell in order. The notebook is divided into sections:

Data loading & preprocessing

Model definition (MM-KPNN layers, loss functions)

Training loop & evaluation

Performance comparison plots

Integration of external prior graphs (gene–TF networks)


## For full documentation, see docs/README.pdf

Contact & Credits
Author: Sally L. Yepes Torres

Email: sallyepes233@gmail.com

Last Updated: May 2025

License: MIT

