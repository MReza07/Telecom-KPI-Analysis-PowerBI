# Telecom-KPI-Analysis-PowerBI

Power BI dashboard analyzing Telecom KPIs  to detect issues and guide network optimization


## 📌 Short description
A Power BI dashboard for monitoring and analyzing telecom network performance across regions and technologies (2G/3G/4G). The dashboard tracks core KPIs such as **Total Traffic (GB)**, **Call Drop Rate (CDR)**, **Call Setup Success Rate (CSSR)**, **Handover Success Rate (HOSR)**, **Availability (%)**, **Downtime (Min)** and **VoLTE MOS**, and visualizes customer complaint correlations.

---

## 🔍 Project objective
- Provide a single-pane dashboard for network operations and management.  
- Detect underperforming clusters/sites and possible root causes.  
- Track trends (MoM/YoY), technology share (4G/3G/2G), and SLA compliance.  
- Provide actionable recommendations for network optimization.

---

📂 Project Structure

Telecom-KPI-Analysis-PowerBI

├── Telecom KPI Analysis.pbix

│   Telecom_KPI_data_set.xlsx


│   Telwcom KPI Analysis Report.JPG

│
└── 📄 README.md

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




## 🚀 How to Open the Dashboard

Navigate to the PBIX folder

Click Download → Raw to download the .pbix file

Open it using Power BI Desktop


🛠️ Tools & Technologies

Power BI Desktop

Power Query (ETL & Data Cleaning)

DAX (Measures & Modeling)

Excel Dataset

Interactive Visual Analytics

📜 License

This project is distributed under the MIT License.

📬 Contact

Md. Rezaul Repon

Data Analyst – Power BI | SQL | Python

📧 Email: reazulrepon@gmail.com

🔗 GitHub: https://github.com/MReza07


