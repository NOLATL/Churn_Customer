# Customer Churn Prediction: Synthetic Data Modeling Pipeline

## Overview

This project demonstrates an end-to-end workflow for customer churn prediction using a synthetic dataset generated to simulate transactional and profile data. Although the data is illustrative and randomly generated, all best practices for data science, preprocessing, feature engineering, modeling (manual and automated), and reporting are showcased.

The notebook is designed as a template and technical demonstration for **real-world churn modeling** that includes robust EDA, careful leakage avoidance, and validation strategies commonly used when forecasting at-risk customers in business settings.

---

## Contents

- `Churn_Customer_Final.ipynb` – Main Jupyter Notebook (data prep → modeling → analysis)
- `Env_CustChurn.yml` – Conda environment file with all dependencies (see below)
- Data files in `data/raw/` (synthetic Parquet format)
    - `customers.parquet`
    - `sites.parquet`
    - `transactions.parquet`
- This README file

---

## Project Steps

1. **Data Creation**  
   - Synthetic customers, sites, and transactions, engineered for realistic structure and feature engineering flexibility.

2. **Exploratory Data Analysis (EDA)**
   - Shape review, basic stats, missingness, outlier treatment, and validation of churn definition.

3. **Churn Analysis**
   - Labeling using inactivity rules, visualization of churn breakdown, and segment comparisons.

4. **Data Preparation for Modeling**
   - Aggregates, ratios, outlier capping, join logic, and rigorous leakage prevention.

5. **Manual Modeling Pipelines**
   - End-to-end workflows for Random Forest, Logistic Regression, SVM, Naive Bayes, and XGBoost using `imblearn` and cross-validation.

6. **Automated PyCaret Modeling**
   - Rapid candidate model comparison, hyperparameter tuning, and leaderboard generation with feature selection support.

7. **Interpretation & Conclusion**
   - Metrics summary, limitations of the synthetic data (AUC expected to be ~0.5), and discussion of future improvement for production use.

---

## Reproducibility & Environment

All dependencies are managed via the provided Conda environment file:

bash conda env create -f Env_CustChurn.yml conda activate CustChurn



**Key Libraries:**
- pandas, numpy, matplotlib, seaborn, plotly
- scikit-learn, imbalanced-learn, xgboost
- pycaret (for automated modeling)
- notebook/jupyterlab

*See `Env_CustChurn.yml` for full specification.*

---

## Results & Limitations

> This project builds a robust, modular churn prediction stack—but uses purely random/simulated (“safe”) data to make the pipeline reproducible for demonstration.  
>
> As expected, **model performance is near random (AUC ≈ 0.5)** due to the lack of real feature-target signal. The primary benefit is to demonstrate pipeline quality, feature engineering, model selection, and rigorous workflow, which can be reused on production business data.

---

## How To Use

1. Clone/download this repository
2. Set up the conda environment (above)
3. Open the notebook and run all cells in order (or stepwise to see commentary/plots for each stage)
4. Review markdown summaries and visualizations for analytical workflow and results best practices

---

## License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Acknowledgements

- This notebook and project structure is inspired by real-world business churn modeling requirements and draws on best practices from both open-source and enterprise data science teams.
- All data is generated synthetically for public demonstration and does **not** reflect any real customer information.

---

*Questions or feedback? Open an issue or submit a pull request!*