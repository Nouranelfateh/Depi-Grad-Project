# Depi-Grad-Project
# Call Center Performance Analytics Dashboard

## 1. **Project Overview**

This project presents an end-to-end **Data Analytics workflow** designed to analyze and monitor **call center performance**.

The system processes operational call center data and transforms it into meaningful insights using multiple analytical tools including **Python**, **SQL**, **Excel**, **Power BI**, **Tableau**, and **Scikit-learn**.

The final output of the project is an **interactive Power BI dashboard** that enables managers to evaluate service performance, monitor agent productivity, and analyze customer satisfaction metrics.

---

## 2. **Project Objective**

The main objective of this project is to build a **data-driven performance monitoring system** for call center operations.

The system allows managers to:

1. Monitor **call center operational performance**
2. Track **answered vs abandoned calls**
3. Evaluate **agent productivity**
4. Analyze **customer satisfaction metrics**
5. Compare **forecasted call volumes with actual performance**

These insights help organizations make **data-driven operational decisions**.

---

## 3. **Project Idea**

Call centers generate large volumes of operational data such as **call logs**, **handling times**, **agent activity**, and **customer feedback**.

Without proper analytics tools, extracting insights from this data becomes difficult.

This project builds a **data analytics pipeline** that transforms raw operational data into structured insights through **data cleaning**, **feature engineering**, and **interactive dashboards**.

---

## 4. **Data Analytics Workflow**

### 4.1 **Data Preparation**

The dataset is prepared using **Excel** and **SQL** to:

- Organize the raw dataset
- Validate column types
- Extract relevant records

### 4.2 **Data Cleaning**

Data cleaning is performed using **Python (Pandas)** to:

- Handle missing values
- Remove duplicate records
- Convert columns to appropriate data types
- Standardize the dataset

### 4.3 **Feature Engineering**

Using **Python** and **Scikit-learn**, additional analytical features are created such as:

- Call duration categories
- Peak call hour indicators
- Agent efficiency metrics

### 4.4 **Data Modeling**

The cleaned dataset is imported into **Power BI** where:

- Table relationships are created
- Date and time dimensions are structured
- Analytical measures are implemented using **DAX**

### 4.5 **Dashboard Development**

Interactive dashboards are developed using **Power BI** and **Tableau** to visualize key performance metrics.

---

## 5. **System Analysis**

### 5.1 **Input Data**

| Attribute | Description |
|----------|-------------|
| Call ID | Unique identifier for each call |
| Call Date | Date of the call |
| Call Time | Time interval when the call occurred |
| Agent Name | Agent handling the call |
| Team Manager | Manager supervising the agent |
| Department | Department responsible for the call |
| Call Status | Indicates whether the call was answered or abandoned |
| Handling Time | Duration of the call |
| Customer Satisfaction Score | Customer feedback rating |
| Forecasted Calls | Predicted call volume |
| Actual Calls | Actual call volume |

---

### 5.2 **System Processing**

The system performs several processing operations including:

- Data cleaning and validation
- Feature engineering
- Aggregation of performance metrics
- KPI calculations
- Time-based performance analysis

---

### 5.3 **System Outputs**

The system generates **interactive dashboards** that display:

- Key Performance Indicators (**KPIs**)
- Call center performance trends
- Agent productivity comparisons
- Call distribution analysis
- Customer satisfaction metrics

---
## **6. Analytical Metrics**

**Abandonment Rate**  
`Abandonment Rate = Abandoned Calls / Total Calls`  

**Average Handling Time (AHT)**  
`AHT = Total Handling Time / Answered Calls`  

**Forecast Accuracy**  
`Forecast Accuracy = Actual Calls / Forecasted Calls`  

---
## 7. **Key DAX Measures**

### **Total Calls**

```DAX
Total Calls =
COUNT(CallCenter[CallID])
```

### **Answered Calls**

```DAX
Answered Calls =
CALCULATE(
    COUNT(CallCenter[CallID]),
    CallCenter[CallStatus] = "Answered"
)
```

### **Abandoned Calls**

```DAX
Abandoned Calls =
CALCULATE(
    COUNT(CallCenter[CallID]),
    CallCenter[CallStatus] = "Abandoned"
)
```

### **Abandonment Rate**

```DAX
Abandonment Rate =
DIVIDE([Abandoned Calls], [Total Calls], 0)
```

### **Average Handling Time**

```DAX
Average Handling Time =
AVERAGE(CallCenter[HandlingTime])
```

### **Customer Satisfaction Score**

```DAX
CSAT Score =
AVERAGE(CallCenter[CustomerSatisfaction])
```

---

## 8. **Technologies Used**

| Technology | Purpose |
|-----------|--------|
| Power BI | Dashboard development and visualization |
| Python | Data cleaning and preprocessing |
| Pandas / NumPy | Data manipulation |
| Scikit-learn | Feature engineering |
| SQL | Data querying |
| Excel | Data preparation |
| Tableau | Additional visualization |

---

## 9. **Repository Structure**

```
call-center-performance-dashboard

data
   raw_data.xlsx
   processed_data.csv

python
   data_cleaning.py
   feature_engineering.py

sql
   queries.sql

powerbi
   call_center_dashboard.pbix

tableau
   dashboard.twb

README.md
```

---

## 10. **Expected Insights**

The dashboard helps decision makers to:

- Identify **high performing agents**
- Detect **call abandonment patterns**
- Monitor **customer satisfaction trends**
- Analyze **call volume trends**
- Improve **workforce planning**
