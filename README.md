# Analysis

A collection of two exploratory data analysis notebooks written in Python with pandas, matplotlib, and seaborn:

- **`ipl.ipynb`** — explores an IPL (Indian Premier League) cricket dataset (`matches.csv`, `deliveries.csv`), looking at player-of-the-match awards, toss results, wins batting first vs. second, matches per season/city, and per-delivery breakdowns for individual matches, visualized with bar plots, histograms, and pie charts.
- **`covid-19.ipynb`** — explores a COVID-19 case/testing dataset (`covid.csv`), filtering by location (India, Brazil, China, Japan, Germany, Spain) and plotting total cases and total tests over time with seaborn line and bar plots.

Note: the CSV data files referenced by the notebooks (`matches.csv`, `deliveries.csv`, `covid.csv`) are not included in this repository, so the notebooks cannot be re-run as-is without supplying that data separately.

## Tech stack

- Python (Jupyter notebooks)
- pandas
- matplotlib
- seaborn
- numpy

## Architecture

```mermaid
flowchart LR
    A[CSV datasets\nmatches.csv / deliveries.csv / covid.csv] --> B[pandas\nload & filter data]
    B --> C[Aggregation\nvalue_counts, groupby-style filters]
    C --> D[matplotlib / seaborn\nbar, pie, histogram, line plots]
    D --> E[Inline notebook output]
```

## How to run

1. Install the dependencies:
   ```
   pip install pandas matplotlib seaborn numpy jupyter
   ```
2. Place the required CSV files (`matches.csv`, `deliveries.csv` for `ipl.ipynb`; `covid.csv` for `covid-19.ipynb`) in the same directory as the notebooks.
3. Launch Jupyter and open the notebook you want to run:
   ```
   jupyter notebook ipl.ipynb
   ```
   or
   ```
   jupyter notebook covid-19.ipynb
   ```
