# 📊 Facebook Ads Bidding A/B Test | Average vs Maximum

## 🧠 Project Summary

In this project, the performance of two different Facebook ad bidding strategies — **Maximum Bidding** and **Average Bidding** — are compared based on purchase results. The client, **bombabomba.com**, wants to find out whether Average Bidding generates more conversions.

The analysis is based on a 1-month A/B test, with **Purchase** (sales) as the main success metric.

---

## 🔎 Methods Used

- **Exploratory Data Analysis (EDA)**
- **Normality and Variance Homogeneity Tests**
  - Shapiro-Wilk Test
  - Levene’s Test
- **Independent Two-Sample T-Test**
- **Visualization with Seaborn & Matplotlib**
- **Interpretation and Recommendations**

---

## 📁 Dataset Description

The dataset consists of two separate groups:

| Column Name | Description                      |
|-------------|----------------------------------|
| Impression  | Number of ad impressions         |
| Click       | Number of ad clicks              |
| Purchase    | Number of purchases after clicks |
| Earning     | Revenue generated from purchases |

- **Control Group**: Maximum Bidding  
- **Test Group**: Average Bidding

The data is stored in two separate sheets within the `ab_testing.xlsx` file.

---

## ✅ Results

- **Normality** and **variance homogeneity** assumptions are satisfied.
- According to the t-test results:
  - **p-value > 0.05** → Fail to reject H₀.
  - This means there is **no statistically significant difference** between the two bidding strategies.
- The average purchase values between the groups are very close.

---

## 🎯 Recommendations

1. **Do not implement Average Bidding immediately.**
   - There's no statistical evidence that it performs better than Maximum Bidding.

2. **Plan new A/B tests with segmentation.**
   - Performance might vary across:
     - New vs loyal users
     - Age groups
     - Device types (mobile/desktop)

3. **Include additional success metrics.**
   - Not just Purchase, but also:
     - Click-Through Rate (CTR)
     - Return on Ad Spend (ROAS)
     - Revenue (Earning)

---

## 🛠 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy.stats`

