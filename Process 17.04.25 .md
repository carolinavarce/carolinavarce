

---

## 📊 Pipeline ETL con Python y Apache Airflow

Este proyecto implementa un pipeline ETL (Extract, Transform, Load) simple utilizando scripts de Python gestionados por Apache Airflow. Actualmente, el flujo de trabajo ya está operativo y visualizable desde la interfaz web de Airflow.

### ✅ Estado actual

El DAG llamado `etl_pipeline` incluye tres tareas principales:

- `extract_data`: Extrae datos desde un archivo local (`empleados.csv`).
- `transform_data`: Realiza transformaciones simples sobre los datos extraídos.
- `load_data`: Carga o guarda los datos transformados.

Este flujo ya ha sido probado y ejecutado correctamente desde Apache Airflow.

### 📁 Estructura del proyecto

```
etl-pipeline/
│
├── data/
│   └── empleados.csv
│
├── dags/
│   └── etl_pipeline_dag.py
│
├── scripts/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
│
└── airflow_venv/
```

### ▶️ Cómo ejecutar

1. **Activar el entorno virtual**:
   ```bash
   source ~/airflow_venv/bin/activate
   ```

2. **Iniciar la base de datos de Airflow** (solo una vez):
   ```bash
   airflow db migrate
   ```

3. **Ejecutar el scheduler y el servidor web**:
   ```bash
   airflow scheduler
   airflow webserver --port 8080
   ```

4. **Acceder desde el navegador**:
   [http://localhost:8080](http://localhost:8080)

---

## 🛠️ Próximas mejoras

Ya puedes empezar a incorporar:

- ✅ **Lectura desde una API real** en `extract_api.py`.
- ✅ **Validaciones automáticas** con `Great Expectations` o `PyTest`.
- ✅ **Exportación a base de datos** PostgreSQL o SQLite.
- ✅ **Exportación a archivo final `.csv` o `.json`**.
- ✅ **Monitoreo y logging con Airflow o herramientas externas.**

---

## 📊 ETL Pipeline with Python and Apache Airflow

This project implements a simple ETL (Extract, Transform, Load) pipeline using Python scripts orchestrated by Apache Airflow. The workflow is now running and visualizable from the Airflow web UI.

### ✅ Current Status

The DAG named `etl_pipeline` includes three main tasks:

- `extract_data`: Extracts data from a local file (`empleados.csv`).
- `transform_data`: Applies simple transformations to the extracted data.
- `load_data`: Loads or saves the transformed data.

This workflow has been successfully tested and run inside Apache Airflow.

### 📁 Project structure

```
etl-pipeline/
│
├── data/
│   └── empleados.csv
│
├── dags/
│   └── etl_pipeline_dag.py
│
├── scripts/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
│
└── airflow_venv/
```

### ▶️ How to run it

1. **Activate the virtual environment**:
   ```bash
   source ~/airflow_venv/bin/activate
   ```

2. **Initialize the Airflow database** (only once):
   ```bash
   airflow db migrate
   ```

3. **Start the scheduler and webserver**:
   ```bash
   airflow scheduler
   airflow webserver --port 8080
   ```

4. **Access in your browser**:
   [http://localhost:8080](http://localhost:8080)

---

## 🛠️ Next Improvements

You can now integrate:

- ✅ **Reading data from a real API** in `extract_api.py`.
- ✅ **Data validation** with `Great Expectations` or `PyTest`.
- ✅ **Data loading into PostgreSQL or SQLite.**
- ✅ **Exporting transformed data to `.csv` or `.json`.**
- ✅ **Monitoring and logging via Airflow or external tools.**
