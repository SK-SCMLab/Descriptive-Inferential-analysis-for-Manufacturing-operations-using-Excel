# 🐱 Descriptive-Inferential-analysis-for-Manufacturing-operations-using-Excel
This repository showcases practical examples of using Microsoft Excel for multivariate and regression-based analytics in a manufacturing operations setting. The dataset simulates production parameters across multiple machines and products. It includes:

1. Multi-variate analysis
2. Correlation
3. Regression analysis
4. Residual analysis
5. Confidence Interval
6. Prediction interval

---

## 🐭 Multi-variate analysis (~Regression analysis)
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

## 🦁 Regression Analysis (R²)
- Regression estimates how one variable (dependent) changes with respect to one or more independent variables
- Correlation provides direction of movement of the dependent variable Y as independent variable X changes
- Does not provide the extent of the movement of Y as X changes
- Regression analysis is an approach for estimating the extent of change in a dependent variable when an independent variable changes
- Regression analysis generates a line on scatter plot that quantifies the relationship between X & Y
- A regression equation describes the line

      Note: 1. If a high percentage of variability in Y (R² > 70%) is explained by changes in X
            2. Predict future values of Y given X, and X given Y
            3. Regress Y on one or more X's simultaneously

### 🐮 Key concepts of regression
- The output of regression is a transfer function f(x)
- The transfer function may not be the best function to control Y, as there are chances of a low-level of correlation between Y & X
- The main focus of regression is to discover whether a significant statistical relationship exists between Y & particular X by looking at p-values
- Based on regression, one can determine the vital X, and eliminate the unimportant X's

      The Simple Linear Regression (SLR) should be used as a statistical validation tool in the beginning of the analysis phase
                  SLR => Y = A + BX ± C
                          Y -> Dependent variable/output/response
                          X -> Independent variable/predictor
                          A -> Intercept of fitted line on Y-axis
                          B -> Regression coefficient/slope of the fitted line
                          C -> Error in the regression model

#### Least squares Method in SLR
                    Sum of Squared Errors (SSE) = ∑i=1^n (yᵢ-ŷᵢ)² || Error/Residuals
In a perfect linear relationship, the points would lie on the line

---

## 🐷 Residual Analysis
- Residuals are differences between observed and predicted values. Analyzing them helps to validate the regression model
- A residual plot is a graph that is used to examine the goodness-of-fit in regression. The different residual plots for Y are:
  1. Normal Probability plot of residuals are used to verify the assumption that the residuals are normally distributed
  2. Residual versus fit is used to verify the assumption that the residuals have a constant variation
  3. Histogram of the residuals is used to determine or whether outliers exist in the data
  4. Residuals versus order of data is used to verify the assumption that the residuals are uncorrelated with each other
  5. The residuals between the actual value and predicted value given an indication of how good the model is:

                              Total Sum of Squares (SST) = SSE + Sum of Squares due to Regression (SSR)
                                                  SSR = SST - SSE
                                                   R² = SSR/SST
                  To get the sense of the error in the fitted model, one must calculate the value of Y for a given data using the fitted equation
  6. To check for error, take two observations of Y at the same X
  7. Prioritization of X's can be done through the SLR equation; run separate regressions on X with each Y
  8. If an X does not explain variation in Y, it should not be explored further

### 🐽 Difference between correlation and causation
- A regression equation denotes only a relationship between two variables
- A change in one variable may not cause change in the other
- The change in the variable could be caused due to the third factor

---

## 🐸 Multiple regression
- If a new variable X₂ is added to the R² model, the impact of X₁ and X₂ on Y gets tested

                          Y = b₀ + b₁x₁ + b₂x₂ + ..... bₙxₙ
                          where x₁, x₂, ...... xₙ are multiple independent variables
- Multiple regression allows us to determine a linear relationship between multiple variables

### 🐵 Multiple Linear regression
- The value of R² changes with the introduction of a new variable
- The resulting value of R² is known as R² adjusted
- The model can be used if 'R² adjusted' value is greater than 70%

                  Any regression model that is not linear is considered non-linear
                  Other non-linear regression models are Cubic, Quadratic, Power, Logarithmic and Logistic

---

## 🙈 Confidence interval
- Indicates how well the mean was determined by the likely location of the true population parameter
- If data is sampled from a Normal distribution many times and a 95% confidence interval of the mean is calculated from each sample, about 95% of those intervals would include the true value of population mean

## 🙉 Prediction interval
- Shows where the next sample data point is expected and given insight about the distribution of values
- If data follows a normal distribution, collect a sample of data and calculate a 95% prediction interval. If this is done many times, the next value sampled will lie within the prediction interval in 95% of the sample
- Strong correlation between variables does not imply they have a casual relationship

---

## 🐧 Case study: Multivariate and regression analysis in Steel manufacturing operation
### 🙊 Objectives
- To study how multiple input factors affect the tensile strength of the steel
- To analyze the correlation between critical process variables and the resulting output thickness of steel sheets in a hot rolling process
- To evaluate how accurately a linear regression model predicts output thickness based on the speed and furnace temperature in hot rolling process by performing residual analysis
- To estimate the confidence interval for the mean predicted output thickness and the prediction interval for the individual future thickness measurement based on rolling speed and furnace temperature

---

### 🐒 Interpretation
1. *Situation: The manufacturing plant operates 65 resources (machines) to produce steel. The Production Planning Manager want to perform analysis to find out the factors that are affecting the output strength of the steel*

   **Inference**: *Multi-variate analysis* || From the excel analysis, there exists:
                   1. No correlation between pressure and thickness
                   2. Weak negative correlation between temperature and thickness
                   3. No correlation between speed and thickness

    **SUMMARY OUTPUT TABLE SIGNIFICANCE (from Excel)**
   |*Term*|*Significance*|
   |------|--------------|
   |**Multiple R** | Correlation coefficient between observed and predicted values. Ranges from -1 to +1. Closer to ±1 means stronger relationship |
   |**R Square** | Proportion of the variance in the dependent variable explained by the model (0 to 1). Higher is better |
   |**Adjusted R Square** | Like R², but adjusts the number of predictors. Use this when comparing models with different number of variables |
   |**Standard Error** | Standard deviation of residuals (error). Lower indicates better fit |
   |**Observations** | Number of data points used in the regression |

   |*Term*|*Significance*|
   |------|--------------|
   |**df**| Degrees of freedom for regression, residual, and total|
   |**SS**| Sum of Squares - measures variability|
   |**MS**| Mean Square = SS/df|
   |**F**| F-statistic. Compares model with no predictors. Higher F = more significant model|
   |**Significance F**|P-value for overall regression. If **< 0.05**, model is statistically significant|

   |*Column*|*Significance*|
   |--------|--------------|
   |**Intercept**|Predicted value when all X's = 0|
   |**X Variable(s)**|Coefficients for each independent variable|
   |**Standard Error**|Uncertainty in coefficient estimate|
   |**t Stat**| Coefficient/std. error. Used to test significance|
   |**P-value**|If <0.05, variable is statistically significant|
   |**Lower/Upper 95%**|Confidence interval for coefficient. If it crosses zero, the variable may not be significant|

   **Conclusion**: 1. Furnace temperature and Speed show no influence
                   2. Hydraulic Pressure has the brief impact comparatively on final thickness of the steel
                   3. The regression model is not strong enough to be statistically significant at 95% confidence. Hence, the model may be acceptable at 90% confidence

3. *Situation: The Production Planning Manager wants to understand the relationships between the variables that are used in the master data for operation purposes*

   **Inference**: *Correlation Analysis* || From the excel analysis, there existed only weak positive or weak negative correlation

    **Conclusion**: 1. Comparatively, furnace temperature has the strongest impact on the sheet thickness
                    2. Parameters that show negative correlation with thickness represents inversely proportionate relation with one another
                    3. These insights helps in process tuning and quality improvement

4. *Situation: The Planning Manager wants to evaluate the quality of the regression model created by the team to predict sheet thickness from rolling speed and furnace temperature*

   **Inference**: *Residual analysis* || From the excel analysis, the residuals are way far from zero. It indicates that model's prediction differ significantly from the actual values.

   **Conclusion**: 1. Poor model fit (wrong variables, missing variables)
                   2. Non-linear relationship
                   3. Outliers or noise in the data
                   4. Multicollinearity among input variables
                   5. Omitted influential variables

5. *Situation: Based on the process parameters, the Planning Manager wants to predict hot rolled sheet thickness to estimate confidence and prediction accuracy*

   **Inference**: *CI & PI* || From the excel analysis, PI is always wider than CI because it includes individual variation

---

## 🐦 Repository structure
Resource_sample dataset
        -ResourceGroups

---

## 🐦‍⬛ Excel functionalities used
- CORREL()
- RAND()
- RANDBETWEEN()
- SQRT()
- DATA ANALYSIS > REGRESSION

---

## 🐤 Requirements
- Microsoft Excel 2016 or later
- Business statistics, Manufacturing operations basics

---

*"Facts are stubborn, but statistics are more pliable" - Mark Twain*
