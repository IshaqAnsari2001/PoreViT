# PoreViT: Automated Pore Typing in Carbonate Rocks

PoreViT is a Vision Transformer-based model developed for the automated classification of macropores in carbonate rocks using high-resolution thin-section images. This repository provides the full implementation of PoreViT, including data pre-processing, training, and evaluation scripts, as well as the dataset used for model training. The repository also includes the final research paper and supplementary materials for further insights into the model and its performance.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [References](#references)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

---

## Overview

The classification of pores into genetic morphotypes is crucial in carbonate petrography for linking pore-scale textures to petrophysical signatures. PoreViT automates this task by leveraging Vision Transformer (ViT) architecture combined with Convolutional Neural Network (CNN) features. This hybrid approach achieves high accuracy in classifying pores into three categories:
- **Interparticle Vug**
- **Separate Vug**
- **Touching Vug**

This repository contains all necessary scripts to replicate the PoreViT model and train it using the provided dataset.

---

## Features

- **Automated pore classification**: Eliminates the need for manual pore typing, making the process scalable and efficient.
- **Vision Transformer integration**: Leverages global spatial features for nuanced classification.
- **CNN augmentation**: Captures local spatial details to complement ViT features.
- **Pre-processing pipeline**: Enhances thin-section images and integrates neighborhood textural information.

---

## Installation

### Prerequisites

- Python 3.8 or later
- CUDA-enabled GPU (recommended for faster training)

### Clone the Repository

```bash
git clone https://github.com/yourusername/PoreViT.git
cd PoreViT
```
## Dataset

The dataset used for training and testing the model is included in the `dataset/` folder. It contains three subdirectories, each corresponding to a pore class:

- `dataset/interparticle_vug/`
- `dataset/separate_vug/`
- `dataset/touching_vug/`

Each folder contains pre-processed images labeled according to the pore type. Ensure the folder structure is maintained for seamless training and evaluation.

## Model Architecture

PoreViT integrates:

- **Vision Transformer (ViT)**: Processes images as sequences of patches to capture global relationships
- **CNN Backbone**: Extracts local spatial features for enhanced context
- **Feature Fusion Block**: Merges global and local features for comprehensive classification
- **Global Token Addition (GTA)**: Incorporates global context for better long-range dependencies

The model processes 224x224 images divided into patches and employs multi-head self-attention mechanisms to classify pores effectively.

## Acknowledgements

This project was supported by:

- Qatar National Research Fund (QNRF)
- ExxonMobil

We also thank the research team for their contributions to data collection and model development.
## Contact

For questions or collaborations, please contact:

- Yemna Qaiser (yemna.qaiser@gmail.com)
- Mohammed Ishaq (m.ishaq.ansari.2001@gmail.com)
## License

See the `LICENSE` file for details.

## References

For details on model performance, methodology, and results, please refer to the **research paper** included in this repository: `paper/PoreViT_Paper.pdf`. Supplementary materials are also provided in the `paper/` folder for additional context.
