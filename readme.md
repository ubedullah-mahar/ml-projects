# 🏠 California Housing Price Prediction

## 📌 Project Overview

This project focuses on predicting housing prices using the California Housing dataset.

The goal of this project was to implement and understand the complete Machine Learning workflow, including:

- Data exploration
- Data preprocessing
- Feature engineering
- Model training
- Model evaluation
- Model comparison

The primary algorithm used was Linear Regression, along with Ridge and Lasso Regression for comparison.

---

## 📊 Dataset Information

The dataset contains district-level housing information from California, including:

- Median income
- Housing median age
- Total rooms
- Total bedrooms
- Population
- Households
- Latitude & Longitude
- Ocean proximity (categorical feature)

🎯 **Target Variable:**
`median_house_value`

---

## 🔎 Exploratory Data Analysis (EDA)

The following steps were performed:

- Checked dataset structure and data types
- Identified and handled missing values
- Filled missing values in `total_bedrooms` using median imputation
- Analyzed target variable distribution
- Generated correlation heatmap
- Created scatter plots for key relationships
- Examined categorical feature (`ocean_proximity`)
- Visualized potential outliers using boxplots

### Key Insights

- Median income showed the strongest correlation with house prices.
- Geographic location (latitude & longitude) influenced pricing.
- The target variable showed right-skewed distribution.

---

## 🛠 Data Preprocessing

- Median imputation for missing values
- One-hot encoding for categorical feature (`ocean_proximity`)
- Converted boolean dummy variables to numeric format
- Train-test split (80% training, 20% testing)
- Feature scaling using `StandardScaler`

---

## 🤖 Models Implemented

### 1️⃣ Linear Regression  
Baseline regression model.

### 2️⃣ Ridge Regression  
L2 regularization applied to reduce multicollinearity.

### 3️⃣ Lasso Regression  
L1 regularization applied for coefficient shrinkage.

---

## 📈 Model Performance

| Model              | R² Score |
|--------------------|----------|
| Linear Regression  | ~0.62    |
| Ridge Regression   | ~0.62    |
| Lasso Regression   | ~0.62    |

### Observation

Regularization did not significantly change the R² score, suggesting:

- The model was not heavily overfitting.
- Linear models have inherent limitations on this dataset.

---

## 🧠 Key Learnings

- Proper preprocessing significantly affects model performance.
- Feature scaling is important for linear models.
- Regularization stabilizes models but does not always increase R².
- Real-world datasets are rarely perfectly linear.
- R² values around 0.6–0.7 are realistic for baseline linear regression on this dataset.

---

## 🚀 Future Improvements

- Log transformation of target variable
- Polynomial feature expansion
- Hyperparameter tuning
- Tree-based models (Random Forest, Gradient Boosting)
- Building a full ML pipeline using `Pipeline`
- Model deployment using Flask or FastAPI

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn