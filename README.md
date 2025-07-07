# 🧾Hospital Emergency Dashboard using Power BI, Power Query, DAX

> A project to modernize emergency department reporting and patient flow analytics using Power BI.

---

## 🚀 Project Overview

This project demonstrates how data visualization and analytics can optimize emergency room operations and improve patient care.
Using Power BI, the dashboard consolidates patient data, enabling stakeholders to monitor admissions, wait times, referrals, and satisfaction, all in real time.
---
## 📌 Business Problem

Hospitals often struggle to maintain efficient ER operations due to:

- High patient volume
- Long wait times
- Limited visibility into hourly and daily patterns
- Manual reporting
- Inconsistent data on patient satisfaction

This dashboard addresses these challenges with a centralized, interactive reporting solution that helps improve service delivery, resource planning, and patient experience.
## 📊 Key KPIs (Important Numbers We Track)

These KPIs (Key Performance Indicators) help us understand how well the tax reporting process is working, and where we need to improve.

| KPI Name                | What It Tells Us |
|-------------------------|------------------|
| **Filed Report %**      | How many clients have submitted their tax reports on time. |
| **Average Compliance Score** | A score (from 0 to 100) that shows how well clients are following tax rules. |
| **Automation Usage %**  | How many cases are handled by automated tools instead of manually. |
| **Late Filing %**       | The percentage of reports that were submitted after the deadline. |
| **High-Risk Clients**   | How many clients are considered risky because of errors or missing reports. |
| **Average Processing Time** | How long it takes (on average) to process a report. |

🧠 **Why These Matter Together**:
- They help spot problems early (like late reports or risky clients)
- Show if automation is helping the team work faster
- Make it easier to decide where to focus attention (like which clients or regions need help)
- Help the company stay compliant and avoid penalties

---

## 🖼️ Dashboard Snapshots

### 📄 1. Executive Summary

High-level KPIs such as compliance score, filing rate, automation usage, and high-risk clients.

![Executive Summary](https://github.com/bhumikabharadwaj2205/-Operational-Tax-and-wealth-management/blob/main/tax%20dashboard%20images/executive_summary.png?raw=true)


---

### 📄 2. FATCA Client Portfolio

FATCA vs non-FATCA breakdown, income vs compliance trends, asset diversity by jurisdiction.

![Client Portfolio](https://github.com/bhumikabharadwaj2205/-Operational-Tax-and-wealth-management/blob/main/tax%20dashboard%20images/client_portfolio.png?raw=true)

---

### 📄 3. Compliance & Risk Analysis

Heatmaps and scatter plots showing late filings, risk hotspots, and jurisdiction performance.

![Risk Page](https://github.com/bhumikabharadwaj2205/-Operational-Tax-and-wealth-management/blob/main/tax%20dashboard%20images/compilance_risk.png?raw=true)


---

### 📄 4. Analyst Performance

Highlights top analysts based on speed, accuracy, and automation usage.

![Analyst Page](https://github.com/bhumikabharadwaj2205/-Operational-Tax-and-wealth-management/blob/main/tax%20dashboard%20images/analyst_performance.png?raw=true)

---

## 📘 Key DAX Insight: Filed Report Percentage

As part of building this dashboard, I came across an impactful DAX function that helped me measure the overall effectiveness of tax reporting: **Filed Report Percentage**. This became one of the most important KPIs in the project.

---

### 📌 DAX Formula


### 🖼️ Screenshot: Filed Report Percentage KPI

![Filed Report Percentage KPI](https://github.com/bhumikabharadwaj2205/-Operational-Tax-and-wealth-management/blob/main/tax%20dashboard%20images/filed_report_percentage.png?raw=true)


### 🧮 What the Formula Does

This DAX formula calculates the **percentage of clients who have filed their tax reports**.

- `COUNTROWS(ClientData)` counts all the clients in the dataset.
- `CALCULATE(..., ClientData[Report Status] = "Filed")` filters only those records where the report status is marked as "Filed".
- `DIVIDE` divides the number of filed reports by the total number of clients, and handles any divide-by-zero errors safely.

📊 **For example**:  
If 3,500 out of 5,000 clients submitted their reports:


