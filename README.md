AI-Driven IDS: Implementing IJCA Vol. 186, No. 69


Project Overview:

This repository contains a machine learning pipeline for Network Intrusion Detection (IDS) using the NSL-KDD dataset. The project benchmarks three distinct architectures (1D-CNN, ANN, and SVM) to evaluate their efficacy in identifying malicious network traffic patterns.

| Model |  Accuracy |  Recall | AUC-ROC | Implementation |
| :--- | :--- | :--- | :--- | :--- |
| **1D-CNN** | **97.58%** | **95.00%** | **0.9952** | Optimized Spatial Filters |
| **ANN (SGD)** | 96.00% | 93.00% | 0.9720 | 128-64-32 Tapered Layers |
| **SVM (RBF)** | 96.38% | 93.00% | 0.9746 | Subsampled (20k rows) |

## Model Architectures

### 1. Convolutional Neural Network (1D-CNN)
Designed to capture spatial correlations between network features. 
* **Layers:** Conv1D (32 filters, kernel size 3) → MaxPool → Dense (64) → Dropout (0.5).
* **Optimizer:** Adam.

### 2. Artificial Neural Network (ANN)
A deep fully-connected network utilizing the paper's specific "funnel" architecture.
* **Layers:** 128 → 64 → 32 neurons with ReLU activation.
* **Optimizer:** SGD with Momentum ($0.9$) and Learning Rate ($0.01$).
  
### 3. Support Vector Machine (SVM)
The traditional baseline using a Radial Basis Function (RBF) kernel.
* **Kernel:** $K(x, x') = \exp(-\gamma \|x - x'\|^2)$.
  To note: I subsampled the dataset.

## Citation
Md. Aminur Rahman, Manjur Ahammed, Mohammad Mizanur Rahaman, Alvi Amin Khan . AI-Driven Cybersecurity: Leveraging Machine Learning Algorithms for Advanced Threat Detection and Mitigation. International Journal of Computer Applications. 186, 69 ( Mar 2025), 50-60. DOI=10.5120/ijca2025924526

[Link to the research article](https://www.ijcaonline.org/archives/volume186/number69/ai-driven-cybersecurityleveraging-machine-learning-algorithms-for-advanced-threat-detection-and-mitigation/)

---
Maintained by **aadhur** | Documenting the journey at [~/notes](https://aadhur.github.io/)