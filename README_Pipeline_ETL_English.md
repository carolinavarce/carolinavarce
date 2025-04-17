# 📌 ETL Pipeline with Data Integration and API Extraction

## 📢 Description
This project implements an ETL pipeline (Extract, Transform, Load) that gathers data from multiple sources (local files and REST APIs), transforms and validates it, and loads it into a centralized PostgreSQL database. The objective is to build an automated and scalable data pipeline using modern orchestration, storage, and validation tools.

## 🎯 Objectives

✅ Extract data from:
- REST APIs
- CSV/JSON files
- SQL Databases

✅ Transform and validate:
- Data cleaning using Pandas
- Check types, nulls, duplicates
- Prepare for structured storage

✅ Load data into:
- PostgreSQL tables (structured)
- Clean JSON/CSV files

✅ Automate with Apache Airflow

✅ Ensure data quality using Great Expectations

---

## 🛠️ Tech Stack

- **Language**: Python 3
- **Processing**: Pandas, SQLAlchemy, requests
- **Storage**: PostgreSQL, CSV
- **Validation**: Great Expectations
- **Orchestration**: Apache Airflow
- **Virtual environment**: airflow_venv
- **Version control**: GitHub
- *(Optional)*: Docker, Azure Data Lake

---

## 🏗️ Project Architecture

1. **Extraction**
   - Read from CSV files (`empleados.csv`)
   - Call REST APIs to retrieve JSON data
   - (Future) Connect to SQL databases

2. **Transformation**
   - Clean columns and rows
   - Convert data types
   - Filter outliers
   - Prepare final clean structures

3. **Loading**
   - Insert into PostgreSQL tables (`raw_data`, `processed_data`)
   - Intermediate storage in CSV files

4. **Automation**
   - Pipeline orchestrated using Airflow DAGs
   - Logging and error handling

5. **Data Validation**
   - Custom validations using Great Expectations
   - Unit testing with PyTest

---

## 📂 Project Structure

```
etl-pipeline/
├── data/
│   ├── empleados.csv
│   ├── api_data.json
│   ├── temp_data.csv
│   └── empleados_limpios.csv
├── scripts/
│   ├── extract.py
│   ├── extract_api.py
│   ├── transform.py
│   └── load.py
├── tests/
│   └── test_transform.py
├── dags/
│   └── dag_airflow.py
├── requirements.txt
└── README.md
```

---

## 🔧 How to Run Locally

### 1. Create virtual environment

```bash
python3 -m venv ~/airflow_venv
```

### 2. Activate virtual environment

```bash
source ~/airflow_venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run pipeline scripts

```bash
cd ~/etl-pipeline/scripts

python extract.py         # Extracts from CSV
python extract_api.py     # Extracts from REST API
python transform.py       # Cleans and transforms
python load.py            # Loads into PostgreSQL
```

> You can also orchestrate the entire pipeline using an Airflow DAG if configured.

---

## 📊 Expected Results

- Data integrated from multiple sources
- Successfully transformed and validated
- `raw_data` and `processed_data` tables populated in PostgreSQL
- Automation enabled via Airflow
- Quality checks passed via Great Expectations

---

## 💡 Next Steps

🔹 Add Spark for large-scale processing  
🔹 Deploy to cloud (Azure or AWS)  
🔹 Connect to dashboards (Power BI, Grafana)  
🔹 Add data versioning (Delta Lake)

---

🛠️ **Author:** Carolina Vargas Arce  
📅 **Created:** March 2025  
🔗 **GitHub Repository:** [https://github.com/carolinavarce/carolinavarce](https://github.com/carolinavarce/carolinavarce)
