# healthcare_Insights

# 🏥 Healthcare Provider Analytics Dashboard | Power BI

A comprehensive Power BI dashboard that provides deep insights into healthcare billing, diagnosis, and cost trends. Designed to help hospital admins and analysts optimize operations and reduce cost inefficiencies.

## 🔍 Features & KPIs
- **Total Billing Amount**: £3.36M
- **Avg. Billing Per Visit**: £674.86
- **Billing by Department**: Cardiology, Orthopedics, General Surgery
- **Billing by Procedure**: X-Ray, CT, MRI, Ultrasound
- **Cost Breakdown**: Medication, Room, Treatment
- **Insurance vs Out-of-Pocket**
- **Monthly, Weekly, and Daily Trends**

## 📊 Visualizations
- Map by State/City Billing
- Dynamic trend slicers for year, quarter, weekday
- Department-wise weekly change tracking
- Emergency vs Inpatient vs Outpatient breakdowns

## 💻 Tools Used
- Microsoft Power BI
- DAX for dynamic calculations
- Custom visuals and bookmarks

## 📎 Live Dashboard
[🔗 Click to View](https://app.powerbi.com/view?r=eyJrIjoiZGY1MTQwNTEtYzNiNy00NmQ3LThhNTctMjViM2MxZDJkYzY1IiwidCI6ImJjZDZjNTAzLTgzZmMtNDU4Ni04MDNlLWQ5OWViNmQ1MjVjNiJ9&pageName=0b6398608032b05ba400)

## 📁 Dataset
- Simulated healthcare billing and patient records
- Aggregated cost breakdowns by department/procedure

# 📘 README: Healthcare Provider Dashboard (Power BI)

---

## 📊 Key Metrics & DAX Calculations

### ✅ Total Billing Amount
```dax
TotalBilling = SUM(FactBilling[BillingAmount])
```

### ✅ Average Billing Cost Per Visit
``` dax
AvgBillingPerVisit = DIVIDE([TotalBilling], DISTINCTCOUNT(FactBilling[VisitID]))
```
### ✅ Room Cost
``` dax
TotalRoomCost = SUM(FactBilling[RoomCost])
AvgRoomCostPerVisit = DIVIDE([TotalRoomCost], DISTINCTCOUNT(FactBilling[VisitID]))
```
### ✅ Medication Cost
``` dax
TotalMedicationCost = SUM(FactBilling[MedicationCost])
AvgMedicationCost = DIVIDE([TotalMedicationCost], DISTINCTCOUNT(FactBilling[VisitID]))
```
### ✅ Treatment Cost
``` dax
TotalTreatmentCost = SUM(FactBilling[TreatmentCost])
AvgTreatmentCost = DIVIDE([TotalTreatmentCost], DISTINCTCOUNT(FactBilling[VisitID]))
```
### ✅ Insurance Covered & Out-of-Pocket
``` dax
TotalInsurance = SUM(FactBilling[InsuranceAmount])
AvgInsurancePerVisit = DIVIDE([TotalInsurance], DISTINCTCOUNT(FactBilling[VisitID]))

OutOfPocket = [TotalBilling] - [TotalInsurance]
AvgOutOfPocket = DIVIDE([OutOfPocket], DISTINCTCOUNT(FactBilling[VisitID]))
```

📌 Dashboard Pages
Overview Page

* KPIs & total billing summaries
* Billing by Procedure, Department, Diagnosis
* Interactive map: State/City filter

Trend Analysis

* Monthly and Weekly Trends
* Previous vs Current Month and Week billing
* Drilldowns by Weekdays and Departments

🧰 Tools & Stack
* Power BI Desktop
* Data Modeling: Star schema
* DAX Measures
* Bing Maps integration


---
📌 **For feedback or collaboration:** [Connect on LinkedIn](https://linkedin.com/in/karthik-vendipalli)

