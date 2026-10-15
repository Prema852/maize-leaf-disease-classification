# Project Progress Log — Maize Leaf Disease Classification

## Update 1: MobileNetV2 Model Development

**Date:** 15 October 2026

### Objective
Develop an image classification model to identify maize leaf diseases using MobileNetV2.

### Disease Classes
1. Cercospora leaf spot (Gray leaf spot)
2. Common rust
3. Northern leaf blight
4. Healthy leaves

### Dataset
- **Dataset source:** PlantVillage
- **Maize images used for training and validation:** 3,058
- **Training images:** 2,446
- **Validation images:** 612
- **Separate official test images:** 794

### Model Development
- Implemented a MobileNetV2 image classification model.
- Trained the classifier and performed fine-tuning.
- Conducted extended training using validation performance to select the best checkpoint.

### Final Test Results
- **Test accuracy:** 96.73%
- **Macro F1-score:** 0.9565
- **Macro-average ROC-AUC:** 0.9968

### Evaluation
Generated a confusion matrix, multiclass ROC curves, and class-wise ROC-AUC results to evaluate classification performance.

### Next Steps
- Verify labels in the external image dataset.
- Analyze misclassified images.
- Evaluate performance on a larger and more representative set of real-world maize leaf images.
