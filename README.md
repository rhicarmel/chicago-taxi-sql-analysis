# 🚖 Chicago Taxi SQL Analysis | Time-Series Project

## Overview
A complete SQL and time-series analysis of **Chicago taxi and weather data** to uncover demand patterns, company performance, and external factors affecting ride durations.

**Goal:** Predict taxi orders with an RMSE ≤ 48.  
**Best Model:** 🏆 Scaled Linear Regression (RMSE = 34.89)

### Project Background
This project is based on a case study for **Zuber**, a new ride-sharing company launching in Chicago.  
The analysis uses competitor taxi data and weather records to:

- Understand passenger preferences and neighborhood demand
- Compare company performance across Chicago
- Test whether **rainy weather on Saturdays** changes the duration of rides from the Loop to O’Hare International Airport

### Data Sources
- Relational database with four main tables: `neighborhoods`, `cabs`, `trips`, and `weather_records`
- Historical hourly weather in Chicago (November 2017), parsed from: 
  [Chicago Weather 2017 HTML](https://practicum-content.s3.us-west-1.amazonaws.com/data-analyst-eng/moved_chicago_weather_2017.html)

## SQL Queries
The original SQL analysis was completed in a database environment.  
All SQL queries used in this project are included in the `sql/` folder.

### Run Notebook
[![Run Notebook](https://img.shields.io/badge/📓_Open_Notebook-orange?style=for-the-badge)](./notebooks/TaxiOrders(TimeSeries).ipynb)

---

## Functionality
- SQL-based data retrieval and cleaning  
- Time-series and spatial exploratory data analysis  
- Weather and trip-condition comparison  
- Hypothesis testing to assess weather impact on O’Hare-bound trips  
- Business-oriented insights for operational optimization  

---


## Key Insights
- Identified high-demand locations and company performance patterns  
- Determined weather’s statistical effect on O’Hare-bound trips  
- Improved SQL query performance and analysis workflow  
- Final model comfortably surpassed project requirements (RMSE ≤ 48).

---

## Results
| Model | RMSE | Notes |
|--------|------|--------|
| **Linear Regression (Scaled)** | **34.89** | Best overall performance |
| Random Forest | 42.45 | Stable, interpretable |
| Gradient Boosting | 45.66 | Slightly weaker |


| Area | Key Finding | Impact |
|------|-------------|--------|
| Demand Patterns | High-volume pickup clusters around O’Hare and downtown | Supports targeted driver allocation |
| Weather Effects | Weather increases delays on airport trips | Improves planning of buffer times |
| Company Trends | Clear performance differences across operators | Guides operational strategy |

---

## Tech Stack
**SQL**, PostgreSQL, Pandas, NumPy, Matplotlib, Seaborn, SciPy

*Developed in Jupyter Notebook*

---

## Installing
```bash
# Clone repo
git clone https://github.com/rhicarmel/chicago-taxi-sql-analysis.git
cd chicago-taxi-sql-analysis

# Install dependencies
pip install -r requirements.txt

# Open notebook
jupyter notebook TaxiOrders(TimeSeries).ipynb
```

---

## Future Improvements

- Integrate flight schedules, city events, or weather data for deeper insight
- Build an interactive Streamlit dashboard
- Add forecasting models using time-series or machine learning
- Expand spatial mapping of pickup and dropoff clusters

---

## Author
**Rhiannon Fillingham**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/rhiannonfilli)

