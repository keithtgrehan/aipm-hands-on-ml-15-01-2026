# ML + Product Exercise: Churn Prediction as a PM

## Business Context (Read First)

You are a Project Manager at XYZ a subscription-based app.

**Goal**

Predict whether a user will churn in the next 30 days so the marketing team can take action.

**Business Constraints**

* Missing a churned user (False Negative) is very costly
* Contacting a non-churn user (False Positive) is cheap
* Model must be explainable to stakeholders

---

## Dataset Description (Business Context)
**Company Overview**

XYZ, a subscription-based SaaS platform that helps teams collaborate on projects.
XYZ sells individual and premium subscriptions, and earns revenue from recurring monthly payments.

The company wants to predict churn — that is, which users are likely to cancel their subscription in the next 30 days — so that the growth and marketing teams can proactively engage at-risk customers with retention offers.

To do this, they have collected behavioral and support data from current and past users. Your team will build and evaluate simple ML models (e.g., logistic regression, KNN, decision trees) to forecast churn, while making product trade-offs.

#### Feature Explanations

Below is a breakdown of each feature in the dataset — expressed in business terms:

1. `tenure_months`
**Description:**  
Number of months the user has been active on the platform.

**Product context:**  
Tenure reflects how long a user has been exposed to the product and how embedded it may be in their workflow.


2. `sessions_per_week`
**Description:**  
Average number of times the user accesses the product in a typical week.

**Product context:**  
Session frequency is a proxy for engagement and how regularly the product is part of the user’s routine.


3. `feature_usage`
**Description:**  
Count of distinct product features the user has interacted with.

**Product context:**  
This indicates the breadth of the product the user has explored, not how well they used any single feature.


4. `support_tickets`
**Description:**  
Total number of customer support tickets raised by the user.

**Product context:**  
Support interactions capture moments where users needed help, clarification, or resolution.


5. `is_premium`
**Description:**  
Indicates whether the user is on a paid subscription plan.

- `1` → Premium (paid user)  
- `0` → Free or basic user  

**Product context:**  
Subscription tier reflects the level of commitment and investment a user has made in the product.

---

##### Target Variable - `churn`

**Description:**  
Whether the user canceled or stopped using the product within the defined time window.

- `1` → User churned  
- `0` → User retained

---

## From the company's perspective

#### Why This Dataset Matters

In projects like XYZ:

* Predicting churn allows proactive retention

* Saves marketing spend by targeting only high-risk users

* Improves customer experience by personalizing engagement

* Helps PMs understand behavioral drivers of churn

---

##### Important Note

- Feature descriptions provide **business context only**  
- They do **not** imply how strongly a feature affects churn  
- Your models and evaluation metrics should reveal those relationships
- This is intentionally a small dataset — our goal is to practice PM decisions, metric trade-offs, and risk assessment, not to build a production-grade model.

##### Business context:
* We want the model to forecast this so we can take action before churn happens.


---

## Post-Exercise Reflection Questions 

### Model Choice & Business Fit
1. Which model would you recommend deploying for XYZ and **why**?
2. Which business constraint mattered most in your decision:  
   recall, explainability, or consistency of predictions?
3. Would your recommendation change if XYZ were an early-stage startup vs a mature company? Why?

### Metrics & Trade-offs
4. Which evaluation metric did you prioritize and why?
5. What are the **real business consequences** of:
   - a false negative in this problem?
   - a false positive?
6. If leadership demanded higher accuracy but lower recall, how would you respond?

### Bias–Variance as Product Risk
7. Did any model show signs of overfitting or underfitting?  
   What **product risks** does that introduce?
8. Would you prefer a slightly underfit or overfit model for this use case? Why?

### Decision Trees & Explainability
9. How does tree depth or number of leaf nodes affect:
   - user experience?
   - stakeholder trust?
10. What is the maximum model complexity you would feel comfortable explaining to a non-technical stakeholder?

### Feature Interpretation & Product Insight
11. Which features appeared most useful in predicting churn?
12. Did any feature surprise you in its impact?  
    What product hypothesis might explain that?
13. How could product or UX changes reduce churn for high-risk users identified by the model?

### Feature Engineering (Optional Section)
14. Did scaling or normalization change model performance?
15. From a PM perspective, when would changing feature treatment be acceptable vs risky?

### Threshold & Policy Decisions
16. How would you choose a decision threshold for contacting users?
17. Would you use different thresholds for premium vs free users? Why or why not?

### Shipping & Ethics
18. Would you ship this model today? If not, what is missing?
19. What safeguards would you put in place before using this model in production?
20. Who should be accountable if the model makes a bad decision?

---

### Final Synthesis Question
**In one paragraph:**  
Explain how you would present this model and its trade-offs to the Head of Marketing.
