**📊 Credit Card Consumption Prediction**
**📌 Project Overview:**
This project aims to predict the average credit card consumption for the next three months for bank customers using demographic and behavioral data. The model helps banks understand customer spending patterns and design targeted marketing strategies.
The solution follows an end-to-end machine learning pipeline, including data preprocessing, feature engineering, model training, validation, and prediction for customers with missing consumption values.

**🏦 Business Context:**
Credit card consumption data provides valuable insights into customer behavior. By predicting future credit card spend, banks can:
•	Identify high-value customers
•	Customize offers and credit limits
•	Improve customer relationship management
•	Optimize marketing campaigns

**🎯 Objective:**
•	Build a regression model to predict average credit card spend (cc_cons) for the next 3 months.
•	Predict values for customers where cc_cons is missing.
•	Evaluate model performance using Root Mean Square Percentage Error (RMSPE).

**🗂️ Datasets Used:**
**The project uses three datasets:**
1.	CustomerDemographics
o	Age, Gender, Income, Account Type, Tenure, Region, etc.
2.	CustomerBehaviorData
o	Credit/Debit card spends, transaction counts, loans, investments, limits, etc.
3.	CreditConsumptionData
o	Target variable: cc_cons (Average credit card spend for next 3 months)
All datasets are merged using a unique Customer ID.

**⚙️ Tech Stack:**
•	Python
•	Pandas, NumPy
•	Scikit-learn
•	Jupyter Notebook

**🔧 Data Preprocessing:**
•	Merged multiple datasets using ID
•	Split data into:
o	Train set: Customers with known cc_cons
o	Test set: Customers with missing cc_cons
•	Handled missing values using:
o	Median imputation for numerical features
o	Most-frequent imputation for categorical features
•	Encoded categorical variables using OneHotEncoder
•	Ensured identical preprocessing for train and test data using Pipeline

**🤖 Model Used:**
•	RandomForestRegressor
•	Hyperparameters:
o	n_estimators = 300
o	max_depth = 10
o	random_state = 42
A unified preprocessing + modeling pipeline was used to avoid data leakage and runtime errors.

**📈 Model Evaluation:**
•	Metric: Root Mean Square Percentage Error (RMSPE)
Validation RMSPE: 0.4074
Interpretation:
•	The model’s predictions deviate by ~40% from actual values on average.
•	This is considered a good baseline performance for customer-level credit consumption prediction, given high variance and skewness in spending behavior.

**📊 Key Results:**
•	Successfully predicted credit consumption for customers with missing target values
•	Built a robust, error-free ML pipeline
•	Established a strong baseline model suitable for further optimization

