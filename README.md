# ECE_8803_Final_Project

# Biomarker Detection Using the OLIVES Dataset

This project explores hybrid deep learning strategies for detecting multiple retinal biomarkers from Optical Coherence Tomography (OCT) images and clinical metadata using the [OLIVES dataset](https://proceedings.neurips.cc/paper_files/paper/2022/file/3be60b4a739b95a07a944a1a2c41e05e-Paper-Datasets_and_Benchmarks.pdf).

We implement and evaluate multiple deep learning models to address key challenges like multi-label classification, class imbalance, and multimodal learning (image + tabular features).



| Notebook               | Backbone                  | Additional Features                    | Notes                               |
|:------------------------|:---------------------------|:----------------------------------------|:-----------------------------------|
| `Baseline_model.ipynb`  | ResNet50                   | Image only                             | Basic model for multi-label classification |
| `Focal_model.ipynb`     | ResNet50                   | Image only + Focal Loss                | Added Focal Loss to handle class imbalance |
| `Hybrid_model.ipynb`    | ResNet50                   | Image + Tabular (BCVA, CST)            | Combined OCT images with clinical metadata |
| `Best_model.ipynb`      | ResNet101 (partially frozen) | Image + Tabular (BCVA, CST) + Deep MLP | Final model with enhanced feature extraction |

## Methods Overview

- **Dataset**: OLIVES dataset (OCT retinal scans + BCVA, CST metadata)
- **Tasks**: Multi-label classification (B1–B6 biomarkers)
- **Backbones**: ResNet50 and ResNet101
- **Loss Functions**:
  - Baseline: Binary Cross Entropy (BCE)
  - Focal_model: Focal Loss to handle class imbalance
- **Multimodal Fusion**:
  - Hybrid and Best models fuse **tabular clinical features** with **deep image embeddings**.

---

## Visualizations

- Per-class F1 score comparisons across models
- Training loss curves
- Confusion matrices for each biomarker
