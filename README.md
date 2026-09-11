# 🏡 KING COUNTY HOUSE PRICE ANALYTICS

### **Exploratory Data Analysis & Regression Modeling for Residential Property Valuation**

> **A practical end-to-end data science project that studies the drivers of house prices and compares multiple regression strategies for price prediction.**

---

## ⭐ PROJECT SNAPSHOT

| Dimension | Project Focus |
|---|---|
| 🎯 **Business Problem** | Understand and predict residential sale prices |
| 📊 **Dataset** | ~21,600 King County house sales |
| 🔍 **Analysis** | EDA, distributions, correlations & relationships |
| 🧠 **Modeling** | Linear, Polynomial & Ridge Regression |
| ⚙️ **Feature Engineering** | Scaling + second-order polynomial features |
| 📈 **Evaluation** | R² score + cross-validation |
| 🏆 **Best Reported Performance** | **Polynomial Regression: ~0.70+ R²** |

---

# 📌 WHY THIS PROJECT MATTERS

House prices are influenced by a combination of **property characteristics, location, quality, and size**.

This project investigates those relationships and turns them into a regression modeling workflow:

```text
Raw Housing Data
       ↓
Data Quality & Structure Review
       ↓
Exploratory Data Analysis
       ↓
Correlation & Feature Relationships
       ↓
Feature Selection
       ↓
Regression Modeling
       ↓
Model Comparison
       ↓
Business Interpretation
```

The focus is not only on fitting a model, but on understanding **which housing characteristics are associated with price and how model complexity affects predictive performance**.

---

# 📊 DATASET

The project uses the **King County House Sales dataset** containing approximately **21,600 residential sales records**.

The notebook works with variables covering:

- `price` — target variable
- `bedrooms`
- `bathrooms`
- `sqft_living`
- `sqft_lot`
- `floors`
- `waterfront`
- `view`
- `condition`
- `grade`
- `sqft_above`
- `sqft_basement`
- `yr_built`
- `yr_renovated`
- `zipcode`
- `lat`
- `long`
- `sqft_living15`
- `sqft_lot15`

The preprocessing step removes identifier columns such as `id` and `Unnamed: 0` before analysis.

---

# 🔎 EXPLORATORY DATA ANALYSIS

The analysis begins by inspecting data types and descriptive statistics before investigating relationships between property attributes and sale price.

### Key questions explored

- How does property size relate to sale price?
- Does waterfront status correspond to different price distributions?
- Which variables show the strongest relationship with price?
- Are there substantial outliers in housing features?
- How do property quality indicators such as `grade` relate to price?

---

## 🔥 CORRELATION STRUCTURE

![Correlation Heatmap](./Correlation%20Heatmap.png)

The correlation analysis highlights several important relationships, including the strong association between **`sqft_living` and `price`**, as well as strong relationships among several size and quality-related variables.

A notable observation is the relationship between:

- `sqft_living` and `price`
- `grade` and `price`
- `sqft_above` and `price`
- `sqft_living` and `grade`

This provides a data-driven basis for selecting meaningful predictors.

---

## 📐 PROPERTY SIZE VS PRICE

![Sqft vs Price](./sqft_above%20vs%20Price.png)

The regression visualization shows a **positive relationship between above-ground living area and sale price**.

Larger living areas generally correspond to higher prices, although the spread of prices also increases substantially for larger properties.

This is an important modeling insight: **house price is not determined by size alone**, motivating the use of multiple predictors.

---

## 🌊 WATERFRONT PREMIUM

![Waterfront Price Distribution](./Waterfront%20vs%20Price%20%28Boxplot%29.png)

The waterfront comparison shows a distinctly different price distribution for properties with waterfront access.

The dataset contains far fewer waterfront properties than non-waterfront properties, making this feature potentially valuable while also requiring careful interpretation.

---

# 🧠 MODELING STRATEGY

Rather than relying on one regression algorithm, the project compares progressively more flexible approaches.

### 1. SIMPLE LINEAR REGRESSION

A single-feature model is used to establish a baseline and demonstrate how limited information can restrict predictive performance.

### 2. MULTIPLE LINEAR REGRESSION

Multiple housing characteristics are combined to provide a stronger representation of property value.

The notebook uses features including:

```text
sqft_living
sqft_above
sqft_living15
bathrooms
bedrooms
```

### 3. POLYNOMIAL REGRESSION

A pipeline combines:

```text
StandardScaler
      ↓
PolynomialFeatures(degree=2)
      ↓
LinearRegression
```

The second-order transformation allows the model to represent **nonlinear relationships and feature interactions** that ordinary linear regression cannot capture.

### 4. RIDGE REGRESSION

Ridge regression introduces L2 regularization to control model complexity.

The notebook evaluates:

```text
alpha = 0.1
```

and also investigates Ridge regression after polynomial transformation.

---

# 📈 MODEL COMPARISON

| Model | Reported R² | Interpretation |
|---|---:|---|
| Simple Linear Regression | ~0.0 | Weak single-feature baseline |
| Multiple Linear Regression | ~0.66 | Stronger multivariable relationship |
| Polynomial Regression | **~0.70+** | Captures nonlinear effects |
| Ridge Regression | ~0.66 | Regularized linear alternative |
| Linear Cross-Validation | ~0.64 avg | Provides a stability check |

The reported results show a clear progression:

```text
Single Feature
     ↓
Multiple Features
     ↓
Polynomial Features
     ↓
Regularization
```

The polynomial approach achieved the strongest reported R² among the approaches summarized for this project.

---

# 🧪 MODEL EVALUATION

The project uses **R²** as the primary regression evaluation measure.

Conceptually:

> **R² measures the proportion of variance in the target that is explained by the model.**

The notebook also uses a train/test split for Ridge regression and performs cross-validation to assess the stability of linear regression.

### Why compare models?

A recruiter should be able to see that the project is not simply:

> `fit()` → `score()` → done.

Instead, the workflow evaluates how:

- feature count affects performance,
- nonlinear transformations affect performance,
- regularization affects model complexity,
- and validation affects confidence in the result.

---

# 💡 DATA-DRIVEN INSIGHTS

### 🏠 SIZE MATTERS

`sqft_living` shows a strong relationship with sale price, supporting the importance of living area in property valuation.

### ⭐ QUALITY MATTERS

`grade` is another important price-related variable, indicating that property quality contributes substantially to valuation.

### 📍 LOCATION MATTERS

Latitude, longitude, and zipcode provide geographic information that can help explain differences in property prices.

### 🌊 WATERFRONT PROPERTIES DIFFER

Waterfront homes occupy a small portion of the dataset but show a substantially different price distribution.

### 🔗 FEATURES ARE NOT INDEPENDENT

Several size and quality variables are strongly correlated with each other. This is relevant when using linear models and motivates consideration of regularization.

---

# 🧩 TECHNICAL WORKFLOW

```text
1. Load housing data
        ↓
2. Inspect data types
        ↓
3. Remove identifier columns
        ↓
4. Generate descriptive statistics
        ↓
5. Analyze feature distributions
        ↓
6. Study feature-price relationships
        ↓
7. Build correlation matrix
        ↓
8. Train regression baselines
        ↓
9. Add polynomial transformations
        ↓
10. Apply Ridge regularization
        ↓
11. Compare R² performance
        ↓
12. Interpret the results
```

---

# 🛠️ TECHNOLOGY STACK

### LANGUAGE
- **Python**

### DATA ANALYSIS
- **Pandas**
- **NumPy**

### MACHINE LEARNING
- **Scikit-learn**
  - LinearRegression
  - Ridge
  - StandardScaler
  - PolynomialFeatures
  - Pipeline
  - train_test_split

### VISUALIZATION
- **Matplotlib**
- **Seaborn**

### ENVIRONMENT
- **Jupyter Notebook / Google Colab workflow**

---

# 📁 PROJECT STRUCTURE

```text
House_Sales_Data_in_King_County/
│
├── House_Sales_Data_in_King_County.ipynb
├── README.md
│
├── Distribution of House Prices.png
├── Correlation Heatmap.png
├── sqft_above vs Price.png
└── Waterfront vs Price (Boxplot).png
```

> The image filenames above follow the project documentation supplied with the notebook. If your GitHub repository uses different filenames, the README image paths should be updated to match them exactly.

---

# 🚀 LIMITATIONS & NEXT STEPS

The current project provides a solid regression foundation, but there are several natural ways to make the analysis more production-oriented.

### Modeling Improvements

- Compare against **Random Forest / Gradient Boosting** models.
- Perform systematic hyperparameter tuning.
- Compare additional regression metrics such as **MAE and RMSE**.
- Investigate log transformation of the price target.
- Use stronger cross-validation strategies for model selection.

### Feature Improvements

- Engineer **house age at sale**.
- Create **renovation-age** features.
- Explore neighborhood-level effects.
- Use geospatial features more explicitly.
- Investigate interactions between size, quality, and location.

### Deployment

A future version could expose the trained model through:

```text
User Inputs
    ↓
Prediction API
    ↓
House Price Estimate
    ↓
Interactive Dashboard
```

---

# 🏆 WHY THIS PROJECT STANDS OUT

This project demonstrates a complete progression from **raw housing data to model comparison and interpretation**.

The strongest portfolio signals are:

| Skill | Evidence |
|---|---|
| 📊 Data Analysis | Statistical summaries & EDA |
| 🔍 Feature Analysis | Correlation and relationship analysis |
| 🧠 Regression | Multiple regression approaches |
| ⚙️ Feature Engineering | Scaling + polynomial expansion |
| 🛡️ Regularization | Ridge regression |
| 📈 Model Evaluation | R² + validation |
| 💼 Business Thinking | Interpreting housing price drivers |
| 📚 Communication | Visual explanations and model comparison |

---

# 🎯 PORTFOLIO TAKEAWAY

> **This project demonstrates the ability to move from exploratory analysis to structured regression modeling, compare alternative approaches, interpret feature relationships, and communicate the factors associated with residential property prices.**

It is particularly useful as a portfolio project because it shows both sides of data science:

**UNDERSTANDING THE DATA**  
→ EDA, correlations, distributions, relationships

**BUILDING THE MODEL**  
→ Linear Regression, Polynomial Regression, Ridge

**EVALUATING THE MODEL**  
→ R², train/test evaluation, cross-validation

**EXPLAINING THE RESULT**  
→ Housing size, quality, location, and waterfront effects

---

## 👨‍💻 AUTHOR

**Shamir Havas**

**Data Science | Machine Learning | Python | Analytics**
