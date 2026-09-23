# hr-analytics-tableau-dashboard
Interactive HR analytics dashboard built in Tableau — headcount, attrition, demographics, and income KPIs with a filterable employee records view. Covers data modeling, calculated fields, and dashboard UX design.
## 📊 Project Overview

- **Goal:** Give HR leaders one interactive view of headcount, attrition, demographics, and pay — built for filtering, not just reading.
- **Data:** Employee ID, demographics, role, geography, salary, status, and tenure, modeled from a single source file.
- **Output:** A 2-page interactive dashboard — an Overview page (KPIs, demographics, income) and an Employee Records page (filterable on every column).

## 🧱 Build Process

1. **Building the Data Source** — collect data, connect it, check data quality and datatypes, explore the fields.
2. **Analysis & Chart Building** — choose the right chart per question, write calculated fields, format each sheet.
3. **Building the Dashboard** — plan the layout (dashboard mockup, container mockup), assemble, fix colors, spacing, tooltips, filters, and legends.

## 🧮 Key Calculated Fields

| Field | Logic |
|---|---|
| Total Active / Terminated | `COUNT([Employee ID])`, split on whether `[Termdate]` is null |
| HQ vs. Branch | `CASE [State] WHEN 'New York' THEN 'HQ' ELSE 'Branch' END` |
| Age | `DATEDIFF('year', [Birthdate], TODAY())` |
| Age Group | `IF/ELSEIF` bucketing `[Age]` into five bands, from `>25` to `55+` |

## 🎨 Design

- **Theme:** Dark background with a custom accent palette
- **Colors:** Persian Green `#03c4a1`, Royal Fuchsia `#c52a87`, neutral grays `#777777` / `#f5f5f5`
- **Dashboard size:** 1400 × 800

## 📁 Repository Structure
├── dashboard/ # .twbx Tableau workbook
├── mockups/ # Dashboard & container mockup images
├── screenshots/ # Overview & Employee Records page previews
└── README.md


## 🛠️ Tools & Skills

Tableau · Data Modeling · Calculated Fields (LOD, CASE, IF/ELSEIF) · Dashboard UX · Data Visualization

## Screenshots
<img width="1397" height="805" alt="Screenshot 2026-09-22 211926" src="https://github.com/user-attachments/assets/86f9c89e-4f78-4d1c-b455-05f5e4157a05" />

<img width="1402" height="805" alt="Screenshot 2026-09-22 211959" src="https://github.com/user-attachments/assets/86a3574b-fb0b-452c-9c03-94bf99ba35ce" />



---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.

## 🌟 About Me

Hi there! I'm Askar Basha, a passionate data enthusiast interested in SQL, data analytics, business intelligence, and turning raw data into meaningful insights.

I created this repository to showcase my Tableau and analytical skills, and my ability to design dashboards that are both visually clear and genuinely useful for decision-making. My goal is to continuously improve my knowledge and share useful projects that demonstrate real-world data analysis techniques.
