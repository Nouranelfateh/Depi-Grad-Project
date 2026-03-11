# Depi-Grad-Project
Call Center Performance Analytics Dashboard
1. Project Overview

This project presents an end-to-end data analytics solution designed to analyze and monitor call center performance. The system processes operational call center data and transforms it into actionable insights using a combination of analytical tools.

The analytics pipeline integrates multiple technologies including Python, SQL, Excel, Power BI, Tableau, and Scikit-learn.

The final output of the system is an interactive Power BI dashboard that enables managers to evaluate service efficiency, agent performance, and customer satisfaction metrics.

2. Project Objective

The primary objective of this project is to build a data-driven monitoring system for call center operations.

The system aims to support decision making by enabling managers to:

Monitor call center performance metrics.

Analyze agent productivity.

Track customer service efficiency.

Evaluate customer satisfaction indicators.

Compare forecasted call volumes with actual performance.

3. System Architecture

The project follows a structured data analytics pipeline composed of several layers.

Data Sources
     │
     ▼
Data Preparation (Excel / SQL)
     │
     ▼
Data Cleaning & Feature Engineering (Python)
     │
     ▼
Data Modeling (Power BI)
     │
     ▼
Data Visualization (Power BI / Tableau)
     │
     ▼
Performance Insights

Additional architecture diagrams are included in the repository.

4. System Analysis
4.1 Input Data

The system processes operational call center datasets containing the following attributes.

Attribute	Description
Call ID	Unique identifier for each call
Call Date	Date of the call
Call Time	Time interval when the call occurred
Agent Name	Agent responsible for the call
Team Manager	Manager supervising the agent
Department	Department responsible for handling the call
Call Status	Indicates whether the call was answered or abandoned
Handling Time	Duration of the call
Customer Satisfaction Score	Customer feedback rating
Forecasted Calls	Predicted call volume
Actual Calls	Actual number of calls received
Transfers	Number of transferred calls
4.2 Processing Components

The system performs several analytical operations on the dataset.

Data Preparation

Data preparation is performed using Excel and SQL queries in order to:

Structure the dataset

Filter relevant attributes

Validate data integrity

Data Cleaning

Python (Pandas) is used to perform data cleaning tasks including:

Removing duplicate records

Handling missing values

Converting data types

Normalizing column formats

Feature Engineering

Feature engineering is implemented using Python and Scikit-learn. Examples include:

Agent efficiency indicators

Call duration categories

Peak call hour detection

Customer satisfaction classification

Data Modeling

Power BI is used to create the analytical data model including:

Table relationships

Time dimension tables

Calculated measures using DAX

4.3 System Outputs

The system generates interactive dashboards that provide:

Key Performance Indicators (KPIs)

Performance trends over time

Agent productivity comparisons

Call distribution analysis

Customer satisfaction insights

5. Analytical Metrics and Algorithms

Several analytical metrics are calculated to evaluate call center performance.

5.1 Abandonment Rate

Abandonment\ Rate = \frac{Abandoned\ Calls}{Total\ Calls}

This metric measures the percentage of calls that were not handled by agents.

5.2 Average Handling Time (AHT)

AHT = \frac{Total\ Handling\ Time}{Answered\ Calls}

This metric evaluates the average time spent by agents handling customer calls.

5.3 Forecast Accuracy

Forecast\ Accuracy = \frac{Actual\ Calls}{Forecasted\ Calls}

This metric measures the accuracy of predicted call volumes.

6. Implementation Workflow

The system implementation follows several structured steps.

Step 1 — Data Preparation

Organize and validate the dataset using Excel.

Extract relevant information using SQL queries.

Step 2 — Data Cleaning

Handle missing data.

Remove duplicates.

Standardize data formats.

Step 3 — Feature Engineering

Using Python and Scikit-learn to generate new analytical features such as:

Call duration groups

Agent efficiency indicators

Time-based call patterns

Step 4 — Data Modeling

Power BI is used to:

Import processed data

Create relationships between tables

Build analytical measures using DAX

Step 5 — Dashboard Development

Interactive dashboards are developed including:

KPI indicators

Trend visualizations

Interactive filters and slicers

Drill-through analysis pages

7. Key DAX Measures

The Power BI dashboard includes several calculated measures.

7.1 Call Volume Metrics

Total Calls

Total Calls =
COUNT(CallCenter[CallID])

Answered Calls

Answered Calls =
CALCULATE(
    COUNT(CallCenter[CallID]),
    CallCenter[CallStatus] = "Answered"
)

Abandoned Calls

Abandoned Calls =
CALCULATE(
    COUNT(CallCenter[CallID]),
    CallCenter[CallStatus] = "Abandoned"
)
7.2 Performance Metrics

Abandonment Rate

Abandonment Rate =
DIVIDE(
    [Abandoned Calls],
    [Total Calls],
    0
)

Average Handling Time

Average Handling Time =
AVERAGE(CallCenter[HandlingTime])
7.3 Forecast Performance

Forecast Accuracy

Forecast Accuracy =
DIVIDE(
    SUM(CallCenter[ActualCalls]),
    SUM(CallCenter[ForecastCalls]),
    0
)
7.4 Customer Satisfaction

CSAT Score

CSAT Score =
AVERAGE(CallCenter[CustomerSatisfaction])
8. Technologies Used
Technology	Purpose
Power BI	Dashboard development and visualization
Python	Data cleaning and preprocessing
Pandas / NumPy	Data manipulation
Scikit-learn	Feature engineering
SQL	Data extraction and querying
Excel	Data preparation
Tableau	Additional visualization exploration
10. Expected Insights

The analytical dashboard allows users to:

Identify high performing agents

Detect call abandonment patterns

Monitor customer satisfaction trends

Analyze call volume trends

Improve workforce planning

11. Future Enhancements

Potential future improvements include:

Predictive models for call volume forecasting

Real-time data integration

Advanced agent performance analytics
