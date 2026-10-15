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

---

## Update 2: Fine-Tuning and Extended Evaluation

**Date:** 15 October 2026

### Objective
Further fine-tune MobileNetV2 and evaluate its performance on a larger maize leaf test set.

### Dataset
- **Dataset source:** PlantVillage
- **Training and validation images:** Used the prepared maize image dataset from the Colab workflow.
- **Test images:** 2,331
- **Disease classes:** Healthy, Common Rust, Northern Leaf Blight, and Cercospora Leaf Spot/Gray Leaf Spot.

### Model Development
- Fine-tuned the trained MobileNetV2 model to improve classification performance.
- Saved the best-performing model checkpoint.
- Evaluated predictions on the test images and inspected both correct and incorrect classifications.

### Test Results
- **Test accuracy:** 99.10%
- **Macro precision:** 0.9887
- **Macro recall:** 0.9883
- **Macro F1-score:** 0.9885
- **Correct predictions:** 2,310 out of 2,331
- **Incorrect predictions:** 21 out of 2,331

### Evaluation and Visualization
- Generated a classification report and confusion matrix.
- Created training and validation accuracy and loss graphs.
- Generated actual-versus-predicted image galleries to visualize correct and incorrect classifications.
- Saved the trained model checkpoint and evaluation results for future analysis.

### Next Steps
- Investigate the misclassified images and their prediction confidence.
- Test the model on additional real-world maize leaf images.
- Verify dataset composition and evaluation settings to ensure reproducibility.
- Document the complete training and evaluation workflow.

---

## Overall Project Status

MobileNetV2 has been trained and evaluated for four-class maize leaf disease classification. Two evaluation results have been recorded: 96.73% accuracy on 794 test images in the initial experiment and 99.10% accuracy on 2,331 test images in the extended experiment.

These results belong to separate experiments and should be interpreted according to their respective datasets and evaluation setups. Further validation on representative real-world images is required to assess generalization.
