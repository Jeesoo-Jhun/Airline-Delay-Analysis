# ✈️ Airline Delays Analysis

This project investigates the causes and patterns behind flight delays in the United States. Using historical flight performance data from the U.S. Bureau of Transportation Statistics, we aim to identify the key drivers of delays, uncover trends across airlines and airports, and build a basic model to estimate delay probability.

---

## 🎯 Objectives

- Understand when and why domestic U.S. flights are delayed.
- Identify delay trends by:
  - Airline carrier
  - Airport (origin/destination)
  - Day of the week / Month / Time of day
  - Flight distance and route
  - Weather conditions (if available)
- Build a basic predictive model for flight delay classification.

---

## ❓ Key Questions

1. Which airlines have the highest and lowest delay rates?
2. Are some airports more prone to delays than others?
3. Does time of day or day of week influence delay likelihood?
4. What are the most common causes of delays (e.g., weather, carrier, late aircraft)?
5. Can we predict if a flight will be delayed based on available features?

---

## 🗃️ Data Overview

- **Source**: [U.S. Bureau of Transportation Statistics (BTS)](https://www.transtats.bts.gov/)
- **Dataset**: On-Time Performance (e.g., 2015–2019)
- **Volume**: Millions of rows per year
- **Key columns**:
  - `FL_DATE`, `OP_UNIQUE_CARRIER`, `ORIGIN`, `DEST`
  - `DEP_TIME`, `DEP_DELAY`, `ARR_DELAY`, `CANCELLED`, `DIVERTED`
  - `CARRIER_DELAY`, `WEATHER_DELAY`, `NAS_DELAY`, `SECURITY_DELAY`, `LATE_AIRCRAFT_DELAY`

*Note: Weather data can be joined from NOAA or OpenWeather APIs (optional).*

---

## 🛠️ Tools & Technologies

- **Languages**: Python, SQL
- **Libraries**: pandas, numpy, matplotlib, seaborn, plotly, scikit-learn
- **Data storage/query**: PostgreSQL or SQLite
- **Development**: Jupyter Notebook, VS Code
- *(Optional)* Tableau or Power BI for dashboarding

---

## 🧪 Project Workflow

1. **Data Ingestion**
   - Download and consolidate CSVs
   - Clean column names, parse date/time fields

2. **Data Cleaning & Transformation**
   - Handle missing values, remove cancelled/diverted flights
   - Create time-based features (hour bucket, weekday, etc.)
   - Calculate binary delay target (e.g., delay ≥ 15 minutes)

3. **Exploratory Data Analysis (EDA)**
   - Distribution of delays by carrier, airport, month
   - Correlation between features and delay duration
   - Visualization of delay trends and delay causes

4. **Modeling (Optional)**
   - Train a classifier (Logistic Regression, Random Forest) to predict delays
   - Evaluate using accuracy, precision, recall, AUC

5. **Visualization & Communication**
   - Bar charts, heatmaps, box plots, time series
   - Optional dashboard using Tableau or Power BI

---
