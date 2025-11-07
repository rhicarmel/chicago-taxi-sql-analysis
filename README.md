# 🚖 CHICAGO TAXI DEMAND FORECASTING (TIME SERIES PROJECT)

## Overview
A machine learning project predicting **hourly taxi orders at Chicago airports** using historical demand data from **Sweet Lift Taxi**.  
The goal is to forecast the number of taxi rides for the next hour, helping dispatchers attract more drivers during peak hours.

**Goal:** Predict taxi orders with an RMSE ≤ 48.  
**Best Model:** 🏆 Scaled Linear Regression (RMSE = 34.89)

🔗 [View the full notebook here](./TaxiOrders(TimeSeries).ipynb)

[▶️ Launch Interactive App](https://deepnote.com/app/projects-8f6f/Rhiannon-Fillinghams-Untitled-project-e4fcc3d3-5168-437d-83da-8e0f449fef77?utm_source=app-settings&utm_medium=product-shared-content&utm_campaign=data-app&utm_content=e4fcc3d3-5168-437d-83da-8e0f449fef77)

---

## Functionality
- Resamples raw order data into hourly intervals.  
- Conducts exploratory data analysis to uncover **trends and seasonality**.  
- Builds lag features and rolling averages to model temporal dependencies.  
- Tests and tunes multiple models: Linear Regression, Random Forest, and Gradient Boosting.  
- Evaluates performance using RMSE and time series cross-validation.

---

## Key Insights
- Taxi demand shows **strong daily seasonality** (predictable hourly cycles).  
- **Feature scaling** improved Linear Regression’s forecasting accuracy.  
- Tree-based models (Random Forest, Gradient Boosting) performed well but were less consistent.  
- Final model comfortably surpassed project requirements (RMSE ≤ 48).

---

## Results
| Model | RMSE | Notes |
|--------|------|--------|
| **Linear Regression (Scaled)** | **34.89** | Best overall performance |
| Random Forest | 42.45 | Stable, interpretable |
| Gradient Boosting | 45.66 | Slightly weaker |

---

## Tech Stack
**Python**, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
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

- Integrate Prophet or SARIMA models for improved seasonality forecasting.

- Add external factors like weather, flight schedules, or city events.

- Deploy as a real-time API for predictive dispatching.

---

## Author

Rhiannon Fillingham

📎 [LinkedIn](www.linkedin.com/in/rhiannonfilli)
