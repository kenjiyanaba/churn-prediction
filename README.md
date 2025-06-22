# 🔄 Customer Churn Prediction

## Overview
This project uses customer account, service, and demographic data to predict churn in a telecom company. The goal is to identify customers likely to cancel their services so the business can take proactive action.

### Tools & Libraries
- **Python**: pandas, numpy, matplotlib, seaborn
- **scikit-learn**: modeling, evaluation, GridSearchCV
- **joblib**: model export

---

## 1. Exploratory Data Analysis (EDA)
- Inspected distribution of key features
- Visualized churn rates by service type, contract length, and charges
- Identified strong relationships between contract type and churn

## 2. Preprocessing
- Dropped `customerID` as a non-predictive ID column
- Converted `TotalCharges` to numeric and filled missing values
- Encoded categorical variables using `pd.get_dummies`

---

## 3. Modeling
### Models Trained:
- Logistic Regression
- Random Forest (base)
- Random Forest (with hyperparameter tuning)

### Evaluation Metrics:
- Confusion Matrix
- Classification Report
- ROC AUC Curve

---

## 4. Results
- **Best model**: Random Forest (GridSearchCV-tuned)
- **AUC Score**: High-performing classifier on test set
- **Top Features**:
  - `Contract_Two year`
  - `MonthlyCharges`
  - `tenure`
  - `OnlineSecurity_No`

---

## 5. Exported Model
The final tuned model is saved using `joblib`:
```python
joblib.dump(best_rf, "churn_rf_model.pkl")
```

---

## 6. Next Steps
- Build an interactive **dashboard** using Streamlit or Flask
- Add **SHAP** explanations for model interpretability
- Deploy model as an API or on a cloud platform

---

## 7. How to Run This Project
1. Clone the repo:
```bash
git clone https://github.com/kenjiyanaba/churn_prediction.git
cd churn_prediction
```
2. Install requirements:
```bash
pip install -r requirements.txt
```
3. Open Jupyter Notebook:
```bash
jupyter notebook 01_eda.ipynb
```
4. Train models, view metrics, and explore results.

---

## Author
**Kenji Liu**  
[GitHub](https://github.com/kenjiyanaba) | [Portfolio](https://kenjiyanaba.github.io/) | [LinkedIn](https://linkedin.com/in/kenji-liu)

---

## License
This project is open-source and free to use under the [MIT License](LICENSE).
