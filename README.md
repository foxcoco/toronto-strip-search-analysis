# Toronto Police Strip Search & Mental Health Analysis

A statistical analysis of 65,276 arrest and strip search records from the Toronto Police Service (2020–2021), investigating the effects of gender, age group, year, and location on strip search practices and mental health-related incidents.

## Key Findings

- **Gender disparity in strip searches**: Males experience significantly more strip searches than females, with an estimated 373.93 more strip searches on average (p = 0.024).
- **Year-over-year decline**: Strip searches decreased significantly from 2020 to 2021 (p = 0.007), but cases involving mentally unstable individuals increased.
- **Location hotspots**: Division 51 had the highest concentration of mental health-related cases — more than double the second-ranked division.
- **Brand loyalty of demographics**: Logistic regression (88% accuracy) confirmed that males aged 25–44 are most likely to be strip searched; a second model (96% accuracy) identified division-level predictors for mental health incidents.

## Methods

| Method | Purpose |
|---|---|
| Power Analysis | Determine required sample size for reliable effect detection |
| Welch's T-Test | Compare strip search and mental health case counts between genders |
| Two-Way ANOVA (×4) | Test main effects and interactions of Sex, Year, Age Group, and Location |
| Tukey HSD Post-Hoc | Identify which specific group pairs differ significantly |
| ANCOVA (×4) | Assess gender effects while controlling for covariates (year, location, age) |
| Interaction Plots | Visualize relationships between categorical predictors |
| Logistic Regression (×2) | Predict strip search likelihood and mental health incident flags |

## Tech Stack

- **Python 3** — Pandas, NumPy, Matplotlib, Seaborn
- **Statistical Modeling** — SciPy, Statsmodels (OLS, ANOVA, Logistic Regression)
- **Machine Learning** — scikit-learn (train/test split, confusion matrix, accuracy scoring)

## Dataset

Source: [Toronto Police Service — Arrests & Strip Searches](https://data.torontopolice.on.ca/datasets/TorontoPS::arrests-strip-searches/about)

The dataset contains **65,276 records** across 25 features including arrest year/month, sex, age group, arrest location division, strip search flag, mental instability flag, and various action-at-arrest indicators.

## Project Structure

```
├── README.md
├── data/
│   └── Arrests_and_Strip_Searches.csv
├── notebook/
│   └── toronto_strip_search_analysis.ipynb
└── report/
    └── Toronto_Strip_Search_Mental_Health_Report.pdf
```

## Contributions

This was a two-person research project completed during my Master's program at the University of Toronto. My primary contributions included:

- Exploratory data analysis and all visualization work (bar charts, box plots, interaction plots)
- Data preprocessing and aggregation pipeline
- ANOVA testing and post-hoc analysis
- ANCOVA modeling and interpretation
- Report writing (Results, Discussion, and Conclusion sections)

## License

This project uses publicly available data from the Toronto Police Service Open Data portal. The analysis is provided for educational and research purposes.
