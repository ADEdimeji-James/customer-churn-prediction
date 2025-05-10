# customer-churn-prediction
Customer Churn Prediction is a machine learning project that aims to identify customers who are likely to stop using a telecom service. The project uses classification models such as Random Forest, XGBoost, and Decision Trees to predict churn based on features like contract type, monthly charges, internet service, and support options.
# Project Overview
- **Goal**: Predict customer churn using structured telecom data.
- **Target Variable**: `Churn` (Yes/No)
- **Models Used**:
  - Decision Tree
  - Random Forest
  - XGBoost (Best Performing)
  - 
  - # Key Steps in the Workflow
1. **Data Cleaning**
   - Handled missing values in `TotalCharges`
   - Converted object datatypes to numerics
   - Simplified multi-category columns to binary `Yes/No`

2. **Feature Engineering**
   - Label Encoding for binary categorical columns
   - One-hot encoding for multi-category features
   - Correlation check and dimensionality simplification

3. **Handling Imbalanced Data**
   - Used **SMOTE** to oversample minority class (Churn = Yes)

4. **Model Building and Tuning**
   - Evaluated multiple models using cross-validation
   - Tuned hyperparameters using **RandomizedSearchCV**
   - Selected XGBoost based on accuracy

5. **Model Evaluation**
   - Evaluated model performance on unseen test data
   - Metrics used: Accuracy, Confusion Matrix
  
   - # Technologies Used
- Python (Pandas, Scikit-learn, XGBoost)
- SMOTE (imbalanced-learn)
- Flask (for deployment)
- Pickle (model serialization)
- Jupyter Notebook (development)

- # Files in this Repo
| File | Description |
|------|-------------|
| `Customer_Churn_Prediction.ipynb` | Full Jupyter Notebook |
| `customer_churn_model.pkl` | Pickled model for deployment |
| `WA_Fn-UseC_-Telco-Customer-Churn` | Dataset used for the project |
| `requirements.txt` | Python dependencies |
| `README.md` | Project summary |
| `Encoders.pkl` | Serialized label encoders used to preprocess categorical features before prediction |
