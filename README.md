# Task 9 – Loan Default Risk with Business Cost Optimization

## Objective
The goal of this task is to predict loan default risk using the Home Credit Default Risk dataset. Unlike standard classification tasks, the focus here is not only on accuracy but also on **business cost optimization** — minimizing financial losses due to false approvals (risky clients approved) and false rejections (safe clients denied).

---

## Dataset
- **Source:** Home Credit Default Risk (Kaggle)

## Approach
1. **Data Understanding & Cleaning**
   - Handled missing values (median for numeric, mode for categorical).
   - Encoded categorical variables using Label Encoding.
   - Verified class distribution of `TARGET`.

2. **Exploratory Data Analysis (EDA)**
   - Checked distributions of key features (age, income, credit amount).
   - Correlation analysis between income, credit, and default rate.

3. **Model Training**
   - Logistic Regression (baseline model).
   - Random Forest Classifier (improved performance).
   - Evaluated models using Accuracy, ROC-AUC.

4. **Business Cost Optimization**
   - Assigned costs:  
     - False Positive (approving a bad loan) = \$5000  
     - False Negative (rejecting a good client) = \$1000  
   - Tested different decision thresholds (0.1–0.9).  
   - Selected the threshold minimizing total financial loss.

---

## Results & Insights
- Random Forest outperformed Logistic Regression in ROC-AUC.  
- Default threshold (0.5) was not optimal for minimizing costs.  
- Cost-sensitive threshold tuning reduced overall financial risk.  
- Demonstrates that **business-aware modeling** can be more valuable than raw accuracy in financial applications.

---

## ✅ Conclusion
This task highlights the importance of incorporating **business impact** into machine learning. By adjusting decision thresholds with cost optimization, financial institutions can reduce potential losses and make smarter credit approval decisions.
