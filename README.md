```markdown
# 🏥 National Health Analysis Dashboard | Power BI

Explore an interactive Power BI report built by **Bhavya Jain**, providing powerful insights into patient demographics, trends, treatment, and costs across multiple years.

---

## 📁 Repository Structure

```

National-Health-Analysis/
├── screenshots/
│   ├── demographics.png
│   ├── key\_trends.png
│   └── treatment\_cost.png
├── Health\_Analysis.pbix
└── README.md

````

---

## 🧩 Project Overview

This dashboard delivers a full view of hospital data across three thematic pages:
1. **Patient Demographics** – Who’s being admitted, their age/gender breakdowns, and occupancy stats  
2. **Key Trends** – How admissions, billing, and length of stay (LOS) evolve over time  
3. **Treatment & Cost** – Medication patterns, cost breakdowns by stay length and hospital

---

## 🛠 Build Steps

### 1. Data Preparation (Power Query)
- Imported raw tables: Admissions, Patients, Physicians, Rooms, Billing, Medications  
- Standardized column names and data types  
- Cleaned nulls, errors, and duplicates  
- Created **Parameters** to dynamically filter the dataset  
- Built a Calendar (Date) table for time-intelligent analysis  

### 2. Data Modeling
- Designed a star schema with **Admissions** as the central fact table  
- Linked dimension tables: Patients, Rooms, Physicians, Medications, Dates  
- Set up one-to-many relationships for efficient filtering

### 3. DAX Measures
- `Distinct Patients`, `Distinct Rooms`, `Distinct Doctors`  
- `Avg Billing Amount = AVERAGE(Billing[Amount])`  
- `Avg LOS = AVERAGE(DATEDIFF(AdmissionDate, DischargeDate, DAY))`  
- Measures support slicer filters for Year and Medical Condition  

### 4. Report Design & Navigation
- Structured into three pages: **Patient Demographics**, **Key Trends**, and **Treatment & Cost**  
- Integrated slicers for Year and Medical Condition  
- Incorporated KPI cards, bar charts, line trends, and data tables  
- Enabled seamless navigation via **Bookmarks** and **Selection Pane**

---

## 📊 Dashboard Pages & Insights

### 🫂 1. Patient Demographics
- KPI cards show admissions, rooms occupied, avg billing, avg LOS, avg age, and doctor count  
- Age group + gender bar charts reveal demographic distributions  
- Interactive filtering by year and medical condition  

### 📈 2. Key Trends
- Line charts display trends in admissions, average billing, and LOS over time  
- Useful for spotting seasonal and annual changes in healthcare usage  

### 💊 3. Treatment & Cost
- KPI visuals highlight patients, rooms, doctors, billing, LOS, and avg age  
- Billing comparisons by length of stay and admission type (Elective, Urgent, Emergency)  
- Hospital-by-hospital billing breakdowns and medication usage tables categorized by condition

---

## 🖼 Screenshots  

**Patient Demographics**  
![Patient Demographics](screenshots/demographics.png)

**Key Trends**  
![Key Trends](screenshots/key_trends.png)

**Treatment & Cost**  
![Treatment & Cost](screenshots/treatment_cost.png)

---

## 🚀 Getting Started

```bash
git clone https://github.com/bhavya19988107/National-Health-Analysis.git
cd National-Health-Analysis
````

* Open `Health_Analysis.pbix` in Power BI Desktop
* Apply slicers for year and medical condition
* Use bookmarks and selection pane to navigate between pages

---

## 🔧 Tools & Techniques

* **Power Query** – Data ETL, parameter controls, calendar table creation
* **Data Modeling** – Star schema for optimized performance
* **DAX** – For building strong insight-driven metrics
* **Report Navigation** – Bookmarks, selection pane, KPI visuals

---

## 👤 About the Author

Built by **Bhavya Jain**, passionate about healthcare analytics and data visualization.
If this was helpful, please ⭐ the repo, share feedback, or reach out to collaborate!

```

