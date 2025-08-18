# Intrusion Detection System (IDS) with NSL-KDD and XGBoost

##  Overview
This project implements an Intrusion Detection System (IDS) using the **NSL-KDD dataset** and the **XGBoost algorithm**. 
The IDS detects malicious network traffic and classifies it as either normal (0) or attack (1).

##  Features
- Data preprocessing (encoding, scaling, SMOTE for imbalance)
- Baseline model: Random Forest
- Main model: XGBoost with hyperparameter tuning
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix
- Model interpretability with **SHAP**
- Ethical considerations of IDS in cybersecurity
- Exported trained model with `joblib`

##  Project Structure
```
├── IDS_NS-KDD_XGBoost_Notebook.ipynb   # Full pipeline notebook
├── IDS_Report.pdf                      # Professional summary report
├── README.md                           # Project documentation
└── model_xgb.joblib                    # Exported trained XGBoost model
```

##  Requirements
- Python 3.8+
- pandas, numpy
- scikit-learn
- xgboost
- imbalanced-learn
- shap
- matplotlib, seaborn

##  Usage
1. Run the notebook step by step to preprocess data and train models.
2. Evaluate results using metrics and SHAP visualizations.
3. The final trained model is saved for reuse in deployment.

##  Results
- XGBoost outperforms Random Forest baseline.
- SHAP reveals the most important features contributing to intrusion detection.

##  Future Work
- Deploy the IDS in a real-time network traffic setting.
- Explore deep learning (LSTM, Autoencoders) for anomaly detection.
- Use MLflow for experiment tracking.

---
Developed by Team 11: *AI for Cybersecurity*
1. Latifah Abubakar - _Experiment Lead_ 
2. Samuel Idana - _Data Engineer_ 
3. Prince Philips - _Model Developer_ 
