# SQL Database Analysis — Taxi Rides in Chicago

Analysis of the results of SQL queries run against a taxi rides database: which companies run the most trips, which neighborhoods receive the most drop-offs, and whether rainy days change ride duration.

TripleTen Data Analyst program project — Mara Torres Blanco.

## What this project does

The SQL queries behind this project were written to answer business questions about a taxi rides database (companies, neighborhoods and rides). This notebook works with the query result files and:

1. **Ranks taxi companies** by number of trips (64 companies).
2. **Ranks neighborhoods** by average number of drop-off trips (94 neighborhoods).
3. **Tests a hypothesis** with a statistical test: does the average duration of rides from the Loop to Chicago O'Hare International Airport change on rainy days?

## Tools

- Python
- Pandas
- Matplotlib
- SciPy (statistical tests)

## Key findings

### Companies and neighborhoods

- A **small number of companies concentrate most of the trips**, suggesting a concentrated market.
- The analysis covers **64 companies** and **94 neighborhoods** (drop-off locations).

### Rainy days and ride duration (Loop → O'Hare)

- Average ride duration on rainy days: **2,427 seconds** vs. **2,000 seconds** on dry days.
- The difference is statistically significant (**p ≈ 6.74e-12**), so the null hypothesis is rejected: rainy days do change the average duration of Loop → O'Hare rides.
- Likely causes noted in the analysis: heavier traffic congestion, lower driving speeds and more difficult road conditions.

## Data

- `project_sql_result_01.csv` — trips per company (64 companies).
- `project_sql_result_04.csv` — average trips per drop-off neighborhood (94 neighborhoods).
- `project_sql_result_07.csv` — ride durations for the hypothesis test.

**The datasets are not included in this repository** — they are the result files of the SQL queries run on the TripleTen learning platform. The notebook will not run without them; the code and outputs are preserved as delivered.

## Files

- `sql_database_analysis.ipynb` — the analysis notebook (36 cells).
- `README.md` — this file.

## How to run

Open `sql_database_analysis.ipynb` in Jupyter Notebook or JupyterLab and run the cells top to bottom. It expects `project_sql_result_01.csv`, `project_sql_result_04.csv` and `project_sql_result_07.csv` in the same folder (not included — see Data above).
