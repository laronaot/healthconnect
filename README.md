# AnalystLab Africa Data Analytics Internship Programme

**Intern:** Larona Othapile
**Track:** Data Analytics
**Programme:** AnalystLab Africa Experience Lab

This repository documents my work through the AnalystLab Africa Data Analytics Internship Programme - from the Week 1–3 foundational projects through to the ongoing **HealthConnect Clinic Experience Lab**, a shared project all tracks contribute to from Week 4 onward.

---

## Weekly Progress

| Week | Project | Focus | Status |
|---|---|---|---|
| 1 | Employee Attrition Analysis - ABC Manufacturing Ltd | Business understanding, dataset inspection, exploratory notebook | Complete |
| 2 | Business Intelligence & Interactive Dashboard - Superstore Sales | Power BI dashboard for a simulated retail client | Complete |
| 3 | Advanced Data Analysis & KPI Development - Superstore Sales | DAX measures, time-based analysis, BI dashboard | Complete |
| 4 | HealthConnect Clinic Experience Lab | Problem understanding, dataset review, data quality assessment, business questions, KPI definition | In Progress |


---

## Week 4: HealthConnect Clinic Experience Lab

### Business Problem
HealthConnect Clinic is a fictional healthcare provider experiencing missed appointments, inefficient use of appointment slots, repetitive patient enquiries, and a need for better patient engagement and administrative support.

**Central Project Question:** How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

### My Role - Data Analytics Track
Review the appointment dataset, assess its quality, define the business questions worth answering, and propose KPIs HealthConnect can track over time. This work is intended to feed directly into the Data Science track's no-show prediction model and give the Generative AI track a factual picture of the problem to design around.

### Data Sources (official project files)
- `HealthConnect_Appointment_Data.csv`- 5,000 appointment records, 18 fields
- `HealthConnect_Data_Dictionary.xlsx` - official field definitions

### Week 4 Deliverables
- `HealthConnect_Week4_Data_Analytics_Initial_Analysis.docx` - dataset overview, data quality assessment, business questions, KPI definitions, initial analysis approach, assumptions/limitations/risks/dependencies
- `HealthConnect_Week4_Project_Summary.docx` - concise summary of Week 4 work and proposed Week 5 focus
- `HealthConnect_PowerBI_DatasetOverview_Guide.docx` - step-by-step guide to building the dataset overview and data quality pages in Power BI
- `HealthConnect_DatasetOverview.pbix` — Power BI file *(add once built, following the guide above)*

### Key Week 4 Findings
- 5,000 appointments across 1,696 unique patients (avg. 2.95 appointments per patient, range 1-9)
- Outcome split: **48.5% No-Show, 46.3% Attended, 5.3% Cancelled** - a notably higher no-show rate than typical real-world clinics
- `reminder_channel` is blank for 27.3% of rows, but this is structural - it's blank exactly where `reminder_sent = No`, not a genuine data gap
- `distance_to_clinic_km` (1.8%) and `waiting_time_minutes` (1.2%) have small, genuine gaps
- No duplicate `appointment_id` values, but 15 records show the same patient booked on the same date - 9 of these also share the same time slot and look like likely duplicates, flagged for resolution in Week 5
- `booking_date`/`appointment_date` are stored as US-style text (M/D/Y), despite the Data Dictionary describing them as "ISO format" — noted so anyone loading the file (Python or Power BI) parses dates correctly

### Business Questions (Week 4)
1. What is the overall no-show rate, and how does it trend by day, time, and month?
2. Which demographic factors (age group, gender) are associated with higher no-show rates?
3. Does booking lead time affect the likelihood of a no-show?
4. Do reminders measurably reduce no-show rates, and does the channel matter?
5. Is distance to the clinic associated with lower attendance?
6. Does a patient's prior no-show history predict a future no-show?

### Proposed KPIs (defined, not yet calculated - per Week 4 scope)
1. Overall No-Show Rate
2. No-Show Rate by Reminder Status
3. No-Show Rate by Lead-Time Band
4. Repeat No-Show Rate
5. No-Show Rate by Distance Band

### Tools Used
Python (pandas) for data review and quality checks · Power BI for the dataset overview report · Microsoft Word/Excel for documentation

### Next Steps: Week 5
- Resolve the 15 same-day duplicate-looking records
- Confirm what `waiting_time_minutes` represents for No-Show/Cancelled appointments
- Calculate baseline values for all five KPIs
- Produce the first exploratory visuals answering the Week 4 business questions

---

## Repository Structure

```
├── README.md
├── week1-employee-attrition/
├── week2-superstore-dashboard/
├── week3-superstore-advanced-kpis/
└── week4-healthconnect/
    ├── data/
    │   ├── HealthConnect_Appointment_Data.csv
    │   └── HealthConnect_Data_Dictionary.xlsx
    ├── HealthConnect_Week4_Data_Analytics_Initial_Analysis.docx
    ├── HealthConnect_Week4_Project_Summary.docx
    ├── HealthConnect_PowerBI_DatasetOverview_Guide.docx
    └── HealthConnect_DatasetOverview.pbix
```


---

## About the Programme
AnalystLab Africa's Experience Lab Internship Programme develops practical skills in data analytics, data science, machine learning engineering, and generative AI through applied, portfolio-ready projects.

`#AnalystLabAfrica`
