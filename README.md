# Retail Demand Intelligence 📈

A comprehensive **Machine Learning project for retail demand forecasting** using Python and Scikit-learn to analyze historical retail data, engineer demand-related features, develop multiple regression models, and build an ensemble-based demand prediction system.

The project focuses on understanding the factors influencing retail demand, accurately predicting future demand, evaluating model performance, and explaining model predictions through error analysis and feature importance.

---

## 🌟 Features

### Core Features

* **Data Understanding & Cleaning:** Inspection of data quality, data types, missing values, duplicates, and dataset structure.
* **Exploratory Data Analysis:** Analysis of demand patterns across categories, regions, time periods, promotions, weather conditions, and other variables.
* **Feature Engineering:** Creation of temporal, inventory, pricing, historical-demand, and rolling-window features.
* **Data Preprocessing:** Numerical and categorical feature preparation using Scikit-learn pipelines.
* **Multiple Machine Learning Models:** Development and comparison of multiple regression models.
* **Ensemble Learning:** Implementation of a stacking-based ensemble to combine predictions from multiple models.
* **Model Evaluation:** Evaluation using MAE, RMSE, and R² along with actual-vs-predicted and residual analysis.
* **Error Analysis:** Investigation of model performance across categories, regions, demand levels, and time periods.
* **Model Explainability:** Permutation feature importance and investigation of individual high-error predictions.
* **Business Insights:** Translation of model results into practical retail demand insights.

---

## 🗂 Project Structure

The project is organized as follows:

```text
Retail_Demand_Intelligence/
│
├── data/
│   ├── raw/                         # Original dataset
│   └── processed/                   # Processed and feature-engineered data
│
├── notebooks/
│   ├── 01_data_understanding.ipynb  # Dataset inspection and understanding
│   ├── 02_eda.ipynb                 # Exploratory Data Analysis
│   ├── 03_data_preparation.ipynb    # Data preprocessing
│   ├── 04_feature_engineering.ipynb # Feature creation
│   ├── 05_model_development.ipynb   # Model development and tuning
│   ├── 06_model_evaluation.ipynb    # Model evaluation and error analysis
│   └── 07_model_explainability.ipynb# Model explainability
│
├── models/                          # Saved trained models (if applicable)
│
├── reports/
│   └── figures/                     # Project visualizations
│
├── requirements.txt                 # Python dependencies
├── README.md                        # Project documentation
└── .gitignore                       # Git ignored files
```

---

## 🏗️ Project Architecture

```text
+---------------------------+
|        DATA LAYER         |
|                           |
|  Raw Retail Dataset       |
|  CSV Data                 |
+-------------+-------------+
              ↓
+---------------------------+
|   DATA UNDERSTANDING      |
|                           |
|  - Dataset inspection     |
|  - Data types             |
|  - Missing values         |
|  - Duplicate analysis     |
+-------------+-------------+
              ↓
+---------------------------+
|        EDA LAYER          |
|                           |
|  - Demand distributions   |
|  - Category analysis      |
|  - Regional analysis      |
|  - Time patterns          |
|  - Correlation analysis   |
+-------------+-------------+
              ↓
+---------------------------+
|    PREPROCESSING LAYER    |
|                           |
|  - Data cleaning          |
|  - Categorical encoding   |
|  - Numerical preparation  |
|  - Train-test preparation |
+-------------+-------------+
              ↓
+---------------------------+
|   FEATURE ENGINEERING     |
|                           |
|  - Temporal features     |
|  - Inventory features     |
|  - Pricing features       |
|  - Historical demand      |
|  - Rolling features       |
+-------------+-------------+
              ↓
+---------------------------+
|     MODELING LAYER        |
|                           |
|  - Multiple regressors    |
|  - Hyperparameter tuning  |
|  - Ensemble learning      |
|  - Stacking               |
+-------------+-------------+
              ↓
+---------------------------+
|     EVALUATION LAYER      |
|                           |
|  - MAE                    |
|  - RMSE                   |
|  - R²                     |
|  - Residual analysis      |
|  - Error analysis         |
+-------------+-------------+
              ↓
+---------------------------+
|   EXPLAINABILITY LAYER    |
|                           |
|  - Permutation importance |
|  - Feature analysis       |
|  - Local error analysis   |
+-------------+-------------+
              ↓
+---------------------------+
|     BUSINESS INSIGHTS     |
|                           |
|  Demand patterns          |
|  Inventory insights      |
|  Model limitations        |
|  Forecasting insights     |
+---------------------------+
```

---

## 🛠 Tech Stack

* **Language:** Python 3.8+
* **Environment:** Jupyter Notebook
* **Libraries:**

  * **Data Manipulation:** Pandas, NumPy
  * **Visualization:** Matplotlib, Seaborn, Plotly
  * **Machine Learning:** Scikit-learn
  * **Model Persistence:** Joblib
* **Version Control:** Git & GitHub

---

## 📊 Dataset Overview

The project uses a retail dataset containing **76,000 observations** and a combination of operational, pricing, environmental, temporal, and demand-related variables.

### Dataset Features

```text
Date
Store ID
Product ID
Category
Region
Inventory Level
Units Sold
Units Ordered
Price
Discount
Weather Condition
Promotion
Competitor Pricing
Seasonality
Epidemic
Demand
```

Additional engineered features were created during the feature engineering stage, including:

```text
Year
Month
Week
Day
Day_of_Week
Is_Weekend
Inventory_to_Sales_Ratio
Inventory_Gap
Price_Difference
Price_Difference_Percentage
Promotion_Discount
Previous_Demand
Previous_Units_Sold
Rolling_7_Day_Demand
Rolling_7_Day_Sales
```

### Target Variable

**Demand**

The objective is to predict retail demand using historical and operational information available within the dataset.

---

## 🎯 Problem Statement

Retail businesses need accurate demand forecasts to make better decisions regarding inventory, purchasing, promotions, and resource allocation.

The objective of this project is to develop a machine learning-based demand forecasting system that can estimate product demand using historical sales patterns, inventory information, pricing, promotions, seasonality, weather conditions, and other relevant variables.

---

## 🚀 Project Objectives

* Understand the major patterns influencing retail demand.
* Analyze demand across different stores, products, categories, and regions.
* Identify important relationships between operational variables and demand.
* Engineer meaningful temporal, inventory, pricing, and historical-demand features.
* Develop and compare multiple machine learning regression models.
* Improve predictive performance using ensemble learning.
* Evaluate the final model using multiple regression metrics.
* Investigate prediction errors and model weaknesses.
* Explain which features contribute most to model predictions.
* Translate technical findings into practical business insights.

---

## 🔍 Exploratory Data Analysis

The EDA stage investigates the underlying structure and behavior of the retail dataset.

### Analysis Areas

* Demand distribution
* Numerical feature distributions
* Category-wise demand
* Region-wise demand
* Demand over time
* Seasonal demand patterns
* Promotion and discount relationships
* Weather-related demand patterns
* Correlation between numerical variables
* Outlier and variability analysis

The EDA stage was used to identify patterns and relationships that guided subsequent preprocessing and feature engineering decisions.

---

## ⚙️ Feature Engineering

Several features were created to improve the model's ability to capture demand patterns.

### Temporal Features

* `Year`
* `Month`
* `Week`
* `Day`
* `Day_of_Week`
* `Is_Weekend`

### Inventory Features

* `Inventory_to_Sales_Ratio`
* `Inventory_Gap`

### Pricing Features

* `Price_Difference`
* `Price_Difference_Percentage`
* `Promotion_Discount`

### Historical Demand Features

* `Previous_Demand`
* `Previous_Units_Sold`
* `Rolling_7_Day_Demand`
* `Rolling_7_Day_Sales`

These features were designed to capture temporal patterns, inventory conditions, pricing differences, recent demand behavior, and short-term sales trends.

---

## 🤖 Machine Learning Approach

The project treats retail demand prediction as a **supervised regression problem**.

The modeling workflow includes:

```text
Data Preparation
       ↓
Feature Engineering
       ↓
Train-Test Split
       ↓
Preprocessing Pipeline
       ↓
Multiple Regression Models
       ↓
Hyperparameter Tuning
       ↓
Model Comparison
       ↓
Stacking Ensemble
       ↓
Final Evaluation
```

Categorical variables were processed using **One-Hot Encoding**, while numerical features were passed through the preprocessing pipeline.

A **Stacking Regressor** was subsequently used to combine the predictive capabilities of multiple models.

---

## 📈 Model Evaluation

Model performance was evaluated using three primary regression metrics:

### Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted demand.

### Root Mean Squared Error (RMSE)

Measures prediction error while assigning greater weight to larger errors.

### R² Score

Measures the proportion of variation in the target variable explained by the model.

### Evaluation Analysis

In addition to numerical metrics, the project includes:

* Actual vs Predicted Demand analysis
* Residual distribution
* Residual vs Predicted Demand
* Largest prediction errors
* Category-wise performance
* Region-wise performance
* Demand-level performance
* Monthly performance

> **Final model metrics will be reported here after the final evaluation results are verified against the completed evaluation pipeline.**

---

## 🔎 Model Explainability

Model explainability was performed using **permutation feature importance** and individual prediction analysis.

### Top Important Features

The strongest original features identified through permutation importance were:

| Rank | Feature                  |
| ---: | ------------------------ |
|    1 | Inventory to Sales Ratio |
|    2 | Inventory Level          |
|    3 | Units Ordered            |
|    4 | Weather Condition        |
|    5 | Promotion                |
|    6 | Seasonality              |
|    7 | Inventory Gap            |
|    8 | Epidemic                 |
|    9 | Rolling 7-Day Demand     |
|   10 | Previous Demand          |

The analysis indicates that inventory-related variables have a particularly strong relationship with the model's predictions.

---

## 💡 Key Findings

* Inventory-related features were among the strongest contributors to model predictions.
* Recent demand history provides useful information for estimating current demand.
* Model errors tend to increase as demand levels become higher.
* The model performs well on typical demand patterns but has greater difficulty with unusually large demand spikes.
* Promotions, weather conditions, and seasonality provide additional predictive information.
* Residual analysis showed that errors were generally centered around zero, with a limited number of larger deviations.
* A detailed high-error case showed that the model could recognize elevated demand but still underestimate an exceptional demand spike.

---

## ⚠️ Limitations & Future Improvements

### Current Limitations

Some engineered features use information from the current observation.

In particular:

* `Units Sold` represents contemporaneous information.
* `Inventory_to_Sales_Ratio` uses current `Units Sold`.
* `Inventory_Gap` is also derived using current-period information.

Therefore, these features should be reviewed carefully when applying the model to a **true pre-demand forecasting scenario**, where the objective is to predict demand before sales occur.

### Future Improvements

* Replace contemporaneous variables with strictly historical information.
* Introduce additional external demand drivers.
* Incorporate holidays and special events.
* Explore advanced time-series forecasting techniques.
* Perform systematic model monitoring after deployment.
* Investigate methods specifically designed to handle demand spikes.
* Evaluate the model using rolling or walk-forward validation for production forecasting.

---

## 📁 Notebook Workflow

The project is divided into seven notebooks to maintain a structured and reproducible workflow.

| Notebook                        | Purpose                                      |
| ------------------------------- | -------------------------------------------- |
| `01_data_understanding.ipynb`   | Dataset inspection and initial understanding |
| `02_eda.ipynb`                  | Exploratory Data Analysis and visualization  |
| `03_data_preparation.ipynb`     | Data cleaning and preprocessing              |
| `04_feature_engineering.ipynb`  | Feature creation and transformation          |
| `05_model_development.ipynb`    | Model development, comparison, and tuning    |
| `06_model_evaluation.ipynb`     | Model performance and error analysis         |
| `07_model_explainability.ipynb` | Feature importance and prediction analysis   |

---

## 🚀 Quick Start

### 1. Clone Repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd Retail_Demand_Intelligence
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
```

### 3. Activate Virtual Environment

#### Windows

```bash
.\.venv\Scripts\activate
```

#### Mac/Linux

```bash
source .venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the `notebooks/` directory and run the notebooks in numerical order.

---

## 📌 Project Status

**Status:** Completed ✅

The project currently includes:

* Data understanding
* Exploratory data analysis
* Data preprocessing
* Feature engineering
* Machine learning model development
* Hyperparameter tuning
* Stacking ensemble
* Model evaluation
* Error analysis
* Model explainability

---

## 👨‍💻 Author

**Tejas Jadhav**

* GitHub: [@tejas-jadhav](https://github.com/TejasMJ)
* LinkedIn: [Tejas Jadhav](https://www.linkedin.com/in/tejas-m-jadhav/)
