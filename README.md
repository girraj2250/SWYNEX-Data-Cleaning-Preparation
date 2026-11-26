# SWYNEX – Data Cleaning & Preparation

A Python/Pandas notebook project for inspecting and preparing an Olist e-commerce dataset.

## Project contents

- `SWYNEX-Data-Cleaning-Preparation.ipynb` – analysis and data-cleaning workflow.
- `olist_master_dataset.csv` – input dataset used by the notebook.
- `output/` – generated cleaned dataset and data-quality reports (created when the notebook is run).

## Work covered

1. Load and inspect the dataset (shape, preview, and data types).
2. Profile missing values and duplicate records.
3. Inspect date columns and convert them to datetime values.
4. Check numeric columns for negative and zero values.
5. Fill missing product categories with `unknown`.
6. Impute missing product dimensions with column medians while preserving flags that identify imputed values.
7. Preserve meaningful missing information such as undelivered-order dates and unavailable review details.
8. Validate the resulting dataset and export quality reports.

## Requirements

- Python 3.9+
- pandas
- numpy
- jupyter

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the project

Keep `olist_master_dataset.csv` in the same folder as the notebook, then open the notebook in VS Code or Jupyter and run all cells from top to bottom.

The final export cell creates an `output/` folder containing:

- `olist_cleaned_dataset.csv`
- `final_missing_values_report.csv`
- `data_quality_summary.csv`

## Notes

The notebook retains selected missing values where filling them would create misleading information. Review the notebook's validation outputs before using the cleaned data for downstream analysis.
