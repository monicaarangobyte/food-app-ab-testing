🍽️ User Behavior & A/A/B Testing — Food Delivery App

**Statistical analysis of user behavior and font redesign impact across a mobile food app conversion funnel.**

---

## 📌 Project Overview

This project analyzes user behavior within a food delivery app and evaluates whether a typographic redesign affects key conversion metrics. Using event-level data, I built a conversion funnel, validated the experimental setup via A/A testing, and assessed the impact of the new font system through A/B hypothesis testing.

---

## 🎯 Business Question

> *Does changing the app's typography affect user behavior across the conversion funnel — and is it safe to roll out the new design?*

---

## 🔬 Methodology

### Funnel Analysis
Mapped the full user journey across four key screens:
- `MainScreenAppear` → `OffersScreenAppear` → `CartScreenAppear` → `PaymentScreenSuccessful`

### Experiment Design
| Group | Description |
|-------|-------------|
| 246 & 247 | Control groups (A/A validation) |
| 248 | Experimental group (new typography) |

### Statistical Testing
- Significance level: **α = 0.05**
- Total hypotheses tested: **8**
- Multiple comparisons correction: **Bonferroni** → adjusted α ≈ 0.00625
- All p-values remained well above even the corrected threshold → results considered **statistically robust**

---

## 📊 Key Findings

### 1. Conversion Funnel
| Stage | Conversion Rate |
|-------|----------------|
| Main Screen | 98.0% |
| Offers Screen | 61.9% |
| Cart Screen | ~49.6% |
| Successful Payment | 46.97% |
| Cart → Payment | **94.8%** |

> **Critical bottleneck:** The steepest drop occurs at **Main → Offers**, losing ~36% of users before they explore products. The checkout experience, by contrast, is highly optimized (94.8% completion from cart).

### 2. A/A Validation
- No statistically significant differences found between control groups 246 and 247 at any funnel stage (p > 0.05 across all events)
- ✅ Random assignment confirmed as correct
- ✅ Groups are comparable — experiment is reliable

### 3. A/B Results — New Typography vs. Combined Control

| Funnel Stage | Significant Difference? |
|---|---|
| MainScreenAppear | ❌ No |
| OffersScreenAppear | ❌ No |
| CartScreenAppear | ❌ No |
| PaymentScreenSuccessful | ❌ No |

The typographic change:
- Does **not** reduce conversion at any stage
- Does **not** create friction in the funnel
- Does **not** affect the critical Main → Offers drop-off
- Does **not** impact payment completion

Results held consistent even after Bonferroni correction.

---

## ✅ Recommendation

**Proceed with the rollout of the new typography.** There is no statistical evidence to justify blocking the design change — it is safe for all key business metrics.

### Future Optimization Opportunities
Since the main bottleneck is the **Main → Offers** transition, future efforts should focus on:
- Strengthening the call-to-action on the main screen
- Improving visual hierarchy and initial navigation clarity
- Increasing product exploration rates before cart

---

## 🛠️ Tools & Libraries

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-blue?style=flat)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4c72b0?style=flat)

- **Python** — data processing and statistical testing
- **Pandas** — data wrangling and funnel construction
- **Statsmodels** — proportion z-tests and p-value computation
- **Matplotlib / Seaborn** — funnel and distribution visualization

---

## 📁 Project Structure

```
food-app-ab-testing/
│
├── food_app_ab_testing.ipynb   # Main analysis notebook
├── data/
│   └── logs_exp_us.csv         # Event-level user data
└── README.md
```

---

## 👩‍💻 Author

**Mónica Arango**  
Data Analyst & Psychologist  
[LinkedIn](https://www.linkedin.com/in/monica-arango-ba271737a) · [Portfolio](https://monicaarangobyte.github.io) · [GitHub](https://github.com/monicaarangobyte)
