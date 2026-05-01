# Survival Analysis in Lung Cancer

## Overview

This project applies survival analysis methods to advanced lung cancer data from the **North Central Cancer Treatment Group (NCCTG)** cohort, a benchmark dataset freely available in the R `survival` package. The analysis covers the full statistical pipeline used in clinical research for time-to-event data: descriptive characterisation, non-parametric survival estimation, multivariate proportional-hazards modelling, and assumption diagnostics.

Reports are available in both **English** and **French**.

## 📊 View the rendered reports

- **English**: [survival_analysis_oncology_EN.html](https://killianfoubert.github.io/survival-analysis-lung-cancer/survival_analysis_oncology_EN.html)
- **Français**: [analyse_survie_oncologie.html](https://killianfoubert.github.io/survival-analysis-lung-cancer/analyse_survie_oncologie.html)

## What this project demonstrates

* **Descriptive analysis** of patient characteristics by sex with appropriate parametric and non-parametric tests
* **Kaplan-Meier estimation** of overall and stratified survival curves with log-rank tests
* **Univariate and multivariate Cox proportional-hazards modelling** with hazard ratio interpretation
* **Forest plot visualisation** of adjusted hazard ratios and confidence intervals
* **Diagnostic testing** of the proportional hazards assumption via Schoenfeld residuals
* **Bilingual reporting** suitable for international clinical research teams

## Key findings

| Result | Detail |
|:-------|:-------|
| **Overall median survival** | 310 days |
| **Effect of sex** | Female patients show significantly better survival |
| **Effect of ECOG score** | Strongest prognostic factor; each level of functional decline corresponds to a substantial drop in survival |
| **Multivariate Cox model** | Sex and ECOG retained as significant independent predictors |
| **Proportional hazards** | Assumption satisfied (Schoenfeld global test, p > 0.05) |

## Project structure

```
survival-analysis-lung-cancer/
├── README.md
├── survival_analysis_oncology_EN.Rmd     # Full analysis report (English)
├── survival_analysis_oncology_EN.html    # Rendered report (English)
├── analyse_survie_oncologie.Rmd          # Full analysis report (French)
├── analyse_survie_oncologie.html         # Rendered report (French)
└── assets/
    ├── styles.css                        # Editorial design styling
    ├── hero_en.html                      # English hero section
    └── hero_fr.html                      # French hero section
```

The dataset is loaded directly from the `survival` package (no external data file required).

## How to reproduce

1. Clone the repository: `git clone https://github.com/KillianFoubert/survival-analysis-lung-cancer.git`
2. Install required packages:

```r
install.packages(c("survival", "survminer", "broom", "gtsummary",
                   "dplyr", "tidyr", "ggplot2", "knitr", "kableExtra",
                   "here", "base64enc", "htmltools"))
```

3. Open `survival_analysis_oncology_EN.Rmd` (or `analyse_survie_oncologie.Rmd`) in RStudio and click **Knit**

## Reference

Loprinzi CL, Laurie JA, Wieand HS, et al. Prospective evaluation of prognostic variables from patient-completed questionnaires. *Journal of Clinical Oncology*. 1994;12(3):601-607.

Therneau TM, Grambsch PM. *Modeling Survival Data: Extending the Cox Model*. Springer, 2000.

## Author

**Killian Foubert, Ph.D.**

* Portfolio: [killianfoubert.github.io](https://killianfoubert.github.io)
* GitHub: [github.com/KillianFoubert](https://github.com/KillianFoubert)
* LinkedIn: [linkedin.com/in/kfoubert](https://linkedin.com/in/kfoubert/)

## License

MIT
