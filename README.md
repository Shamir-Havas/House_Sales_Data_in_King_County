# 🏡 House Sales Data in King County  

![Status](https://img.shields.io/badge/Looking%20for%20Opportunities-Data%20Science-blue)  

## 📌 Project Overview  
This project analyzes the **King County House Sales dataset** to explore relationships between house features and sale price.  
It demonstrates a complete **end-to-end data science workflow**, including:  

- Data cleaning & preprocessing with **Pandas/Numpy**  
- Exploratory Data Analysis (EDA) with **Matplotlib/Seaborn**  
- Correlation analysis to identify key drivers of price  
- Regression modeling with **Scikit-Learn** (Linear, Polynomial, Ridge)  
- Pipelines for feature scaling & transformation  
- Model evaluation using **R² score and cross-validation**  
- Communicating results with clear visuals  

The goal is to **predict housing prices** and showcase skills in **data analysis, machine learning, and model evaluation**.  

---

## 📊 Dataset  
- Source: [IBM Developer Skills Network – King County Housing Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DA0101EN-SkillsNetwork/labs/FinalModule_Coursera/data/kc_house_data_NaN.csv)  
- Records: ~21,600 house sales in King County, USA  
- Features: Bedrooms, bathrooms, living space, lot size, floors, waterfront, view, condition, grade, year built, renovated year, zipcode, latitude/longitude, and sale price  

### 🔎 Dataset Preview  
![Dataset Preview](images/dataset_head.png)  
*A sample of the King County dataset*  

---

## 🔬 Exploratory Data Analysis (EDA)  

### Distribution of House Prices  
![Price Distribution](images/price_distribution.png)  

### Correlation Heatmap  
![Correlation Heatmap](images/correlation_heatmap.png)  

### sqft_above vs Price  
![Sqft vs Price](images/sqft_vs_price.png)  

### Waterfront vs Price (Boxplot)  
![Waterfront Boxplot](images/waterfront_boxplot.png)  

---

## 🤖 Modeling Approach  

Models implemented in this notebook:  
1. **Simple Linear Regression** – predicting price from longitude (`long`)  
2. **Multiple Linear Regression** – using features: `sqft_living, sqft_above, sqft_living15, bathrooms, bedrooms`  
3. **Polynomial Regression (via Pipeline)** – scaling + polynomial features + linear regression  
4. **Ridge Regression** – applied with train/test split  
5. **Cross-Validation** – assessed stability of linear regression  

---

## 📈 Results  

| Model                          | R²   | Notes |
|--------------------------------|------|------------------------------|
| Simple Linear (longitude)      | ~0.0 | Very weak predictor |
| Multiple Linear Regression     | ~0.66 | Better predictive power |
| Polynomial Regression (Pipeline) | ~0.70+ | Captures nonlinear effects |
| Ridge Regression               | Similar to MLR | Helps control overfitting |
| Cross-Validation (Linear)      | ~0.64 avg | Confirms model stability |

---

## ✅ Key Learnings  
- Location (`long`, `lat`), `sqft_living`, and `grade` are strong drivers of price.  
- Polynomial features improved performance compared to plain linear regression.  
- Ridge regression helps balance model complexity and prevent overfitting.  
- Cross-validation confirmed that the models generalize reasonably well.  

---

## 🚀 Future Improvements  
- Experiment with **tree-based models** (Random Forest, Gradient Boosting)  
- Perform **hyperparameter tuning** for Ridge regression  
- Include **geospatial clustering** to capture neighborhood effects  
- Deploy as an interactive **prediction app** (Streamlit/Dash)  

---

## 🛠️ Tech Stack  
- **Language**: Python  
- **Libraries**: Pandas, Numpy, Scikit-Learn, Matplotlib, Seaborn  
- **Environment**: Jupyter Notebook  

---

## 📂 Project Structure  

├── House_Sales_Data_in_King_County.ipynb # Main analysis notebook
└── README.md # Project documentation
