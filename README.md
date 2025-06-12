# 🐱 Descriptive-Inferential-analysis-for-Manufacturing-operations-using-Excel
This repository showcases practical examples of using Microsoft Excel for multivariate and regression-based analytics in a manufacturing operations setting. The dataset simulates production parameters across multiple machines and products. It includes:

1. Multi-variate analysis
2. Correlation
3. Regression analysis
4. Residual analysis
5. Confidence Interval
6. Prediction interval

---

## 🐭 Multi-variate analysis
Multi-variate analysis examines more than two variables simultaneously to understand complex relationships. It is used to:
- Analyze variation in a process
- Identifies investigation areas
- Breaks downs the variations into component families
- Multi-variate analysis is used when you have multiple discrete XΔ (like workshift, operator, plant location) and YΔ is continuous (like material length or resource cycle time)

### 🦊 Classification of variation sources
Multi-variate anaylsis classifies variation sources into three major component types:
1. *Positional*
    - Deals with variations within a single unit where variation is due to location
    - Eg: Pallet stocking in a truck, variation observed from cavity-to-cavity within a mold, region of country and line on invoice

2. *Cyclical*
    - Focuses on variations among sequential repetitions over a short time
    - Eg: Every nᵗʰ pallet broken, batch-to-batch variation, lot-to-lot variation, invoice received day-to-day, and amount of activity week-to-week

3. *Temporal*
    - Handles variations which occur over longer periods of time
    - Eg: Process drift, performance before and after breaks, seasonal and shift based differences, month-to-month closings and quarterly returns

### 🐻 Steps to create Multi-variate chart
Multi-variate chart shows the type of variation in the product and helps in identifying the root cause
1. *Select process and characteristics*
   - Select the process where 7 mm steel plates are manufactured with four resources
   - Measure the thickness within a specified range of 6.95 mm to 7.05 mm

2. *Decide sample size*
   - Assume a sample size is five units from each resource
   - Calibrate the frequency of data collection for every two hours starting from 8 AM until 2 PM

3. *Create a tabulation sheet*
   - The tabulation sheet with data records contains the columns with time, equipment, number and thickness as headers

4. *Plot the chart*
   - Plot the chart with time on X-axis and the plate thickness on Y-axis

5. *Link the observed values*
   - The observed values are linked by appropriate lines

---

## 🐼 Correlation
- Correlation quantifies the strength and direction of the relationship between two variables
- It represents the assoication or relationship between variables
- The coefficient of the correlation shows the strength of hte relationship between variables X & Y
- Correlation is used to find the behavior of Y when there is a change in the value of one of the many X-values
- Correlation helps to predict the direction of movement in the values of Y when X changes
- It is denoted by 'r' or "Pearson's coefficient of correlation

|*Value*|*Significance*|
|--------|-------------|
|-1| Movement in both variables is inverse |
|0| No correlation between the two variables |
|+1| Movement in both variables is same |

### 🐻‍❄️ Correlation levels
Correlation measures the linear association between the dependent variable or output variable Y and one independent variable X

### 🐨 Correlation coefficient and p-value
- The strength of the relationship between two variables is r
- The significance of the relationship is p
     => if p < α

                  H₀: r = 0
                  H₁: r ≠ 0

### 🐯 Caution with Correlation
- Be careful with claims of casuality
- Exercise caution while correlating averaged data
- Check for outliers
- Beware of non-linear relationships

---



