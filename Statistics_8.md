# Inferential Statistics

Inferential statistics helps us make **predictions and decisions about a population** based on data from a sample.

---


## Why do we need Inferential Statistics? 
- Correlation Vs. Causation
- Controlled Experiment
    - Examples 
        - A/B Testing
        - Medical Trials

---


## Population

The entire group we are interested in studying.

## Sample

A smaller subset of the population used for analysis.

### Why do we need sampling ?

- Studying an entire population is expensive and time-consuming.
  
- A well-chosen sample allows us to generalize results to the population.
  
#### Sampling bias

When the sample does not represent the population correctly.

#### Types of sampling

Sampling is the process of selecting a small group (sample) from a large population to study and make conclusions.

1. Random Sampling

Every member of the population has an equal chance of being chosen.

Example: Picking names from a hat.

2. Systematic Sampling

Select every kth member from a list after a random start.

Example: Choosing every 10th person from a queue.

3. Stratified Sampling

Population is divided into groups (strata) based on characteristics (like age, gender, income), and samples are taken from each group.

Example: If a class has 60 girls and 40 boys, we take 6 girls and 4 boys to keep proportion.

4. Cluster Sampling

Population is divided into clusters (groups), and entire clusters are randomly selected.

Example: Randomly selecting 3 schools in a city and surveying all students in those schools.

5. Convenience Sampling

Selecting people who are easiest to reach.

Example: Asking your friends for a survey because they are nearby.

6. Quota Sampling

Similar to stratified sampling, but instead of random selection, the researcher chooses until a quota is filled.

Example: Surveying 50 men and 50 women by picking whoever is available.

---


### Sampling Distribution

- Probability distribution → Shows how probabilities are distributed over values.

- Area under the curve → Represents probabilities.

- Gaussian distribution and Normal distribution  → Bell-shaped distribution.
  
- Sampling Distribution of the Mean → Distribution of sample means.
  
- Central Limit Theorem (CLT)
    - [Online stats visualization](https://onlinestatbook.com/stat_sim/sampling_dist/)
    - If you take many samples from a population and calculate their averages, those averages will form a bell-shaped curve (normal distribution), even if the original data isn’t bell-shaped. This is useful because it lets us make predictions about the population.

---


## Hypothesis Testing

Hypothesis testing is a statistical method used to make decisions or draw conclusions about a population based on sample data.

1. **State the Null Hypothesis ($H_0$):**  
   - Assumes there is **no effect** or **no difference**.  
   - Example: "The average weight of a chocolate bar is 50g."

2. **State the Alternate Hypothesis ($H_1$):**  
   - Assumes there **is an effect** or **a difference**.  
   - Example: "The average weight of a chocolate bar is not 50g."

3. **Choose Significance Level ($\alpha$):**  
   - Probability of rejecting $H_0$ when it is true (Type I error).  
   - Common values:  
     - 0.05 (5% chance of error – business, social sciences)  
     - 0.01 (1% chance of error – medicine, pharma)  

4. **Select the Test and Calculate the Test Statistic:**  
   - Z-test, T-test, Chi-Square, ANOVA (depends on data and problem).  

5. **Find the P-value:**  
   - The probability of getting results as extreme as the sample, assuming $H_0$ is true.  

6. **Decision Rule:**  
   - If **p-value < α** → Reject $H_0$ (evidence supports $H_1$).  
   - If **p-value ≥ α** → Fail to reject $H_0$ (not enough evidence against $H_0$).  

---

## Example
A company claims its chocolate bar weighs 50g.  
We take a sample and find the average = 49.5g.  
- $H_0$: μ = 50  
- $H_1$: μ ≠ 50  
- α = 0.05  

If the p-value = 0.02 → Reject $H_0$ (evidence that the bars don’t weigh exactly 50g).  

---

## Key Terms
- **Type I Error (False Positive):** Rejecting $H_0$ when it is true.  
- **Type II Error (False Negative):** Failing to reject $H_0$ when it is false.  
- **One-tailed Test:** Tests for effect in **one direction only**.  
- **Two-tailed Test:** Tests for effect in **both directions**.  

---

### Null Hypothesis ($H_0$)

Assumes no effect or no difference.

Example: "Average chocolate bar weight = 50g."

### Alternate Hypothesis ($H_1$)

Assumes there is an effect or difference.

Example: "Average chocolate bar weight ≠ 50g."

### Significance Level (α)

Probability of rejecting $H_0$ when true (Type I error).

- Typically used values are 0.05 (e.g. e-commerce  ) and 0.01 (e.g in fileds like medicine)
  
### P-value

Probability of obtaining results as extreme as the sample if $H_0$ is true.

---


# Major Statistical Tests

## Z-test

A Z-test is used to compare means when the sample size is large $n>30$ and the population variance is known. It follows the standard normal distribution ($Z$-distribution).
The steps to do this as follows
1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your Z-test Statistic

$Z=\dfrac{\bar{x}-\mu}{\left(\frac{\sigma}{\sqrt{n}}\right)} \nonumber$

- $\bar{x}$ = sample mean
- $\mu$ = population mean
- $\sigma$ = population standard deviation
- $n$ = sample size

5. Find p-value using [Z-Table](https://math.arizona.edu/~rsims/ma464/standardnormaltable.pdf) and Z-test statistic computed
6. if p-value < $\alpha$, then we fail to reject null Hypothesis
7. There are one-tailed and two-tailed tests

## Z-test Practice Problem

A particular companies chocolate bars are supposed to have an average weight of 50 grams according to the maufacturer.
We want to test if a sample of chocolate bars deviates significantly from this weight.
Data: 50.8, 49.5, 50.2, 51, 49.7, 50.3, 49.8, 50.5, 49.6, 50.1
Population standard deviation: 1.5 grams (assumed based on production tolerance)

---

## T-test

- We need T-test because population standard deviation $\sigma$ is not always available
- Here we will be computing T-test statistic (based on the problem statement and type of t-test)


| **Type of T-test**        | **Null Hypothesis**                                        | **Alternate Hypothesis**                                       | **Degrees of Freedom** |
|---------------------------|------------------------------------------------------------|----------------------------------------------------------------|------------------------|
| One Sample t-test         | The sample mean is equal to the reference value            | The sample mean is not equal to the reference value            | $df = n-1$             |
| Independent Sample t-test | The mean values in both groups are the same                | The mean values in both groups are not equal                   | $df = n_1+n_2-2$       |
| Paired Samples t-test     | The mean value of the difference between the pairs is zero | The mean value of the difference between the pairs is not zero | $df = n-1$             |

### One Sample T-test
Compares the sample mean to a known population mean

The steps are as follows

1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your T-test Statistic

$t=\dfrac{\bar{x}-\mu}{\left(\frac{s}{\sqrt{n}}\right)} \nonumber$

- $\bar{x}$ = sample mean
- $\mu$ = population mean
- $s$ = sample standard deviation

$s = \sqrt{\frac{1}{n-1} \sum_{i=1}^N (x_i - \overline{x})^2}$
- $n$ = sample size
5. Find the critical t-value from [T-Table](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf) using significance ($\alpha$) level
6. if t-statistic < critical t-value, we fail to reject Null Hypothesis

### Independent Sample T-test

Compares means of two independent groups

The steps are as follows

1. State the Null Hypothesis
2. State the Alternate Hypothesis
3. Choose Your Significance level ($\alpha$)
4. Calculate Your T-test Statistic

- $t = \dfrac{\overline{x_{1}}-\overline{x_{2}}}{\sqrt{(\dfrac{s_{1}^2}{n_{1}}+\dfrac{s_{2}^2}{{n_{2}}}})}$; for one tailed
- $t = \dfrac{\overline{x_{1}}-\overline{x_{2}}}{S_p\sqrt{(\dfrac{1}{n_{1}}+\dfrac{1}{{n_{2}}}})}$; for two tailed
  - $S_p = \frac{(n_1-1){s_1}^2+(n_2-1){s_2}^2}{n_1+n_2-2}$; known as pooled standard deviation

- $\bar{x_1}$ = sample mean of group 1
- $\bar{x_2}$ = sample mean of group 2
- $s_1$ = sample standard deviation of group 1
- $s_2$ = sample standard deviation of group 2
- $n_1$ = sample size of group 1
- $n_2$ = sample size of group 2

5. Find the critical t-value from [T-Table](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf) using significance ($\alpha$) level
6. if t-statistic < critical t-value, we fail to reject Null Hypothesis

Sample Data 
- Brand A: 49.5, 50.1, 49.8,50.3, 50
- Brand B: 50.4, 49.9, 50.6, 50.2, 50.1

### Paired Sample T-test
- Compares means from the same group at different times (before/after)

---

## F-Distribution

The F-Distribution is a **probability distribution** used to compare **variances of two or more groups**.  
It is primarily used in **ANOVA (Analysis of Variance)** tests.

### Key Points

- It is **right-skewed** (not symmetric like normal distribution).  
- Values are always **positive**.  
- Shape depends on **degrees of freedom**:  
  - df1 = numerator degrees of freedom  
  - df2 = denominator degrees of freedom  
- Used to test whether the **variances of two populations are equal**.  


### When to Use F-Distribution

1. **Compare two variances:**  
   - Example: Testing if two machines produce products with the same variability.  
2. **ANOVA (Analysis of Variance):**  
   - Compare means of **3 or more groups**.  


### F-test Hypotheses

- **Null Hypothesis ($H_0$):** All group variances are equal.  
- **Alternate Hypothesis ($H_1$):** At least one group variance is different.  


### F-test Statistic

\[
F = \frac{\text{Variance of Group 1}}{\text{Variance of Group 2}}
\]

- If **F ≈ 1**, variances are similar.  
- If **F > critical F-value**, reject $H_0$.  


### ANOVA Using F-Distribution

1. **State $H_0$ and $H_1$**  
   - $H_0$: μ1 = μ2 = μ3 … (all group means equal)  
   - $H_1$: At least one group mean is different  

2. **Choose significance level ($\alpha$)**  
   - Typically 0.05  

3. **Compute F-statistic** using **between-group variance / within-group variance**  

\[
F = \frac{MS_{between}}{MS_{within}}
\]

- \(MS_{between} = \frac{SS_{between}}{df_{between}}\)  
- \(MS_{within} = \frac{SS_{within}}{df_{within}}\)  

4. **Compare F-statistic with critical F-value** from F-table.  

- If F-statistic > F-critical → Reject $H_0$  
- If F-statistic ≤ F-critical → Fail to reject $H_0$  

---

### Example

Suppose we have 3 groups of students with test scores:

- Group 1: 85, 90, 88  
- Group 2: 78, 82, 80  
- Group 3: 92, 94, 90  

We want to test if **all groups have the same average score**.

1. $H_0$: μ1 = μ2 = μ3  
2. $H_1$: At least one mean is different  
3. Compute **between-group variance** and **within-group variance**  
4. Compute F-statistic and compare with critical value  

If F-statistic > F-critical → Reject $H_0$ → At least one mean is different  

---

## Reference 
1 . [Data Lab Tutorial](https://datatab.net/tutorial/hypothesis-testing)
