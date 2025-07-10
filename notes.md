# Time Series Data

Observations collected over a sequence of intervals. 
Wind Speed data is collected hourly. No missing values.

---

## Decomposition

### 1. Trend
- Long tern direction of data. Can be upward, downward or mix of both.

### 2. Seasonality
-   Pattern that repeats after a fixed interval of time.

### 3. Cyclic
-   The pattern that occurs is not necessarily at fixed intervals.

### 4. Noise
-   Sudden fluctuation in data

----

## Types of Decomposition

### Addititve
-   Adding the components of data to get original   (T + S + N)

### Multiplicative
-   Multiplying the components of data to get original  (T * S * N)

---

## STL decomposition using LOESS (locally estimated scatterplot smoothing)

Helps in finding the actual seasonal pattern and can handle outliers.       (Additive only)

Classical decomposition assumes that data has fixed seasonal patterns and is easily affected by outliers.

---

## Stationarity

These 3 stay constant overtime.
- Mean
- Variance
- Auto correlation 

### Why do we need stationary time series model?

- Statistical properties remain similar therefore helping us predict the values.

- Forecasting models require stationarity data for efficient prediction.

## Types of Stationarity

### Weak Stationarity
Constant mean, variance and auto correlation     (Preferred for forecasting and short period of data)

### Strong Stationarity
Properties of weak and joint distribution remains unchanged when shifted along any time period  (Modeling distribution of entire data)

---

## Testing for stationarity 

### Weak Stationarity:
#### ADF Test
---
Check for the presense of unit root *(non stationary trend)*

H_o Null Hypothesis : data has a unit root therefore non stationary<br>
H_l Alternate Hypothesis : data does not have unit root therefore stationary

##### Decision Criteria :  
    p < significance value      -> stationary
    ADF statistic < critical value  -> reject null hypothesis

#### KPSS Test
---
Fits a constant mean model on the data abd neasures the variance of cumilative sum of residuals.

H_o : stationary<br>
H_l : non stationary

##### Decision Criteria :  
    p < significance value      -> non - stationary
    KPSS statistic > critical value  -> non - stationary

### Strick Stationarity:

#### KS Test
---
Compare the cumilative distribution functions of two samples
##### Decision Criteria :  
    p < significance value      -> no difference in distribution therefore stationary
    ADF statistic < critical value  -> reject null hypothesis


---


## Making a time series stationary

### Differencing

y_t   : current value
y_t-1 : past value

** Can be done for seasonal values **

#### first order differrencing : y'_t = y_t - y_t-1         
#### second order differencing : y"_t = y'_t - y'_t-1     


---

### Transformation

stabilizes the variance of time series data

- Logarithimic   

- Power

- Box Cox

### De-trending

removing trend component

- Linear De-trending
- Moving average

### Seasonality Adjustment

removing seasonal component

---

## Time Series Forecasting Models
 Univariate Models

### Auto Regressive (AR)

uses past values to predict future models.

Order : number of past values

### Moving Average

uses past error terms



| Name                                | Rank (US News CS) | Avg Admitted GPA | Min IELTS | Avg GRE Quant | Avg GRE Verbal | Category     |        |
| ----------------------------------- | ----------------- | ---------------- | --------- | ------------- | -------------- | ------------ | ------ |
| University of Washington            | 13                | 3.4              | 7.0       | 162           | 155            | Backup       |        |
| Michigan–Dearborn                   | N/A               | 3.2              | 6.5       | 160           | 150            | Backup       |        |
| University of Illinois Chicago      | Illinois DS       | N/A              | 3.3       | 6.5           | 162            | 152          | Backup |
| Michigan State University           | N/A               | 3.3              | 6.5       | 160           | 152            | Backup       |        |
| San Jose State University           | N/A               | 3.2              | 6.5       | 160           | 150            | Backup       |        |
| NYU Tandon                          | 13                | 3.3              | 7.0       | 164           | 152            | Realistic    |        |
| University of Maryland–College Park | 26                | 3.4              | 7.0       | 163           | 154            | Realistic    |        |
| Texas A&M                           | 18                | 3.4              | 7.0       | 162           | 154            | Realistic    |        |
| University of Florida               | 28                | 3.4              | 6.5       | 162           | 153            | Realistic    |        |
| Georgia Tech                        | 8                 | 3.7              | 7.5       | 165           | 156            | Aspirational |        |
| UC Irvine                           | 35                | 3.4              | 7.0       | 163           | 154            | Aspirational |        |
| UCLA                                | 13                | 3.6              | 7.0       | 165           | 156            | Aspirational |        |
| UC Santa Barbara                    | 23                | 3.5              | 7.0       | 164           | 154            | Aspirational |        |
| UC Davis                            | 27                | 3.5              | 7.0       | 163           | 154            | Aspirational |        |
| UC San Diego                        | 11                | 3.6              | 7.0       | 165           | 156            | Aspirational |        |
| Purdue University                   | 9                 | 3.6              | 7.0       | 165           | 155            | Aspirational |        |
| Northwestern University             | 12                | 3.7              | 7.5       | 166           | 155            | Aspirational |        |
| Brown University                    | 14                | 3.7              | 7.5       | 165           | 158            | Aspirational |        |
| University of Virginia              | 30                | 3.5              | 7.0       | 163           | 154            | Aspirational |        |
| University of Pennsylvania          | 10                | 3.8              | 7.5       | 166           | 157            | Aspirational |        |
| UC Berkeley                         | 2                 | 3.7              | 7.5       | 166           | 157            | Out of Reach |        |
| Carnegie Mellon                     | 1                 | 3.8              | 7.5       | 167           | 158            | Out of Reach |        |
| MIT                                 | 1                 | 3.9              | 7.5       | 167           | 158            | Out of Reach |        |
|                                     |                   |                  |           |               |                |              |        |