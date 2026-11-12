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
