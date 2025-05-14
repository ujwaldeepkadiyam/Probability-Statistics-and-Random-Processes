  # <p style="text-align:center;"><font color="brown"> Statistics For Data Analytics and Machine Learning </font> </p>
 
 ## <p style="text-align:center;"><font color="blue"> Hypothesis Testing</font> </p>

**Hypothesis testing** is a formal statistical method used to make decisions or inferences about population parameters based on sample data. It starts with a claim, known as the **null hypothesis ($H_0$)**, which represents a baseline assumption (e.g., no difference, no effect, or status quo). Alongside the null, we define an **alternative hypothesis ($H_1$ or $H_a$)**, which is what we aim to support (e.g., a new drug is effective, or a machine produces fewer defects). We then use data from a sample to decide whether to reject the null hypothesis in favor of the alternative or not.

The process involves calculating a **test statistic** from the sample data and comparing it to a critical value or using a **p-value** approach. If the p-value is below a predetermined significance level (commonly $\alpha = 0.05$), we reject the null hypothesis. This does not "prove" the alternative is true, but suggests there is statistically significant evidence against the null. Hypothesis testing is widely used in scientific research, quality control, marketing studies, and more to assess claims and make data-driven decisions.

## 
<p style="text-align:center;"><font color="red">Inferential Statistics</font></p>

**Inferential statistics** is the branch of statistics that allows us to:
> **Make predictions or generalizations** about a population based on a sample of data.

Instead of studying an entire population (which is often impractical or impossible), we:
- Collect a **sample**
- Analyze it
- Use the results to **draw conclusions** about the whole population

---

## Key Elements of Inferential Statistics

1. **Population vs. Sample**
   - **Population**: The entire group we're interested in.
   - **Sample**: A smaller, randomly selected subset of the population.

2. **Parameter vs. Statistic**
   - **Parameter**: A value that describes a population (e.g., population mean $\mu$).
   - **Statistic**: A value computed from the sample (e.g., sample mean $\bar{X}$).

3. **Estimation**
   - Using sample data to estimate population parameters.
   - Example: **Confidence intervals**

4. **Hypothesis Testing**
   - Making decisions or inferences about population characteristics.
   - Example: Testing if a new drug is effective.

5. **Regression and Correlation**
   - Modeling relationships between variables and making predictions.

---

## Why It Works

Inferential statistics relies heavily on:
- **Probability theory**
- The **Central Limit Theorem** (which ensures sample statistics follow predictable patterns)

---

## Summary

| Concept               | Purpose                                     |
|------------------------|---------------------------------------------|
| Inferential Statistics | Draw conclusions about populations          |
| Based on               | Data from samples                           |
| Tools Used             | Confidence intervals, hypothesis tests, regression |
| Depends on             | Random sampling and probability theory      |

---

**Key Insight**:  
Inferential statistics transforms **uncertainty** into informed **probabilistic statements**, helping us make data-driven decisions about large groups using limited information.


## <p style="text-align:center;"><font color="red">Point Estimate vs. Interval Estimate</font></p>

### Point Estimate

A **point estimate** is a single value used to estimate a population parameter.  
For example, if you take a random sample and calculate its mean ($\bar{X}$), that mean is a **point estimate** of the population mean ($\mu$).

- **Advantage**: Simple and easy to calculate.
- **Limitation**: Gives no information about the uncertainty or variability of the estimate.

### Example:
If a sample of students has an average height of 170 cm, then 170 cm is the point estimate of the population’s average height.

---

### Interval Estimate

An **interval estimate** provides a range of values — rather than a single number — that is likely to contain the population parameter.  
This range is called a **confidence interval** and is often expressed as:

$$
\bar{X} \pm z^* \cdot \text{Standard Error}
$$

- **Advantage**: Accounts for variability and gives a measure of certainty.
- **Interpretation**: A 95% confidence interval means we are 95% confident that the interval contains the true population parameter.

### Example:
A 95% confidence interval for the population mean might be [168 cm, 172 cm].

---

### Summary

| Estimate Type     | Description                                | Tells About Uncertainty? |
|-------------------|--------------------------------------------|---------------------------|
| Point Estimate    | Single best guess of a parameter            | ❌ No                     |
| Interval Estimate | Range likely to contain the parameter       | ✅ Yes                    |

---

**Key Insight**:  
While point estimates give a specific value, **interval estimates provide more reliable and informative insight** by showing how much uncertainty is associated with the estimate.

## <p style="text-align:center;"><font color="red"> 95% Confidence Interval for a Normal Distribution</font></p>

### The Formula

For a normal distribution (with known standard deviation), the 95% confidence interval for the population mean $\mu$ is given by:

$$
\bar{X} \pm z^* \cdot \frac{\sigma}{\sqrt{n}}
$$

### Explanation of Terms:

- **$\bar{X}$**: Sample mean  
  The average value of the sample data, used as a point estimate for $\mu$.

- **$z^*$**: Critical value from the standard normal distribution  
  For 95% confidence, $z^* = 1.96$ (since 95% of the data lies between -1.96 and +1.96 in the standard normal curve).

- **$\sigma$**: Population standard deviation  
  Measures the spread of the population. Assumed to be known here.

- **$n$**: Sample size  
  The number of observations in the sample.

- **$\frac{\sigma}{\sqrt{n}}$**: Standard Error (SE)  
  Represents the variability of the sample mean — smaller SE means more precision.

---

### How It’s Derived

The confidence interval is derived from the **sampling distribution** of the sample mean.  
According to the **Central Limit Theorem (CLT)**, if the sample size is large enough, the sample mean follows an **approximately normal distribution**, even if the original data is not normal.

This implies:

$$
\frac{\bar{X} - \mu}{\sigma / \sqrt{n}} \sim N(0, 1)
$$

Rearranging this gives:

$$
P\left( -1.96 < \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} < 1.96 \right) = 0.95
$$

Solving for $\mu$, we get:

$$
P\left( \bar{X} - 1.96 \cdot \frac{\sigma}{\sqrt{n}} < \mu < \bar{X} + 1.96 \cdot \frac{\sigma}{\sqrt{n}} \right) = 0.95
$$

This is the 95% confidence interval.

### Key Insight

- A **wider interval** gives more confidence but less precision.
- A **larger sample size** reduces the margin of error and narrows the interval.
- If $\sigma$ is unknown, we use the **t-distribution** instead of $z$.

## <p style="text-align:center;"><font color="red"> Steps of Hypothesis Testing</font></p>
Hypothesis testing is a systematic method to decide whether there is enough evidence in a sample to support a specific claim about a population.

### 1. State the Hypotheses

- **Null Hypothesis ($H_0$)**: The default assumption or claim (e.g., no difference, no effect).
- **Alternative Hypothesis ($H_1$ or $H_a$)**: What you want to test or prove (e.g., a new effect, a difference).

### Example:
$H_0$: The mean salary is $50,000  
$H_a$: The mean salary is not $50,000

---

### 2. Choose the Significance Level ($\alpha$)

- Common choices: **0.05, 0.01, or 0.10**
- This is the probability of **rejecting $H_0$ when it's actually true** (Type I error).

---

### 3. Select the Test and Compute the Test Statistic

- Choose the appropriate test based on the type of data and hypothesis (e.g., z-test, t-test).
- Compute the **test statistic**, which measures how far the sample result is from the null hypothesis.
- $$
\text{Test Statistic} = \frac{\text{Observed value} - \text{Hypothesized value}}{\text{Standard Error}}
$$

---

### Explanation of Terms:

- **Observed value** ($\bar{X}$):   The value obtained from the sample (e.g., sample mean).

- **Hypothesized value** ($\mu_0$):  The value stated in the null hypothesis ($H_0$).

- **Standard Error (SE)**:  The standard deviation of the sampling distribution of the statistic.  
  For a sample mean:  
  $$
  SE = \frac{\sigma}{\sqrt{n}}
  $$  
  (or use sample standard deviation $s$ if population $\sigma$ is unknown).

- The test statistic tells you **how many standard errors** the observed result is away from the hypothesized value.
- A **large test statistic** (in absolute value) suggests the result is far from what we’d expect under $H_0$, and may lead to rejection of $H_0$.

---

### 4. Determine the Critical Value or P-value

- **Critical value method**: Find the cutoff value from the distribution of H<sub>0.
	- Critical value is the value at which the $\alpha$ is calculated.
	- For example,  for a right tailed test, critical value is the point, beyond with the area under the curve is equal to significance level $(\alpha)$.
- **P-value method**: Compute the probability of observing the test result (or more extreme) if $H_0$ is true.
	- It is the value at which p-value is calculated. 
	- For example, for a right tailed test, p-value is the area under the curve beyond the test statistic point.

---

### 5. Make a Decision

- If using **p-value**:  
  - Reject $H_0$ if **p-value < $\alpha$**
- If using **critical value**:  
  - Reject $H_0$ if the test statistic is in the rejection region.

---

### 6. State the Conclusion

- **Reject $H_0$**: There is sufficient evidence to support the alternative hypothesis.
- **Fail to reject $H_0$**: There is not enough evidence to support the alternative.

---

### Summary Table

| Step                        | What You Do                           |
|-----------------------------|----------------------------------------|
| 1. Hypotheses               | Define $H_0$ and $H_a$                 |
| 2. Significance Level       | Choose $\alpha$ (e.g., 0.05)           |
| 3. Test Statistic           | Compute from sample data               |
| 4. Critical Value / P-value | Determine threshold or probability     |
| 5. Decision                 | Reject or fail to reject $H_0$         |
| 6. Conclusion               | Interpret in the context of the claim  |

---

**Key Insight**:  
Hypothesis testing bridges sample data with population claims, helping make informed, data-driven decisions.

## <p style="text-align:center;"><font color="red"> One-Tailed vs Two-Tailed Tests</font></p>

The type of hypothesis test (left-tailed, right-tailed, or two-tailed) depends on the form of the **alternative hypothesis ($H_1$)**.

---

## 1. Two-Tailed Test

Used when you're testing for any significant difference — either higher or lower — from the hypothesized value.

### Hypotheses:
- $H_0$: $\mu = \mu_0$ (no difference)
- $H_1$: $\mu \ne \mu_0$ (difference in either direction)

### When to Use:
- You're checking **if something has changed**, without specifying the direction.

### Rejection Region:
- Both ends (tails) of the distribution.

---

## 2. Right-Tailed Test

Used when you are testing if the population parameter is **greater than** a specified value.

### Hypotheses:
- $H_0$: $\mu \le \mu_0$
- $H_1$: $\mu > \mu_0$

### When to Use:
- You're checking **if the mean has increased**, for example, testing if a new method yields **higher** performance.

### Rejection Region:
- Right tail of the distribution.

---

## 3. Left-Tailed Test

Used when you are testing if the population parameter is **less than** a specified value.

### Hypotheses:
- $H_0$: $\mu \ge \mu_0$
- $H_1$: $\mu < \mu_0$

### When to Use:
- You're checking **if the mean has decreased**, for example, testing if a process produces **lower** emissions.

### Rejection Region:
- Left tail of the distribution.

---

## Visual Summary

| Test Type      | $H_1$ Form       | Rejection Region  |
|----------------|------------------|--------------------|
| Two-tailed     | $\mu \ne \mu_0$  | Both tails         |
| Right-tailed   | $\mu > \mu_0$    | Right tail only    |
| Left-tailed    | $\mu < \mu_0$    | Left tail only     |

---

**Key Insight**:  
The choice of test direction is driven by the research question or hypothesis — always define $H_1$ first.

## <p style="text-align:center;"><font color="red">Type I and Type II Errors</font></p>

In hypothesis testing, two types of errors can occur depending on whether the null hypothesis ($H_0$) is rejected or not.

---

## Type I Error (False Positive)

- **Definition**: Rejecting the null hypothesis when it is actually true.
- **Symbol**: $\alpha$
- **Also called**: Significance level
- **Example**: Saying a new drug works when it actually doesn’t.

### Significance Level ($\alpha$):
- The probability of making a Type I error.
- Common values: 0.05, 0.01
- Chosen before the test begins.
- It defines the threshold for rejecting $H_0$.

---

## Type II Error (False Negative)

- **Definition**: Failing to reject the null hypothesis when the alternative hypothesis is actually true.
- **Symbol**: $\beta$
- **Example**: Saying a new drug doesn’t work when it actually does.

---

## Power of a Test

- **Definition**: The probability of correctly rejecting $H_0$ when the alternative hypothesis is true.
- **Formula**:  
  $$
  \text{Power} = 1 - \beta
  $$
- A higher power means a better test — it’s more likely to detect a true effect.

---

## Summary Table

| Decision           | $H_0$ True       | $H_0$ False      |
|--------------------|------------------|------------------|
| **Reject $H_0$**   | Type I Error ($\alpha$) | Correct Decision (Power) |
| **Fail to Reject $H_0$** | Correct Decision       | Type II Error ($\beta$) |

---

## Key Insight

- **Reducing $\alpha$** lowers the chance of Type I error but may increase $\beta$ (more likely to miss a real effect).
- **Increasing sample size** helps reduce both errors and increases test power.
## <p style="text-align:center;"><font color="red">Summary of One-Sample Tests</font></p>

### Overview of One-Sample Tests

| Test Name             | When to Use                                                    | Data Type       | Population Info Known? |
|-----------------------|----------------------------------------------------------------|------------------|-------------------------|
| One-Sample Z-Test     | Test population mean, known population SD ($\sigma$)          | Quantitative     | Yes                     |
| One-Sample t-Test     | Test population mean, unknown population SD                   | Quantitative     | No                      |
| One-Sample Proportion | Test population proportion (e.g., % of success)               | Binary (Yes/No)  | Yes (for large $n$)     |
| Chi-Square GOF Test   | Test if data fits a categorical distribution (goodness of fit)| Categorical      | Yes (expected counts)   |

---

## Table 2: Details, Assumptions, and Test Statistics

| Test                  | Null Hypothesis ($H_0$)        | Alternative ($H_1$)            | Assumptions                                               | Test Statistic |
|-----------------------|----------------------------------|----------------------------------|------------------------------------------------------------|----------------|
| One-Sample Z-Test     | $\mu = \mu_0$                  | $\mu \ne$, $>$, or $<$ $\mu_0$  | Normal population or large $n$; $\sigma$ known             | $z = \frac{\bar{x} - \mu_0}{\sigma/\sqrt{n}}$ |
| One-Sample t-Test     | $\mu = \mu_0$                  | $\mu \ne$, $>$, or $<$ $\mu_0$  | Normal population or large $n$; $\sigma$ unknown           | $t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}}$ |
| One-Sample Proportion | $p = p_0$                      | $p \ne$, $>$, or $<$ $p_0$      | np ≥ 10, n(1-p) ≥ 10; binomial approximation to normal     | $z = \frac{\hat{p} - p_0}{\sqrt{p_0(1 - p_0)/n}}$ |
| Chi-Square GOF Test   | Data follows expected distribution | Data differs from expected      | Expected count ≥ 5 for each category                       | $\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$ |

---

## Notes:

- Use a **Z-test** when the population standard deviation is known and the sample size is large.
- Use a **t-test** when $\sigma$ is unknown and you're estimating it using the sample standard deviation.
- **Proportion test** applies when data represents binary outcomes (e.g., success/failure).
- **Chi-Square GOF** (Goodness of Fit) checks if observed frequencies differ from expected ones in categorical data.

## <p style="text-align:center;"><font color="red">Two-Sample and Paired Sample Tests</font></p>

## Table 1: Overview – When to Use Each Test

| Test Name                       | When to Use                                                       | Data Type       | Groups     | Assumes Equal Variance? |
|--------------------------------|--------------------------------------------------------------------|------------------|------------|--------------------------|
| Two-Sample Z-Test              | Compare means of two groups, known variances                     | Quantitative     | Independent| Yes                      |
| Two-Sample t-Test (pooled)     | Compare means, unknown but equal variances                       | Quantitative     | Independent| Yes                      |
| Two-Sample t-Test (Welch’s)    | Compare means, unknown & unequal variances                       | Quantitative     | Independent| No                       |
| Two-Proportion Z-Test          | Compare proportions of two independent groups                    | Binary           | Independent| Large sample required    |
| Paired t-Test                  | Compare means of matched/paired observations (before-after)      | Quantitative     | Paired     | Normal diff. assumption  |
| McNemar's Test                 | Compare paired proportions (binary yes/no outcomes)              | Binary           | Paired     | Yes                      |

---

## Table 2: Hypotheses, Assumptions, and Test Statistics

| Test                       | Null Hypothesis ($H_0$)     | Alternative ($H_1$)              | Assumptions                                       | Test Statistic                                                                             |
| -------------------------- | --------------------------- | -------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Two-Sample Z-Test          | $\mu_1 = \mu_2$             | $\mu_1 \ne$, $>$, or $<$ $\mu_2$ | Normal distribution; $\sigma_1$, $\sigma_2$ known | $z = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}$ |
| Two-Sample t-Test (pooled) | $\mu_1 = \mu_2$             | Same as above                    | Normal data, equal variances, unknown $\sigma$    | $t = \frac{\bar{x}_1 - \bar{x}_2}{s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}$               |
| Welch’s t-Test             | $\mu_1 = \mu_2$             | Same as above                    | Normal data, unequal variances                    | $t$ with adjusted df (Welch-Satterthwaite)                                                 |
| Two-Proportion Z-Test      | $p_1 = p_2$                 | $p_1 \ne$, $>$, or $<$ $p_2$     | Large samples (np ≥ 10), independent groups       | $z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{p(1-p)(\frac{1}{n_1} + \frac{1}{n_2})}}$           |
| Paired t-Test              | $\mu_d = 0$ (mean diff = 0) | $\mu_d \ne$, $>$, or $<$ 0       | Normality of differences                          | $t = \frac{\bar{d}}{s_d / \sqrt{n}}$                                                       |


---

## Notes:

- Use **two-sample tests** when comparing different groups (e.g., treatment vs control).
- Use **paired tests** when observations are linked (e.g., before-after or matched pairs).
- Choose **Welch's t-test** when variances are clearly unequal or sample sizes differ significantly.


## <p style="text-align:center;"><font color="red"> Summary of ANOVA (Analysis of Variance of means)</font></p>

## Overview of ANOVA

| Test Name              | When to Use                                                   | Data Type        | Groups    | Assumptions                         |
|------------------------|---------------------------------------------------------------|-------------------|-----------|--------------------------------------|
| One-Way ANOVA           | Compare means across more than two independent groups        | Quantitative      | Independent| Normality, equal variances, independent samples |
| Two-Way ANOVA           | Compare means across two independent variables (factors)     | Quantitative      | Independent| Normality, equal variances, independent samples |

---

## Details of ANOVA Tests

| Test                   | Null Hypothesis ($H_0$)                        | Alternative ($H_1$)                | Assumptions                                                 | Test Statistic                    |
|------------------------|------------------------------------------------|------------------------------------|-------------------------------------------------------------|-----------------------------------|
| One-Way ANOVA           | All group means are equal ($\mu_1 = \mu_2 = \cdots = \mu_k$) | At least one group mean differs    | Normal distribution, equal variances, independent samples    | $F = \frac{\text{Between-group variance}}{\text{Within-group variance}}$ |
| Two-Way ANOVA           | All group means for each factor combination are equal | At least one group mean differs    | Normal distribution, equal variances, independent samples    | $F = \frac{\text{Between-group variance}}{\text{Within-group variance}}$ (calculated for each factor and interaction) |

---

## Key Points for ANOVA:

- **One-Way ANOVA** is used when comparing means across more than two independent groups.
- **Two-Way ANOVA** is used when there are two independent variables and you want to evaluate their individual effects as well as any interaction effect.
  
---

## F-Statistic Formula

For **both One-Way and Two-Way ANOVA**, the **F-statistic** is calculated as:

$$
F = \frac{\text{Variance between groups}}{\text{Variance within groups}}
$$

Where:
- **Variance between groups**: Measures how much the group means differ from the overall mean.
- **Variance within groups**: Measures the variability within each group.
  
---

## Post-Hoc Testing

If the **null hypothesis** is rejected (i.e., at least one group mean is different), **post-hoc tests** like **Tukey’s HSD** are performed to determine which specific group means differ.

---

## Notes:

- ANOVA can only tell you that at least one mean is different, but **post-hoc tests** tell you which ones are different.
- Ensure that the assumptions (normality, equal variances, independence) are met, or use alternative methods like **Kruskal-Wallis test** for non-parametric data.

## 
<p style="text-align:center;"><font color="red">Null and Alternate Hypothesis -  A deeper Understanding</font></p>

### Hypothesis Testing: Distributions of $H_0$ and $H_1$

#### 🔹 1. What are the distributions of $H_0$ and $H_1$?

- **$H_0$** (null hypothesis) assumes **no effect** or **no difference**. Under $H_0$, we assume the sample data comes from a **known distribution** (e.g., normal distribution with specific parameters).
- **$H_1$** (alternative hypothesis) assumes there **is** an effect or a difference. The distribution under $H_1$ typically reflects a **shift** or **change** in parameters (like the mean or variance) relative to $H_0$.

> So:  
> - $H_0$: baseline distribution (e.g., $\mu = \mu_0$)  
> - $H_1$: alternative distribution (e.g., $\mu \ne \mu_0$, or $\mu > \mu_0$, etc.)

---

## 🔹 2. Why do they take these distributions?

### 📌 Under $H_0$

We **assume** a known population and use it to:

- Build the **sampling distribution** of a test statistic (e.g., $t$, $z$, $F$, etc.)
- This distribution is **derived mathematically** based on assumptions like:
  - The data follows a normal distribution
  - The variance is known/unknown
  - The sample size

#### 🔍 Example:

For testing the mean of a normal distribution:

- If $\sigma$ is known → use **standard normal $Z$**  
- If $\sigma$ is unknown → use **$t$-distribution**

---

### 📌 Under $H_1$

We’re asking: **"What would the sampling distribution look like if the alternative is true?"**

- This is often a **shifted version** of the $H_0$ distribution.
- The mean moves to a new value (e.g., from $\mu_0$ to $\mu_1$), but the **shape** (normal, $t$, etc.) may remain the same.

This helps compute **power** and **Type II error ($\beta$)**, because:

- Power = probability of correctly rejecting $H_0$ when $H_1$ is true
- To compute this, we need to know the distribution under $H_1$

---

## 🔹 3. Visual Intuition

- The **$H_0$ distribution** is centered around the hypothesized value $\mu_0$
- The **$H_1$ distribution** is centered around a different value $\mu_1$
- The **overlap** between them leads to:
  - **Type I error**: rejecting $H_0$ when it's true (denoted $\alpha$)
  - **Type II error**: failing to reject $H_0$ when $H_1$ is true (denoted $\beta$)

---

## 🔹 4. Summary

| Hypothesis | Distribution Type                     | Centered Around   | Purpose                                               |
| ---------- | ------------------------------------- | ----------------- | ----------------------------------------------------- |
| $H_0$      | Sampling distribution under no effect | $\mu_0$           | Used to compute p-values and critical regions         |
| $H_1$      | Sampling distribution under effect    | $\mu_1 \ne \mu_0$ | Used to calculate power and visualize the alternative |

---
