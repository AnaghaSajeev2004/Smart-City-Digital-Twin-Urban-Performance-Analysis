# 🏙️ Smart City Digital Twin: Urban Performance Analysis

## 📊 Power BI Project

An interactive **Power BI dashboard project** that analyzes urban performance using a synthetic Smart City Digital Twin dataset.

The project integrates data from multiple interconnected city systems, including **air quality, traffic, power grid, weather, public transport, emergency events, and city events**. The goal is to transform large volumes of urban data into meaningful insights that can support **data-driven urban planning and decision-making**.

---

## 🎯 Project Objective

The main objective of this project is to analyze:

* 🌫️ Air quality across city districts
* 🚦 Traffic congestion and incidents
* ⚡ Power grid performance and renewable energy
* 🌦️ Weather conditions and their impact
* 🚌 Public transportation performance
* 🚑 Emergency incidents and response times
* 🏙️ District-level urban performance

The dashboard helps identify **high-stress districts, time-based patterns, and major factors affecting urban performance**.

---

## 📁 Dataset

The project uses a **synthetic Smart City Digital Twin dataset** covering:

* **20 districts**
* **3 years of data (2023–2025)**
* Multiple interconnected urban systems
* Hourly sensor and operational records

### Dataset Components

| Dataset             | Description                                             |
| ------------------- | ------------------------------------------------------- |
| 🏙️ Districts       | District information and infrastructure characteristics |
| 🌫️ Air Quality     | Pollutant levels and AQI measurements                   |
| 🚦 Traffic          | Congestion, accidents and road incidents                |
| ⚡ Power Grid        | Grid load, renewable generation and outages             |
| 🌦️ Weather         | Temperature and weather conditions                      |
| 🚌 Public Transport | Passenger activity, delays and disruptions              |
| 🚑 Emergency Events | Emergency types, severity and response time             |
| 🎉 City Events      | Events, attendance and their urban impact               |

## The source project documentation reports **527,132 hourly air-quality records** and **527,132 traffic records**, while the Power Grid, Weather and Public Transport datasets each contain **526,080 records**.

## 🛠️ Tools & Technologies

* **Microsoft Power BI Desktop**
* **Power Query**
* **DAX**
* **Data Modeling**
* **Data Visualization**
* **CSV Dataset**
* **Star Schema**

---

## 🗂️ Data Model

A **star schema** was created for the analysis.

A dedicated `DimDate` table was created and connected to the date fields of the seven major data tables.

The `Districts` table was connected through `district_id` to the corresponding datasets.

### Main Dimensions

* `DimDate`
* `Districts`

### Main Data Tables

* Air Quality
* Traffic
* Power Grid
* Weather
* Public Transport
* Emergency Events
* City Events

This model enables consistent filtering and cross-analysis across districts and time periods.

---

## 📈 Dashboard Pages

### 1. 🏙️ Overview Dashboard

Provides an overall view of city performance using key indicators such as:

* Average AQI
* Average congestion
* Emergency count
* Public transport disruptions
* Average grid load
* District-level performance
* Monthly congestion trends

---

### 2. 🌫️ Environment & Weather Dashboard

Focuses on environmental conditions and weather patterns.

### Visualizations include:

* Average AQI by District
* Air Quality Category Breakdown
* Average Temperature by Month
* Weather Condition Counts
* District and year filters

The dashboard shows that **Industrial Zone recorded the highest average AQI at 126**, compared with a citywide average of approximately 50.

---

### 3. 🚦 Mobility Dashboard

Analyzes traffic and public transportation performance.

### Visualizations include:

* Average Congestion by District
* Rush Hour vs Non-Rush Hour Congestion
* Public Transport Delay by Month
* Total Accidents
* Public Transport Disruptions

The analysis identifies **Old Town as the highest-congestion district**, with an average congestion index of 67. Rush-hour congestion is substantially higher than non-rush-hour congestion.

---

### 4. ⚡ Energy & Safety Dashboard

Analyzes electricity infrastructure and emergency response.

### Visualizations include:

* Grid Load & Renewable Share
* Power Outages by District
* Emergencies by Type
* Average Response Time by Severity
* Grid performance indicators

The analysis shows an average grid load of approximately **61.59%**, while renewable generation contributes around **12%** of the power supply.

---

## 📊 Key DAX Measures

Several measures were created to summarize the datasets.

```DAX
Avg AQI =
AVERAGE(air_quality[synthetic_aqi])
```

```DAX
Avg Congestion =
AVERAGE(traffic[congestion_index])
```

```DAX
Total Accidents =
SUM(traffic[accident_count])
```

```DAX
Renewable % =
AVERAGE(power_grid[renewable_generation_percent])
```

```DAX
AvgResponse(min) =
AVERAGE(emergency_events[response_time_minutes])
```

The project documentation states that **11 measures** were created for the analysis.

---

## 🔍 Key Insights

### 🌫️ Air Quality

* Industrial Zone has the highest average AQI.
* Industrial Zone recorded an AQI of **126**.
* This is significantly higher than the citywide average.

### 🚦 Traffic

* Old Town has the highest average congestion.
* Average congestion in Old Town reaches **67**.
* Rush-hour congestion is considerably higher than non-rush-hour congestion.

### ⚡ Power Grid

* Average grid load is approximately **62%**.
* Renewable generation contributes around **12%**.
* Stadium District and Central Park experience the highest number of outages.

### 🚑 Emergency Response

* Medical emergencies and traffic accidents represent the largest categories of incidents.
* Emergency response time varies according to severity.
* Critical emergencies have an average response time of approximately **14.6 minutes**, while low-priority cases average approximately **24.8 minutes**.

---

## 💡 Recommendations

Based on the analysis, the project recommends:

1. **Improve emissions control in Industrial Zone**
2. **Introduce targeted traffic management during rush hours in Old Town**
3. **Increase renewable energy generation**
4. **Improve power-grid reliability in high-outage districts**
5. **Use weather information when planning traffic management**
6. **Monitor emergency response performance by severity**

---


## 🎓 Skills Demonstrated

This project demonstrates practical experience in:

* Power BI Dashboard Development
* Data Cleaning & Transformation
* Power Query
* DAX
* Data Modeling
* Star Schema
* Data Visualization
* KPI Development
* Interactive Filters & Slicers
* Exploratory Data Analysis
* Urban Data Analytics
* Business Intelligence
* Data-Driven Decision Making

---

## 👩‍💻 Author

**Anagha Sajeev**

B.Tech Computer Science Graduate

Interested in **Data Analytics, Power BI, Python, SQL and Business Intelligence**.

---

## 🔗 Dataset Source

Smart City Digital Twin Ecosystem Dataset – Kaggle

https://www.kaggle.com/datasets/razanihababdellatif/smart-city-digital-twin-ecosystem-dataset

---

## 📌 Project Status

**Completed ✅**

This project was developed as a Power BI data analytics project to demonstrate dashboard development, data modeling, DAX calculations and urban performance analysis.
