# Telecom-KPI-Analysis-PowerBI
Power BI dashboard analyzing Telecom KPIs  to detect issues and guide network optimization
# Telecom KPI Monitoring & Performance Analysis — Power BI

**Project type:** Power BI | Telecom KPI Analysis  
**Author:** Md Reazul Repon  
**Contact:** reazulrepon@gmail.com | https://github.com/MReza07

---

## 📌 Short description
A Power BI dashboard for monitoring and analyzing telecom network performance across regions and technologies (2G/3G/4G). The dashboard tracks core KPIs such as **Total Traffic (GB)**, **Call Drop Rate (CDR)**, **Call Setup Success Rate (CSSR)**, **Handover Success Rate (HOSR)**, **Availability (%)**, **Downtime (Min)** and **VoLTE MOS**, and visualizes customer complaint correlations.

---

## 🔍 Project objective
- Provide a single-pane dashboard for network operations and management.  
- Detect underperforming clusters/sites and possible root causes.  
- Track trends (MoM/YoY), technology share (4G/3G/2G), and SLA compliance.  
- Provide actionable recommendations for network optimization.

---

## 📁 Repository structure

---

## 🛠 Tools & Tech
- Power BI Desktop (PBIX)  
- DAX, Power Query (M)  
- Excel (data prep)  
- (Optional) Python / SQL for preprocessing

---

## 🧩 Data & privacy
- The full original dataset contains proprietary telecom data and is **not** public.  
- `data_sample/sample_dataset.csv` contains an **anonymized sample** and the table schema to reproduce the analysis.

---

## 📊 Dashboard features & visuals
- KPI cards: Total Traffic (GB), Total Dropped Calls, Downtime %, Average Availability, Daily Downtime (Min)  
- Region-level bar charts and technology donut chart (4G/3G/2G)  
- Time series: Total Traffic by Month and MoM Growth%  
- Customer complaints vs traffic trends (line chart)  
- Binned analysis: Traffic by Downtime (mins) and Availability bins  
- Top 5 worst-performing sites table by average availability  
- Filters: Technology, Region, Month

---

## ✅ Key DAX measures (examples)
```DAX
Total Traffic (GB) =
SUM('Dataset'[Total_Traffic_GB])

Total Dropped Calls =
SUM('Dataset'[Dropped_Calls])

Downtime % =
DIVIDE(
    SUM('Dataset'[Downtime_Min]),
    SUM('Dataset'[Total_Traffic_GB]) + 1
)

SLA_Compliance % =
DIVIDE(
    CALCULATE(COUNTROWS('Dataset'), 'Dataset'[SLA_Compliance] = "Yes"),
    CALCULATE(COUNTROWS('Dataset'))
)
