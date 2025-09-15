# COVID-19 Power BI Report

**File:** `covid19.pbix`  
**Repository:** Rakeshrallabandi/Covid-19

---

## Overview
This repository contains a Power BI Desktop report file (`covid19.pbix`) that visualizes COVID-19 data. The report includes dashboards, charts and tables built in Power BI to explore cases, deaths, testing, and other pandemic-related metrics.

---

## Contents
- `covid19.pbix` — Power BI Desktop report file (source file for the visuals and queries).

> NOTE: The `.pbix` is a binary Power BI file. If you want to view or edit the report you need Power BI Desktop (Windows) or Power BI Desktop for the web (limited).

---

## Prerequisites
- **Power BI Desktop (recommended)** — Download from Microsoft (install the latest stable release).
- If the report connects to external data sources (CSV, Excel, web API), ensure you have access/credentials for those sources.
- Basic familiarity with Power Query / Power BI modelling and DAX is helpful.

---

## How to open the report
1. Install and open **Power BI Desktop**.
2. From the menu choose **File → Open** and select `covid19.pbix`.
3. If the report uses external data sources, Power BI may prompt you to:
   - Provide credentials (Data source settings → Edit permissions).
   - Apply privacy level / enable data extraction.
4. After opening, click **Refresh** to refresh the dataset (if online sources are available).

---

## Data & Transformations (what to check)
- **Date columns**: Ensure the `Date` column(s) are set to Date data type in Power Query. For consistent formatting, convert to `YYYY-MM-DD` if needed.
- **Data types**: Verify numeric columns (cases, deaths, tests) are set as Whole Number or Decimal Number as appropriate.
- **Relationships**: If the model has multiple tables, check relationships in the Model view to confirm joins (1:N, Many:Many) are correct.
- **M Query / Power Query**: If you modify queries, click **Close & Apply** to load changes.

---

## Common troubleshooting
- **"Expression.Error: The name 'Word'..."** — This kind of error usually indicates a broken reference or a renamed column in a query. Open Power Query and inspect the applied steps for each query; look for steps referencing missing column names.
- **Many-to-many relationship warnings** — Understand the consequences: Many-to-many can alter filter propagation. Consider creating proper dimension tables or using `TREATAS` / bridging tables where needed.
- **Missing visuals or blank values** — Check filters, slicers, and visual-level filters. Also ensure the underlying data types are correct (e.g., Date vs Text).
- **Data refresh failures** — Confirm data source credentials are valid and that the machine has internet access for web APIs. For Power BI Service scheduled refresh, configure gateway if the source is on-premises.

---

## Suggestions for improvement / contribution
If you want to improve this report or extend it:
1. Fork the repo.
2. Edit or extend the `.pbix` in Power BI Desktop.
3. Save your changes and, if appropriate, export visuals or documentation.
4. Open a Pull Request describing the changes. (Because `.pbix` is a binary file, include a short changelog and screenshots in the PR description.)

---

## Export & Sharing
- To share visuals without `.pbix`: Export to **Power BI Service**, publish to your workspace (requires Power BI account).
- Use **Export → Power BI template (.pbit)** to create a template that contains the model and queries but excludes the data. This is useful for sharing structure while letting others load their own data.

---


## Author / Contact
**Rallabandi Rakesh**  
(Repository owner: `Rakeshrallabandi`)  
If you want me to add an email or additional contact line, tell me what to include.
![WhatsApp Image 2025-09-15 at 19 54 20_f0361370](https://github.com/user-attachments/assets/d72151e4-e0f7-4c0b-bdaa-89e99eddfdf8)

![WhatsApp Image 2025-09-15 at 19 54 21_c246b125](https://github.com/user-attachments/assets/e1917427-7f1d-4d81-b58f-8b1c7b8344bf)

![WhatsApp Image 2025-09-15 at 19 54 21_fcc36317](https://github.com/user-attachments/assets/3bda14d6-5777-4a8b-8040-7c0f70cc3ebd)

![WhatsApp Image 2025-09-15 at 19 54 22_74625d9d](https://github.com/user-attachments/assets/c7f29994-07ba-4d55-b70d-0510bb59f632)

---

## README Quick Checklist (before opening)
- [ ] Install Power BI Desktop (latest)
- [ ] Verify data source access/credentials
- [ ] Confirm `Date` column format (`15-09-2025`) if doing time-series analysis
- [ ] Backup original `covid19.pbix` before editing


