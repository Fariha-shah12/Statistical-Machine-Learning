# Health Behavior and Diabetes Prediction using Support Vector Machines (SVMs)

This project explores the relationship between health behaviors, demographic factors, and the risk of diabetes using Support Vector Machine (SVM) models.
The analysis is based on data from the **National Health Interview Survey (NHIS)**.

We evaluated the performance of **Linear**, **Polynomial**, and **RBF kernel SVMs** to classify individuals as diabetic or non-diabetic.

---

## Dataset
- **Source:** IPUMS Health Survey (NHIS Extract)
- **Features Used:**
  - Demographic: `AGE`, `SEX`, `WEIGHT`, `BMICALC`
  - Health behavior: `ALCANYNO`, `HRSLEEP`, `FRIESPNO`, `VEGENO`, and others
- **Target Variable:** `DIABETICEV` (Ever diagnosed with diabetes: 1 = No, 2 = Yes)

---

## Methodology
- **Data Scaling:**
  - Selected only those responses who are from South Region.
  - Selected only those responses who are greater than equal to 18 years old.
  - Selected only male responses.
  - Scaled down the data from 35k rows to approx 4.5k rows
- **Data Cleaning:**
  - Dropped missing values and invalid codes (e.g., 997, 998, 999)
  - Handled class imbalance using `class_weight='balanced'` in SVM models
- **Feature Engineering:**
  - Selected important variables based on correlation and permutation importance
  - Standardized features using `StandardScaler`
- **Modeling Approach:**
  - Applied Linear, RBF, and Polynomial SVMs
  - Hyperparameter tuning using `GridSearchCV`
  - Visualized decision boundaries using `mlxtend.plotting`
- **Evaluation Metrics:**
  - Accuracy
  - Precision, Recall, F1-Score
  - Confusion Matrix
---

## Results
- **Best Performing Model:** RBF SVM
- **Key Observations:**
  - RBF SVM captured nonlinear relationships better compared to Linear and Polynomial kernels.
  - Class imbalance (low diabetic cases) negatively impacted precision for diabetic prediction.
  - Important predictors included BMI, weight, age, and alcohol consumption patterns.

---

## Visualizations
- SVM Decision Boundaries (Linear, RBF, Polynomial)
- Correlation Matrix of Top Predictors
- Class Distribution Plot

---

## Project Structure
```
nhis_2022.csv                  # Dataset from National Health Interview Survey (NHIS)
PracticalWorksheet02.ipynb      # Main Jupyter Notebook with code, models, and visualizations
README.md                       # Project description
Poster_Presentation_By_Fariha.pptx # Poster With summarise results description of Practical Worksheet
```

---

## Key Learnings
- Designing predictive pipelines using SVMs
- Managing imbalanced health datasets
- Visualizing decision boundaries for model interpretability
- Applying hyperparameter tuning to improve model generalization

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Fariha-shah12/DATA-5322-01-25SQ-Statistical-Machine-Learning-2.git
   ```
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn mlxtend
   ```
3. Open `PracticalWorksheet02.ipynb` and run all cells sequentially.

---

## Acknowledgements
- IPUMS Health Survey
- Seattle University (Course: Statistical Machine Learning II)
- Course Instructor ( Ariana Mendible - mendible@seattleu.edu )

# Contact
- If you have any questions or feedback, feel free to reach out to me:
Email: fshah1@seattleu.edu

---

