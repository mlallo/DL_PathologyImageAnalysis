# CNNs for Chest X-ray Diagnosis
This repository implements a convolutional neural network (CNN) framework for chest X-ray disease classification and model interpretability. The model is trained to distinguish between cardiomegaly, pneumothorax, and infiltration and uses occlusion sensitivity analysis to highlight image regions that contribute most to each prediction.

### Overview
Chest X-ray images are commonly used to evaluate thoracic pathology. Here, a deep learning CNN is applied to:
- Classify chest X-rays into clinically relevant disease categories
- Visualize spatial regions that influence model predictions
- Compare model-derived attention with known pathology localization

The approach is designed to support interpretability - helping users understand where the model focuses when making diagnostic decisions.

### Dataset
- **Modality:** Chest X-ray
- **Annotations:**
  - Cardiomegaly
  - Pneumothorax
  - Infiltration
- **Input format:** PNG images listed in visualize.csv

### Model Architecture
The CNN consists of:
- Five convolutional blocks with batch normalization and max pooling
- Global average pooling
- Fully connected layers with dropout regularization
- Softmax output for multi-class classification

The trained model weights are loaded from `model1.pth`

### Occlusion Sensitivity Analysis
Occlusion sensitivity is used to interpret model predictions:
- Small square regions of the image are systematically masked
- The change in predicted class probability is measured
- Regions whose occlusion causes the largest confidence drop are considered most important

### Output visualizations include:
- Original chest X-ray
- Occlusion sensitivity heatmap
- Heatmap overlaid on the original image

This provides insight into whether the model focuses on clinically meaningful regions (e.g., lung fields, cardiac silhouette).
