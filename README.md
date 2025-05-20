# 📡 Monitor a Data Warehouse in Microsoft Fabric

## 🎯 Purpose
The purpose of this lab is to explore how to monitor a data warehouse in Microsoft Fabric. It demonstrates how to use **Dynamic Management Views (DMVs)** and **Query Insights** to observe activity such as connections, sessions, and queries within the data warehouse environment.

---

## 🛠️ Steps

### 1. Create a Workspace
- Navigated to the Microsoft Fabric homepage and signed in.
- Created a new workspace with Fabric trial or capacity enabled.

### 2. Create a Sample Data Warehouse
- From the menu, selected **Create > Sample Warehouse** and created a data warehouse named `sample-dw`.
- The warehouse was automatically populated with sample data for taxi ride analysis.

### 3. Use Dynamic Management Views (DMVs)
- Executed SQL queries on:
  - `sys.dm_exec_connections` to view connection details.
  - `sys.dm_exec_sessions` to view session details.
  - `sys.dm_exec_requests` to view current running requests.
- Joined all three DMV tables to analyze currently running queries in the database.
- Launched a long-running query using `WHILE 1 = 1 SELECT * FROM Trip;` in a new tab.
- Monitored that long-running query in the original DMV query tab and observed changes in elapsed time.
- Canceled the running query and verified that it no longer appeared in the DMV results.

### 4. Explore Query Insights
- Used the `queryinsights.exec_requests_history` view to analyze previously executed queries.
- Queried `frequently_run_queries` to identify the most commonly executed queries.
- Used `long_running_queries` to identify the queries with the longest execution durations.

---

## 📘 What I Learned

- Gained hands-on experience using **Dynamic Management Views (DMVs)** to monitor data warehouse activity.
- Learned how to track active connections, sessions, and running queries in Microsoft Fabric.
- Practiced joining DMVs to write more insightful monitoring queries.
- Explored **Query Insights** to analyze historical query performance.
- Understood how monitoring tools in Fabric can help with query optimization and performance tuning.
- Improved my familiarity with the Microsoft Fabric interface and its SQL-based monitoring tools.

---

🔗 *This lab provided foundational experience in monitoring, performance analysis, and query diagnostics for data engineering workflows using Microsoft Fabric.*

---

## Screenshots

<img width="1400" alt="1" src="https://github.com/user-attachments/assets/66dcba30-6d1a-479e-bd6b-0c635bc68c7e" />

<img width="1409" alt="2" src="https://github.com/user-attachments/assets/9c201a9a-2dd1-4d65-bab3-50d1d4590f70" />

<img width="1144" alt="4" src="https://github.com/user-attachments/assets/eaf2ac64-04bb-41ca-aa56-c084bc4ff0f1" />

<img width="1262" alt="5" src="https://github.com/user-attachments/assets/08c7d253-8a10-4b11-a536-70ebabd9d187" />

<img width="912" alt="6" src="https://github.com/user-attachments/assets/1c8f20bd-3a27-42bb-8f33-e36e677b592d" />

<img width="1162" alt="7" src="https://github.com/user-attachments/assets/58928d9c-ac55-493b-9f47-bf4eebc56c8c" />

<img width="1145" alt="8" src="https://github.com/user-attachments/assets/db381a2d-19ea-4f9c-a32c-da82788e7bdb" />
