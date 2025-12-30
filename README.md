# **SyriaTel Customer Churn Prediction**
### **Overview**

SyriaTel has been losing immense revenue as a result of customer churn. It is in the best interest of any business to retain its existing customers. For this reason, the telecom is incurring marketing costs in a bid to reach new customer base. It is a zero sum game as a significant number of the acquired customers end up churning as well. The task at hand is to determine customers likely to churn by looking out for patterns and come up with measures that would prevent that from happening.

### **Objective**
Predict customers most likely to churn

### Stakeholders

1. **Executive Management (CEO, COO, Strategy Team):** This stakeholder group will use this project to quantify expected revenue loss. They will then be able to track churn trends over time by customer segment. That way they can make strategic decisions on whether to invest more in retention programs or acquisition.
2. **Marketing Team:** The marketing team will use this project to target high-risk customers with personalized retention offers. This will reduce spending on mass acquisition campaigns. Additionally, the marketing team can run data-driven retention campaigns instead of blanket promotions.
3. **Customer Service Team:** The project will enable this stakeholder group to flag high-risk customers in the CRM system.This make it possible to prioritize support for customers likely to churn. They will also provide proactive outreach before customers cancel.
4. **Data & Analytics Team:** This group will be interested in monitoring model accuracy, recall, and drift.They might also retrain the model with new data and identify new churn drivers as customer behavior changes.

### Dataset Overview

- The dataset contains **3,333 customer records** and **21 features (20 predictors + 1 target)**.
- Each record represents a **unique SyriaTel customer account**.
- The features include a mix of **numerical variables** (such as call minutes, call counts, charges, account length, and customer service calls) and **categorical variables** (including state, area code, international plan, and voicemail plan).
- The target variable is **churn**, a binary indicator showing whether a customer discontinued the service.
- Descriptive statistics were generated for all features to understand data distributions, detect potential outliers, and inform preprocessing decisions.

### Data preprocessing
1. There were no missing values.
2. phone number, state, area code columns were dropped
3. international plan, voice mail plan columns were encoded
4. The last step was feature scaling

### Modeling
A baseline model was created followed by a logistic regression and decision tree. Because it identifies more customers who are likely to churn, misses fewer at-risk customers, and is easy to explain, the decision tree was chosen as the final model for assessing churn risk at SyriaTel.

## **Recommendations**

* Focus on **retaining high-risk customers** instead of broad customer acquisition.
* Prioritize **frequent customer service callers** for faster resolution and proactive outreach.
* Review **international plan pricing and billing clarity** to reduce cost-driven churn.
* Introduce **early engagement programs** for new customers with short account tenure.
* Integrate churn predictions into **marketing and customer service workflows**.

## **Conclusion**

* SyriaTel’s churn problem can be effectively addressed using **predictive analytics**.
* The decision tree model accurately identifies customers at risk of churn.
* Targeted retention strategies are **more cost-effective** than continuous customer replacement.
* Ongoing model monitoring will ensure sustained impact over time.
