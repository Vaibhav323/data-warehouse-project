# 🧠 Data Warehouse Project

  

A complete **end-to-end Data Warehouse system** designed and implemented using **SQL Server**.  

This project demonstrates data integration from multiple sources (CRM and ERP), applying ETL logic across **Bronze → Silver → Gold** layers, and building analytical models following **Star Schema design**.

  

---

  

## 📘 Overview

  

The project simulates a real-world business scenario where data is collected from **two operational systems**:

- A **CRM system** containing customer and sales information  

- An **ERP system** containing product and location master data  

  

The objective is to:

1. Ingest this raw data into a warehouse.  

2. Clean, integrate, and standardize it using ETL processes.  

3. Build analytical models for reporting and insights.  

  

---

  

## 🏗️ Data Flow Architecture

 

### ETL Flow

1. **Bronze Layer (Raw Zone)**  

   - Stores raw data ingested from CRM and ERP CSVs.  

   - Focus on preserving original structure and lineage.  

  

2. **Silver Layer (Refined Zone)**  

   - Cleans and harmonizes CRM + ERP data.  

   - Applies business rules, joins, and data standardization.  

  

3. **Gold Layer (Analytics Zone)**  

   - Star schema built for reporting and BI tools.  

   - Consists of fact and dimension tables for analysis.  

  

---

  

## 📂 Repository Structure

  

```

data-warehouse-project/
│
├── datasets/                     # Raw data from CRM and ERP
│   ├── source_crm/
│   │   ├── cust_info.csv         # Customer master from CRM
│   │   ├── prd_info.csv          # Product information from CRM
│   │   └── sales_details.csv     # Sales transactions from CRM
│   └── source_erp/
│       ├── CUST_AZ12.csv         # Customer data from ERP
│       ├── LOC_A101.csv          # Location mapping data
│       └── PX_CAT_G1V2.csv       # Product category and pricing info
│
├── docs/
│   ├── Data Architecture.png     # High-level warehouse architecture
│   ├── Data Integration.png      # Data flow / ETL pipeline diagram
│   ├── Star Schema.png           # Final gold model star schema
│   ├── data_catalog.md           # Table and field-level documentation
│   └── naming_conventions.md     # Naming and design guidelines
│
├── scripts/
│   ├── init_database.sql         # Creates initial database & schemas
│   │
│   ├── bronze/
│   │   ├── ddl_bronze.sql        # Table definitions for raw layer
│   │   └── proc_load_bronze.sql  # Procedures to load CSV data
│   │
│   ├── silver/
│   │   ├── ddl_silver.sql        # Table definitions for refined data
│   │   └── proc_load_silver.sql  # Transformation and join logic
│   │
│   └── gold/
│       └── ddl_gold.sql          # Star schema DDL (fact + dimension)
│
└── tests/
    ├── quality_checks_silver.sql # Data quality checks after transformation
    └── quality_check_gold.sql    # Referential and integrity tests for gold layer

```

  

---

  

## 🧩 Documentation

  

- **[`docs/data_catalog.md`](docs/data_catalog.md)** → Detailed description of each table, column, and business rule.  

- **[`docs/naming_conventions.md`](docs/naming_conventions.md)** → Naming standards for schemas, tables, columns, and stored procedures.  

- **Architecture Diagrams** → Explain how data moves across layers and how the star schema is structured.

  

---

  

## 📊 Key Concepts Demonstrated

  

- ETL (Extract → Transform → Load)  

- Multi-source data integration  

- Schema design (3NF → Dimensional)  

- Data quality and validation  

- SQL automation via stored procedures  

- Star schema modeling for BI  

  

---

  

## 🧠 Skills Showcased

  

- SQL Server scripting (DDL, DML, stored procedures)

- Data modeling & architecture

- Data pipeline design

- ETL orchestration logic

- Documentation and data governance practices

  

---

  

## 🧪 Future Enhancements

  

- Add incremental load logic (CDC or timestamp-based).  

- Automate execution using Python or Airflow.  

- Connect the gold layer to a BI tool like **Tableau** or **Power BI**.  

- Add data lineage tracking and audit tables.

  
---

### 🙌 Credits

I learned and understood core data warehousing concepts through tutorials from the **[Data with Baraa - YouTube](https://www.youtube.com/@DataWithBaraa)**, which helped me design and implement this project independently.

---
