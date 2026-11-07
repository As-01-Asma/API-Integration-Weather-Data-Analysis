# 🌦️ Open-Meteo Weather API – End-to-End ETL Pipeline

## 📑 Table of Contents

1. [Project Overview](#project-overview)
2. [Project Architecture](#project-architecture)
3. [Project Objectives](#project-objectives)
4. [Tools & Technologies](#tools-technologies)
5. [ETL Workflow](#etl-workflow)
   - [Extract – API Integration](#extract-api-integration)
   - [Transform – Data Processing](#transform-data-processing)
   - [Validate – Data Quality Checks](#validate-data-quality-checks)
   - [Export – Data Storage](#export-data-storage)
   - [Load – SQL Server Integration](#load-sql-server-integration)
6. [Dataset Overview](#dataset-overview)
7. [Source-to-Target Data Mapping](#source-to-target-data-mapping)
8. [Key Results](#key-results)
9. [Logging & Pipeline Monitoring](#logging-pipeline-monitoring)
10. [Project Files](#project-files)
11. [Future Enhancements](#future-enhancements)
12. [Author](#author)

---

<a id="project-overview"></a>
## 📌 Project Overview

This project demonstrates an end-to-end weather data ETL pipeline using Python and API integration.

The pipeline extracts hourly weather forecast data from the Open-Meteo API, transforms the JSON response into a structured Pandas DataFrame, performs data quality checks, exports the processed data, and loads it into SQL Server.

It follows the ETL process: **Extract → Transform → Validate → Load**.

---

<a id="project-architecture"></a>
## 🖼️ Project Architecture

### Weather Data ETL Pipeline – From API to Database

This architecture illustrates the complete workflow, from API data extraction and Python-based processing to database storage.

![Weather Data ETL Pipeline](weather-data-etl-pipeline.png.jpeg)

**Image filename:** `weather-data-etl-pipeline.png.jpeg`

---

<a id="project-objectives"></a>
## 🎯 Project Objectives

- Retrieve hourly weather forecast data through API integration.
- Implement automatic retries for failed API requests.
- Convert JSON responses into structured datasets.
- Process and transform data using Python and Pandas.
- Inspect dataset structure, missing values, and duplicate records.
- Implement logging and pipeline execution-time monitoring.
- Export processed data into CSV and JSON formats.
- Load weather data into SQL Server.
- Verify the records stored in the database.

---

<a id="tools-technologies"></a>
## 🛠️ Tools & Technologies

- **Programming Language:** Python
- **Data Processing:** Pandas
- **API Integration:** Requests
- **Data Source:** Open-Meteo Weather API
- **Data Formats:** JSON, CSV
- **Database:** Microsoft SQL Server
- **Database Connectivity:** PyODBC, SQLAlchemy
- **Logging & Monitoring:** Python Logging, Time
- **Development Environment:** Jupyter Notebook (Anaconda)

---

<a id="etl-workflow"></a>
## 🔄 ETL Workflow

<a id="extract-api-integration"></a>
### 1. Extract – API Integration

- Connected to the Open-Meteo Weather API.
- Retrieved hourly weather forecast data for Hyderabad, India.
- Used latitude and longitude coordinates to specify the location.
- Extracted temperature, relative humidity, wind speed, and precipitation data.
- Configured automatic retries for unsuccessful API requests.
- Used exception handling to manage API errors.

<a id="transform-data-processing"></a>
### 2. Transform – Data Processing

- Converted the API JSON response into a Pandas DataFrame.
- Structured the extracted information into rows and columns.
- Converted the time column into datetime format.
- Prepared the dataset for validation and database storage.

<a id="validate-data-quality-checks"></a>
### 3. Validate – Data Quality Checks

Performed data quality checks using Pandas:

- Inspected dataset columns and structure.
- Checked the number of rows and columns.
- Checked for missing values.
- Identified duplicate records.
- Generated descriptive statistics.
- Inspected column data types.

<a id="export-data-storage"></a>
### 4. Export – Data Storage

- Exported the original API response into JSON format.
- Exported the processed weather dataset into CSV format.

<a id="load-sql-server-integration"></a>
### 5. Load – SQL Server Integration

- Installed and configured PyODBC and SQLAlchemy.
- Connected Python to Microsoft SQL Server.
- Verified the connected database.
- Created a SQLAlchemy database engine.
- Loaded the processed weather dataset into the SQL Server table.
- Verified the number of records stored in the database.

---

<a id="dataset-overview"></a>
## 📊 Dataset Overview

The project collected hourly weather forecast data for Hyderabad, India.

| Attribute | Details |
|---|---|
| Location | Hyderabad, India |
| Latitude | 17.3850 |
| Longitude | 78.4867 |
| Forecast Period | 1 Day |
| Total Records | 24 |
| Total Columns | 5 |

### Dataset Columns

| Column | Description |
|---|---|
| time | Weather timestamp |
| temperature_2m | Temperature at 2 metres |
| relative_humidity_2m | Relative humidity |
| wind_speed_10m | Wind speed at 10 metres |
| precipitation | Precipitation amount |

---

<a id="source-to-target-data-mapping"></a>
## 🔄 Source-to-Target Data Mapping

| API Source Field | DataFrame / SQL Server Column | Data Type | Transformation |
|---|---|---|---|
| time | time | datetime | Converted to datetime format |
| temperature_2m | temperature_2m | float | Structured using Pandas |
| relative_humidity_2m | relative_humidity_2m | integer | Structured using Pandas |
| wind_speed_10m | wind_speed_10m | float | Structured using Pandas |
| precipitation | precipitation | float | Structured using Pandas |

---

<a id="key-results"></a>
## 📈 Key Results

The processed dataset contained:

- **24** hourly weather records.
- **5** structured columns.
- **0** missing values.
- **0** duplicate records.
- Successfully exported the original API response into JSON.
- Successfully exported the processed dataset into CSV.
- Successfully loaded the weather records into SQL Server.
- Verified the database record count.

---

<a id="logging-pipeline-monitoring"></a>
## 📋 Logging & Pipeline Monitoring

Implemented Python logging to track the pipeline execution.

The logging and monitoring process includes:

- Pipeline execution status.
- API data extraction status.
- Data validation status.
- Data transformation status.
- CSV and JSON export status.
- Database loading status.
- Total records processed.
- Total pipeline execution time.

A log file named `weather_pipeline.log` is generated to record pipeline activities.

---

<a id="project-files"></a>
## 📁 Project Files

| File | Description |
|---|---|
| Hyderabad_Weather_API_Data_Pipeline.ipynb | Complete Python ETL implementation |
| api_response.json | Original API response |
| hyderabad_weather_data.csv | Processed weather dataset |
| weather_pipeline.log | Pipeline execution logs |
| weather-data-etl-pipeline.png.jpeg | Project architecture visual |
| README.md | Project documentation |

---

<a id="future-enhancements"></a>
## 🚀 Future Enhancements

- Automate scheduled API data extraction.
- Extend data collection to multiple locations.
- Integrate additional weather APIs.
- Develop interactive Power BI dashboards.
- Perform weather trend analysis.

---

<a id="author"></a>
## 👩‍💻 Author

**Shaik Asmatha**

Aspiring Data Analyst | Data Science Graduate

- **GitHub:** https://github.com/As-01-Asma
- **Portfolio:** https://celadon-tartufo-fc56fc.netlify.app

---
