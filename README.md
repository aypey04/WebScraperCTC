# Salary Profiling Bot 💼📊

A smart, automated salary intelligence engine that scrapes salary data for multiple companies from public platforms like **AmbitionBox**, classifies them by role and compensation tier, and generates a visual Excel report.

---

## Features

- Uses **Selenium (Undetected ChromeDriver)** to automate Google searches and navigate AmbitionBox salary pages
- Extracts salary data for roles like **Software Engineer**, **Data Analyst**, and **QA** from structured HTML tables
- Classifies companies into **salary tiers (High / Medium / Low / Unknown)** based on role-specific average CTC
- Outputs an Excel file with **color-coded rows** highlighting the highest-paying roles per company
- Accepts a **CSV of company names** as input; supports batch scraping for 100+ companies
- Robust scraping with dynamic waits, exception handling, and clean exit on failures

---

##  Input Format (CSV)

Your input file should be a `.csv` with at least one column named `Company`:

```csv
Company
Google
Amazon
TCS
...
```

---

##  How to Run

```bash
# Install dependencies
pip install pandas openpyxl selenium undetected-chromedriver

# Place your input CSV (e.g., input.csv) in the same folder

# Run the scraper
python scraper.py
```

The output will be saved as `salaries_output.xlsx`.

---

## Tech Stack

- Python 3.x
- Selenium (Undetected ChromeDriver)
- Pandas
- OpenPyXL
- Google Search + AmbitionBox

---

## Sample Output (Excel)

- Columns: Company | Top 3 Roles | Highest Paying Role
- Color-coded rows:
  - 🟩 Green = ₹20L+ CTC
  - 🟨 Yellow = ₹15L–₹20L
  - 🟧 Orange = ₹10L–₹15L
  - 🟥 Red = < ₹10L

---

## Disclaimer

This project is for educational purposes. Data is scraped from public sources and may not reflect accurate or updated compensation figures.

---

##  License

MIT License. Free to use, modify, and extend.

---
