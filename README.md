# Maize Leaf Disease Classification Using MobileNetV2

## Project Overview

This project focuses on classifying maize leaf images into four categories using a MobileNetV2 deep learning model. The objective is to identify diseased leaves and distinguish them from healthy leaves.

## Disease Classes

1. **Cercospora Leaf Spot (Gray Leaf Spot)**
2. **Common Rust**
3. **Northern Leaf Blight**
4. **Healthy Leaves**

## Dataset

- **Dataset:** PlantVillage
- **Crop:** Maize
- **Training and validation images:** 3,058
- **Training images:** 2,446
- **Validation images:** 612
- **Separate official test images:** 794

The training images were used to train the model, while the validation set was used to monitor model performance and select checkpoints.

## Model and Methodology

The project uses **MobileNetV2**, a convolutional neural network architecture pretrained on ImageNet.

The workflow includes:
- Dataset preparation and preprocessing
- Transfer learning using pretrained MobileNetV2
- Classifier training
- Fine-tuning of selected model layers
- Extended training with validation-based checkpoint selection
- Evaluation using accuracy, F1-score, confusion matrix, ROC curves, and ROC-AUC

## Results

The final extended-training model was evaluated on 794 official test images.

| Evaluation Metric | Result |
|---|---:|
| Test Accuracy | **96.73%** |
| Correct Predictions | 768 / 794 |
| Macro F1-score | 0.9565 |
| Macro-average ROC-AUC | 0.9968 |

### Confusion Matrix

The confusion matrix shows the correct and incorrect predictions for each of the four classes.

![MobileNetV2 Confusion Matrix](results/MobileNetV2-Confusion%20Matrix.png)

### Multiclass ROC Curves

The ROC curves evaluate the model's ability to distinguish each class across different classification thresholds.

![MobileNetV2 Multiclass ROC Curves](results/MobileNetV2%20Multiclass-ROC%20Curve.png)

### Class-wise ROC-AUC

| Class | ROC-AUC |
|---|---:|
| Cercospora | 0.9931 |
| Common Rust | 0.9999 |
| Northern Leaf Blight | 0.9942 |
| Healthy | 0.9999 |
| **Macro-average** | **0.9968** |

![MobileNetV2 ROC-AUC by Class](results/MobileNetV2-ROC_AUC%20by%20Class.png)

## Preliminary External Evaluation

An initial evaluation was conducted using 20 external Google images, with five images per class.

- **Accuracy:** 60% (12/20 images)

This is a preliminary result. The external image labels require verification, and a larger, representative field-image dataset is needed to assess real-world generalization reliably.

## Repository Structure

```text
maize-leaf-disease-classification/
├── notebooks/
│   └── Maize_Disease_MobileNetV2_Benchmark.ipynb
├── results/
│   ├── MobileNetV2-Confusion Matrix.png
│   ├── MobileNetV2 Multiclass-ROC Curve.png
│   └── MobileNetV2-ROC_AUC by Class.png
├── PROGRESS.md
└── README.md
```

## Next Steps

- Verify external image labels.
- Analyze misclassified images.
- Collect more representative maize field images.
- Evaluate generalization on a larger external dataset.

## Tools and Technologies

Python · PyTorch · Torchvision · MobileNetV2 · Google Colab · Scikit-learn · Matplotlib

## Acknowledgements

Dataset source: [PlantVillage on Hugging Face](https://huggingface.co/datasets/mohanty/PlantVillage).

Please review the dataset licence and attribution requirements before redistributing dataset material or using it commercially.
