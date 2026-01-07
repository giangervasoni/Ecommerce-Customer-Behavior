E-Commerce Customer Churn Defense & Strategic Segmentation

Project Overview

This project addresses a critical business challenge: Customer Attrition. Using a dataset of 50,000 customers, I developed a machine learning pipeline that not only predicts which customers are likely to leave but also identifies why they are leaving and categorizes them into strategic segments for personalized retention campaigns.

Key Business Insights

The Support-Churn Loop: High frequency of Customer_Service_Calls was identified as the strongest predictor of churn, indicating service friction.

Revenue Protection: The analysis reveals that we are disproportionately losing high-value customers (High Lifetime_Value).

Engagement Shield: Increased platform activity (measured by a custom Engagement_Index) is the best defense against customer loss.

Technical Workflow

1. Data Profiling & Cleaning
Missingness Analysis: Identified systematic gaps in engagement metrics using matrix visualizations.

Outlier Management: Rigorously handled non-physical age values (e.g., 200 years) and negative purchase data to ensure model integrity.

Target Balance: Addressed a 28.9% churn baseline to ensure the model learned to identify the minority class effectively.

2. Feature Engineering & Exploratory Data Analysis (EDA)
Custom Metrics: Developed an Engagement_Index combining login frequency and session duration.

Correlation Mapping: Utilized heatmaps to uncover the strong 0.29 correlation between support calls and churn.

3. Predictive Modeling (Random Forest)
Optimization: Tuned the model specifically for Recall (83%) to minimize "False Negatives"—ensuring we catch as many churners as possible before they leave.

Performance: Achieved high diagnostic power, correctly identifying over 2,100 churned users in the test set.

4. Explainable AI (SHAP)
Global Interpretability: Used SHAP summary plots to visualize how features like Lifetime_Value and Cart_Abandonment_Rate influence the model globally.

Local Interpretability: Implemented waterfall plots to explain individual predictions, providing "reason codes" for why specific customers are at risk.

5. Customer Segmentation (K-Means)
To move from prediction to action, customers were clustered into three strategic personas:

Champions: High value, low risk. Strategy: Reward loyalty and maintain engagement.

At-Risk VIPs: High value, high risk. Strategy: Immediate support intervention and concierge outreach.

Low-Value Browsers: Low value, high risk. Strategy: Automated re-engagement or low-resource monitoring.

Strategic Recommendations

* Red Flag Support: Flag any customer with >3 support calls for immediate escalation to senior retention specialists.

* Checkout UI/UX: Reduce Cart_Abandonment_Rate (a top-3 churn driver) through streamlined payment flows and recovery emails.

* LTV Preservation: Launch a VIP-only loyalty program specifically for the "At-Risk VIP" segment to counteract their high churn probability.