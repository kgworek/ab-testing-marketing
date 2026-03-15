# ab-testing-marketing
##  Overview
This project analyzes the results of a marketing A/B experiment designed to evaluate the impact of online advertisements on user conversion behavior. The goal is to determine whether showing advertisements (tested group) increases the probability of purchase compared to showing a public service announcement (PSA controled group).

---

## Dataset

The dataset contains information about user exposure to advertisements and conversion outcomes.

Key variables include:

- **test_group** – indicates whether the user saw an advertisement (`ad`) or a public service announcement (`psa`)
- **converted** – indicates whether the user completed a purchase
- **total_ads** – total number of advertisements seen by the user
- **most_ads_day** – day of the week when the user saw the most advertisements
- **most_ads_hour** – hour of the day when the user saw the most advertisements

---

## Project structure 

### 1. Data Analysis
Initial exploration of the dataset, including variable distributions and data quality checks.

### 2. Conversion Rate and Lift Analysis
Comparison of conversion rates between the advertisement and PSA groups.

### 3. Hypothesis Testing
A two-proportion z-test is used to determine whether the observed difference in conversion rates between groups is statistically significant.

### 4. Confidence Interval Estimation
A 95% confidence interval is calculated for the difference in conversion rates to estimate the range of the true effect.

### 5. Power Analysis
Statistical power is calculated to assess whether the experiment had sufficient sample size to detect the observed effect.

### 6. Bootstrap Sampling
Bootstrap resampling is used to estimate the sampling distribution of the treatment effect and validate the stability of the results.

### 7. Segment Analysis
Conversion rates are analyzed across different time of the day and day of the week of ad exposure.

### 8. Logistic Regression
A logistic regression model is used to estimate the probability of conversion while controlling for other variables to ensure the robustness of the A/B testing results.

---

## Key Results

- The conversion rate for users exposed to advertisements is **2.55%**, compared to **1.79%** for the PSA group.
- The advertising campaign produced a **43% relative lift** in conversion probability.
- The difference in conversion rates is **statistically significant (p < 0.001)**.
- The **95% confidence interval** suggests that the true increase in conversion rate lies between **0.6% and 0.9%**.
- Logistic regression confirms that the positive effect of advertisements remains significant even after controlling for day of the week, time of exposure, and the number of advertisements seen.

The results indicate that exposure to advertisements significantly increases the probability of conversion. Although the absolute increase in conversion rate is relatively small, the relative improvement is substantial due to the low baseline conversion rate.


