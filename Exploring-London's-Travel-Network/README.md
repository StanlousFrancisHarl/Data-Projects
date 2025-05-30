# 🚇 Exploring London's Travel Network

This project uses **SQL** to explore and analyze **Transport for London (TfL)** journey data spanning over **12 years** (2010–2022). Leveraging multiple cloud data warehouse options—**Snowflake**, **Amazon Redshift**, **Google BigQuery**, and **Databricks SQL**—this guided project demonstrates real-world querying of large-scale urban mobility data using SQL.

---

## 📌 Project Overview

**Dataset Source**: `TFL.JOURNEYS`  
**Time Range**: 2010 – 2022  
**Cloud Warehouses Supported**:  
- 🧊 **Snowflake**  
- 🟥 **Amazon Redshift**  
- 🟦 **Google BigQuery**  
- 🟧 **Databricks SQL**

**Platform**: [DataCamp Guided Projects](https://app.datacamp.com)  
**Project Type**: SQL-Based Exploratory Analysis  
**Skill Level**: Intermediate SQL  

---

## 🔍 Project Objectives & Queries

### 1. 🔝 Most Popular Transport Types  
Find transport types with the **highest total journeys**.

- **Columns Returned**:
  - `JOURNEY_TYPE`
  - `TOTAL_JOURNEYS_MILLIONS`
- **Sorting**: Descending order of journey volume
- **Save As**: `most_popular_transport_types`

---

### 2. ✈️ Emirates Airline Monthly Trends  
Identify the **five peak months and years** for **Emirates Airline** journeys.

- **Columns Returned**:
  - `MONTH`
  - `YEAR`
  - `ROUNDED_JOURNEYS_MILLIONS` (rounded to two decimal places)
- **Filters**: Exclude NULLs
- **Ordering**: 
  1. By `ROUNDED_JOURNEYS_MILLIONS` (DESC)
  2. By `YEAR` (ASC)
- **Save As**: `emirates_airline_popularity`

---

### 3. 🚇 Least Popular Years for Underground & DLR  
Find **five years with the lowest journey volume** on **Underground & DLR**.

- **Columns Returned**:
  - `YEAR`
  - `JOURNEY_TYPE`
  - `TOTAL_JOURNEYS_MILLIONS`
- **Save As**: `least_popular_years_tube`

---

## 🛠️ SQL Syntax Guidelines by Platform

| Platform        | Table Reference Syntax                     | Special Notes                                                                 |
|----------------|---------------------------------------------|--------------------------------------------------------------------------------|
| **Snowflake**   | `FROM TFL.JOURNEYS`                        | Use uppercase schema and table names.                                          |
| **Redshift**    | `FROM tfl.journeys`                        | Use lowercase and schema-qualified table names.                               |
| **BigQuery**    | `FROM TFL.JOURNEYS`                        | Uppercase required; same as Snowflake.                                        |
| **Databricks**  | `FROM tfl.journeys`                        | Must use original column names in `WHERE` (aliases not supported).            |

---

## 🧠 Skills Demonstrated

- SQL Aggregation (`SUM`)
- Filtering and NULL handling
- Aliasing and rounding (`ROUND(...) AS`)
- Ordering results by multiple columns
- Schema-based querying in cloud data platforms
- Data storytelling from real-world public datasets

---

## 📁 Folder Structure

London_Travel_Network_SQL_Project_Portfolio_Stanlous/
│
├── screenshots/
│ ├── project_overview.png
│ ├── query_1_most_popular_transport.png
│ ├── query_2_emirates_airline.png
│ ├── query_3_least_popular_years.png
│
├── README.md
└── Exploring_London_Travel_Network_SQL_Stanlous.pdf

yaml
Copy
Edit

---

## 📄 License
This project was built as a guided exercise on DataCamp. Educational purpose only.

---

## 🙋‍♂️ Author
**Stanlous Francis Harley**  
Data Analyst | BI & SQL Enthusiast  
[LinkedIn Profile](#) *(https://www.linkedin.com/in/stanlous-francis-harley-047a31230/)*  
