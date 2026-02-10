# Smart-MRP-Inventory-Management-System

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Tool](https://img.shields.io/badge/Tool-MS_Excel-blue)
![Process](https://img.shields.io/badge/Process-ETL_|_MRP_|_Inventory-red)

## 🎯 Overview
This project is an automated **Material Requirements Planning (MRP)** system built entirely within Excel using **Power Query**. It bridges the gap between production planning and warehouse management by calculating real-time material shortages based on active work orders and Bill of Materials (BOM).

---

## 🛠 How It Works (The Logic)
I developed a relational data model that connects three separate data silos:
1. **Work Orders:** Active production targets and quantities.
2. **BOM (Bill of Materials):** Multi-level product recipes mapped by version.
3. **Inventory:** Real-time stock levels and warehouse data.

### 🔄 The ETL Process (Power Query)
* **Data Merging:** Connected `WorkordersAndMaterials`, `BOM_VERSIONS`, and `STOK` tables using unique Part Numbers and Version IDs.
* **Dynamic Calculation:** Created a calculated column for `Required Amount` by multiplying `Production Quantity` x `BOM Usage Unit`.
* **Inventory Gap Analysis:** Automated the calculation of `Remaining Stock` and `Stock Coverage Percentage`.

---

## 📊 Key Features & Visuals
### 1. Automated Stock Status
The system categorizes stock health into three visual alerts:
- ⚪ **STOK YOK (Out of Stock):** No physical inventory available in the warehouse.
- 🔴 **STOK YETERSİZ (Critical):** Immediate action required (Shortage).
- 🟠 **STOK BİTMEK ÜZERE (Critical Level):** Stock is available but will reach zero shortly (Running low).
- 🟡 **STOK YARIDA (Warning):** Low stock level.
- 🟢 **STOK YETERLİ (Healthy):** Sufficient for production.


> ![Stock Analysis Screenshot](./stok_analiz_dashboard.png) 
> *Caption: Real-time inventory status mapping with conditional formatting.*

### 2. Data Pipeline
By utilizing **Applied Steps** in Power Query, the report refreshes with a single click whenever a new work order or stock update is received.

---

## 📈 Business Impact
- **Risk Mitigation:** Identifies shortages before production begins, preventing costly downtime.
- **Efficiency:** Replaced manual Excel lookups with an automated ETL pipeline, reducing reporting time by 90%.
- **Decision Support:** Provides purchasing teams with precise "Net Requirement" data.

---
**Author:** [Nilay Özel]

**Connect with me:** [https://www.linkedin.com/in/nilay-%C3%B6zel-2927a7210/]
