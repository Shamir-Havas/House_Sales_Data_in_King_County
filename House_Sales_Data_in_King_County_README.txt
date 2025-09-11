House Sales Data in King County – Regression Analysis

[Colab Badge: Open in Colab]
(Link will be updated after uploading to GitHub)

------------------------------------------------------------
Project Overview
------------------------------------------------------------
This project analyzes the King County House Sales dataset, which contains 
information on house prices and features such as square footage, 
number of bedrooms/bathrooms, floors, and location.

The goal is to explore the data and build predictive models using:
- Linear Regression (simple & multiple)
- Polynomial Regression (via pipeline)
- Ridge Regression (with and without polynomial features)

------------------------------------------------------------
Dataset
------------------------------------------------------------
- File: kc_house_data.csv
- Rows: 21,613
- Columns: 21
- The dataset includes house features (sqft_living, bedrooms, bathrooms, floors, lat, long)
  and the target variable price.

------------------------------------------------------------
Tools & Libraries
------------------------------------------------------------
- Python 3
- pandas – Data manipulation
- matplotlib & seaborn – Visualization
- scikit-learn – Machine Learning models

------------------------------------------------------------
Analysis Steps
------------------------------------------------------------
1. Data exploration – data types, descriptive statistics
2. Value counts & visualizations – floors, waterfront vs. price, sqft_above vs. price
3. Simple Linear Regression – predict price from sqft_living
4. Multiple Linear Regression – using several features
5. Pipeline with scaling & polynomial features
6. Ridge Regression – regularization to prevent overfitting
7. Polynomial Ridge Regression – Ridge with polynomial transform

------------------------------------------------------------
Results (R² Scores)
------------------------------------------------------------
- Simple Linear Regression (sqft_living): 0.49
- Multiple Linear Regression: 0.66
- Pipeline with polynomial transform: 0.75
- Ridge Regression (α=0.1): 0.65
- Ridge Regression with polynomial transform: 0.70

------------------------------------------------------------
How to Run
------------------------------------------------------------
1. Clone the repository:
   git clone https://github.com/YourUsername/YourRepoName.git
   cd YourRepoName

2. Open the notebook in Google Colab (or Jupyter Notebook).

3. Run the cells step by step.

------------------------------------------------------------
Conclusion
------------------------------------------------------------
This project demonstrates:
- How house price predictions improve with multiple features.
- The impact of polynomial features on model performance.
- The usefulness of Ridge Regression for regularization.

Polynomial + Ridge Regression achieved the best performance 
with an R² score of ~0.70 on test data.
