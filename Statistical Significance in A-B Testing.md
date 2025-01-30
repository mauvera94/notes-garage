---
title: Statistical Significance in A-B Testing
created: 2025-01-29
updated: 2025-01-29
description: 
aliases:
  - stat sig
---
Statistical significance determines whether the outcome of an A/B test is likely due to the introduced change rather than random chance. It is often used as a threshold to decide if an experiment's result is reliable.

## Why It Matters:

A statistically significant result increases confidence that the change was responsible for the observed effect. However, significance alone does not confirm practical impact—magnitude and business relevance should also be considered.

## Key Concepts:

- **p-value**: Measures the probability that the observed result happened by chance. A p-value below 0.05 is commonly considered significant.
- **Confidence interval**: A range that estimates where the true impact lies. If the range does not cross zero, it strengthens confidence in the result.
- **Type I error (false positive)**: Concluding a change had an effect when it didn’t.
- **Type II error (false negative)**: Missing a real effect because the test lacked enough data.
- **Sample size**: Larger samples reduce randomness and make results more reliable.

### How to Calculate Statistical Significance:

1. **Define Hypotheses**: Establish the null hypothesis (no effect) and the alternative hypothesis (a real effect exists).
2. **Collect Data**: Run the A/B test and gather sample data.
3. **Choose a Significance Level**: Typically set at 0.05 (95% confidence)
	- The confidence level is tied to the p-value threshold:
		- A 95% confidence level means we set 0.05 (default standard)
		- A 90% confidence level means we set 0.10
4. **Calculate the Test Statistic**: Use the Z-test for proportions (eg. when dealing with [[conversion rate]])
	>[!code]- Using Python
	>```python
	> import statsmodels.api as sm
	> # Example data: conversion counts and sample sizes
	> conversions_1 = 50  # Number of conversions in Group 1 (UPDATE WITH DATA)
	> samples_1 = 1000    # Total users in Group 1 (UPDATE WITH DATA)
	> conversions_2 = 40  # Number of conversions in Group 2 (UPDATE WITH DATA)
	> samples_2 = 1000    # Total users in Group 2 (UPDATE WITH DATA)
	> # Proportion test
	> count = [conversions_1, conversions_2]  # Successes
	> nobs = [samples_1, samples_2]  # Total trials
	> z_stat, p_value = sm.stats.proportions_ztest(count, nobs, alternative='two-sided')
	> # Print results
	> print(f"Z-statistic: {z_stat}")
	> print(f"P-value: {p_value}")
	> # Determine significance
	> if p_value < 0.05:
	> print("Result is statistically significant.")
	> else:
	> print("Result is NOT statistically significant.")
	>   ```
	
	>[!sheets]- Using Google sheets
	>
	><u>Z-score formula</u>
	>```excel
	>=ABS((C1 - C2) / SQRT((C1*(1-C1)/N1) + (C2*(1-C2)/N2)))
	>```
	>Where:
	>- `C1` and `C2` are the conversion rates (e.g., 0.05 for 5%).
	>- `N1` and `N2` are the sample sizes.
	>
	><u>Convert Z-score to p-value</u>
	>```excel
	>=2 * (1 - NORMSDIST(Z))
	>```
	>Where:
	>- The `2 *` accounts for a two groups (two-tailed test)
	>- `Z` is for Z-score

5. **Compare p-value to Significance Level**: If p-value < 0.05, reject the null hypothesis and conclude the result is statistically significant.

>[!note]
>  If working with continuous metrics like revenue or time spent, a t-test is the right choice.

### Further Questions:

- How does statistical significance differ from practical significance?
- What methods exist to calculate required sample size before running an experiment?
- How can multiple A/B tests increase the risk of false positives (p-hacking)?