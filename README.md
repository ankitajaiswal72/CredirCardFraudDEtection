# CredirCardFraudDEtection

## Overview
This project develops a machine learning model to detect fraudulent credit card transactions using a dataset that includes transaction amount, time, and other features. The goal is to create a highly accurate fraud detection system while minimizing false positives.

## Dataset
The dataset contains:
- **Transaction Time** (normalized to hours)
- **Transaction Amount** (standardized)
- **Various anonymized features**
- **Class Label** (0: Legitimate, 1: Fraudulent)

## Preprocessing Steps
1. **Data Normalization**:
   - The `Amount` and `Time` features are scaled using `StandardScaler`.
2. **Handling Class Imbalance**:
   - Since fraudulent transactions are rare, **SMOTE (Synthetic Minority Over-sampling Technique)** is applied to balance the dataset.

## Model Selection
The fraud detection model uses **XGBoost (Extreme Gradient Boosting)** due to its high performance on imbalanced datasets. The model is trained with:
- **100 estimators**
- **Learning rate of 0.1**
- **Random state set to 42** for reproducibility

## Model Evaluation
The model is assessed using:
- **Classification Report** (Precision, Recall, F1-score)
- **ROC-AUC Score** (Measures overall model performance)

## Installation & Usage
### **Requirements**
Ensure the following libraries are installed:
```sh
pip install pandas numpy scikit-learn imbalanced-learn xgboost
```

### **Running the Model**
Execute the following command:
```sh
python fraud_detection.py
```

## Future Improvements
- Feature engineering to extract meaningful transaction patterns.
- Deployment as a real-time fraud detection API.
- Experimenting with other algorithms like Autoencoders or Deep Learning.

## Repository Structure
```
📁 Fraud-Detection
│── fraud_detection.py  # Model training script
│── creditcard.csv      # Dataset
│── README.md           # Project documentation
```

## License
This project is open-source and available for educational and research purposes.

