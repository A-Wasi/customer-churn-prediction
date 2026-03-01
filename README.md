# Customer Churn Prediction
## Predicting Customer Churn for a Telecom Company Using Machine Learning

### Project Overview
This project builds a machine learning model to predict which customers 
are likely to cancel their subscription (churn) before they actually do. 
Early identification of at-risk customers allows the business to intervene 
with targeted retention strategies, potentially saving significant monthly revenue.

### Business Problem
A telecom company with 7,032 customers has a 26.5% churn rate. 
At an average monthly charge of $64.76 per customer, undetected churn 
represents significant revenue loss. This model identifies at-risk customers 
early so the business can act before losing them.

### Key Findings
- Contract type is the strongest predictor of churn (-0.40 correlation)
- Month-to-month customers churn at 42.7% vs only 2.8% for two-year contracts
- Fiber optic customers churn at 41.9% - nearly double the overall rate
- Electronic check users churn at 45.3% - highest of all payment methods
- Senior citizens churn at 41.7% vs 23.7% for non-senior customers
- Customers with Online Security and Tech Support addons churn significantly less

### Model Performance
| Metric | Default (0.5) | Tuned (0.3) |
|--------|--------------|-------------|
| Recall | 49% | 76% |
| Precision | 63% | 52% |
| F1 Score | 0.55 | 0.62 |

### Business Impact
By tuning the decision threshold from 0.5 to 0.3:
- Catches 284 churners vs 183 with default threshold
- Potentially saves $18,392/month vs $11,851/month
- Extra value from tuning alone: $6,541/month

### High Risk Customer Profile
A customer matching ALL of these criteria is extremely likely to churn:
- Month-to-month contract
- Fiber optic internet service
- Electronic check payment method
- High monthly charges ($80+)
- Low tenure (under 12 months)
- Senior citizen

### Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Files
- `churn_analysis.ipynb` - Complete analysis notebook
- `Telco_customer_churn.xlsx` - Dataset

### How to Run
1. Clone this repository
2. Install requirements: `pip install pandas numpy matplotlib seaborn scikit-learn openpyxl`
3. Open `churn_analysis.ipynb` in Jupyter Notebook
4. Run all cells
