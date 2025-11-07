# PowerBI-Excel-ER-Dashboard
End-to-End Hospital Emergency Room Dashboard built using Excel and Power BI to analyze patient flow, service timeliness, and department performance for data-driven healthcare insights.
# 🏥 End-to-End Hospital Emergency Room Analysis Dashboard  
**Project Type:** Data Analytics | Excel | Power BI  
**Author:** Manoj Kumar  

---

## 📘 Project Overview  
This project demonstrates how **Excel** and **Power BI** can be used together to analyze and visualize **Hospital Emergency Room data**.  
The goal is to help hospital management and stakeholders **monitor, analyze, and make data-driven decisions** to improve patient care and operational efficiency.

---

## 🎯 Objective  
To build an **interactive and insightful dashboard** that provides a complete overview of emergency room performance through various KPIs and visualizations.

---

## 📊 Key Features  
- 🏥 **Patient Admission Status:** Tracks admitted vs. non-admitted patients  
- ⏱️ **Timeliness KPI:** Measures percentage of patients attended within 30 minutes  
- 👨‍⚕️ **Gender Analysis:** Shows distribution of male and female patients  
- 👶 **Age Group Distribution:** Categorizes patients into defined age groups  
- 🩺 **Department Referrals:** Highlights departments with the most patient referrals  
- 🗓️ **Calendar Table:** Enables accurate time-based trend analysis  
- ⚡ **Fully Interactive Dashboard:** Built with slicers and filters for better insights  

---

## 🧮 DAX Formulas Used  

### ➤ Age Group Classification  
```DAX
Age Group = 
IF([Patient Age]>=70,"70-79",
IF([Patient Age]>=60,"60-69",
IF([Patient Age]>=45,"45-59",
IF([Patient Age]>=30,"30-44",
IF([Patient Age]>=15,"15-29",
IF([Patient Age]>=5,"05-14","0-4"))))))
Patient Attend Status
Patient Attend Status =
IF([Patient Waittime]<30, "Within Time", "Delayed")

➤ Calendar Table Formula
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
