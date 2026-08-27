# HR Analytics Dashboard | Employee Attrition & Workforce Analysis (ExceL)

### HR Analytics, Attrition Analysis, Workforce Analytics, Exploratory Data Analysis (EDA), Human Resources, Excel Dashboard, DAX, Data Visualization


---

## Executive Summary

This project analyzes workforce data across **988 employees** in **7 departments** to identify the drivers behind an alarming **50.3% attrition rate**. The interactive dashboard surfaces attrition hotspots by department, tenure, and employment type, revealing that Legal and IT carry the highest headcount-adjusted risk and that contract workers churn far more than permanent staff. These insights give HR leadership a data-driven basis to prioritize retention interventions where they will have the greatest financial and operational impact.

---

## Business Problem

The organization was experiencing high employee turnover without a clear, centralized view of *where* and *why* it was happening. HR stakeholders lacked visibility into:

- Which departments and job grades were losing employees fastest
- Whether attrition was concentrated among short-tenure or long-tenure staff
- How employment type (contract vs. permanent vs. internship) related to churn
- Seasonal patterns in hiring that might be straining onboarding capacity

Without this visibility, retention budgets and HR initiatives were being allocated reactively rather than strategically. The goal of this project was to build a self-service dashboard that consolidates HR data into a single source of truth, enabling leadership to diagnose attrition drivers and act before losses compound.

---

## Methodology

The project followed a standard analytics workflow:

1. **Data Preparation** — Consolidated raw HR records (employee status, department, gender, grade, tenure band, hire date, contract type) into a clean, structured dataset with consistent categorical labels.
2. **Exploratory Data Analysis (EDA)** — Profiled the dataset to understand distributions of headcount by department, gender, grade, and tenure, and to detect outliers or data quality issues.
3. **Attrition Segmentation** — Cross-tabulated employee status (On-Board vs. Attrition) against department, tenure band, and employment type to isolate high-risk segments.
4. **Trend Analysis** — Aggregated hiring activity by month to identify seasonality and correlate hiring spikes with downstream attrition.
5. **KPI Design** — Defined core workforce KPIs (Total Employees, Active Employees, Attrition Rate %, Average Experience) using aggregation and ratio calculations.
6. **Dashboard Design** — Built an interactive, filterable dashboard (Year, Department slicers) so stakeholders can drill into any segment without needing analyst support.

---

## Granular Skills & Tools

**Tools**
- Microsoft Excel (Pivot Tables, Pivot Charts, Power Query, Power Pivot)
- Power BI-style dashboard design principles (applicable to either Excel or Power BI implementation)

**Technical Skills**
- Data cleaning and transformation (Power Query: deduplication, type casting, category standardization)
- DAX / Excel formulas: `COUNTIFS`, `SUMIFS`, `AVERAGEIFS`, calculated ratio fields (Attrition Rate %)
- Data modeling: relationships between employee, department, and tenure tables
- Interactive slicers/filters for Year and Department
- Chart design: clustered bar charts, donut charts, pie charts, stacked bar charts, line/trend charts
- KPI card design for executive-level summary metrics
- Dashboard UX: layout hierarchy, color coding for status (red = attrition, green = active), consistent visual grammar
- Cross-tabulation / segmentation analysis (Department × Employee Status)

---

## Results & Business Recommendations

**Key Findings**

| Finding | Insight |
|---|---|
| Overall attrition rate is 50.3% | Roughly 1 in 2 employees has left — this is a critical retention crisis, not a normal churn level |
| Legal has the highest headcount (169) and one of the highest attrition counts (84) | Legal is the single largest driver of absolute attrition losses |
| Contract employees (524 headcount) show disproportionately high churn vs. Permanent (415) | Contract workforce is the least stable segment |
| 743 employees have 5+ years of tenure, yet attrition remains at 50% | Long-tenured staff are still leaving — attrition is not solely an onboarding/early-tenure problem |
| Hiring dropped sharply from ~110/month (Jul) to ~50/month (Aug–Dec) | Recruiting slowed significantly in H2, compounding headcount losses from attrition |
| Gender split is near-even (52% Male / 48% Female) | Attrition does not appear to be gender-skewed at a high level (recommend deeper segmentation to confirm) |

**Recommendations for Business Stakeholders**

1. **Prioritize Legal and IT for retention programs** — these departments combine high headcount with high absolute attrition; even a small % improvement yields large employee-count savings.
2. **Re-evaluate the contract workforce strategy** — investigate whether contract-to-permanent conversion pathways, pay parity, or engagement programs could reduce churn among the 524 contract employees.
3. **Investigate long-tenure attrition specifically** — since 5+ year employees still churn at similar rates, conduct exit interviews focused on career stagnation, compensation compression, or leadership issues rather than assuming onboarding is the problem.
4. **Restore H2 hiring capacity** — the steep drop in monthly hires (Aug–Dec) should be reviewed against attrition timing to ensure the organization isn't running structurally understaffed.
5. **Set a department-level attrition rate target** (e.g., reduce Legal and IT attrition by 10 percentage points in 2 quarters) and track progress using this dashboard as the single source of truth.

---

## Next Steps & Limitations

**Next Steps (with more time/data)**
- Incorporate **exit reason** and **compensation** data to move from *where* attrition happens to *why*
- Build a **predictive attrition model** (e.g., logistic regression or classification tree) to flag at-risk employees proactively rather than reporting attrition after the fact
- Add **cohort/survival analysis** to understand time-to-attrition by hire cohort
- Layer in **manager-level** and **performance rating** dimensions to test whether attrition correlates with specific leadership or performance segments
- Benchmark attrition rate against industry standards to contextualize severity

**Limitations**
- Dataset does not include exit reasons, compensation, or performance data, limiting root-cause analysis to structural/demographic variables only
- Attrition rate (50.3%) is unusually high and may reflect a specific reporting period, data extract anomaly, or definition difference (e.g., contract expirations counted as attrition) — this should be validated with HR data owners before being presented externally
- Data covers only 2025–2026; longer historical trends would improve confidence in seasonality conclusions
- No geographic/location dimension is available, which could otherwise reveal site-specific retention issues

---

