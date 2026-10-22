# Healthcare Data Analytics & Executive Dashboard

A healthcare analytics portfolio project using Python, Pandas, NumPy and Matplotlib, with a standalone HTML executive dashboard for management-oriented review.

## Project overview

The notebook explores a healthcare records dataset, performs basic cleaning and date preparation, derives length of stay, and investigates patient mix, billing patterns, insurance-provider record counts and emergency admission signals. The HTML dashboard presents selected business findings without exposing the analysis workflow.

## Key findings in the current analysis

- **54,966 records** after duplicate removal.
- **Average billing:** 25,594.54 per record (the dataset does not specify a currency in the analysis).
- **Average patient age:** about 51.5 years; ages range from 13 to 89.
- **Average length of stay:** about 15.5 days.
- **Arthritis** has the highest record count (9,218), closely followed by Diabetes (9,216).
- **Obesity** has the highest average billing among the six medical conditions in the analysis.
- The linear correlation between age and billing is approximately **-0.003**, essentially zero.
- Insurance counts are record counts, not confirmed unique patients, because the dataset has no unique patient identifier.
- Emergency admissions with abnormal test results: **6,038 records** in the analysis.

These are dataset-level findings, not clinical recommendations or conclusions about the entire real-world healthcare network.

## Files

- `healthcare_analysis.ipynb` — Jupyter Notebook source. Outputs have been cleared in this repository copy to avoid publishing rendered patient-level rows/names.
- `Healthcare Analytics Dashboard.html` — self-contained executive dashboard; open directly in a browser.
- `data/README.md` — instructions for placing the source CSV locally.
- `requirements.txt` — Python dependencies for the notebook.

## Run the notebook

1. Install Python 3.9+ and Jupyter.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Place your authorized copy of `healthcare_dataset.csv` in the project root, beside `healthcare_analysis.ipynb`.
4. Open `healthcare_analysis.ipynb` in Jupyter Notebook or JupyterLab and run the cells.

The source CSV is intentionally not included. Only upload a dataset you are authorized to share, and remove real patient identifiers or protected health information before publishing.

## View the dashboard

Open `healthcare_executive_dashboard.html` directly in a modern browser. It does not require a server or external JavaScript libraries.

## Tools

- Python
- Pandas and NumPy
- Matplotlib
- Jupyter Notebook
- Claude (AI-assisted dashboard development)

## Limitations

- The source data does not provide a unique patient ID, so counts are treated as records rather than verified unique individuals.
- Average billing is grouped by admission month in the notebook; it represents the average bill for records admitted in that month, not spending incurred during that month.
- Correlation measures linear association and does not prove causation.
- The dashboard is built from the summarized results available in the notebook; filters only affect supported category breakdowns and do not recalculate every KPI from row-level data.
