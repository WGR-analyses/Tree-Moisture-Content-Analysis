\# Tree Moisture Content Analysis



\## Project Overview



This project investigates the \*\*factors influencing the moisture content of trees\*\* using statistical analysis and modeling. The dataset comes from Carnegie Mellon University’s Statistics Data Library (\[treemoist.dat](http://lib.stat.cmu.edu/datasets/treemoist.dat)).



The study applies \*\*exploratory data analysis (EDA)\*\*, \*\*ANOVA\*\*, and \*\*linear regression models\*\* to determine the most significant factors that affect tree moisture.



\## Dataset



\* \*\*Source:\*\* \[CMU Statistics Data Library – treemoist.dat](http://lib.stat.cmu.edu/datasets/treemoist.dat)

\* \*\*Variables considered:\*\*



&nbsp; \* \*\*Species\*\* (Loblolly Pine, Shortleaf Pine, Yellow Poplar, Red Gum)

&nbsp; \* \*\*Branch\*\* (five branches per tree)

&nbsp; \* \*\*Location\*\* (proximal, central, distal)

&nbsp; \* \*\*Transpiration type\*\* (rapid vs. slow)

&nbsp; \* \*\*Response variable:\*\* Moisture content of tree xylem



\## Methodology



1\. \*\*Exploratory Data Analysis (EDA):\*\*



&nbsp;  \* Summary statistics, boxplots, and correlation analysis.

&nbsp;  \* Identified that \*\*species\*\* has the strongest relationship with moisture content.



2\. \*\*ANOVA Testing:\*\*



&nbsp;  \* Conducted one-way and two-way ANOVA to evaluate factor significance.

&nbsp;  \* Found \*\*species, location, and transpiration type\*\* significantly influence moisture content.

&nbsp;  \* The \*\*branch factor\*\* was discarded (no meaningful impact).



3\. \*\*Model Fitting (Linear Regression):\*\*



&nbsp;  \* Built two models:



&nbsp;    \* \*\*Model 1:\*\* Species + Location + Transpiration

&nbsp;    \* \*\*Model 2:\*\* Adds interaction effects (e.g., Species × Transpiration, Location × Transpiration)

&nbsp;  \* \*\*Model 1 performed best\*\*: Simpler, interpretable, and statistically valid.



4\. \*\*Model Assessment:\*\*



&nbsp;  \* Residual plots, QQ plots, and homoscedasticity checks confirm that Model 1 adequately explains variance.

&nbsp;  \* Outliers exist but do not invalidate the model.



\## Final Regression Model



$$

Moisture = β\_0 + β\_1 \\cdot Loblolly + β\_2 \\cdot Shortleaf + β\_3 \\cdot YellowPoplar + γ\_1 \\cdot Proximal + γ\_2 \\cdot Central + ψ\_1 \\cdot Transpiration + ϵ

$$



Where coefficients were estimated as:



\* $β\_0 = 1119.8$

\* $β\_1 = 140.2$

\* $β\_2 = -153.3$

\* $β\_3 = 74.5$

\* $γ\_1 = 112.3$

\* $γ\_2 = 65.0$

\* $ψ\_1 = -114.6$



\## Key Findings



\* \*\*Species is the most significant factor\*\* in determining tree moisture content.

\* \*\*Location and transpiration\*\* also play an important role.

\* \*\*Branch variable\*\* has no significant effect and was excluded.

\* A \*\*simpler regression model (Model 1)\*\* is preferred over complex interaction models.



\## Technologies Used



\* \*\*Python / R\*\* (statistical modeling and visualization)

\* \*\*Pandas, NumPy, Matplotlib, Statsmodels / Scikit-learn\*\*

\* \*\*ANOVA and Linear Regression\*\*



\## Project Structure



```

├── Report\_1.Rmd

├── A2 group 48 anova.pdf

└── README.md                 # Project documentation

```



\## Authors



Group 48 — Rongjun Gao, Wanchai Grossrieder, Niels Willems





