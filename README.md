# ✈️ Flight Delay Prediction with Machine Learning

This project aims to predict **flight departure delays** using flight and weather-related features. It includes data preprocessing, feature engineering, exploratory analysis, and training/testing of multiple machine learning regression models.

---

## 📦 Dataset

- **Target variable**: `DEP_DELAY` (departure delay in minutes)
- **Features**: Flight metadata, time-based variables, and weather conditions
- **Cleaning steps**:
  - Removed irrelevant columns (`TAIL_NUM`, `OP_UNIQUE_CARRIER`, etc.)
  - Filtered out extreme delays (kept delays < 60 minutes)
  - Handled nulls and outliers
  - One-hot encoded categorical features (`Condition`, `Wind`)

---

## 🔍 Exploratory Data Analysis

- Histograms and boxplots for numeric feature distribution
- Heatmap of feature correlations
- Focused analysis on variables correlated with `DEP_DELAY`

---

## 🔧 Modeling Approach

### Data Split
- Training: 80%
- Testing: 20%

### Models Used

**Linear Models**
- Linear Regression (with scaling and polynomial features)
- Ridge Regression
- Lasso Regression

**Tree-based Models**
- Decision Tree
- Random Forest
- Gradient Boosting
- AdaBoost
- Bagging Regressor
- XGBoost

**Other Models**
- Support Vector Regression (Linear & RBF kernels)
- k-Nearest Neighbors

### Hyperparameter Tuning
- Used `GridSearchCV` with 5-fold cross-validation

---

## 📊 Evaluation Metrics

Each model was evaluated on:
- **MAE**: Mean Absolute Error
- **RMSE**: Root Mean Squared Error
- **R² Score**: Coefficient of Determination

Performance comparison is visualized using bar charts.

---

## ✅ Results

- Top-performing models included:
  - **XGBoost**
  - **Gradient Boosting**
  - **SVR (RBF kernel)**
- Visual comparison of metrics across all models

---

## 📈 Visualizations

- Feature histograms and boxplots
- Correlation matrix heatmap
- Model performance comparisons (bar plots)

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
