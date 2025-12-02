# 🗂️ SQL Queries Overview

This folder contains all SQL scripts and the Python weather parser used in the first phase of the **Chicago Taxi SQL Analysis | Time-Series Project**.  
These queries were executed before the Python notebook and produced the CSV files stored in the `/data` directory.

The SQL phase identifies company activity, neighborhood patterns, weather conditions, and the specific rides used for hypothesis testing.  
These outputs feed directly into the Python-based EDA, visualization, and forecasting steps.

---

## 📄 Files and Their Purpose

### **01_parse_weather.py**
Parses historical Chicago weather data for November 2017 from:

https://practicum-content.s3.us-west-1.amazonaws.com/data-analyst-eng/moved_chicago_weather_2017.html

Outputs the full `weather_records` table for later SQL joins.

---

### **02_company_trips_15_16.sql**  
**Output CSV:** `project_sql_result_01.csv`

Counts all taxi rides per company for **November 15–16, 2017**.

**Columns:**
- `company_name`
- `trips_amount`

Used in visualization of company performance.

---

### **03_yellow_blue_companies.sql**  
**Output CSV:** `project_sql_result_02.csv`

Counts rides for companies containing **“Yellow”** or **“Blue”** for **November 1–7, 2017**.

**Columns:**
- `company_name`
- `trips_amount`

---

### **04_flash_vs_other.sql**  
**Output CSV:** `project_sql_result_03.csv`

Groups all taxi companies into:

- `Flash Cab`
- `Taxi Affiliation Services`
- `Other`

Then counts all rides for **November 1–7, 2017**.

**Columns:**
- `company`
- `trips_amount`

---

### **05_neighborhood_ids.sql**  
**Output CSV:** `project_sql_result_04.csv`

Retrieves IDs for:
- **Loop**
- **O’Hare**

These IDs are later used to filter directional trips.

**Columns:**
- `neighborhood_id`
- `name`

---

### **06_weather_conditions.sql**  
**Output CSV:** `project_sql_result_05.csv`

Classifies each hourly weather record as:
- `Good`
- `Bad` (rain or storm)

**Columns:**
- `ts`
- `weather_conditions`

This classification is used in the hypothesis test.

---

### **07_loop_to_ohare_weather_join.sql**  
**Output CSV:** `project_sql_result_07.csv`

Retrieves all rides that:
- start in the **Loop** (`pickup_location_id = 50`)
- end at **O’Hare** (`dropoff_location_id = 63`)
- occur on **Saturdays**
- have matched weather conditions

Used for the statistical test:  
*“Does ride duration from Loop → O’Hare change on rainy Saturdays?”*

**Columns:**
- `start_ts`
- `weather_conditions`
- `duration_seconds`

---

## 📦 How These SQL Outputs Are Used

These CSV files are consumed inside the Python notebook to perform:

- Exploratory Data Analysis  
- Neighborhood-level demand analysis  
- Weather-condition grouping  
- Hypothesis testing  
- Time-series forecasting  

This SQL → CSV → Python workflow creates a complete and reproducible analytical pipeline.

---

## 📁 Folder Structure
```
sql/
├─ 01_parse_weather.py
├─ 02_company_trips_15_16.sql
├─ 03_yellow_blue_companies.sql
├─ 04_flash_vs_other.sql
├─ 05_neighborhood_ids.sql
├─ 06_weather_conditions.sql
└─ 07_loop_to_ohare_weather_join.sql
```

Each script corresponds to a numbered project step and produces a matching CSV in the `/data` folder.

---

## Author
**Rhiannon Fillingham**

