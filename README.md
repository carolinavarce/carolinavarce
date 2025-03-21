# 📌 Pipeline ETL con Integración de Datos

## 📢 Descripción
Este proyecto implementa un pipeline ETL (Extract, Transform, Load) para extraer datos de varias fuentes, transformarlos y cargarlos en una base de datos centralizada. El objetivo es construir un flujo de datos automatizado y escalable utilizando herramientas de procesamiento de datos.

## 🎯 Objetivos
✅ Extraer datos de diferentes fuentes (APIs, bases de datos SQL, archivos CSV/JSON)
✅ Limpiar, transformar y validar los datos para asegurar calidad y coherencia
✅ Cargar los datos en un Data Warehouse o base de datos optimizada
✅ Automatizar el proceso utilizando Apache Airflow
✅ Implementar validaciones de calidad con Great Expectations

## 🛠️ Tech Stack
- **Lenguaje**: Python
- **Orquestación**: Apache Airflow
- **Almacenamiento**: PostgreSQL, Azure Data Lake
- **Procesamiento**: Pandas, SQLAlchemy
- **Validación**: Great Expectations
- **Herramientas auxiliares**: Docker, GitHub Actions

## 🏗️ Arquitectura del Proyecto
1. **Extracción (Extract)**
   - Obtención de datos desde APIs REST
   - Lectura de datos desde archivos CSV/JSON
   - Conexión a bases de datos SQL
2. **Transformación (Transform)**
   - Limpieza de datos con Pandas
   - Validaciones de tipos y valores nulos
   - Agregación y filtrado de datos relevantes
3. **Carga (Load)**
   - Inserción de datos en PostgreSQL
   - Almacenamiento en Azure Data Lake
   - Creación de tablas optimizadas para consultas
4. **Automatización**
   - Definición de DAGs en Apache Airflow
   - Monitorización de tareas y manejo de errores
5. **Validación de Datos**
   - Uso de Great Expectations para garantizar calidad de datos
   - Pruebas unitarias con PyTest

## 🚀 Desarrollo del Proyecto
### 1️⃣ Configurar el entorno
- Instalación de dependencias con `pip install -r requirements.txt`
- Configuración de variables de entorno para conexiones
- Creación de base de datos en PostgreSQL

### 2️⃣ Implementar el pipeline ETL
- Desarrollo de scripts de extracción en Python
- Transformaciones con Pandas
- Inserción de datos en PostgreSQL
- Creación de DAGs en Apache Airflow

### 3️⃣ Validación y pruebas
- Pruebas unitarias con PyTest
- Validaciones con Great Expectations
- Evaluación de calidad de datos

### 4️⃣ Documentación y despliegue
- Creación de README detallado
- Publicación en GitHub
- Configuración de CI/CD con GitHub Actions

## 📂 Estructura del Proyecto
```
project-root/
│── etl_pipeline/
│   ├── extract.py
│   ├── transform.py
│   ├── load.py
│   ├── validations.py
│   ├── dag_airflow.py
│── data/
│   ├── raw_data.csv
│── tests/
│   ├── test_transform.py
│── Dockerfile
│── requirements.txt
│── README.md
```

## 📊 Resultados Esperados
🔹 Pipeline ETL funcionando con datos extraídos, transformados y cargados
🔹 Datos limpios y estructurados listos para análisis
🔹 Automatización con Airflow para ejecutar tareas periódicamente
🔹 Validaciones que aseguran la calidad y fiabilidad del dataset

## 💡 Siguientes Pasos
🔹 Optimizar tiempos de procesamiento con Apache Spark
🔹 Implementar una API para consulta de datos
🔹 Incluir dashboard de monitoreo con Grafana

---
🛠️ **Autor:** Carolina Vargas Arce  
📅 **Fecha de Creación:** Marzo 2025  
🔗 **Repositorio GitHub:** [[Enlace al repo](https://github.com/carolinavarce/carolinavarce/blob/main/README.md#-siguientes-pasos)]

