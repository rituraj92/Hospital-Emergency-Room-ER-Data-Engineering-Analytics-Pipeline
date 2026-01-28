📌 Project Overview
This project demonstrates the design and implementation of an end-to-end data engineering pipeline for hospital emergency room operations using Excel as the analytics layer.
The focus is on ETL automation, data modeling, and metric reliability, culminating in an interactive dashboard for operational decision-making.The project simulates how raw 
clinical data is transformed into a structured analytical model suitable for reporting and KPI tracking.

🏗️ Data Engineering Architecture
Raw CSV Data---Bronze layer
     ↓
Power Query (ETL)---Silver layer
     ↓
Cleaned & Modeled Tables----Silver layer
     ↓
Power Pivot Data Model (Star Schema)------Silver layer
     ↓
DAX Metrics Layer-----Gold layer
     ↓
Executive Dashboard----Gold layer

🔄 ETL Pipeline (Power Query)
Data Extraction
Connected to raw CSV data sources.
Designed queries to support schema evolution and refresh safety.
Data Transformation
Removed duplicates and handled missing/null values.
Standardized categorical fields (e.g., gender normalization).
Engineered derived attributes such as patient age and visit duration.
Consolidated fragmented patient identifiers into a unified key.
Data Load
Loaded curated tables into Power Pivot for analytical modeling.
Ensured type consistency and refresh-safe transformations.

🧩 Data Modeling (Power Pivot)

Designed a Star Schema for analytics:
Fact Table: ER Visits
Dimension Tables: Calendar, Patient Demographics
Built a custom Calendar Dimension to support:
Time-series analysis
Month-over-month and trend comparisons
Enforced one-to-many relationships to guarantee metric accuracy.

📐 Analytics & Business Logic (DAX)

Implemented reusable DAX measures:
Total ER Visits
Average Patient Wait Time
On-Time vs Delayed Visit Classification
Patient Satisfaction KPIs
Centralized business logic at the model level to ensure:
Consistent metric definitions
Scalable dashboard expansion

📊 Key Insights Generated

Identified peak admission periods and seasonal demand patterns.
Tracked operational efficiency through average wait-time trends.
Analyzed patient demographics to uncover age and gender distributions.
Monitored service quality using satisfaction score metrics.

🧰 Tech Stack

Excel – Analytics & visualization layer
Power Query – ETL & data transformation
Power Pivot – Data modeling
DAX – Metrics & business logic
