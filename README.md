#  Customer Churn Prediction and Customer Segmentation

## About the Project

Customer churn is a major challenge for subscription-based businesses, where retaining existing customers is often more cost-effective than acquiring new ones. This project explores how machine learning can be used to identify customers who are likely to churn and how customer segmentation can provide additional business context for targeted retention strategies.

Rather than stopping at building a predictive model, I wanted to understand **why customers leave**, evaluate different modeling approaches, and translate the results into actionable customer segments. This project combines **Exploratory Data Analysis (EDA), Machine Learning, and K-Means Clustering** into a complete end-to-end workflow.

---

# 📂 Dataset Overview

| Attribute | Value |
|-----------|------:|
| Dataset | Telco Customer Churn |
| Total Customers | **7,043** |
| Features | **21** |
| Target Variable | Churn (Yes / No) |
| Problem Type | Binary Classification |
| Customer Segments | **3 (K-Means)** |

---

#  Project Workflow

```text
Customer Data
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Data Cleaning & Feature Engineering
      │
      ▼
Random Forest Baseline Model
      │
      ▼
Handling Class Imbalance
      │
      ▼
Hyperparameter Tuning
      │
      ▼
Model Evaluation
      │
      ▼
Customer Segmentation (K-Means)
      │
      ▼
Business Insights
```

---

# 📈 Project Journey

## 1. Understanding the Data

Before building any models, I explored the dataset to understand customer behaviour and identify the factors contributing to churn.

Some of the questions I investigated included:

- Which customers are more likely to churn?
- Does contract type affect churn?
- How does customer tenure influence loyalty?
- Are customers with higher monthly charges more likely to leave?
- Does technical support improve retention?

### Key Findings

| Question | Observation |
|----------|-------------|
| Which customers churn the most? | Customers on month-to-month contracts showed the highest churn rate. |
| Does tenure matter? | Customers with shorter tenure were significantly more likely to churn. |
| Monthly Charges | Higher monthly charges were associated with increased churn. |
| Technical Support | Customers without technical support churned more frequently. |
| Contract Type | Longer contracts resulted in much lower churn rates. |

### What I Learned

- Used visualization to uncover customer behaviour and business trends.
- Learned to approach the dataset from a business perspective before building models.
- Understood how EDA guides feature selection and model development.

---

## 2. Data Preparation

To prepare the dataset for machine learning, I performed several preprocessing steps:

- Handled missing values
- Converted categorical variables into numerical features
- Encoded categorical variables
- Prepared feature and target variables
- Split the dataset into training and testing sets

### What I Learned

This stage reinforced that model performance depends heavily on data quality. Careful preprocessing and feature engineering often have a greater impact than changing algorithms.

---

## 3. Building the Churn Prediction Model

I developed a **Random Forest Classifier** to predict whether a customer would churn.

Rather than evaluating the model using accuracy alone, I assessed its performance using multiple evaluation metrics.

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

---

# 📊 Model Performance

| Metric | Result |
|---------|-------:|
| Baseline Random Forest Accuracy | **78.57%** |
| Balanced Random Forest Accuracy | **79.21%** |
| ROC-AUC Score | **0.858** |

The balanced Random Forest model produced the best balance between identifying customers likely to churn while maintaining strong overall performance.

---

# 🔬 Hyperparameter Experiments

Instead of stopping after training a single model, I experimented with different values for **n_estimators** and **max_depth** to understand how they influenced model performance.

| Trees | Max Depth | Accuracy | Recall | Precision | F1 Score |
|------:|----------:|---------:|-------:|----------:|---------:|
|100|5|0.746|0.820|0.534|0.647|
|100|10|0.776|0.753|0.581|0.656|
|100|15|0.803|0.630|0.660|0.645|
|200|5|0.742|0.810|0.530|0.641|
|200|10|0.782|0.745|0.592|0.660|
|200|15|0.805|0.635|0.663|0.649|
|300|5|0.744|0.820|0.532|0.645|
|300|10|0.783|0.748|0.593|0.662|
|300|15|**0.806**|0.640|**0.665**|0.652|
|400|5|0.744|0.813|0.532|0.643|
|400|10|0.783|0.748|0.593|0.662|
|400|15|0.803|0.638|0.659|0.648|

### Key Takeaways

- Increasing tree depth improved **accuracy** and **precision**.
- Shallower trees achieved the highest **recall**, making them better at identifying customers likely to churn.
- Deeper trees produced a more balanced trade-off between precision and recall.
- Comparing multiple configurations helped me understand how model parameters influence performance rather than relying on a single experiment.

---

#  Feature Importance

Feature importance analysis helped identify the variables that contributed most to churn prediction.

The most influential features included:

- Contract Type
- Customer Tenure
- Monthly Charges
- Total Charges
- Technical Support

This analysis made the model more interpretable by linking predictions back to real business drivers.

---

## 4. Customer Segmentation

To complement churn prediction, I used **K-Means Clustering** to group customers based on their characteristics and predicted churn probability.

### Features Used

- Tenure
- Monthly Charges
- Total Charges
- Predicted Churn Probability

### Customer Segments

| Segment | Description | Business Action |
|----------|-------------|-----------------|
| Loyal Customers | Long-tenure customers with low churn probability | Reward loyalty and promote premium services |
| High-Risk Customers | New customers with higher churn probability | Target early retention campaigns |
| Premium Customers | High-value customers with higher monthly spending | Focus on personalized engagement and retention |

### What I Learned

Customer segmentation transformed predictive outputs into actionable business insights by identifying different customer profiles that require different retention strategies.

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# 💡 Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- Feature Engineering
- Random Forest Classification
- Model Evaluation
- Hyperparameter Tuning
- Handling Class Imbalance
- Feature Importance Analysis
- ROC-AUC Evaluation
- K-Means Clustering
- Business Analytics

---

#  What This Project Taught Me

This project strengthened my understanding of the complete machine learning workflow—from exploring raw customer data to communicating business insights.

Some of my key takeaways were:

- Understanding customer behaviour before modeling leads to better analytical decisions.
- Data preprocessing is just as important as model selection.
- Evaluating multiple metrics provides a more complete picture of model performance than accuracy alone.
- Experimenting with different model configurations helps reveal important trade-offs.
- Customer segmentation complements prediction by making results easier to interpret from a business perspective.
- Machine learning creates the most value when its outputs support real business decisions.

---

#  Future Improvements

Future enhancements for this project include:

- Compare Random Forest with XGBoost, LightGBM, and CatBoost.
- Use SHAP values for model explainability.
- Deploy the model using Streamlit.
- Build an interactive dashboard using Power BI or Tableau.
- Automate hyperparameter optimization using GridSearchCV or Optuna.

---

# 📁 Repository Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Segmentation.ipynb
├── Telco_customer_churn.xlsx
└── README.md
```

---

#  Final Thoughts

This project represents one of my first complete machine learning workflows—from understanding raw customer data to building predictive models and generating meaningful customer segments. Beyond improving model performance, it taught me the importance of experimentation, evaluation, and translating technical findings into business-focused recommendations.

Overall, this project strengthened my skills in data analysis, machine learning, and problem-solving while giving me practical experience in applying predictive analytics to a real-world business problem.
