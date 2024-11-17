# PoreViT: Automated Pore Typing in Carbonate Rocks

PoreViT is a Vision Transformer-based model for classifying macropores in carbonate rocks from high-resolution thin-section images. The model is designed to automate the labor-intensive process of pore typing, leveraging both local and global spatial features to achieve state-of-the-art performance. This repository contains the code, pre-processing steps, model implementation, and evaluation scripts required to replicate the results presented in the accompanying research paper.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Pre-processing](#pre-processing)
  - [Training](#training)
  - [Evaluation](#evaluation)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Overview

PoreViT introduces a new approach to automate the classification of pores in carbonate rocks. By integrating Vision Transformer (ViT) features with spatial features extracted from Convolutional Neural Networks (CNNs), PoreViT classifies pores into **interparticle**, **separate vug**, and **touching vug** categories. The model leverages:
- **Feature Fusion Block**: Combines ViT and CNN features.
- **Global Token Addition (GTA)**: Captures global context for enhanced classification.
- **Neighborhood Textural Embedding**: Enriches input data with local pore system topology.

The repository provides tools for end-to-end implementation, from pre-processing thin-section images to training and evaluating the model.

---

## Features

- Automated pore classification using Vision Transformers.
- Integration of local and global spatial features for high accuracy.
- Pre-processing pipeline for high-resolution thin-section images.
- Comprehensive evaluation with precision, recall, F1-score, and confusion matrix.
- High throughput, allowing classification of thousands of pores in minutes.

---

## Installation

### Prerequisites

- Python 3.8 or later
- CUDA-enabled GPU (optional but recommended for faster training)

### Clone the Repository

```bash
git clone https://github.com/yourusername/PoreViT.git
cd PoreViT
