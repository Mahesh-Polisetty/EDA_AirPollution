---

# 🌫️ AirStat India: Statistical Analysis of Air Pollution Data (1998–2020)

This project presents a detailed statistical analysis of air pollution data across major Indian cities from 1998 to 2020. By combining EDA, statistical hypothesis testing, and predictive modeling, it uncovers relationships among pollutants like PM2.5, NO₂, SO₂, CO, O₃, and their effects on Air Quality Index (AQI).

---

## 📝 Abstract

Air pollution continues to be a major concern in urban India, with pollutants such as PM2.5 and NO₂ significantly exceeding safety standards. This project analyzes over 400,000 records to detect trends, outliers, and pollutant interactions. Using box plots, scatter plots, histograms, and normality assessments, it draws connections between pollutants and identifies statistically significant patterns. The results serve as a foundation for environmental policy development and pollution mitigation strategies.

---

## 🛠️ Tech Stack

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, Jupyter Notebook

---

## 📂 Dataset Information

Source: Kaggle - Air Pollution India Dataset (1998–2020): https://www.kaggle.com/datasets/xyz/air-pollution-india
Scope: Air quality and meteorological data from major Indian cities
Key Variables: PM2.5, PM10, SO₂, NO₂, CO, O₃, temperature, humidity, wind speed
Records: 400,000+ entries
Features: 13 environmental variables

--- 

## 🔬 Project Goals

-  Analyze pollutant distributions and outliers across cities and years
-  Evaluate normality of pollutant concentrations
-  Compute key parameters (mean, SD, % exceedance)
-  Identify inter-pollutant correlations (e.g., PM2.5 vs NO₂)
-  Build and compare predictive models for PM2.5

---

## 📈 Exploratory Data Analysis (EDA)

-  Scatter Plots: PM2.5 vs NO₂, NO₂ vs O₃, CO vs AQI, SO₂ vs O₃
-  Box Plots: Pollutant spread across cities and combined pollutants
-  Histograms: Year-wise and city-wise distribution of PM2.5 and other gases
-  Line Graphs: Time trends (2015–2020) for PM2.5, PM10, NO₂, O₃
-  Normality Tests: Q-Q plots for PM2.5, SO₂, O₃, CO, NO₂

---

##  📊 Statistical Insights

Mean PM2.5: ~67.45 µg/m³

Exceedance (>35 µg/m³):
-  PM2.5: 71.9%
-  NO₂: 24.6%
-  O₃: 36.0%
-  CO: 0.9%

Strongest AQI Predictor: CO (correlation ~0.65)

---

## 📉 Hypothesis Testing Results

PM2.5 Mean ≠ 60 µg/m³: Rejected (p = 0.0327)

Proportion of PM2.5 > 35 µg/m³ ≠ 0.5: Rejected (p = 6.66e-08)

NO₂ vs SO₂ Mean Difference: Significant (p = 1.66e-09)

Correlations:
-  NO₂ & PM2.5: 0.25 (Significant)
-  NO₂ & CO: 0.36 (Significant)


---

##  📉 Predictive Modeling Results

In this project, multiple linear regression models were developed to predict PM2.5 concentrations using different combinations of air pollutants as predictors. The first model (Model 1) used NO₂ and SO₂ as predictors and achieved an R-squared value of 0.0646, with an adjusted R-squared of 0.0453. This suggests that the model explains approximately 6.5% of the variance in PM2.5 levels, which is relatively low.

In an attempt to improve performance, Model 2 incorporated an additional variable—CO—alongside NO₂ and SO₂. This resulted in a slight increase in R-squared to 0.0659, but the adjusted R-squared dropped to 0.0367, indicating that the inclusion of CO did not significantly enhance predictive power and may have introduced noise.

Model 3 extended the predictor set by adding O₃, using NO₂, SO₂, CO, and O₃ to predict PM2.5. While the R-squared remained the same at 0.0659, the adjusted R-squared decreased further to 0.0265, confirming that additional predictors did not improve the model and possibly contributed to overfitting.

Among the three, Model 1 was identified as the best-performing model based on its relatively higher adjusted R-squared and simplicity. However, all models demonstrated limited predictive capability, indicating that linear regression alone is insufficient for modeling PM2.5 concentrations. These results suggest the need for more sophisticated or non-linear approaches—such as Random Forests or Support Vector Regression—and the inclusion of additional environmental or contextual features to better capture the underlying relationships.

---

## 🔮 Future Scope

-  Implement non-linear models (Random Forest, SVR)
-  Integrate meteorological features like wind direction
-  Develop city-wise air quality dashboards
-  Conduct seasonal pattern analysis

---
