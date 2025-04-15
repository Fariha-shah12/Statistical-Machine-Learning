
#  Youth Substance Use Prediction with Machine Learning

This Practical Worksheet leverages data science and machine learning techniques to explore and predict patterns of youth substance use (Marijuana and Alcohol). It includes binary classification, multi-class classification, and regression modeling using scikit-learn.

---

##  Dataset Overview

The dataset consists of youth responses on drug usage, peer influence, risk perception, and demographics. Key columns include:
- **MRJFLAG**: Binary marijuana use indicator.
- **MRJYDAYS**: Frequency of marijuana use (multi-class target).
- **IRALCAGE**: Age of first alcohol use (regression target).

---

##  Project Tasks

### 1. Binary Classification – Predicting Marijuana Use (`MRJFLAG`)
####  Models Used:
- Decision Tree
- Pruned Decision Tree (GridSearchCV for max_depth and min_samples_leaf)
- Random Forest
- Gradient Boosting

####  Key Features:
- `FRDMJMON`, `YFLMJMO`, `FRDMEVR2`, `YFLTMRJ2`, `PRMJMO`, `PRMJEVR2`  
(Peer and parental attitudes towards marijuana)

### 2. Multi-Class Classification – Predicting Marijuana Use Frequency (`MRJYDAYS`)
Remapped to categories:
- `0`: Light (1–2 times)
- `1`: Moderate (3–4 times)
- `2`: Heavy (5–6 times)

####  Models Used:
- Decision Tree
- Pruned Tree (with GridSearchCV)
- Random Forest
- Gradient Boosting

####  Key Features:
- `STNDSMJ`, `STNDALC`, `YOSTOLE2`, `STNDDNK`, `YOSELL2`  
(Youth perception of risk and risky behavior)

### 3. Regression – Predicting Age of First Alcohol Use (`IRALCAGE`)
####  Models Used:
- Decision Tree Regressor
- Pruned Tree (GridSearchCV for optimal tree size)
- Random Forest Regressor
- Gradient Boosting Regressor

####  Key Features:
- `YOFIGHT2`, `YOGRPFT2`, `YOSTOLE2`, `TALKPROB`, `YOATTAK2`  
(Youth engagement in physical fights, theft, and communication problems)

---

##  Evaluation Metrics

- **Classification**: Accuracy, Precision, Recall, F1-score, Confusion Matrix
- **Regression**: Mean Squared Error (MSE)

---

## Repository Structure

```
.
├── PracticalSheet_Fariha.ipynb
├── youth_data.csv
└── README.md
```

---

## Requirements

Install all required dependencies using:

```bash
pip install -r requirements.txt
```

**Key Libraries**:
- pandas, numpy
- scikit-learn
- matplotlib, seaborn

---

## Author

**Fariha Shah**  
[LinkedIn](https://www.linkedin.com/in/shahfariha/)  
_Data Engineer | ML Enthusiast | Full Stack Developer_

---

## Key Insights

- Peer and parental perception significantly affect youth marijuana use.
- Class imbalance must be handled carefully in multi-class classification.
- Risky behavior is weakly correlated with earlier alcohol use.

---

##  Future Improvements

- Apply SMOTE or other class balancing techniques.
- Test neural networks and ensemble stacking.
- Deploy models with interactive dashboards (e.g., Streamlit).

