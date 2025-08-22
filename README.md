# Intrusion Detection System (IDS) with NSL-KDD and XGBoost
Developed by Team 11 for the **Artificial Intelligence and its Applications** course, taken in our third year, second semester,at the **University of Ghana**, under the **Computer Engineering** programme.
This project focuses on building an Intrusion Detection System (IDS) using the **NSL-KDD dataset** and the **XGBoost algorithm** to classify network traffic as normal or attack.

**Project Summary:**  
We designed and implemented a machine learning pipeline for intrusion detection, including data preprocessing, model training, evaluation, and interpretability. The IDS leverages XGBoost for high accuracy and uses SHAP for feature importance analysis. The final model is exported for deployment.

**Team Contributions:**  
1. **Latifah Abubakar** – _Experiment Lead_: Coordinated experiments, managed workflow, and ensured reproducibility of results.  
2. **Samuel Idana** – _Data Engineer_: Handled data preprocessing, feature engineering, and balanced the dataset using SMOTE.  
3. **Prince Philips** – _Model Developer_: Developed and tuned the XGBoost model, performed evaluation, and implemented SHAP for interpretability.


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
├── data                                # Datasets directory
├── models                              # Models directory
└── model_xgb.joblib                    # Exported trained XGBoost model
├── Team 11-IDS.ipynb                   # Full pipeline notebook
├── model_demo.ipynb                    # Model test demo notebook
├── IDS_Report-team11.pdf               # Professional summary report
├── README.md                           # Project documentation

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


