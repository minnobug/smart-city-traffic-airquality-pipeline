🏙️ 1. Overview
This project represents a real Smart City data pipeline that collects, processes, and analyzes:
Traffic Data (vehicle count, speed, congestion level)
Air Quality Data (PM2.5, PM10, CO, NO₂, AQI)
The primary goal is to build a complete, production-like Data Engineering pipeline that shows how traffic affects pollution levels in a city.
This project is designed for:
Data Engineering portfolio
Hands-on ETL/ELT practice
Showcasing architecture design, pipelines, analytics & dashboards

🎯 2. Project Objectives
✔ Build an end-to-end, reproducible pipeline
✔ Apply Data Lake architecture: Bronze → Silver → Gold
✔ Automate ingestion & processing with Python
✔ Analyze correlation between traffic and air pollution
✔ Build visual dashboards (Power BI / Grafana)
✔ Demonstrate production-style coding & folder structure

🏗 3. Architecture Diagram
        +------------------------------+
        | Traffic API / Air Quality API|
        +---------------+--------------+
                        |
                        v
               +-------------------+
               |   Data Ingestion  |
               |   (Python ETL)    |
               +-------------------+
                        |
                        v
        +--------------------------------------+
        |        Data Lake (Bronze Layer)      |
        | raw/traffic      raw/air_quality     |
        +--------------------------------------+
                        |
                        v
        +--------------------------------------+
        |   Cleaning & Validation (Silver)     |
        | clean_traffic   clean_air_quality    |
        +--------------------------------------+
                        |
                        v
        +--------------------------------------+
        |    Analytics Dataset (Gold Layer)     |
        | merged_traffic_airquality.parquet     |
        +--------------------------------------+
                        |
                        v
              +-------------------------+
              |     Dashboards (BI)     |
              +-------------------------+

📂 4. Repository Structure
smart-city-traffic-airquality-pipeline/
│
├── data/
│   ├── raw/
│   │   ├── traffic/
│   │   └── air_quality/
│   ├── silver/
│   └── gold/
│
├── src/
│   ├── ingestion/
│   │   ├── fetch_traffic.py
│   │   └── fetch_air_quality.py
│   ├── transformation/
│   │   └── clean_merge.py
│   ├── pipeline/
│       └── run_pipeline.py
│
├── notebooks/
│   ├── EDA_traffic.ipynb
│   ├── EDA_air_quality.ipynb
│   └── Correlation_Analysis.ipynb
│
├── dashboards/
│   └── smart_city_dashboard.pbix
│
├── docs/
│   └── architecture_diagram.png
│
├── requirements.txt
├── README.md
└── .gitignore

🔧 5. Technologies Used
Purpose	Technologies
Data Ingestion	Python (requests, json, sched)
Processing	Pandas, PyArrow
Storage	Local Data Lake (CSV/Parquet)
Orchestration (optional)	Apache Airflow
Visualization	Power BI / Grafana
Version Control	Git + GitHub

📥 6. Data Sources
Traffic Data APIs
TomTom Traffic
OpenTraffic APIs
Simulated JSON generator
Air Quality APIs
OpenAQ
IQAir AirVisual API
Government AQI open data

⚙️ 7. How to Run the Pipeline
1️⃣ Install dependencies
pip install -r requirements.txt
2️⃣ Fetch Traffic Data
python src/ingestion/fetch_traffic.py
3️⃣ Fetch Air Quality Data
python src/ingestion/fetch_air_quality.py
4️⃣ Transform & Merge Data
python src/transformation/clean_merge.py
5️⃣ Run Entire Pipeline
python src/pipeline/run_pipeline.py

📊 8. Dashboard Insights
The final BI dashboard includes:
Traffic congestion heatmaps
PM2.5 / PM10 pollution trends
Correlation analysis chart
AQI vs Traffic volume scatter plot
Hourly / daily insights

🧪 9. Future Enhancements

Replace Python ingestion with Kafka streaming
Move data lake to cloud (AWS S3 / GCP Storage)
Add dbt for transformation
Build a real-time dashboard with Grafana & TimescaleDB
Deploy Airflow on Docker

👤 10. Author

Le Minh
Smart City – Traffic & Air Quality Data Pipeline
Data Engineering Project
