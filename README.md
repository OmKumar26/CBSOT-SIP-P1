# Customer Churn Prediction and Customer Segmentation

## About the Project

This project started as an exercise to understand how machine learning can be used to solve a real business problem—customer churn. Along the way, I realized that predicting churn alone isn't enough. Businesses also need to understand *which* customers are leaving and *how* different customer groups behave.

To explore this, I built a churn prediction model using Random Forest and then segmented customers using K-Means clustering to identify groups with similar characteristics.

This project helped me connect data analysis, machine learning, and business thinking into one workflow.

---

## Project Journey

### 1. Understanding the Data

I began by exploring the dataset to answer questions like:

- Which customers are more likely to leave?
- Does contract type affect churn?
- How does tenure relate to customer loyalty?
- Are customers with higher monthly charges more likely to churn?

Using visualizations helped me identify patterns before building any models.

**What I learned**

- How to perform meaningful exploratory data analysis
- How visualization can reveal trends that summary statistics often miss
- How to think about data from a business perspective instead of only a technical one

---

### 2. Preparing the Data

Before training a model, I cleaned and transformed the dataset by:

- Handling missing values
- Converting categorical variables into numerical features
- Preparing feature and target variables
- Splitting the data into training and testing sets

This stage showed me that preprocessing has a major impact on model performance.

---

### 3. Building the Churn Prediction Model

I trained a Random Forest classifier to predict whether a customer would churn.

Instead of stopping at accuracy, I also looked at:

- Confusion Matrix
- Precision
- Recall
- F1 Score
- ROC-AUC

I experimented with class balancing and parameter tuning to improve the model's performance.

**Big takeaway**

A model isn't useful just because it has high accuracy. Understanding *why* it performs well (or poorly) is just as important.

---

### 4. Customer Segmentation

After generating churn predictions, I grouped customers using K-Means clustering.

The segmentation revealed different customer profiles, including:

- Long-term loyal customers
- New customers with high churn risk
- Customers paying higher monthly charges

This was the part I enjoyed most because it transformed predictions into something a business could actually use.

---

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## What This Project Taught Me

This project gave me hands-on experience with much more than training a machine learning model.

I learned how to:

- Explore and understand unfamiliar datasets
- Clean and preprocess real-world data
- Build and evaluate classification models
- Handle imbalanced data
- Interpret feature importance
- Apply clustering for customer segmentation
- Connect technical results with business decisions

More importantly, I learned that data science is not just about building models—it's about solving problems and communicating insights.

---

## Future Improvements

If I continue working on this project, I'd like to:

- Compare Random Forest with XGBoost and LightGBM
- Use SHAP values to explain predictions
- Deploy the model with Streamlit
- Build an interactive dashboard for business users
- Test different clustering techniques

---

## Final Thoughts

This project represents one of my first complete machine learning workflows—from exploring raw data to building predictive models and generating business insights. Looking back, it helped me develop a much better understanding of both the technical and practical aspects of applied machine learning.
