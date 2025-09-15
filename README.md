# 🏡 House Sales Data in King County  

## 📌 Project Overview  
This project analyzes the **King County House Sales dataset** to explore relationships between house features and sale price.  
It demonstrates a complete **end-to-end data science workflow**, including:  

- Data cleaning & preprocessing with **Pandas/Numpy**  
- Exploratory Data Analysis (EDA) with **Matplotlib/Seaborn**  
- Feature engineering & transformation (Polynomial features, derived variables)  
- Regression modeling with **Scikit-Learn** (Linear, Polynomial, Ridge)  
- Model evaluation using **R², RMSE, MAE**  
- Communicating results with clear visuals  

The goal is to **predict housing prices** and showcase strong skills in **data analysis, machine learning, and model evaluation**.  

---

## 📊 Dataset  
- Source: [King County House Sales Dataset (Kaggle)](https://www.kaggle.com/harlfoxem/housesalesprediction)  
- Records: ~21,000 house sales in King County, USA  
- Features: Bedrooms, bathrooms, living space, lot size, floors, waterfront, view, condition, grade, year built, renovated year, zipcode, latitude/longitude, and sale price  

### 🔎 Dataset Preview  
![Dataset Preview](images/dataset_head.png)  
*A sample of the King County dataset*  

---

## 🔬 Exploratory Data Analysis (EDA)  

### Distribution of House Prices  
![Price Distribution](images/price_dist.png)  

### Correlation Heatmap  
![Correlation Heatmap](images/corr_heatmap.png)  

### sqft_living vs Price  
![Sqft vs Price](images/sqft_vs_price.png)  

---

## ⚙️ Feature Engineering  
- Created derived features such as **house age** and **renovation flag**  
- Applied **Polynomial Features** to capture nonlinear relationships  

![Feature Engineering](images/feature_engineering.png)  

---

## 🤖 Modeling Approach  

Models implemented:  
1. **Simple Linear Regression** (using sqft_living only)  
2. **Multiple Linear Regression** (using all features)  
3. **Polynomial Regression (degree=2)**  
4. **Ridge Regression** (regularized linear model)  
5. **Ridge + Polynomial Regression**  

---

## 📈 Results  

| Model                          | R²   | Notes |
|--------------------------------|------|------------------------------|
| Simple Linear (sqft_living)    | 0.49 | Baseline |
| Multiple Linear Regression     | 0.66 | Improved with more features |
| Polynomial Regression (deg=2)  | 0.75 | Captures nonlinear patterns |
| Ridge Regression               | 0.65 | Regularization reduces overfit |
| Ridge + Polynomial Regression  | 0.70 | Balanced complexity & regularization |

### Model Performance Comparison  
![Model Performance](images/model_performance.png)  

### Predicted vs Actual (Best Model)  
![Predicted vs Actual](images/pred_vs_actual.png)  

---

## ✅ Key Learnings  
- Increasing model complexity (polynomial features) significantly improved performance.  
- Regularization (Ridge) helped reduce overfitting but slightly reduced R² compared to plain polynomial regression.  
- Visualization and EDA revealed strong correlations between **sqft_living, grade, and location** with house prices.  

---

## 🚀 Future Improvements  
- Experiment with **tree-based models** (Random Forest, XGBoost, LightGBM)  
- Perform **hyperparameter tuning** (GridSearchCV/RandomizedSearchCV)  
- Add **geospatial features** (distance to city center, neighborhood clusters)  
- Build an interactive **prediction app** with Streamlit or Dash  
- Apply **SHAP values** for model interpretability  

---

## 🛠️ Tech Stack  
- **Language**: Python  
- **Libraries**: Pandas, Numpy, Scikit-Learn, Matplotlib, Seaborn  
- **Environment**: Jupyter Notebook  

---

## 📂 Project Structure  

├── House_Sales_Data_in_King_County.ipynb # Main analysis notebook
├── data/ # Dataset (not included here, link to Kaggle)
├── images/ # Screenshots & visuals
└── README.md # Project documentation

yaml
Copy code

---

## 🙋 About Me  
I am a **Data Science fresher** with strong foundations in Python, machine learning, and data visualization.  
This project demonstrates my ability to:  
- Clean and analyze real-world datasets  
- Build and evaluate predictive models  
- Communicate insights clearly with visuals and structured reporting  

---

✨ *This repository is part of my data science portfolio to showcase my skills for recruitment opportu
