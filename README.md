# 🌤️ WW2 Weather Data Analysis & Temperature Prediction

Welcome to my Machine Learning portfolio project! In this project, I built an end-to-end Machine Learning pipeline to analyze historical weather data (recorded during World War II between 1940-1945) and predict the daily maximum temperature based on the minimum temperature.

## 🎯 Project Objective
The main goal of this project is to apply Data Science and Machine Learning best practices: transforming messy data into a clean structure, performing Exploratory Data Analysis (EDA) to detect anomalies, and benchmarking over 30 Regression models to find the most accurate predictor.

## ⚙️ Project Pipeline

### 1. Data Cleaning & Preprocessing
* Checked for missing values and imputed `NaN` values in the "Snowfall" column with `0`.
* Corrected data types: Converted object types to `float64` and handled `datetime` conversions for time-series validity.
* Removed duplicate rows to prevent data leakage.

### 2. Exploratory Data Analysis (EDA) & Outlier Removal
* Plotted a scatter plot (`sns.scatterplot`) between Minimum and Maximum temperatures which revealed a strong positive linear correlation.
* **Anomaly Detection:** Discovered and removed physically impossible data points (e.g., `MinTemp > MaxTemp`) and daily temperature swing sensor errors (swings > 35°C), ensuring the model learns from scientifically accurate data.

### 3. Baseline Modeling
* Split the cleaned dataset into Training (80%) and Testing (20%) sets.
* Trained a fundamental **Simple Linear Regression** model to establish a baseline.
* **Baseline Result:** Achieved an initial R² score of **0.7737**.

### 4. Algorithmic Benchmarking (LazyPredict)
* Instead of settling for the baseline, I utilized the `LazyPredict` library to run and evaluate over 30 popular supervised regression algorithms simultaneously.
* Compared models based on their R-Squared and Adjusted R-Squared scores.

### 5. Final Champion Model 🏆
* The benchmarking revealed that the **Gradient Boosting Regressor** significantly outperformed the linear models.
* Successfully trained the final Gradient Boosting model and boosted the prediction accuracy matrix.
* **Final Result:** Jumped from 0.77 to a final R² score of **0.8118**.

## 💻 Technologies & Libraries Used
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Linear Regression, Ridge, Lasso, Decision Tree, RandomForest, GradientBoosting)
* **AutoML / Benchmarking:** LazyPredict

---
*Feel free to explore the Jupyter Notebook attached to see the code, visualizations, and step-by-step comments!*
