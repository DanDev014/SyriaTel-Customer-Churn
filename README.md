# 📶**SyriaTel Customer Churn Prediction**
## **Project Overview**

Customer churn poses a significant revenue risk for telecommunications companies. This project builds a binary classification model to predict whether a SyriaTel customer is likely to churn (stop doing business with the company), enabling proactive and targeted retention strategies.

The analysis focuses on identifying predictable behavioral patterns in customer usage and service interactions that signal churn risk.

# **Business Problem**

SyriaTel loses revenue when customers discontinue their service. Acquiring new customers is more expensive than retaining existing ones, making churn prevention a critical business priority.

**Objective:**
Predict which customers are likely to churn so SyriaTel can intervene before revenue is lost.

## **Stakeholders**

*SyriaTel Management & Marketing Teams* – Use predictions to design targeted retention campaigns

*Customer Support Teams* – Prioritize outreach to high-risk customers

*Data & Analytics Teams* – Build, evaluate, and maintain predictive models

## **Dataset**

- Source: SyriaTel customer usage data

- Observations: 3,333 customers

- Features: 20 predictors + 1 target variable

- Target: churn (binary: churned vs not churned)

- Missing Values: None

The dataset includes:

- Customer tenure and service plans

- Day, evening, night, and international usage

- Customer service call history

# **Modeling Approach**
## **Data Preparation**

- Dropped non-actionable or high-cardinality features (phone number, state, area code)

- Encoded binary categorical variables (international plan, voice mail plan)

- Scaled numerical features where required

- Used stratified train-test split to preserve churn distribution

## **Models Evaluated**

1. **Baseline Model (Dummy Classifier)**

- Represents a “do nothing” strategy

- Recall for churn = 0.0

2. **Logistic Regression**

Logistic Regression Confusion Matrix

- Evaluated at default and lowered decision thresholds

- Improved churn recall but missed many churners

3. **Decision Tree (Final Model)**

Decision Tree Confusion Matrix

- Constrained to prevent overfitting

- Best balance between recall and precision

- Chosen for final evaluation

# **Evaluation Metrics**

**Primary Metric:** Recall (Churn)

- False negatives are more costly than false positives because losing a customer results in direct revenue loss.

**Final Model Performance (Decision Tree):**

- Recall (Churn): 64%

- Precision (Churn): 76%

- Accuracy: 92%

This means the model correctly identifies the majority of customers who churn while limiting unnecessary retention efforts.

**Key Findings**

- Customer churn is predictable, not random.

- Usage patterns and customer service interactions strongly indicate churn risk.

- A decision tree model provides strong performance while remaining interpretable for business use.

**Business Impact**

The model enables SyriaTel to:

- Identify high-risk customers before they churn

- Focus retention resources where they matter most

- Reduce churn-related revenue loss

- Avoid blanket retention campaigns and unnecessary incentives

# **Recommendations**

- Use the decision tree model as a decision-support tool to flag high-risk customers.

- Prioritize retention efforts around customer service experience and pricing concerns.

- Periodically retrain the model as customer behavior evolves.

# **Conclusion**

This project demonstrates that SyriaTel can reliably predict customer churn using historical usage and service data. By deploying an interpretable decision tree model, the company can proactively retain customers, reduce revenue loss, and allocate retention resources more efficiently.

# **Repository Structure**
```
├── data/
│   └── Telecom.csv

├── index.ipynb
├── Presentation.pdf
├── README.md
```