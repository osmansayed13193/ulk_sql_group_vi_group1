# Kigali Retail & Savings Cooperative - SQL JOINs & Window Functions Project

## 1. Project Title
SQL Database Development and Advanced Analytical Processing Project

## 2. Group Members
* **Group:** Group VI (Data Science - Year 2, Day Session)
* **Members:**
  * Osman Nuseri — Student ID: `202513193`
  * [Group Member 2 Name] — Student ID: `[ID Number]`
  * [Group Member 3 Name] — Student ID: `[ID Number]`
  * [Group Member 4 Name] — Student ID: `[ID Number]`
  * [Group Member 5 Name] — Student ID: `[ID Number]`

## 3. Business Background
The Kigali Retail & Savings Cooperative operates across four major regions in Rwanda (Kigali, North, South, and West), providing registered members with agricultural inputs, renewable energy equipment, and financial savings services while tracking branch-level transactions and employee performance.

## 4. Problem Statement
Branch managers currently track daily sales in isolated logs without a centralized relational analytical database. Consequently, leadership lacks automated visibility into regional product demand, dormant member accounts, unsold inventory, and sequential revenue growth trends.

## 5. Project Objectives
1. **Identify Top Products per Region:** Rank products by revenue within each branch using `RANK()`.
2. **Calculate Cumulative Monthly Revenue:** Monitor financial accumulation over time using `SUM() OVER()`.
3. **Compare Sequential Transaction Performance:** Measure revenue changes between consecutive transactions using `LAG()` and `LEAD()`.
4. **Segment Customer Spending Tiers:** Divide registered members into four equal spending quartiles using `NTILE(4)`.
5. **Calculate Moving Sales Averages:** Smooth out short-term transaction volatility using a three-transaction rolling average with `AVG() OVER()`.

## 6. Database Schema & Table Descriptions
The database consists of 5 normalized relational tables:
* `branches`: Stores regional branch details and locations (`branch_id` PK).
* `employees`: Maintains staff records, branch assignments, and self-referencing managerial hierarchies (`employee_id` PK).
* `customers`: Tracks cooperative member profiles, regions, and join dates (`customer_id` PK).
* `products`: Categorizes inventory items and unit prices (`product_id` PK).
* `sales`: Records multi-table transaction logs connecting customers, employees, products, and branches (`sale_id` PK).

## 7. ER Diagram & Repository Structure
The Entity Relationship Diagram illustrating primary keys, foreign keys, and cardinalities is located at `documentation/ERD.png`. 

The public repository is organized as follows:
```text
ulk_sql_group_vi_groupX/
├── README.md
├── database/
│   ├── 01_create_tables.sql
│   ├── 02_insert_data.sql
│   └── 03_constraints.sql
├── queries/
│   ├── 01_inner_join.sql
│   ├── 02_left_join.sql
│   ├── 03_right_join.sql
│   ├── 04_full_outer_join.sql
│   ├── 05_self_join.sql
│   ├── 06_ranking_functions.sql
│   ├── 07_aggregate_window_functions.sql
│   ├── 08_navigation_functions.sql
│   └── 09_distribution_functions.sql
├── documentation/
│   └── ERD.png
└── screenshots/
    ├── joins/
    └── window_functions/
