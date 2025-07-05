# IrisGuard: ML-Powered Secure Authentication System

## Overview
A machine learning pipeline for reliable iris recognition with integrated anti-spoofing capabilities, comparing traditional and deep learning approaches. The system achieves up to **99.75% accuracy** (ResNet) while maintaining edge-device compatibility through optimized traditional models (SVM/Logistic Regression).

## Key Features
- **Multi-Model Architecture**:
  - Traditional ML (SVM, Logistic Regression) for edge deployment
  - Hybrid (ViT + Traditional features) for balanced performance
  - Deep Learning (ResNet, Autoencoder) for high-security scenarios

- **Anti-Spoofing Framework**:
  - FAR/FRR metrics for security validation
  - Precision-recall and ROC-AUC evaluation
  - Handcrafted (HOG+LBP) and deep features

- **Optimized Pipeline**:
  - PCA-reduced features (640 → 326 dim)
  - Grayscale normalization + noise reduction
  - Benchmarking suite for model comparison

## Performance Highlights
| Model Type          | Accuracy | Use Case                |
|---------------------|----------|-------------------------|
| ResNet (Deep)       | 99.75%   | High-security facilities|
| Autoencoder         | 99.5%    | Cloud-based auth        |
| ViT + Traditional   | 93%      | Balanced deployments    |
| SVM                 | 73%      | Edge devices           |
| Logistic Regression | 72%      | Interpretable systems   |

## Repository Structure
/irisguard
├── /data_preprocessing # Histogram equalization, resizing
├── /feature_engineering # HOG, LBP, PCA
├── /models
│ ├── traditional_ml # SVM, Logistic Regression
│ ├── hybrid # ViT integration
│ └── deep_learning # ResNet, Autoencoder
├── /evaluation # FAR/FRR, ROC-AUC scripts
└── /deployment # Edge optimization scripts


## Getting Started
```bash
git clone https://github.com/yourrepo/irisguard
cd irisguard
pip install -r requirements.txt
python train.py --model svm --pca True

