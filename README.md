# 🏥 **Papollo Hospitals: Leads Flow Dashboard**

---

## **Problem Statement**

The **Papollo Hospitals Leads Flow Dashboard** helps hospital management gain a complete understanding of their patient flow, diagnosis trends, doctor performance, and financial statistics.
It provides detailed insights into **patient admissions, discharges, billing patterns, and bed occupancy rates**, while also tracking **doctor feedback and diagnosis-wise patient count**.

Through this dashboard, hospital administrators can:

* Monitor patient admissions and discharge patterns.
* Track total billing and health insurance claims.
* Evaluate the performance of doctors based on patient feedback.
* Identify the most common diagnoses and treatment trends.
* Optimize hospital resources such as beds and equipment.

---

## **Steps Followed**

### **Step 1: Data Loading**

* Imported hospital data (CSV/Excel file) into **Power BI Desktop**.
* Dataset fields included:
  *Patient_ID, Admit_Date, Discharge_Date, Followup_Date, Diagnosis, Doctor_Name, Bed_Type, Bill_Amount, Health_Insurance_Amount.*

---

### **Step 2: Data Cleaning**

* Opened **Power Query Editor** and:

  * Removed null, duplicate, and invalid entries.
  * Ensured proper data types (Date, Text, Numeric, Currency).
  * Verified data consistency for fields such as dates and bill amounts.

---

### **Step 3: Data Transformation**

* Created calculated columns and measures for KPIs:

  * Total Bill Amount
  * Health Insurance Amount
  * Bed Occupancy Count
  * Diagnosis Count
  * Doctor Feedback Count

---

### **Step 4: DAX Measures Used**

```DAX
-- Total Bill Amount
Total Bill Amount = SUM(Hospital[Bill_Amount])

-- Total Insurance Amount
Total Insurance Amount = SUM(Hospital[Health_Insurance_Amount])

-- Bed Occupancy Count
Bed Occupancy = COUNT(Hospital[Bed_Type])

-- Diagnosis-wise Patient Count
Diagnosis Count = COUNT(Hospital[Diagnosis])

-- Feedback Volume per Doctor
Feedback Count = COUNT(Hospital[Doctor_Name])
```

---

### **Step 5: Dashboard Design**

* KPI Cards:

  * Admit Date: **05-Dec-2022**
  * Discharge Date: **12-Jan-2023**
  * Follow-Up Date: **10-Dec-2022**
  * Total Bill Amount: **₹190.43M**
* **Slicer:** Patient_ID and Date Range
* **Visuals Created:**

  * Bar Chart → Bed Occupancy (Private, General, ICU)
  * Donut Chart → Feedback Volume per Doctor
  * Funnel Chart → Diagnosis-wise Patient Count
  * Line Chart → Billing vs Insurance Amount by Test Type

---

### **Step 6: Dashboard Publishing**

* Applied a custom hospital theme (pink & purple gradient) for clarity and consistency.
* Published the report to **Power BI Service** for real-time sharing and insights.

---

## **Snapshots**

### **Dashboard View (Power BI Service)**

*(Include image in GitHub README or PDF report)*

---

## **Insights**

A single-page interactive report was created on **Power BI Desktop** and then published online.
The following key inferences can be drawn from the dashboard:

---

### **[1] Patient Flow Details**

* **Admit Date:** 05-Dec-2022
* **Discharge Date:** 12-Jan-2023
* **Follow-Up Date:** 10-Dec-2022
* **Total Bill Amount:** ₹190.43 Million

🩺 *The hospital handled a large volume of patients with significant billing across departments.*

---

### **[2] Bed Occupancy**

| Bed Type | Count |
| -------- | ----- |
| Private  | 3K+   |
| General  | 2K+   |
| ICU      | 1K+   |

🏥 *Private wards have the highest occupancy, indicating higher demand and profitability.*

---

### **[3] Feedback Volume per Doctor**

| Doctor Name    | Feedback Count |
| -------------- | -------------- |
| Ravi D         | 4.83K          |
| Naresh Goyenka | 4.83K          |
| Niki Sharma    | 4.83K          |
| Jay Sinha      | 4.83K          |
| Jaya Yaadav    | 4.83K          |
| Tejas Saxena   | 4.83K          |
| Mark Joy       | 4.83K          |

💬 *All doctors have received consistent feedback, showing balanced patient distribution.*

---

### **[4] Diagnosis-wise Patient Count**

| Diagnosis       | Patient Count |
| --------------- | ------------- |
| Viral Infection | 2.0K          |
| Flu             | 1.7K          |
| Malaria         | 1.4K          |
| Typhoid         | 1.1K          |
| Pneumonia       | 0.57K         |
| Fracture        | 0.29K         |

🧾 *Viral Infections and Flu are the most common diagnoses, forming nearly 40% of total cases.*

---

### **[5] Billing & Insurance Comparison**

| Procedure  | Billing Amount | Insurance Amount |
| ---------- | -------------- | ---------------- |
| CT Scan    | ₹60M           | ₹57M             |
| Ultrasound | ₹58M           | ₹52M             |
| MRI        | ₹53M           | ₹49M             |
| Blood Test | ₹11M           | ₹10M             |
| X-Ray      | ₹5M            | ₹5M              |

💰 *Billing and insurance values are closely aligned, indicating transparent and consistent pricing.*

---

## **Key Findings**

1. **Total Bill Amount** reached ₹190.43M across all patients.
2. **Private wards** are the most occupied, suggesting preference for comfort and care.
3. **Viral infections** and **flu** are the top diagnoses treated.
4. **Health insurance coverage** nearly matches billing totals — a sign of effective claim management.
5. **Doctors’ feedback scores** are uniform, reflecting high service consistency.

---

## **Tools & Technologies**

| Tool                                | Purpose                            |
| ----------------------------------- | ---------------------------------- |
| **Microsoft Power BI Desktop**      | Dashboard creation & visualization |
| **Power Query Editor**              | Data cleaning & transformation     |
| **DAX (Data Analysis Expressions)** | Calculations & measures            |
| **Excel/CSV**                       | Data Source                        |
| **Power BI Service**                | Publishing and collaboration       |

---

## **Conclusion**

The **Papollo Hospitals Leads Flow Dashboard** serves as a comprehensive tool for tracking hospital operations and patient management.
It provides **data-driven insights** that help management optimize:

* Bed occupancy and resource allocation
* Billing accuracy and insurance tracking
* Doctor performance monitoring
* Diagnosis and treatment efficiency

With real-time insights, the hospital can improve **decision-making, patient satisfaction, and operational efficiency**.

---

## **Future Enhancements**

* Integrate **AI models** to predict patient admission trends.
* Add **real-time data refresh** for live updates from hospital databases.
* Include **patient satisfaction sentiment analysis** using Power BI and Python integration.

