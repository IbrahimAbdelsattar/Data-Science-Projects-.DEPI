# DEPI Employee Attrition Analysis

An employee attrition project combining exploratory analysis, classification experiments, a Streamlit prediction interface, reports, and Power BI dashboards.

**Technology:** Python · scikit-learn · LightGBM/XGBoost/CatBoost · Streamlit · Power BI

## Features

- Analyze employee attributes and associations with attrition.
- Compare classifiers, resampling strategies, feature engineering, and hyperparameter searches.
- Present a Streamlit form for an employee's demographic and employment details.
- Provide separate univariate and bivariate Power BI dashboards and written project reports.

## Repository guide

| Path | Purpose |
|---|---|
| [employee_attrition_prediction_analysis .ipynb](employee_attrition_prediction_analysis%20.ipynb) | EDA, feature engineering, training, and experiment logging. |
| [app (3).py](app%20%283%29.py) | Streamlit attrition prediction form. |
| [streamlit.txt](streamlit.txt) | Recorded hosted-app URL; this is not a pip requirements file. |
| [Dashboard/Univariate dashboard.pbix](Dashboard/Univariate%20dashboard.pbix) | Univariate Power BI dashboard. |
| [Dashboard/Bivariate dashboard.pbix](Dashboard/Bivariate%20dashboard.pbix) | Bivariate Power BI dashboard. |
| [Employee_Attrition_Prediction_Documentation.pdf](Employee_Attrition_Prediction_Documentation.pdf) | Project documentation. |

## Requirements and current limitations

The app expects `final_model.pkl`, which is not committed in the current checkout. Restore the fitted artifact and check its expected column order and categorical mappings before launching. The notebook references several Colab paths and intermediate CSVs; these data files are not all included and must be supplied to reproduce the full workflow.

Power BI `.pbix` files require Power BI Desktop. Notebook training imports additional ML packages beyond the Streamlit runtime list. Predictions are experimental and should not be treated as established employee retention outcomes. `streamlit.txt` contains a hosted URL rather than package requirements; the installation command installs the source app's core runtime packages.

## Getting started

```bash
git clone https://github.com/IbrahimAbdelsattar/Data-Science-Projects-.DEPI.git
cd Data-Science-Projects-.DEPI
```

Use a Python virtual environment:

```bash
python -m venv .venv
```

Activate it with `source .venv/bin/activate` on macOS/Linux or `.venv\Scripts\Activate.ps1` in PowerShell.

```bash
python -m pip install streamlit pandas numpy joblib scikit-learn lightgbm
python -m streamlit run "app (3).py"
```
