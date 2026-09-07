# Seasonal Agriculture Performance Analysis

This project looks at how farm performance changes across the **Kharif, Rabi, and Zaid** seasons. I use the dataset to compare yield, profit, water use, environmental conditions, crop choice, and irrigation methods.

The goal is not to declare one season or farming method universally best. It is to understand the patterns in this dataset and identify questions worth checking more closely in real farm settings.

## What is in this project?

- `Seasonal_Agriculture_Performance_Analysis.ipynb` - the full exploratory analysis, calculations, charts, and statistical checks
- `seasonal_agriculture_performance_dataset.csv` - the farm-level data used by the notebook

Each row represents a farm observation for a season. The data includes location, crop, season, farm area, weather and soil conditions, inputs, yield, production, costs, revenue, profit, water use, and disease or pest risk.

## Questions explored

- How does performance differ between the three seasons?
- Which seasons have stronger yield, profit, water efficiency, and loss-rate results?
- How do crop and irrigation choices compare within a season?
- What relationships appear between inputs, environmental conditions, yield, and profit?
- Are there unusual records that deserve a second look?

## Approach

The notebook:

1. Loads and inspects the CSV file.
2. Checks missing values, duplicate rows, unusual values, and basic financial consistency.
3. Fills missing numeric values with column medians when needed.
4. Adds ROI, profit margin, profit-per-hectare, revenue-to-cost ratio, and outcome labels.
5. Compares seasons using summary tables and visualizations.
6. Reviews crop-season and crop-irrigation groups, using minimum group sizes where small samples could mislead.
7. Examines distributions, correlations, regional patterns, and high-yield outliers.
8. Uses a Kruskal-Wallis test to check whether profit distributions differ across seasons.

## Tools

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- SciPy

## Running the notebook

Open the notebook in JupyterLab, Jupyter Notebook, or VS Code, then run the cells from top to bottom. The CSV file should stay in the same folder as the notebook because it is loaded with a relative path.

To install the libraries in a local Python environment:

```bash
python -m pip install pandas numpy matplotlib scipy jupyter
```

The notebook uses `display()` in one section, so a normal Jupyter or VS Code notebook session is recommended instead of running the file as a plain Python script.

## A note about interpretation

These results describe associations in the available records. They do not prove that a season, crop, irrigation method, or input caused a particular outcome. Farms may differ in ways that are not fully captured here, including soil, local prices, management practices, and weather.

The outlier flags are also prompts for review, not automatic evidence of bad data. Any practical farming decision should be checked against local conditions, costs, and field experience.