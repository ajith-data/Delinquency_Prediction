Delinquency Prediction Project
📌 Project Overview

The Delinquency Prediction Project aims to predict whether a customer will become delinquent based on their financial and demographic attributes. This predictive model helps financial institutions minimize credit risk and make better loan approval decisions.

🛠️ Objective

Predict delinquent accounts using machine learning techniques.

Provide insights into financial behavior based on customer data.

Assist financial institutions in identifying high-risk borrowers early.

📂 Dataset

The dataset contains customer financial and demographic information including:

Customer_ID: Unique identifier for customers

Income: Annual income of the customer

Credit_Score: Customer's credit score

Loan_Balance: Outstanding loan balance

Employment_Status: Employment status of the customer

Delinquent_Account: Target variable (Yes/No)

The dataset is stored as Delinquency_prediction_dataset.xlsx.

🔍 Data Understanding & Cleaning

Checked the dataset structure and missing values:

Filled missing Income and Loan_Balance values with median.

Dropped rows with missing Credit_Score.

Created new features:

Debt-to-Income Ratio = Loan_Balance / Income

Credit Segment: Categorized credit scores into At-risk, Moderate, Healthy, Premium.

DTI Buckets: Categorized debt-to-income ratio into Low, Medium, High, Very High.

📊 Exploratory Data Analysis (EDA)

Target variable distribution analyzed with bar charts.

Correlation heatmap to identify relationships among numerical features.

Cross-tab analysis to observe:

Credit segment vs delinquency

Debt-to-income ratio vs delinquency

Employment status vs delinquency

Boxplots to compare income distribution for delinquent and non-delinquent customers.

🧩 Data Preparation for Modeling

Dropped unnecessary features: Credit_segment and DTI_Bucket.

Split the dataset into features (X) and target (Y).

Identified column types:

Numerical columns: int64 / float64

Categorical columns: object

Train-test split:

80% training, 20% testing

Stratified sampling to maintain target distribution

⚙️ Preprocessing Pipeline

Used a ColumnTransformer for preprocessing:

Numerical features: StandardScaler

Categorical features: OneHotEncoder (handle unknown categories)

🤖 Model Building
1. Logistic Regression

Used class_weight='balanced' to handle class imbalance

Metrics:

Classification Report

ROC-AUC Score

2. Decision Tree Classifier

Maximum depth = 5

class_weight='balanced'

Evaluated using:

Classification Report

ROC-AUC Score

Confusion Matrix

📈 Results

Both models were able to identify delinquent customers with reasonable accuracy.

Logistic Regression provides probabilistic predictions, useful for risk scoring.

Decision Tree provides interpretable rules for financial decision-making.

💻 Libraries Used
pandas, numpy, matplotlib, seaborn, scikit-learn

🔗 How to Run

Clone the repository

git clone <your-repo-link>


Install dependencies

pip install -r requirements.txt


Run the Jupyter notebook

jupyter notebook delinquency_prediction.ipynb


Ensure the dataset Delinquency_prediction_dataset.xlsx is in the same directory.

📌 Key Takeaways

Debt-to-Income ratio and Credit Score are strong indicators of delinquency.

Employment status also influences default probability.

Machine learning models can assist in early identification of high-risk customers.

🔖 Future Improvements

Use ensemble models like Random Forest or XGBoost for better accuracy.

Perform hyperparameter tuning to optimize model performance.

Incorporate additional features like payment history and credit utilization.
