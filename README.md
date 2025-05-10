# A/B Test Analysis: Ad vs PSA Conversion

This project analyzes the effectiveness of an online ad campaign compared to a public service announcement (PSA) using real-world user conversion data. We apply both classical and Bayesian statistical methods to estimate the treatment effect and understand the impact of ad exposure.

---

## 🔍 Dataset Overview

- **User ID**: Unique user identifier  
- **Test Group**: Indicates whether user saw an ad or PSA  
- **Converted**: Boolean indicating whether the user converted  
- **Total Ads**: Total number of ads shown to the user  
- **Most Ads Day**: Day of the week when most ads were seen  
- **Most Ads Hour**: Hour of day when most ads were seen  

Source: [Marketing A/B Testing Dataset on Kaggle](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)

---


## 📊 Key Results

### ✅ Conversion Rate (EDA + Z-Test):
- Ad group conversion rate: **2.55%**
- PSA group conversion rate: **1.79%**
- Z-test p-value: **< 0.001** → Statistically significant

### 📈 Logistic Regression:
- PSA group has **odds ratio = 0.66** compared to ad group
- Each additional ad increases conversion odds by ~0.8%
- Monday and Tuesday ad exposure correlated with higher conversion

### 🔁 Bootstrap:
- Estimated uplift: **0.0077**
- 95% CI: **[0.0060, 0.0093]** → Significant, tight interval

### 🎲 Bayesian Inference:
- Posterior uplift distribution: Entirely > 0  
- P(ad > psa): **1.000**  
- Credible interval (95%): **[0.0059, 0.0094]**

---

## 🧰 Tools & Libraries

- `pandas`, `numpy`, `matplotlib`, `seaborn`  
- `statsmodels` for logistic regression and z-tests  
- `scipy.stats` for beta distributions

---

## 📎 Author Notes

This project is intended for PhD-level DS/ML internship applications and demonstrates a full statistical pipeline with thoughtful inference and modeling. Feel free to reuse, cite, or build upon this structure.

---

