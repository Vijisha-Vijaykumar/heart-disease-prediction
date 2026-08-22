# heart-disease-prediction
Binary classification model predicting heart disease presence from 13 clinical features (blood pressure, cholesterol, ECG results, etc.), with EDA and hospital-facing recommendations for early cardiovascular risk detection.

## Heart Disease Prediction

**Domain:** Healthcare / Cardiology
**Type:** EDA + Binary Classification

### Dataset
Two linked files — `values.csv` (13 clinical features) and `labels.csv` (target: `heart_disease_present`), merged on `patient_id`. 180 patients total.

### Objective
- Complete EDA on patient cardiac data
- Build a model predicting potential heart disease
- Provide suggestions to hospitals for early detection and prevention

### Approach
- Merged `values.csv` and `labels.csv` on `patient_id`
- Confirmed no missing values and no data entry errors (cleaner dataset than the other healthcare project)
- Target distribution: 100 patients without disease, 80 with (balanced)
- EDA: distributions of age, blood pressure, cholesterol, max heart rate, oldpeak (ST depression); correlation heatmap against the target
- *(In progress: classification model comparison — Logistic Regression, Decision Tree, Random Forest — with cross-validation and tuning, following the same workflow as AutoPricePred)*

### Status
EDA and correlation analysis complete; predictive modeling and Task 3 (hospital suggestions) in progress.

---

## Common Workflow Across All Projects

1. **Data loading & structural checks** (`.shape`, `.info()`, `.head()`)
2. **Data cleaning** — handling missing values (structural vs. genuine), fixing malformed files
3. **EDA** — distributions, summary statistics, correlation heatmaps
4. **Feature preparation** — scaling (StandardScaler) and/or encoding (one-hot) as needed
5. **Train-test split** — stratified where class imbalance is present
6. **Model building** — baseline comparison across Linear/Logistic Regression, Decision Tree, Random Forest
7. **Model evaluation** — regression (MAE/RMSE/R²) or classification (accuracy, precision/recall/F1) metrics as appropriate
8. **Advanced evaluation** (later projects) — 5-fold cross-validation, GridSearchCV hyperparameter tuning, feature importance analysis
9. **Reporting** — Model Comparison Report and Challenges Report for every project, documenting reasoning behind every technique used

## Tools & Libraries Used

`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn` (LinearRegression, LogisticRegression, DecisionTreeClassifier/Regressor, RandomForestClassifier/Regressor, StandardScaler, train_test_split, cross_val_score, GridSearchCV, classification/regression metrics)

All projects were built and run in **Google Colab**, with each submitted as a single Jupyter notebook containing code, outputs, and inline markdown explanations.
