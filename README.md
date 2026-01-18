2. Retail Sales Performance Analysis 

Power BI | SQL | DAX | Star Schema Modeling

Project Overview :
This project analyzes large-scale retail sales data to evaluate sales performance, unit trends, and store productivity using a star-schema data model.
The focus is on accurate time-grain analysis, clean modeling, and business-ready KPIs suitable for decision-making and interviews.

Business Objectives:
   - Understand overall sales and unit movement
   - Analyze monthly sales trends at the correct date grain
   - Compare store-level productivity
   - Enable scalable analysis using fact–dimension modeling

Data Model (Star Schema):
The model follows a classic star schema for performance and clarity.
Fact Table
   - fact_sales
   - units_sold
   - sales_value
   - item_id
   - store_id
   - d (day key)
Dimension Tables
   - dim_date → calendar attributes (year, month, month-year)
   - dim_item → product/category hierarchy
   - dim_store → store and state details

✔ Power BI auto date hierarchy disabled
✔ Single-direction relationships
✔ One-to-many joins from dimensions to fact


Data Engineering & Processing :
   - Raw sales data reshaped from wide to long format using Python (Pandas melt)
   - Cleaned and loaded into SQL Server
   - Fact and dimension tables created using SQL
   - Indexed fact table for query performance
   - Connected SQL Server to Power BI for reporting

Key KPIs & Metrics (DAX) :
   - Total Sales Value
   - Total Units Sold
   - Average Daily Units
   - Store Productivity (Sales per Store)
   - Monthly Sales Trend (correct time grain)
 MoM / YoY % intentionally excluded to avoid misleading aggregation on sparse retail data.

Dashboard Highlights :
   - KPI cards for Sales, Units, Productivity
   - Monthly trend line using custom date dimension
   - Store-wise and category-wise performance views
   - Clean layout optimized for recruiter review

Key Insights :
   - Sales are highly seasonal, with clear monthly fluctuations
   - A small number of stores contribute disproportionately to revenue
   - Unit volume trends do not always correlate linearly with sales value

Tools & Technologies :
   - Power BI – Data modeling & visualization
   - SQL Server – Fact & dimension storage
   - Python (Pandas) – Data transformation
   - DAX – KPI calculations
   - Power Query – Data shaping

Repository Structure :
Project_2_Walmart/
│
├── 1_raw/                # Original datasets
├── 2_processed/          # Transformed fact data
├── 3_scripts/            # Python ingestion & SQL load scripts
├── sql/                  # Table creation & indexing scripts
├── powerbi/              # .pbix dashboard
└── README.md

Why This Project Matters :
   - Demonstrates real-world data modeling, not just charts
   - Shows control over time intelligence pitfalls
   - Built for interview discussion, not cosmetic dashboards
   - Scales well for large datasets (~30M+ rows)

Dashboard Preview : 

(Add screenshots here — very important for recruiters)

👤 Author

Teja Tejavath
Data Analyst | SQL • Power BI • Python
📍 Hyderabad, India
