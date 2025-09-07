HR Employee Attrition Analysis with SHAP
📌 Overview

This project analyzes the HR Employee Attrition dataset to identify the main causes of employee resignation and predict future attrition.
We use Python (Pandas, Seaborn, Scikit-learn, SHAP) for analysis and model building, and Power BI for visualization.

The pipeline includes:

Exploratory Data Analysis (EDA) – department-wise attrition, salary bands, promotions.
Modeling – Random Forest classifier with preprocessing (scaling + encoding).
Explainability – SHAP values for global and local feature impact.
Visualization – Power BI dashboards for HR stakeholders.

🛠 Tools & Libraries
Python
pandas → data preprocessing
seaborn, matplotlib → EDA and visualization
scikit-learn → model pipeline (scaling, encoding, RandomForest)
shap → explainable AI (feature importance & predictions explanation)

Power BI
For dashboards on attrition, salary, promotions, department trends

⚙️ Steps Performed
1. Data Preprocessing
Encoded categorical variables (OverTime, etc.) using OneHotEncoder.
Standardized numeric variables like Age, MonthlyIncome, DistanceFromHome, etc.

2. Model Training
Used RandomForestClassifier with class balancing and 300 trees.
Pipeline = Preprocessor (scaler + encoder) → RandomForest.

3. SHAP Value Analysis
Global SHAP Summary Plot
Explains which features (salary, promotions, overtime, job satisfaction, etc.) drive attrition across all employees.
Local SHAP Force Plot
Explains why a single employee is predicted to stay or leave (personalized explanation).

4. Outputs
Generated inside the outputs/ folder:
shap_summary.png → Global drivers of attrition.
shap_force_first_employee.png → Local explanation for one employee.

📊 Power BI Integration

Import model outputs (predictions + SHAP values) into Power BI.
Build dashboards showing:
Attrition by department, salary band, and promotion history
Top SHAP features contributing to attrition
Drill-downs for individual employee risk explanations

🚀 How to Run
Clone the repo and place HR-Employee-Attrition.csv inside.
Install requirements:
pip install pandas seaborn scikit-learn shap matplotlib


Run the analysis script:
python hr_attrition_shap.py


Check generated plots inside the outputs/ folder.

✅ Deliverables
Python script for training + SHAP explanations
SHAP plots for global & local insights
Power BI dashboard for HR stakeholders
