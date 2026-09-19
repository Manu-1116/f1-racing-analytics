# F1 Racing Performance Analytics (2019-2023)

An end-to-end analytics project on Formula 1 racing performance, built entirely on live data pulled from a public REST API (Jolpica-F1), covering race results, lap-by-lap timing, and pit stop data.

## Dashboard

![Dashboard Screenshot](dashboard/dashboard_screenshot.png)

## Project Overview

This project analyzes real F1 data to answer key performance questions:

- Which constructors dominated the 2019-2023 seasons?
- How did the 2023 championship battle unfold race by race?
- Which teams have the fastest pit crews?
- Which races produced the most unpredictable, high-scoring drives?

## Tools Used

- **Python** (requests, pandas, matplotlib) — API data collection, cleaning, and exploratory analysis
- **SQL** (PostgreSQL) — window functions for lap-by-lap position tracking, pit stop analysis
- **Tableau** — interactive dashboard

## Key Findings

- Red Bull and Mercedes led constructor points from 2019-2023, with Red Bull's dominance peaking in 2023
- Max Verstappen's 2023 championship progression shows a dramatic, early points lead that widened every race
- Red Bull's pit crew ranked among the fastest, averaging under 23 seconds per stop (excluding red-flag-affected stops)
- The Belgian Grand Prix (Round 13, 2023) showed the highest lap-by-lap position churn of the season, driven by a rain-affected red flag restart

## Project Structure

- `data/` — collected datasets (race results, lap times, pit stops)
- `notebooks/` — Python data collection and analysis (Jupyter notebooks)
- `sql/` — SQL queries (pit stop performance, position battles)
- `dashboard/` — Tableau dashboard (.twbx) and screenshot

## Data Source

[Jolpica-F1 API](https://github.com/jolpica/jolpica-f1) — a free, open replacement for the retired Ergast F1 API

## How to Run

1. Clone this repo
2. Run `01_data_collection.ipynb` to pull fresh data from the API (or use the CSVs already saved in `data/`)
3. Run `02_sql_analysis.ipynb` to load data into PostgreSQL for SQL analysis
4. Open `dashboard/f1_dashboard.twbx` in Tableau (Public or Desktop) to view the interactive dashboard
