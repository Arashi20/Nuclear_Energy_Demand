# Nuclear Energy Demands

Is nuclear energy necessary to meet rising global electricity demand through 2050 while staying within international emissions targets? This project examines the question both globally and regionally, with particular focus on fast-growing developing regions (South/Southeast Asia, Sub-Saharan Africa) where the answer may diverge from advanced economies.

## Methodology

The project follows a five-phase structure:

1. **Data Collection & Cleaning** — ingest and unify three source datasets into a single pipeline (Parquet format)
2. **EDA** — establish the current global energy mix by technology and region
3. **Three Parallel Analysis Modules**
   - *Energy mix analysis* — current technology share by region
   - *Demand gap model* — IEA scenario projections vs. bottom-up renewable buildout from GEM pipeline data
   - *Nuclear pipeline analysis* — planned nuclear capacity discounted by historical delivery rates
4. **GIS Visualizations** — Folium maps of current and pipeline infrastructure; highlight supply-deficit regions
5. **Synthesis** — a data-driven verdict on nuclear necessity

## Data Sources

All raw files live in `data/raw/` (not tracked in git):

| File | Source | Contents |
|---|---|---|
| `Global-Integrated-Power-March-2026-II.xlsx` | GEM — Global Integrated Power Tracker | Unit-level power plants worldwide: capacity, status, fuel type, location, timeline |
| `Global-Nuclear-Power-Tracker-September-2025.xlsx` | GEM — Global Nuclear Power Tracker | Nuclear-specific unit data including development stage |
| `WEO2025_AnnexA_Free_Dataset_World.csv` | IEA World Energy Outlook 2025 | Global electricity demand projections to 2050 (3 scenarios) |
| `WEO2025_AnnexA_Free_Dataset_Regions.csv` | IEA World Energy Outlook 2025 | Regional electricity demand projections to 2050 (3 scenarios) |
| `Statistical Review of World Energy Narrow format.csv` | Energy Institute 2025 | Historical energy production/consumption by country & fuel, 1965–2024 |

IEA scenarios: **Current Policies**, **Stated Policies (STEPS)**, **Net Zero Emissions by 2050 (NZE)**.

Cleaned, unified data is written to `data/processed/` as Parquet files.

## Tech Stack

- **Language:** Python, primarily via Jupyter notebooks
- **Data wrangling:** pandas, GeoPandas
- **Storage:** Parquet
- **Interactive viz:** Folium (maps), Plotly (charts)
- **Static viz:** Matplotlib, Seaborn
- **Modeling:** Scikit-learn (trend modeling)


## Setup

```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
jupyter lab
```

## Status

Data ingestion and cleaning into Parquet is complete (`notebooks/00_sanity_check.ipynb`, `notebooks/01_data_ingestion.ipynb`). EDA and the three analysis modules are in progress.
