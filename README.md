# NHS A&E Performance Analysis and Patient Admission Predictive Modelling

## Project Overview
This project analyzes **NHS England Accident & Emergency (A&E) department performance** and develops predictive models for patient admissions and waiting times. Using open NHS datasets, we explore trends in hospital attendances, evaluate performance against the 4-hour waiting target, visualize regional patterns on interactive maps, and forecast future A&E volumes.

The project demonstrates **data acquisition, cleaning, exploratory data analysis (EDA), interactive visualization, feature engineering, classification, and time-series forecasting** using Python and Jupyter Notebook/Google Colab.

---

## Dataset
**Source:** NHS England Open Data  
- [A&E Attendances and Emergency Admissions](https://www.england.nhs.uk/statistics/statistical-work-areas/accident-and-emergency/)  

**Dataset file used in this project:**  
`AE_attendances_england_monthly.csv`  

**Key columns:**
- `date`: Month of reporting (YYYY-MM-DD)
- `Name`: Hospital/Trust name
- `Type 1/2/3 Departments`: Attendances and waiting times per department type
- `Total attendances`: Total A&E visits
- `Percentage in 4 hours or less (all)`: Key KPI for performance
- `Emergency Admissions via Type 1/2/3`
- `lat` & `lon`: Latitude and longitude for mapping

> Note: The dataset originally had wrongly formatted `month` and `year` columns, which are fixed during preprocessing.

---

## Project Objectives
1. **Analyze NHS A&E performance**:
   - Trends in attendances over time
   - Seasonal spikes and monthly variations
   - Hospital-level and regional comparisons

2. **Visualize hospital performance**:
   - Interactive maps of hospitals using Folium
   - Scatter plots and line charts for attendances and 4-hour target performance

3. **Predictive modelling**:
   - **Classification:** Predict whether hospitals will meet the 4-hour waiting time target (>=95%)
   - **Forecasting:** Predict total A&E attendances for future months using Prophet

4. **Provide insights**:
   - Hospitals consistently missing 4-hour targets
   - Seasonal trends in A&E visits
   - Key factors affecting waiting times

---

## Tools & Technologies
- **Programming Language:** Python 3.x
- **Data Analysis & ML Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Prophet
- **Visualization:** Matplotlib, Seaborn, Plotly, Folium
- **Environment:** Jupyter Notebook / Google Colab
- **Version Control:** GitHub

---


---

## Workflow / Step-by-Step
1. **Data Acquisition**
   - Load CSV from Kaggle/NHS dataset
   - Use Colab cache for faster access

2. **Data Cleaning & Preprocessing**
   - Convert `date` column to datetime
   - Fix `month` and `year` columns
   - Fill missing values for lat/lon and numeric columns

3. **Exploratory Data Analysis (EDA)**
   - Plot trends in total A&E attendances
   - Evaluate distribution of 4-hour target performance
   - Identify top 10 hospitals by attendances

4. **Map Visualizations**
   - Folium maps showing hospital locations, total attendances, and 4-hour performance

5. **Feature Engineering**
   - Lag features (`Total_attendances_Lag1`, `Lag3`)
   - Binary classification target for 4-hour KPI (`Target_4h_met`)

6. **Predictive Modelling**
   - **Classification:** Random Forest to predict whether 4-hour target is met
   - **Forecasting:** Prophet to predict next 12 months total A&E attendances

7. **Insights & Reporting**
   - Top hospitals missing 4-hour target
   - Seasonal attendance patterns
   - Feature importance for predictive model

8. **Interactive Dashboard**
   - Plotly line charts, bar charts, and scatter maps for dynamic exploration

---

## Key Insights
- Some hospitals consistently miss the 4-hour waiting target.
- Winter months show higher A&E attendances, reflecting seasonal spikes.
- Lagged attendances and month indicators are important features for predicting 4-hour KPI performance.
- Interactive maps help visualize hospital performance geographically.

---

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/stephen0111/NHSAandE.git

