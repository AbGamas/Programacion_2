# Breast Cancer Classification - KNN

## Overview
An end-to-end machine learning pipeline for breast cancer diagnosis using K-Nearest Neighbors (KNN).  
**Goal**: Classify tumors as malignant (1) or benign (0) based on cell features.

## Requirements
```bash
Python 3.8+  
pip install pandas scikit-learn matplotlib seaborn mlflow joblib

# How to Run
Clone the repository:

git clone https://github.com/AbGamas/Challenges_programacion2.git

Navigate to the project:

cd Challenges_programacion2/Challenge_1

Execute the script:

python breast_cancer_knn.py

# Outputs

Metrics: Printed in console (Accuracy, Precision, Recall, etc.)

Visualizations: Saved in Imágenes/:

confusion_matrix.png

roc_curve.png

Models:

knn_model.pkl (Trained KNN)

scaler.pkl (Feature scaler)

# MLFlow Tracking

Start MLFlow server:

mlflow ui --backend-store-uri sqlite:///mlflow.db

Access results at:
http://localhost:5000