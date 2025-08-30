# Banking Customer Churn Python Analysis  

## 📌 Project Overview  
This project explores **customer churn in a retail bank** using exploratory data analysis (EDA), statistical tests, and machine learning. The goal is to identify factors that drive churn, visualize patterns across customer segments, and build a predictive model to support retention strategies.  

## 🔍 Key Objectives  
- Understand the demographics and financial behavior of customers who churn.  
- Visualize churn rates across different groups (age, gender, geography, balance).  
- Engineer new features to capture meaningful relationships (e.g., age–balance interaction, tenure grouping).  
- Apply statistical tests to validate associations between features and churn.  
- Build and tune a **Random Forest Classifier** to predict churn.  

## 📊 Exploratory Data Analysis  
The analysis includes:  
- **Churn Segmentation:** Churn rates by age group, balance group, country, and gender.  
- **Distributions:** Histograms with skewness & kurtosis annotations for age, balance, credit score, and salary.  
- **Bivariate Analysis:** Boxplots comparing churn vs. numerical features.  
- **Demographics:** Count plots for gender, geography, activity status, and product holding.  
- **Correlation Heatmap:** Identifying linear relationships among key features.  

**Key Insights:**  
- Higher churn observed among customers aged **41–50** and those with **mid-range balances**.  
- **Geography** plays a role, with churn rates varying across countries.  
- Inactive members are significantly more likely to churn.  

## 🧪 Statistical & Feature Engineering  
- **Chi-square tests** confirm associations between categorical variables (e.g., tenure group, activity status) and churn.  
- **T-tests** highlight differences in continuous variables (e.g., age, balance) between churned and retained customers.  
- **Engineered features** include:  
  - Age group categories  
  - Balance-to-salary ratio  
  - Age–balance interaction feature  
  - Tenure grouping  

## 🤖 Machine Learning Model  
- **Model:** Random Forest Classifier  
- **Steps:**  
  1. Train-test split (70/30)  
  2. One-hot encoding for categorical variables  
  3. Baseline random forest training and evaluation  
  4. Hyperparameter tuning via **RandomizedSearchCV** with cross-validation  
- **Metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix  
- **Outcome:** Improved balanced performance with tuned parameters, highlighting the most important churn predictors.  

## 📂 Project Structure  
- `refined_banking_churn.py` → Main analysis script  
- `joined_bank2.csv` → Input dataset (not included here)  
- `*.png` → Saved visualization outputs (e.g., churn rates by segments, heatmaps, random forest feature importance)  

## ⚙️ Dependencies  
- Python 3.x  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn  
- scipy  

## 🚀 How to Run  
1. Clone this repository.  
2. Place `joined_bank2.csv` in the same working directory or update the file path in the script.  
3. Run the script:  
   ```bash
   python refined_banking_churn.py
4. Generated plots and model evaluation metrics will be saved in the working directory.

## 📈 Potential Improvements
- Extend to other ML models (XGBoost, LightGBM)
- Deploy as interactive dashboard e.g., Power BI
- Incorporate time-based churn prediction
