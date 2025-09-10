# Descriptive Statistics

## Measures of central tendency

- Mean

Average of all values.

```python
data = [10, 20, 30, 40, 50]
```

```python
np.mean(data) # 30.0
```

- Median

Middle value when data is sorted.

```python
np.median(data) # 30.0
```

- Mode

 Most frequently occurring value.

 ```python
stats.mode(data, keepdims=True)[0][0] # 10

# (if tie, lowest value is returned)
```
- Percentile

Value below which a given % of data falls.

```python
np.percentile(data, 90) # 90th percentile
```
- Quartiles (Q1, Q2, Q3)

Q1: 25th percentile
```python
Q1 = np.percentile(data, 25)
```
  
Q2: Median

  
Q3: 75th percentile

```python
Q3 = np.percentile(data, 75)
```

- Interquartile range (IQR = Q3 - Q1)
```python
IQR = Q3 - Q1
```
   
- Min
```python
np.min(data)
```
- Max
```pyhton
np.max(data)
```
---

## Finding outliers using Quartiles
 - Lower Bound (Q1-1.5*IQR)
 - Upper Bound (Q3+1.5*IQR)
 - Outliers: values lower than LB or higher than UB

## Measures of dispersion
 - range
 - variance
 - standard deviation
 - z-score (used for standardization)
 - Confidence Interval (CI)

## Correlation coefficient (-1 to 1)
 - Pearson correlation coefficient
 - Sphearman's rank correlation

## Scatter plot (Bivariate analysis)
 - Visually inspecting correlation bw two varialbes

## Box plot
 - Shows median(Q2), Q1, Q3, Lower bound, upper bound, outliers

## Histograms
 - Frequency/relative frequency

## Probability density function
## Cumulative density function
 - Advantage compared to PDF
