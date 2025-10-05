# -Statistical-Power-AB-Test-Case-Study
# A/B Test Analysis: E-commerce Landing Page Redesign

![AB Testing](https://img.shields.io/badge/Project-AB_Testing-blue)
![Statistics](https://img.shields.io/badge/Analysis-Statistical_Power-orange)
![Business](https://img.shields.io/badge/Focus-Risk_Mitigation-green)
![Dataset](https://img.shields.io/badge/Data-Kaggle_E--commerce-lightgrey)

##  Project Overview

This project analyzes an A/B test for an e-commerce landing page redesign using real-world data from Kaggle. The test results were statistically inconclusive due to low statistical power, providing a perfect case study in proper experimental interpretation.

**Dataset Source**: [E-commerce A/B Testing on Kaggle](https://www.kaggle.com/code/ahmedmohameddawoud/e-commerce-a-b-testing-project-walk-through/input)

This analysis demonstrates:
- **Proper interpretation** of underpowered test results
- **Business risk assessment** for inconclusive findings  
- **Statistical power analysis** and its practical implications
- **Data-driven decision making** under uncertainty with real data

##  Key Insights

> **"Working with real e-commerce data taught me that the most valuable insight from an A/B test isn't whether you should launch, but whether you can trust your results at all."**

| Metric | Control (Old) | Treatment (New) |
|--------|---------------|-----------------|
| Conversion Rate | 12.9% | 12.8% |
| Absolute Difference | -0.15% | |
| Relative Change | -1.2% | |
| P-value | 0.2291 | |
| Statistical Power | 6.8% | |

##  The Critical Finding

Using the Kaggle e-commerce dataset, I discovered that while the observed difference was small (-1.2%), the extremely low **statistical power (6.8%)** meant the test was highly unlikely to detect a real effect even if one existed. This transformed the analysis from a simple "winner/loser" determination to a methodological case study.

##  Analysis Highlights

### Statistical Assessment
- **P-value**: 0.2291 (> 0.05 threshold → Not significant)
- **95% Confidence Interval**: [-0.11%, +0.28%] (Includes zero)
- **Statistical Power**: 6.8% (Severely underpowered)

### Business Impact
- **Potential loss**: 14 conversions per 10,000 visitors
- **Decision**: Recommended keeping old page due to inconclusive results
- **Risk avoided**: Preventing potential revenue loss based on weak evidence

##  Technical Implementation

### Data Source & Tools
- **Dataset**: [Kaggle E-commerce A/B Testing Data](https://www.kaggle.com/code/ahmedmohameddawoud/e-commerce-a-b-testing-project-walk-through/input)
- **Tools Used**: Python, Pandas, SciPy, StatsModels, Matplotlib
- **Analysis Types**: Hypothesis testing, power analysis, confidence intervals, segmentation analysis

### Key Code Features
```python
# Power analysis calculation
from statsmodels.stats.power import TTestIndPower
analysis = TTestIndPower()
required_n = analysis.solve_power(effect_size=0.02, power=0.8, alpha=0.05)
print(f"Required sample size: {required_n:.0f}")

## Project structure
├── data/
│   └── README.md                 # Data source attribution
├── analysis/
│   └──ab_test_analysis.ipynb    # Main analysis notebook
│   
├── docs/
│   ├── business_recommendation.md # Executive summary
│   └── methodology_improvements.md # Lessons learned
├── assets/
│   └── analysis board.jpg     # Analysis visualization
└── README.md




