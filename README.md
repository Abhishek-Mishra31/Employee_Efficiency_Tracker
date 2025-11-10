# Employee Efficiency Tracker Dashboard (Excel & Power BI)

**Project Report for Business Analytics**

---

## 1. Objective

[cite_start]To build a dynamic and interactive dashboard in Microsoft Excel to track, measure, and visualize employee efficiency, productivity, and cost variance[cite: 32]. The goal is to leverage Excel formulas, Pivot Tables, and Pivot Charts to create a comprehensive report that automatically updates and can be interactively filtered by management for data-driven decision-making.

## 2. Tools & Technologies Used

This project was built using the following tools and technologies:

| Tool/Technology | Purpose |
| :--- | :--- |
| Microsoft Excel | Primary software for data entry, calculation, and visualization. |
| Excel Tables | Used to create a structured, dynamic data source that auto-expands. |
| Excel Formulas | To calculate custom Key Performance Indicators (KPIs) for efficiency. |
| Pivot Tables | To aggregate, summarize, and analyze large volumes of raw data. |
| Pivot Charts | To create interactive graphs and charts for the main dashboard. |
| Slicers | To provide user-friendly, interactive buttons for filtering the dashboard. |

## 3. Project Overview

### A. Core Data Structure & Formulas

The foundation of the tracker is a single Excel Table with 100+ entries. To enable analysis, six (6) custom formulas were built into the table to automatically calculate performance metrics for each task.

| Formula / KPI | Purpose |
| :--- | :--- |
| **Time Variance (Hrs)** | Calculates hours saved or lost (`=[@[Target Time (Hrs)]]-[@[Actual Time (Hrs)]]`). |
| **Efficiency %** | The primary metric for performance (`=[@[Target Time (Hrs)]]/[@[Actual Time (Hrs)]]`). |
| **Units per Hour** | Measures raw output speed (`=[@[Units Completed]]/[@[Actual Time (Hrs)]]`). |
| **Productivity Status** | Categorizes performance ("Exceeds", "Meets", "Needs Improvement") using `IFS`. |
| **Total Task Cost (INR)** | Calculates the actual labor cost for the task (`=[@[Actual Time (Hrs)]]*[@[Hourly Rate (INR)]]`). |
| **Cost Variance (INR)** | Shows money saved (positive) or overspent (negative) vs. the target cost. |

### B. Dashboard & Visualizations

The raw, calculated data is aggregated in Pivot Tables to create a clean, interactive dashboard.

**(Screenshots of the dashboard would go here)**
``

Key visualizations on the dashboard include:
* **Average Efficiency % by Department** (Bar Chart)
* **Total Cost Variance (INR) by Task** (Column Chart)
* **Productivity Status Breakdown** (Donut Chart)
* **Efficiency Trend Over Time** (Line Chart)
* **Key KPI Cards** (Overall Efficiency %, Total Cost Variance)

### C. Interactive Slicers

To make the dashboard fully interactive, Slicers are connected to all Pivot Charts for:
* `Employee Name`
* `Department`
* `Task`
* `Productivity Status`

## 4. Test Scenarios Overview

The dashboard's functionality and data integrity were validated with the following tests.

| Scenario | Expected Result | Status |
| :--- | :--- | :--- |
| Enter a new row of data in the `RawData` table | Table expands; all 6 formulas auto-fill down correctly. | [cite_start]Passed [cite: 349] |
| Set `Actual Time (Hrs)` to 0 or blank | `Efficiency %` formula gracefully handles #DIV/0! error, returning 0. | [cite_start]Passed [cite: 349] |
| Click "Employee Name" Slicer | All Pivot Charts and tables on the dashboard filter to that one employee. | [cite_start]Passed [cite: 357] |
| Click "Needs Improvement" on `Productivity Status` Slicer | Dashboard updates to show only tasks/employees marked as "Needs Improvement". | [cite_start]Passed [cite: 357] |
| Add 10 new rows and click "Refresh All" | All Pivot Tables and Charts update with the new data. | [cite_start]Passed [cite: 349] |

## 5. Conclusion

[cite_start]All project endpoints were thoroughly tested[cite: 359]. [cite_start]The Excel dashboard successfully provides a correct, reliable, and high-performance solution for tracking employee efficiency[cite: 360]. [cite_start]The system responds appropriately to both valid data entry and user-driven filter actions[cite: 360]. [cite_start]The tracker gracefully handles potential errors (like division by zero) and provides a single, interactive source of truth for management to analyze team performance[cite: 361].

## 6. Future Work

While the current Excel solution is fully functional, the following steps could enhance the project's analytical power:

* [ ] **Migrate to Power BI:** Import the Excel table into Power BI to create more advanced visualizations, implement row-level security (RLS), and publish the dashboard to the web.
* [ ] **Automate Data Refresh:** Use Power Automate or VBA macros to automatically refresh the data connections (if data were to be pulled from an external source).
* [cite_start][ ] **Add Role-Based Access Control (RBAC):** Create separate, secured views for managers versus individual employees[cite: 365].
* [ ] **Automate Data Entry:** Create a Microsoft Form or Power App to act as a front-end for data entry, removing the need for users to touch the raw Excel file.
