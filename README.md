# Sales Performance & Revenue Analysis Dashboard

A data analytics project that bridges relational database storage with visual business intelligence. The workflow starts with a structured **MySQL database**, transforms the records into optimized **CSV flat files**, and compiles them into an interactive executive dashboard.

## 📊 Live Interactive Dashboard
You can interact with the fully published visualization here:  
👉 **[Tableau Public: Sales Revenue Dashboard]([https://tableau.com "Aman Kumar Tableau Dashboard"](https://public.tableau.com/app/profile/aman.kumar6183/viz/SalesRevenue_17833296877370/DashboardRevenue?publish=yes))**

---

## 🛠️ Data Pipeline & Workflow
[ Raw MySQL Dump (.sql) ] ➔ [ SQL Data Querying & ETL ] ➔ [ Flat Files (.csv) ] ➔ [ Tableau Star Schema Model ]
1. **Database Ingestion**: The project data originated inside a **MySQL** relational database engine, housing core transaction logs, regional lookup markets, and client accounts.
2. **ETL & Data Extraction**: Used structured SQL queries to filter, aggregate, and pull the transactional records into distinct table structures.
3. **Format Transformation**: Exported the records out of the database into individual **CSV flat files**. This step bypasses Tableau Public's lack of live database connections and ensures optimized data import.

---

## 📁 Dataset Schema Map
The underlying star-schema model uses five flat files cleanly extracted from the MySQL database:

* **`transactions.csv` (Fact Table)**: Tracks core financial metrics including product keys, customer markers, regional nodes, transactional counts (`sales_qty`), and localized currency denominations (`sales_amount`).
* **`customers.csv` (Dimension)**: Groups client records by account identifiers, business names, and distinct operational distribution networks (e.g., Brick & Mortar vs. E-Commerce).
* **`markets.csv` (Dimension)**: Maps regional trade hubs by physical city names and macro geographical classifications (North, South, Central).
* **`products.csv` (Dimension)**: Catalogues product lists, detailing individual stock items against classifications like "Own Brand".
* **`date.csv` (Dimension)**: Standardises fiscal calendars, enabling fluid time-series evaluation spanning years, named months, and rolling intervals.

---

## 📉 Core Analysis Goals & Modeling
* **Star Schema Implementation**: Tables are joined inside Tableau using logical relationships centered directly on the transaction fact table.
* **Currency Normalisation**: Handled inconsistent multi-currency formats during the query/import stage to enforce a singular, uniform financial ledger.
* **Volume Analysis**: Isolates seasonal demand variations, pinpointing underperforming regional markets and identifying top consumer accounts.

  

