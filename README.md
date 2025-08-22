# Tree Moisture Content Analysis

## Project Overview

This project investigates the **factors influencing the moisture content of trees** using statistical analysis and modeling. The dataset comes from Carnegie Mellon University’s Statistics Data Library ([treemoist.dat](http://lib.stat.cmu.edu/datasets/treemoist.dat)).

The study applies **exploratory data analysis (EDA)**, **ANOVA**, and **linear regression models** to determine the most significant factors that affect tree moisture.

## Dataset

- **Source:** [CMU Statistics Data Library – treemoist.dat](http://lib.stat.cmu.edu/datasets/treemoist.dat)
- **Variables considered:**
  - **Species** (Loblolly Pine, Shortleaf Pine, Yellow Poplar, Red Gum)
  - **Branch** (five branches per tree)
  - **Location** (proximal, central, distal)
  - **Transpiration type** (rapid vs. slow)
  - **Response variable:** Moisture content of tree xylem

## Methodology

1. **Exploratory Data Analysis (EDA):**
   - Summary statistics, boxplots, and correlation analysis.
   - Identified that **species** has the strongest relationship with moisture content.

2. **ANOVA Testing:**
   - Conducted one-way and two-way ANOVA to evaluate factor significance.
   - Found **species, location, and transpiration type** significantly influence moisture content.
   - The **branch factor** was discarded (no meaningful impact).

3. **Model Fitting (Linear Regression):**
   - Built two models:
     - **Model 1:** Species + Location + Transpiration
     - **Model 2:** Adds interaction effects (e.g., Species × Transpiration, Location × Transpiration)
   - **Model 1 performed best**: Simpler, interpretable, and statistically valid.

4. **Model Assessment:**
   - Residual plots, QQ plots, and homoscedasticity checks confirm that Model 1 adequately explains variance.
   - Outliers exist but do not invalidate the model.

## Final Regression Model

Moisture = β₀ + β₁ · Loblolly + β₂ · Shortleaf + β₃ · YellowPoplar + γ₁ · Proximal + γ₂ · Central + ψ₁ · Transpiration + ϵ

Where coefficients were estimated as:

- β₀ = 1119.8
- β₁ = 140.2
- β₂ = -153.3
- β₃ = 74.5
- γ₁ = 112.3
- γ₂ = 65.0
- ψ₁ = -114.6

## Key Findings

- **Species is the most significant factor** in determining tree moisture content.
- **Location and transpiration** also play an important role.
- **Branch variable** has no significant effect and was excluded.
- A **simpler regression model (Model 1)** is preferred over complex interaction models.

## Technologies Used

- **Python / R** (statistical modeling and visualization)
- **Pandas, NumPy, Matplotlib, Statsmodels / Scikit-learn**
- **ANOVA and Linear Regression**

## Project Structure

```
├── Report_1.Rmd
├── A2 group 48 anova.pdf
└── README.md                 # Project documentation
```

## Authors

Group 48 — Rongjun Gao, Wanchai Grossrieder, Niels Willems
