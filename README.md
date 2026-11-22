# Food Delivery Operations — Complete Data Analytics Project

**Kagnus project | End-to-end Python analysis (all four stages in one submission)**

## Objective
Prepare the food-delivery dataset, document quality checks, explore operational factors associated with delivery duration, create six charts, and communicate evidence-backed recommendations. **Association is not causation.**

## Dataset
Kagnus dataset: https://drive.google.com/file/d/1O9WYS92iJPZoC6skyYlpcdP8Kre7eW6z/view?usp=sharing

- Original dataset: **45,584 rows × 20 columns**.
- Cleaned dataset: **45,584 rows**; no automatic row deletion.
- Mean delivery duration: **26.29 minutes**.
- Original CSV is not redistributed until its license is confirmed. Follow `data/raw/README.md`.

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter / Google Colab.

## Repository contents
```
data/raw/README.md                       # dataset access instructions
data/processed/cleaned_food_delivery.csv # prepared dataset
notebooks/01_data_understanding_and_cleaning.ipynb # raw-data inspection and cleaning
notebooks/02_complete_food_delivery_analysis.ipynb # complete EDA, charts, findings
docs/cleaning_log.csv                    # documented cleaning decisions
docs/*_summary.csv                       # group comparison tables
charts/*.png                             # six evidence-backed visualizations
reports/Food_Delivery_Analysis_Final_Report.pdf
requirements.txt
```

## How to run
1. Download repository ZIP or clone it. Install dependencies with `pip install -r requirements.txt`.
2. Open `notebooks/02_complete_food_delivery_analysis.ipynb` in Jupyter, or upload to Google Colab with repository files available in the expected directory layout.
3. Run all cells. It reads the already-prepared `data/processed/cleaned_food_delivery.csv`.
4. To reproduce raw cleaning, first obtain the raw CSV from Kagnus and run `01_data_understanding_and_cleaning.ipynb` from the project root. Note: Colab file paths require mounting/uploading the project directory.
5. Read the final PDF report and inspect `charts/` and `docs/`.

## Findings and caveats
- **Traffic**: highest mean category `Jam` (31.18 min), lowest `Low` (21.27 min). Compare sample sizes in `docs/traffic_summary.csv`.
- **Weather**: highest mean category `Cloudy` (28.92 min), lowest `Sunny` (21.86 min). Compare sample sizes in `docs/weather_summary.csv`.
- **Vehicle**: highest mean category `motorcycle` (27.61 min), lowest `electric_scooter` (24.47 min). Compare sample sizes in `docs/vehicle_summary.csv`.
- **City**: highest mean category `Semi-Urban` (49.73 min), lowest `Urban` (22.98 min). Compare sample sizes in `docs/city_summary.csv`.
- **Multiple**: highest mean category `3.0` (47.82 min), lowest `0.0` (22.88 min). Compare sample sizes in `docs/multiple_summary.csv`.

Missing fields, anomalous coordinates, undocumented variable codes and observational confounding limit interpretation. Straight-line distance is not road distance. No machine learning is required by the brief.



## Week 2 — Exploratory Data Analysis (EDA)

Continued using the cleaned dataset from Week 1 (45,584 records).

### Analysis completed
- Calculated delivery-time statistics: count, mean, median, minimum, maximum, quartiles, and standard deviation.
- Compared delivery durations across traffic conditions, weather conditions, and vehicle types.
- Examined delivery-person ratings and multiple-delivery counts.
- Calculated the Pearson correlation between approximate straight-line distance and delivery duration.
- Created an initial distance-versus-duration scatter plot.
- Documented six numerical observations with group sizes and interpretations.

### Week 2 deliverables
- `notebooks/02_exploratory_data_analysis.ipynb`
- `visualizations/initial_distance_vs_duration.png`

### Limitations
Delivery-partner experience in years is not available in the dataset. Delivery-person age is not used as a substitute for experience. Approximate straight-line distance differs from actual road distance. Observed relationships do not establish causation.

## Week 3 — Visualization & Interpretation

Continued using the cleaned food delivery dataset from Weeks 1 and 2 to create five finalized visualizations using Python, Pandas, NumPy, Matplotlib, and Seaborn.

### Visualizations Created

1. **Delivery Duration Distribution — Histogram:** Shows the frequency and distribution of delivery durations, including the concentration of values and potential extreme observations.
2. **Traffic Comparison — Bar Chart:** Compares median delivery duration across traffic categories to highlight observed differences.
3. **Weather Comparison — Bar Chart:** Compares mean delivery duration across weather conditions to identify higher and lower averages.
4. **Distance vs Delivery Duration — Scatter Plot:** Examines the relationship between approximate straight-line delivery distance and delivery duration, including unusual coordinate-derived distances.
5. **Vehicle Comparison — Box Plot:** Compares delivery-duration medians, interquartile ranges, spread, and outliers across vehicle types.

### Week 3 Deliverables

- [Week 3 Visualization Notebook](notebooks/03_visualization.ipynb)
- [01 — Delivery Duration Distribution](visualizations/01_delivery_duration_distribution.png)
- [02 — Traffic Comparison](visualizations/02_traffic_comparison.png)
- [03 — Weather Comparison](visualizations/03_weather_comparison.png)
- [04 — Distance vs Duration](visualizations/04_distance_vs_duration.png)
- [05 — Vehicle Comparison](visualizations/05_vehicle_comparison.png)

### Main Observations and Limitations

The dataset has an overall average delivery duration of approximately 26.29 minutes. Earlier exploratory analysis found higher average delivery durations for Jam traffic than Low traffic, and for Cloudy weather than Sunny weather. The Week 3 charts present the corresponding distributional and group comparisons, with numerical results and 2–3 sentence interpretations in the visualization notebook.

Delivery distances are approximate straight-line measurements rather than actual road distances. Some coordinate values are anomalous, and differences between categories may reflect other operational factors. The observed associations do not establish causation.

The Week 1 and Week 2 notebooks and outputs have been preserved.
