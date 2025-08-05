# Data Preprocessing Pipeline — IDS Team 11

## Overview
This document describes the data exploration and preprocessing workflow for the **NSL-KDD dataset**, used to train and evaluate our Intrusion Detection System (IDS) machine learning models.

The workflow is divided into **two Jupyter notebooks**:

1. `notebooks/01_exploratory_data_analysis.ipynb` — Understand and explore the raw dataset.
2. `notebooks/02_preprocessing_test.ipynb` — Clean, encode, scale, and balance the data for model training.

---

## 1. Data Sources
The following raw files are stored in `data/raw/`:
- `KDDTrain+.txt` — Training dataset
- `KDDTest+.txt` — Testing dataset

These are from the NSL-KDD dataset

---

## 2. Notebook 01 — Exploratory Data Analysis (EDA)
**Purpose:**  
To understand the structure, distribution, and quality of the raw data before preprocessing.

**Key Steps:**
- Loaded the raw training dataset with column names.
- Displayed dataset shape, sample rows, and data types.
- Checked for missing values and duplicates.
- Plotted:
  - Class distribution (attack types & normal)
  - Numerical feature distributions (histograms)
  - Correlation heatmap
  - Frequency of categorical features (`protocol_type`, `service`, `flag`)
- Documented observations for preprocessing.

---

## 3. Notebook 02 — Data Preprocessing
**Purpose:**  
To transform the raw dataset into a clean, machine-learning-ready format.

**Steps Performed:**

### **3.1 Missing Value Handling**
- Checked for missing values in both train and test sets.
- Filled numeric NaNs with the column median.
- Filled categorical NaNs with the most frequent value.

### **3.2 Duplicate Removal**
- Removed duplicate rows from both training and testing datasets.

### **3.3 Outlier Handling**
- Outliers were **kept** to preserve rare attack patterns.

### **3.4 Categorical Encoding**
- Encoded `protocol_type`, `service`, `flag`, and `label` using `LabelEncoder`.
- Combined train and test data for encoding to avoid unseen category errors.

### **3.5 Conversion of Object Columns**
- Converted `duration` and `dst_host_srv_rerror_rate` to numeric using `pd.to_numeric(errors="coerce")`.
- Filled any resulting NaNs with `0`.

### **3.6 Feature Scaling**
- Used `MinMaxScaler` to scale all features **except** the `label`.
- Fitted the scaler on the training set and applied to both train and test.

### **3.7 Class Balancing (SMOTE)**
- Applied **SMOTE** only to the **training set** to balance classes.
- Plotted class distribution before and after SMOTE.
- Test set remained unchanged for realistic evaluation.

---

## 4. Output Files
The following files are generated in `data/processed/`:
- `train_processed.csv` — Fully cleaned and balanced training data.
- `test_processed.csv` — Fully cleaned testing data.

---

## 5. Usage
To run the workflow:


