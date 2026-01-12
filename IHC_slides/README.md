# Histopathology IDC Classification with CNN

### Overview
This project implements a **Convolutional Neural Network (CNN)** to classify histopathology image tiles for the presence of **Invasive Ductal Carcinoma (IDC)**.  

The goal is to enable rapid, automated diagnosis of malignancies from immunohistochemistry (IHC) slides.  

The model takes image tiles from patient histopathology slides and predicts whether each tile contains IDC (`1`) or normal tissue (`0`).

## Modality
- **Data Type:** Histopathology / IHC images  
- **Task:** Binary classification (IDC vs Normal)  
- **Input:** Image tiles (`.png`)  
- **Output:** Prediction per tile (IDC or Normal)
