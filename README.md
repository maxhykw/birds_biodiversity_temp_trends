# Final Project - Birds Biodiversity Temporal Trends

**Course:** Applied Statistics

**Authors:**
* Maxime HAYAKAWA IVANOVIC, 22200290
* Lubin LONGUEPEE, 22203008
* Lounès KEBDI, 22205548

## 1. Project Overview

This project analyzes the long-term monitoring data from the **Martinique Breeding Bird Monitoring Initiative** (2012-2025).

The primary goal is to conduct an independent statistical analysis to:
* Quantify how biodiversity indicators have evolved over time.
* Provide sound statistical uncertainty assessments for these trends.
* Highlight and analyze species-specific population changes.

This repository contains the full analysis, from raw data loading and cleaning to indicator calculation, trend modeling (linear and LOESS), species-level investigation, and weather effects analysis (bonus).

### A Note on Project Structure
Per the assignment brief, the analysis is structured into parts. **Part 4 (Synthesis and Recommendations)** is integrated throughout Parts 1, 2, and 3. Additionally, we include a **Bonus Part 4: Weather Effects Analysis** that examines how meteorological conditions (rainfall and cloud cover) influence bird observations and species-specific detection patterns.

## 2. Folder Contents

This archive contains the following files and directories:

```
├── README.md                 <-- This file
├── report.pdf                <-- The technical report PDF
├── projet_stats_final.ipynb  <-- The main Jupyter Notebook with all code
|
├── data/
│   └── raw/
│       └── Observations 2012-2025.xlsx  <-- The raw dataset
|
├── figures/                  <-- All generated plots and visualizations
│   ├── part_1/
│   │   ├── effort_metric.png
│   │   ├── categorical_metric.png
│   │   ├── heatmap_points_par_transect_annee.png
│   │   └── heatmap_visites_par_transect_annee.png
│   ├── part_2/
│   │   ├── all_indicators_2x2.png
│   │   ├── all_indicators_with_trends_2x2.png
│   │   └── indicators_with_loess.png
│   └── part_3/
│       ├── species_all_comparison_counts_presence.png
│       ├── species_comparison_heatmap_counts.png
│       ├── species_comparison_by_group.png
│       ├── species_temporal_correlation_matrix.png
│       └── species_trends_normalized_overlay.png
│   └── part_4/                <-- Bonus: Weather effects analysis -- not the assignment 'Part 4'.
│       ├── global_weather_effects.png
│       └── weather_sensitive_species.png
|
└── results/                  <-- All generated tables, CSVs, and method notes
    ├── part_1/
    │   └── removed_rows_clean.csv
    ├── part_2/
    │   ├── indicators_annual_with_ci.csv
    │   ├── indicators_trends_linear.csv
    │   ├── indicators_trends_loess.csv
    └── part_3/
        ├── species_annual_counts_presence_ci.csv
        ├── species_trends_counts_presence.csv
        ├── species_selection_reasons.csv
        ├── species_habitat_specificity.csv
        ├── species_comparative_stats.csv
        ├── species_temporal_correlations.csv
    └── part_4/                <-- Bonus: Weather effects analysis -- not the assignment 'Part 4'.
        └── species_weather_sensitivity.csv
```

## 3. Environment & Reproduction

### 3.1. Environment Details

This analysis was conducted using Python 3. The main libraries required are listed below. It is recommended to use a virtual environment.

* `python (>= 3.9)`
* `jupyter`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `statsmodels`
* `scipy`

You can install these using pip:
`pip install pandas numpy matplotlib seaborn statsmodels scipy jupyter`

### 3.2. Reproduction Instructions

To reproduce the analysis, please follow these steps:

1.  **Place Data:** Ensure the raw data file, `Observations 2012-2025.xlsx`, is placed inside the `data/raw/` directory.
2.  **Run Notebook:** Open and run the `projet_stats_final.ipynb` notebook from top to bottom.
3.  **Check Outputs:** The notebook will automatically create the `figures/` and `results/` directories (and their sub-parts) and regenerate all the plots and CSV files listed in Section 2.
4.  **Read Report:** For a full, self-contained explanation of our approaches, indicators choice, and for the conclusions, please refer to `report.pdf`. The notebook itself also contains markdown cells with code-level explanations.labels 