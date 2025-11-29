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

🔧 3. Technologies Used
Purpose	Technologies
Data Ingestion	Python (requests, json, sched)
Processing	Pandas, PyArrow
Storage	Local Data Lake (CSV/Parquet)
Orchestration (optional)	Apache Airflow
Visualization	Power BI / Grafana
Version Control	Git + GitHub

📥 4. Data Sources
Traffic Data APIs
TomTom Traffic
OpenTraffic APIs
Simulated JSON generator
Air Quality APIs
OpenAQ
IQAir AirVisual API
Government AQI open data

⚙️ 5. How to Run the Pipeline
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

📊 6. Dashboard Insights
The final BI dashboard includes:
Traffic congestion heatmaps
PM2.5 / PM10 pollution trends
Correlation analysis chart
AQI vs Traffic volume scatter plot
Hourly / daily insights

🧪 7. Future Enhancements
Replace Python ingestion with Kafka streaming
Move data lake to cloud (AWS S3 / GCP Storage)
Add dbt for transformation
Build a real-time dashboard with Grafana & TimescaleDB
Deploy Airflow on Docker

👤 8. Author

Le Van Minh
Smart City – Traffic & Air Quality Data Pipeline
Data Engineering Project
