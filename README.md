# ECE_8803_Final_Project


| Notebook               | Backbone                  | Additional Features                    | Notes                               |
|:------------------------|:---------------------------|:----------------------------------------|:-----------------------------------|
| `Baseline_model.ipynb`  | ResNet50                   | Image only                             | Basic model for multi-label classification |
| `Focal_model.ipynb`     | ResNet50                   | Image only + Focal Loss                | Added Focal Loss to handle class imbalance |
| `Hybrid_model.ipynb`    | ResNet50                   | Image + Tabular (BCVA, CST)            | Combined OCT images with clinical metadata |
| `Best_model.ipynb`      | ResNet101 (partially frozen) | Image + Tabular (BCVA, CST) + Deep MLP | Final model with enhanced feature extraction |
