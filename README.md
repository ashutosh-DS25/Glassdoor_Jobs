# Glassdoor Salary Prediction

This project focuses on analyzing job postings data collected from Glassdoor to understand salary trends and predict estimated salaries for different job roles.

The dataset contains company and job-related information such as job title, company size, sector, location, ownership type, and skills mentioned in job descriptions.  
The objective is to study how these factors influence salaries and to build a machine learning model that can estimate salary ranges.

---

## Workflow

### 1. Data Understanding & Cleaning
- Removed redundant and identifier columns.
- Cleaned salary estimates and converted them into numerical annual salary values.
- Handled missing, unknown, and inconsistent categorical values.
- Engineered features such as average salary from salary ranges.
- Extracted skill indicators (Python, ML, AWS, Tableau, etc.) from job descriptions.

### 2. Exploratory Data Analysis (EDA)
- Analyzed salary distribution across:
  - Company size
  - Sector
  - Location
  - Job titles
- Studied demand for technical skills across job roles.
- Identified patterns showing how salary varies with organizational scale and geography.

### 3. Feature Engineering
- Reduced high-cardinality categorical variables.
- Grouped similar sectors and ownership types to control dimensionality.
- Encoded categorical variables using a combination of ordinal and one-hot encoding.
- Scaled and prepared features using a preprocessing pipeline.

### 4. Model Building
- Trained and compared multiple regression models:
  - Linear Regression
  - Lasso
  - Decision Tree
  - Random Forest
  - Gradient Boosting
  - XGBoost
  - Support Vector Regressor
- Used MAE and MSE as evaluation metrics.

### 5. Model Tuning
- Applied RandomizedSearchCV on XGBoost to optimize hyperparameters.
- Selected the final model based on cross-validated performance.

---

## Results

- XGBoost Regressor performed best among all models.
- The final model achieved a Mean Absolute Error (MAE) of approximately **14k salary units**.
- This indicates that, on average, the predicted salary differs from the actual salary by around this margin.

Rather than exact salary prediction, the model is intended to provide **reasonable salary range estimates** and identify the key factors influencing compensation.

---

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook
- GitHub

---

## Key Insights

- Company size and sector have a noticeable impact on salary levels.
- Certain locations consistently offer higher median salaries.
- Skills such as Python, Machine Learning, and cloud technologies are strongly associated with higher pay.

---

## Conclusion

This project demonstrates an end-to-end data science workflow — from raw data cleaning and exploratory analysis to feature engineering and model tuning.

The focus is on **understanding salary drivers** rather than producing an exact salary figure, making the solution more realistic and interpretable for real-world use cases.
