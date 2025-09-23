```markdown
# COVID-19 Data Analysis — Assignment 5

This repository contains a Jupyter Notebook that performs exploratory analysis on the provided COVID-19 (confirmed & deaths) datasets and the Worldwide Happiness Report. The goal is to explore potential relationships between COVID-19 impact and happiness indicators (Score, GDP per capita, life expectancy, social support, etc.).

Files included:
- `covid19_happiness_analysis.ipynb` — Jupyter Notebook with code and visualizations.
- Datasets (place in the same folder as the notebook):
  - `covid19_deaths_dataset.csv`
  - `covid19_Confirmed_dataset.csv`
  - `worldwide_happiness_report.csv`
- `requirements.txt` — Python packages used.

How to run:
1. Ensure you have Python 3.7+ installed.
2. (Recommended) Create a virtual environment:
   - python -m venv venv
   - source venv/bin/activate  (Linux/macOS) or venv\Scripts\activate (Windows)
3. Install requirements:
   - pip install -r requirements.txt
4. Start Jupyter:
   - jupyter notebook
5. Open `covid19_happiness_analysis.ipynb` and run the cells.

Notebook overview:
- Loads the CSV datasets.
- Aggregates COVID-19 data to the latest country-level confirmed & deaths totals.
- Attempts to match COVID country names to Happiness dataset country names (fuzzy matching + manual mapping).
- Computes simple metrics (CFR, log confirmed).
- Produces scatter plots and a correlation heatmap between happiness indicators and COVID metrics.
- Provides notes on limitations and suggested next steps (add population data, improve matching, time-series analysis).

Notes & limitations:
- The provided COVID datasets are in wide format (dates as columns); the notebook uses the latest column as the snapshot. If you need a specific date, update the code to use that column.
- Country name matching is heuristic. For robust merges, use ISO country codes or a curated name mapping.
- Per-country totals do not account for population; include population for per-capita rates (cases/deaths per 100k).
- Differences in testing, reporting, age-structure, and policies affect observed COVID metrics and must be considered when drawing conclusions.

If you want, I can:
- Add automatic population lookups (from World Bank) and compute per-capita rates.
- Improve country matching using `pycountry` and ISO codes.
- Produce a cleaned CSV output with merged metrics.
- Generate an HTML summary report / slides.

```
