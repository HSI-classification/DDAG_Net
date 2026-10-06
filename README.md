# DDAG-Net: Dual-Dictionary Learning and Adaptive Graph Reasoning for Hyperspectral Image Classification

This repository contains an implementation of the paper:

*"DDAG-Net: Spatial-Spectral Collaborative Hyperspectral Image Classification via Dual-Dictionary Learning and Adaptive Graph Reasoning"*

## Overview

Hyperspectral image classification under limited labeled samples remains challenging due to insufficient spatial-spectral collaborative modeling. We propose DDAG-Net, a collaborative classification framework with dual-dictionary discriminative learning, dynamic graph evolution, and adaptive fusion. The dual-dictionary module constructs class-specific and globally shared dictionaries, and performs ISTA-based sparse coding to decouple discriminative information from common background. A channel attention mechanism then refines the sparse features. The dynamic graph evolution module uses superpixels as nodes, constructs an initial graph topology from dual-dictionary sparse features, and adaptively updates adjacency through dynamic graph convolution. Laplacian regularization and spatial attention further enhance spatial continuity. Finally, an adaptive fusion module aligns pixel-level spectral and superpixel-level spatial features and learns to balance their contributions. Experiments on public hyperspectral datasets demonstrate consistent improvements over representative methods. Ablation studies verify the effectiveness of each proposed module.

## Project Structure

- ├── `main.py`
  - Main entry for training and evaluation
- ├── `data_utils.py`
  - Data loading, PCA, superpixel segmentation, and data split
- ├── `model.py`
  - ISTA layer, spectral/spatial attention, dynamic graph convolution, and DDAG-Net
- ├── `train_eval.py`
  - Training and evaluation loop
- ├── `utils.py`
  - Visualization and colormap utilities

- ├── `requirements.txt`
- ├── `LICENSE`

- ├── `data/`
- └── `results/`

## Environment

- Python 3.10+
- PyTorch 2.0+
- numpy, scipy, scikit-learn, scikit-image, matplotlib

Install dependencies:

```bash
pip install -r requirements.txt
