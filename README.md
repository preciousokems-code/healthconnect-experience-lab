# HealthConnect Experience Lab
**AnalystLab Africa Experience Lab Internship Programme — Data Analytics Track**

> Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

---

## 📌 Project Overview

HealthConnect is a fictional healthcare provider facing a critical operational challenge: **over half of all non-cancelled appointments end in a no-show.** This project explores the clinic's appointment data to understand attendance patterns, identify factors associated with missed appointments, and develop data-driven recommendations to improve appointment utilisation and patient engagement.

This repository documents my Data Analytics track contribution to the HealthConnect Experience Lab across multiple weeks.

**Central Project Question:**
*How can HealthConnect use data and AI to reduce missed appointments and improve the patient support experience?*

---

## 🗂️ Week 4: Problem Understanding

### My Role
- Reviewed and understood the available appointment data
- Assessed initial data quality and suitability
- Identified variables relevant to appointment attendance and no-shows
- Defined meaningful business questions
- Proposed relevant KPIs
- Developed an initial analytical approach

### Dataset
| Detail | Value |
|---|---|
| Records | 5,000 appointments |
| Variables | 18 |
| Unique patients | 1,696 |
| Booking date range | 7 Nov 2024 – 27 Jun 2026 |
| Appointment date range | 1 Jan 2025 – 30 Jun 2026 |

### Data Quality Summary
- ✅ 0 exact duplicate records; 0 duplicate appointment IDs
- ✅ 0 date, booking-lead-time, and age-group consistency issues
- ⚠️ Missing values: Distance to Clinic (90 records, 1.80%), Waiting Time (60 records, 1.20%)
- ✅ All categorical fields checked for clean, consistent values

### Initial Outcome Split (share of all appointments)
| Outcome | Count | Percentage |
|---|---|---|
| No-Show | 2,423 | 48.46% |
| Attended | 2,314 | 46.28% |
| Cancelled | 263 | 5.26% |

---

## 📊 Week 5: Exploratory Analysis, KPI Development & Business Insights

### KPI Results (share of non-cancelled appointments, per Week 4 KPI definitions)
| KPI | Result |
|---|---|
| Total Appointments | 5,000 |
| Attendance Rate | 48.85% |
| No-Show Rate | 51.15% |
| Cancellation Rate | 5.26% |
| Previous No-Show Rate | 41.58% |

> **Note:** The Week 5 Attendance/No-Show rates (48.85% / 51.15%) differ slightly from the Week 4 figures (46.28% / 48.46%) because Week 5 calculates them as a share of *non-cancelled* appointments only, consistent with the Week 4 KPI definitions — not because of any data discrepancy.

### Key Findings
- **41.58%** of patients have a history of at least one previous missed appointment, and this history is strongly associated with current no-show behaviour.
- **Reminders reduce no-shows:** 49.89% no-show rate with a reminder vs. 54.63% without. **SMS** performs best; **WhatsApp** performs worst.
- **Booking lead time matters:** longer lead times are associated with higher no-show rates.
- **Day of week matters:** highest no-show rates on Monday, Sunday, and Wednesday; lowest on Friday.
- **Distance to clinic** shows a broadly increasing no-show trend, with an unexplained anomaly at 40–50km flagged for further investigation.
- **Age, gender, and waiting time** show weak or inconsistent relationships with no-show behaviour.
- **Appointment type:** no-shows highest for Follow-up, lowest for General Consultation.

### Cross-Track Collaboration
Shared KPI results and the strongest observed predictors of no-show (previous no-show history, reminder status/channel, booking lead time, appointment day, appointment type) with the **Data Science track**, to support feature selection for their proposed no-show prediction model. Also flagged `distance_to_clinic_km` and `waiting_time_minutes` as variables needing closer inspection.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Loading, inspecting, and validating the appointment dataset — data quality checks, consistency checks, and KPI calculations |
| **Power BI** | Data modelling, DAX measures, and the initial analytical dashboard |

---

## 📁 Repository Contents

```
├── Week4_DataAnalytics_Initial_Analysis_Document.docx       # Week 4 Deliverable 1: problem understanding report
├── Week4_DataAnalytics_Project_Summary.docx                 # Week 4 Deliverable 2: concise summary
├── HealthConnect_Week4_DataQuality_Excel.xlsx               # Week 4 Deliverable 3: data quality checks
├── Week5_DataAnalytics_HealthConnect_Analytics_Report.docx  # Week 5: full EDA, KPIs, insights, recommendations
├── Week5_DataAnalytics_Project_Summary.docx                 # Week 5: concise summary
├── HealthConnect_Week5_Dashboard_PowerBI.pbix               # Week 5: KPI dashboard
└── README.md
```

---

## 🔭 Remaining Work / Next Steps

- Insert final Power BI dashboard screenshots into the Week 5 report
- Verify the exact definition of `waiting_time_minutes` against the HealthConnect Data Dictionary
- Investigate the cause of the 40–50km distance anomaly
- Confirm the exact peak no-show rate associated with the longest booking lead times
- Continue building toward later stages of the HealthConnect Experience Lab (deeper analysis, refined dashboard, final presentation)

---

## 👤 About Me

Data Analytics intern at AnalystLab Africa, with a background in the pharmaceutical field. This project sits at the intersection of healthcare operations and data — an area I'm especially motivated to work in.

---

*This project uses fictional, anonymised data provided by AnalystLab Africa for educational purposes as part of the Experience Lab Internship Programme.*

`#AnalystLabAfrica`.
