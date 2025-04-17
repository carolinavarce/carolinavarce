# 📌 Pipeline ETL con Integración de Datos y Extracción desde API

## 📢 Descripción
Este proyecto implementa un pipeline ETL (Extract, Transform, Load) para extraer datos de múltiples fuentes (archivos locales y API REST), transformarlos, validarlos y cargarlos en una base de datos centralizada. El objetivo es construir un flujo de datos automatizado y escalable utilizando herramientas modernas de orquestación, almacenamiento y validación.

## 🎯 Objetivos

✅ Extraer datos desde:
- APIs REST
- Archivos CSV/JSON
- Bases de datos SQL

✅ Transformar y validar los datos:
- Limpieza con Pandas
- Validación de tipos, nulos y duplicados
- Preparación para carga masiva

✅ Cargar datos en:
- Base de datos PostgreSQL (estructurada)
- Archivos transformados (JSON/CSV limpios)

✅ Automatizar el flujo con Apache Airflow

✅ Validar la calidad del dato con Great Expectations

---

## 🛠️ Tech Stack

- **Lenguaje**: Python 3
- **Procesamiento**: Pandas, SQLAlchemy, requests
- **Almacenamiento**: PostgreSQL, CSV
- **Validación**: Great Expectations
- **Orquestación**: Apache Airflow
- **Entorno virtual**: airflow_venv
- **Control de versiones**: GitHub
- *(Opcional)*: Docker, Azure Data Lake

---

## 🏗️ Arquitectura del Proyecto

1. **Extracción (Extract)**
   - Lectura de archivos CSV (`empleados.csv`)
   - Llamadas a API REST para recoger datos JSON
   - Conexión a bases de datos SQL (futuro)

2. **Transformación (Transform)**
   - Limpieza de columnas y filas
   - Conversión de tipos de datos
   - Filtrado de outliers
   - Preparación de estructuras limpias

3. **Carga (Load)**
   - Inserción en tablas PostgreSQL (`raw_data`, `processed_data`)
   - Almacenamiento intermedio en archivos CSV

4. **Automatización**
   - Pipeline orquestado con Airflow y DAGs
   - Logs y manejo de errores

5. **Validación de Datos**
   - Validaciones personalizadas con Great Expectations
   - Pruebas unitarias con PyTest

---

## 📂 Estructura del Proyecto

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

## 🔧 Instrucciones para Ejecutar Localmente

### 1. Crear entorno virtual

```bash
python3 -m venv ~/airflow_venv
```

### 2. Activar entorno virtual

```bash
source ~/airflow_venv/bin/activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Ejecutar scripts del pipeline

Primero tenemos activado el entorno virtual: 

source ~/airflow_venv/bin/activate


```bash
cd ~/etl-pipeline/scripts

python extract_api.py       # Extrae datos desde una API REST y guarda un CSV
python extract.py           # Extrae datos desde un CSV/JSON ya existente
python transform.py         # Limpia y transforma los datos
python load.py              # Carga los datos a PostgreSQL



---

## 📊 Resultados Esperados

- Datos integrados desde múltiples fuentes
- Transformaciones realizadas y validadas
- Tablas `raw_data` y `processed_data` en PostgreSQL
- Carga automatizada vía Airflow
- Validaciones exitosas con Great Expectations

---

## 💡 Siguientes Pasos

🔹 Añadir procesamiento con Apache Spark para grandes volúmenes  
🔹 Desplegar en la nube con Azure o AWS  
🔹 Conectar el flujo con dashboards interactivos como Power BI o Grafana  
🔹 Incluir control de versiones de datos con Delta Lake

---

🛠️ **Autor:** Carolina Vargas Arce  
📅 **Fecha de Creación:** Marzo 2025  
🔗 **Repositorio GitHub:** [https://github.com/carolinavarce/carolinavarce](https://github.com/carolinavarce/carolinavarce)
