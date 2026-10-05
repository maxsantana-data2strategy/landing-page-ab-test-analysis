# Landing Page A/B Test — Conversion and Revenue Validation

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

<!-- TODO: infographic badge + embed, once the analysis is done
[![Download Infographic PDF](https://img.shields.io/badge/📥_Download_Infographic_PDF-2EA44F?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://raw.githubusercontent.com/maxsantana-data2strategy/landing-page-ab-test-analysis/main/assets/Infographic_LandingAB_EN.pdf)
-->

## 🔍 Overview

<!-- TODO: one paragraph. What was tested, on how many users, with which methods, and the headline result. Write this LAST. -->

## 🎯 Problem Statement

**Business Question:** Which version of the homepage — A (control) or B (variant) — should be implemented?

An A/B experiment was run on the homepage of an e-commerce platform, comparing two versions against conversion rate and economic value per user. The decision has to rest on statistical evidence rather than on raw differences, and has to account for behavior by traffic channel and user type.

Supporting questions:

1. Is there a significant difference in average spend per converted user between versions?
2. Which version produces the higher conversion rate?
3. Does conversion depend on traffic source?
4. Does user type (new vs returning) influence conversion?
5. What follows for marketing strategy and homepage design?

---

## 💡 What I Did

### Phase 0: Experiment Validation

<!-- TODO: SRM check, duplicate user_id check, gasto>0 ⟺ converted==1 rule, date-range parity. -->

### Phase 1: Load & Validate

<!-- TODO: shape, dtypes, nulls, class balance. -->

### Phase 2: Average Spend — A vs B

<!-- TODO: assumption checks, test chosen and why, result with confidence interval and effect size. -->

### Phase 3: Conversion Rate — A vs B

<!-- TODO: two-proportion test, absolute and relative lift, CI. -->

### Phase 4: Conversion by Traffic Source

<!-- TODO: independence test, effect size, and whether the landing effect differs by channel. -->

### Phase 5: Conversion by User Type

<!-- TODO: same, plus interaction with landing version. -->

### Phase 6: Composite Decision Metric

<!-- TODO: revenue per exposed user, compared with bootstrap. -->

---

## 🛠️ Technologies Used

| Category | Tools |
|----------|-------|
| **Python** | pandas, numpy |
| **Statistics** | <!-- TODO: list the tests actually used --> |
| **Visualization** | seaborn, matplotlib |
| **Techniques** | <!-- TODO --> |
| **Environment** | Jupyter Notebook |

---

## 📊 Key Findings

<!-- TODO: results table -->

### Context → Findings → Implications (C→F→I)

**📍 Context:** <!-- TODO -->

**🔍 Findings:** <!-- TODO -->

**💡 Implications:** <!-- TODO -->

---

## 🚀 How to Use

```
landing-page-ab-test-analysis/
├── Landing_Page_AB_Test_Analysis.ipynb
├── landing_experiment.csv
├── assets/
├── LICENSE
└── README.md
```

1. **Read without running** — every cell in the notebook retains its executed output
2. **Run it yourself:**

   ```bash
   git clone https://github.com/maxsantana-data2strategy/landing-page-ab-test-analysis.git
   cd landing-page-ab-test-analysis
   pip install pandas numpy scipy seaborn matplotlib jupyter
   jupyter notebook Landing_Page_AB_Test_Analysis.ipynb
   ```

### Dataset schema

| Column | Type | Description |
|---|---|---|
| `user_id` | UUID | Unique user identifier |
| `date` | date | Date the user was exposed to the page |
| `landing` | categorical | Page version shown — A (control) or B (variant) |
| `region` | categorical | Norte, Centro, Sur, Occidente, Oriente |
| `dispositivo` | categorical | Mobile, Desktop |
| `traffic_source` | categorical | Organic, Ads, Email, Referral |
| `user_type` | categorical | Nuevo, Recurrente |
| `converted` | binary | 1 if the user converted, 0 otherwise |
| `gasto` | float | Amount spent (0 when `converted` = 0) |

**Unit of analysis:** one row per user, each exposed to exactly one page version.

---

## ⚖️ Limitations

<!-- TODO: what the experiment cannot establish — segment analyses as exploratory, multiple comparisons, test duration, novelty effects, external validity. -->

## 🧭 Next Steps

<!-- TODO -->

---

## 📚 Learnings & Best Practices

<!-- TODO -->

---

**Author:** Max Santana — Data Analyst, Business Intelligence & Strategic Foresight · [GitHub](https://github.com/maxsantana-data2strategy) · [Portfolio](https://maxsantana-data2strategy.github.io)

**Status:** 🚧 In progress | **Data Quality:** <!-- TODO --> | **Ready for Decisions:** <!-- TODO -->
