# ETL Pipeline – Data Cleaning & Transformation

This project is part of the portfolio for the Data Engineer position at Inception. It demonstrates the creation of a basic ETL (Extract, Transform, Load) pipeline using Python and Pandas.

## 🚀 Objective

Implement a functional ETL pipeline to:

- Extract data from a CSV file
- Apply transformations and cleaning
- Store the processed data in a clean CSV file

## 🛠️ Tech Stack

- **Python 3**
- **Pandas**
- **Virtual Environment** (airflow_venv)
- *(Optional)* Great Expectations (for future validation)

## 📂 Project Structure

```
etl-pipeline/
├── data/
│   ├── empleados.csv
│   ├── temp_data.csv
│   └── empleados_limpios.csv
├── scripts/
│   ├── extract.py
│   └── transform.py
├── requirements.txt
└── README.md
```

## 🔧 How to Run Locally

### 1. Activate Virtual Environment

```bash
source ~/airflow_venv/bin/activate
```

> ⚠️ If the environment is not created, run:
> ```bash
> python3 -m venv ~/airflow_venv
> ```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

> For data validation (optional):
> ```bash
> pip install great_expectations
> ```

### 3. Run Scripts

```bash
cd ~/etl-pipeline/scripts

python extract.py
python transform.py
```

## 📊 Data

The `empleados.csv` file contains synthetic employee data. The pipeline detects and handles:

- Null values
- Duplicates
- Type mismatches
- Outliers (WIP)

## 👤 Author

**Carolina Vargas Arce**

- [GitHub](https://github.com/carolinavarce/carolinavarce)
- [LinkedIn](https://www.linkedin.com/in/carolinavargasarce)

---

This repository is part of a larger portfolio showcasing Data Engineering skills for real-world business and AI scenarios.
