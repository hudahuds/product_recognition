
 #  Product Recognition using YOLO Classification

##  Project Overview
This project focuses on **product recognition from images** using a YOLO-based classification model.
The objective is to evaluate the robustness of the model under **realistic conditions**, including
**poor image quality**, motion blur, noise, and compression artifacts.

The work is carried out using **Ultralytics YOLO**, **Albumentations** for data augmentation,
and **MLflow** for experiment tracking.

---

## Dataset Structure
The dataset follows a standard classification structure:

data/

├── train/

│ ├── class_1/
│ ├── class_2/
│ └── ... (80classes)

├── val/

│ ├── class_1/
│ ├── class_2/
│ └── ...

└── test/

├── class_1/
├── class_2/
└── ...

Several versions of the dataset were created:
- **Original dataset** (good image quality)
- **Degraded dataset** simulating real-world capture conditions
- **Multiple validation splits with different augmentation pipelines**

---

## 🧪 Data Augmentation Strategy
To simulate realistic scenarios (poor lighting, motion blur, low resolution), we applied:
- Downscaling
- Strong JPEG compression
- Motion blur and Gaussian blur
- Gaussian noise
- Brightness and contrast degradation
- Affine transformations

Albumentations library was used to ensure reproducibility and flexibility.

---

##  Model Training
- Model: `YOLOv11x-cls`
- Task: Image classification
- Image size: 128 × 128
- Training tracked using **MLflow**
- Multiple experiments conducted with different augmentation and training parameters

---

## Evaluation Metrics
The following metrics are monitored:
- **Top-1 Accuracy**
- **Top-5 Accuracy**
- **Training Loss**
- **Validation Loss**
- **Learning Rate per parameter group**

---

## Experiment Tracking
All experiments are logged using **MLflow**, including:
- Hyperparameters
- Training curves
- Accuracy metrics
- Model checkpoints

---

##  Tools & Technologies
- Python
- Ultralytics YOLO
- Albumentations
- MLflow
- OpenCV
- Kaggle GPU environment

---

##  Key Objective
Demonstrate that **very high accuracy on clean data does not necessarily imply robustness**, and
highlight the importance of **data realism** in computer vision models.








