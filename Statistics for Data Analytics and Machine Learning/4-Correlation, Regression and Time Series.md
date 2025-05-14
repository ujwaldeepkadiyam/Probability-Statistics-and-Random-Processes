<p style="text-align:center;"><font color="red">Correlation</font></p>

## 📊 Correlation and Its Types

### What is Correlation?

**Correlation** is a statistical measure that describes the strength and direction of a relationship between two variables.

- It answers the question: _"Do two variables move together?"_
    
- Denoted by **r** (correlation coefficient), which ranges from **-1 to +1**:
    
    - **+1** → perfect positive correlation
        
    - **0** → no correlation
        
    - **–1** → perfect negative correlation
        



### Types of Correlation

### 1. **Positive Correlation**

- Both variables move in the **same direction**.
    
- As one increases, the other increases too.
    
- Example: Height and weight.
    

```
r > 0
```

### 2. **Negative Correlation**

- Variables move in **opposite directions**.
    
- As one increases, the other decreases.
    
- Example: Number of hours studied vs. number of hours spent watching TV.
    

```
r < 0
```

### 3. **Zero Correlation**

- No predictable relationship between the variables.
    
- Example: Shoe size and intelligence.
    

```
r ≈ 0
```

---

## Types Based on Degree of Correlation

|Correlation Type|Correlation Coefficient (r)|
|---|---|
|Perfect Positive|r = +1|
|Strong Positive|+0.7 ≤ r < +1|
|Moderate Positive|+0.3 ≤ r < +0.7|
|Weak Positive|0 < r < +0.3|
|No Correlation|r = 0|
|Weak Negative|-0.3 < r < 0|
|Moderate Negative|-0.7 < r ≤ -0.3|
|Strong Negative|-1 < r ≤ -0.7|
|Perfect Negative|r = -1|

---

## Visual Representation

> Scatter plots are commonly used to visualize correlation:

- **Positive Correlation**: points trend upwards.
    
- **Negative Correlation**: points trend downwards.
    
- **No Correlation**: points are scattered randomly.
    

---

## Important Notes

- **Correlation does NOT imply causation.**
    
- Use **Pearson** correlation for linear relationships.
    
- Use **Spearman** correlation for ranked or non-linear data.




<p style="text-align:center;"><font color="red">Linear Regression</font></p>

## 📈 Linear Regression: A Complete Overview

### 🔹 What is Linear Regression?

**Linear regression** is a statistical method used to model the relationship between a **dependent variable** (target) and one or more **independent variables** (predictors), assuming the relationship is **linear**.

---

### 🔹 Types of Linear Regression

1. **Simple Linear Regression**
    
    - One independent variable (x), one dependent variable (y)
        
    - Model:
        
        ```
        y = a + bx
        ```
        
2. **Multiple Linear Regression**
    
    - More than one independent variable
        
    - Model:
        
        ```
        y = a + b₁x₁ + b₂x₂ + ... + bₙxₙ
        ```
        

---

## 🔹 Components of the Model

- **y**: Dependent variable (response)
    
- **x**: Independent variable (predictor)
    
- **a**: Intercept (value of y when x = 0)
    
- **b**: Slope (change in y per unit change in x)
    
- **ε (epsilon)**: Error term (difference between actual and predicted values)
    

---

## 🔹 Assumptions of Linear Regression

1. **Linearity**: Relationship between x and y is linear.
    
2. **Independence**: Observations are independent.
    
3. **Homoscedasticity**: Constant variance of residuals.
    
4. **Normality**: Residuals are normally distributed.
    
5. **No multicollinearity** (for multiple regression): Predictors should not be highly correlated.
    

---

## 🔹 How It Works

Linear regression finds the **line of best fit** by minimizing the **sum of squared residuals (errors)** — this is known as **Ordinary Least Squares (OLS)**.

### Formula (OLS Objective):

```
Minimize ∑(yᵢ - ŷᵢ)²
```

Where:

- `yᵢ` is the actual value
    
- `ŷᵢ` is the predicted value
    

---

## 🔹 Model Evaluation Metrics

|Metric|Description|
|---|---|
|**R-squared (r²)**|Proportion of variance in y explained by x|
|**MAE**|Mean Absolute Error (average absolute difference)|
|**MSE**|Mean Squared Error|
|**RMSE**|Root Mean Squared Error|

---

## 🔹 Use Cases

- Predicting sales based on ad spending
    
- Estimating housing prices from features
    
- Forecasting demand or trends over time
    

---

## 🔹 Limitations

- Assumes a linear relationship
    
- Sensitive to outliers
    
- Poor performance if assumptions are violated
    

---

## 🔹 Visual Example

> A scatter plot with a line through the data points:

- The closer the points to the line, the better the model.
    
- Residuals (errors) are the vertical distances from the points to the line.
    

---

## ✅ Summary

- **Simple, fast, interpretable** model
    
- Best for linear, continuous data
    
- Good baseline for predictive analytics
    

<p style="text-align:center;"><font color="red">Logistic Regression</font></p>
### 🔐 Logistic Regression: A Complete Overview

### 🔹 What is Logistic Regression?

**Logistic regression** is a **classification** algorithm used to predict a **binary outcome** (e.g., Yes/No, 0/1, True/False) based on one or more independent variables.

It estimates the **probability** that a given input belongs to a particular category.

---

### 🔹 When to Use Logistic Regression?

- Target variable is **categorical** (mostly binary)
    
- You want to predict the **likelihood** of an event
    
- Examples:
    
    - Will a customer buy a product? (Yes/No)
        
    - Is an email spam or not?
        

---

## 🔹 Logistic vs Linear Regression

|Feature|Linear Regression|Logistic Regression|
|---|---|---|
|Output|Continuous|Probability (0 to 1)|
|Purpose|Predict value|Classify categories|
|Algorithm|OLS (least squares)|MLE (maximum likelihood)|
|Linearity|Models y as linear|Models log-odds as linear|

---

## 🔹 The Logistic Function (Sigmoid)

The logistic model uses the **sigmoid function** to map any real value to a probability between 0 and 1.

```
Sigmoid(z) = 1 / (1 + e^(–z))
```

Where:

- `z = a + b₁x₁ + b₂x₂ + ... + bₙxₙ` (linear combination of inputs)
    

---

## 🔹 Model Equation

```
P(y=1|x) = 1 / (1 + e^(–(a + bx)))
```

- Predicts the **probability** that `y = 1`
    
- Decision rule:
    
    ```
    If P ≥ 0.5 → Class = 1  
    If P < 0.5 → Class = 0
    ```
    

---

## 🔹 Types of Logistic Regression

1. **Binary Logistic Regression**
    
    - Two possible outcomes (e.g., 0 or 1)
        
2. **Multinomial Logistic Regression**
    
    - More than two unordered categories
        
3. **Ordinal Logistic Regression**
    
    - More than two **ordered** categories
        

---

## 🔹 Model Evaluation Metrics

|Metric|Description|
|---|---|
|**Accuracy**|% of correct predictions|
|**Precision**|True Positives / (True Positives + FP)|
|**Recall**|True Positives / (True Positives + FN)|
|**F1 Score**|Harmonic mean of precision and recall|
|**ROC Curve**|Graph of True Positive Rate vs. False Positive Rate|
|**AUC**|Area under ROC curve; higher is better|

---

## 🔹 Assumptions of Logistic Regression

1. **Binary outcome** (for basic logistic regression)
    
2. **Independence** of observations
    
3. **Linearity in the logit** (log-odds, not raw y)
    
4. **No multicollinearity** among independent variables
    
5. **Large sample size** preferred for stability
    

---

## 🔹 Limitations

- Cannot handle non-linear relationships without transformations
    
- Sensitive to outliers and imbalanced data
    
- Assumes independence of observations
    

---

## ✅ Summary

- **Used for classification**, not regression
    
- Outputs probabilities → converted to classes
    
- Widely used in healthcare, marketing, finance, etc.
    
- Easy to interpret and quick to train
    


<p style="text-align:center;"><font color="red">Time Series</font></p>



## ⏳ Time Series: A Complete Overview

### 🔹 What is a Time Series?

A **time series** is a sequence of data points collected or recorded at **regular time intervals** (e.g., hourly, daily, monthly).

Examples:

- Daily stock prices
    
- Monthly sales
    
- Annual rainfall
    

---

### 🔹 Key Components of Time Series

1. **Trend**
    
    - Long-term direction in the data
        
    - 📈 Example: Gradual increase in sales over years
        
2. **Seasonality**
    
    - Repeating patterns at regular intervals (e.g., monthly, quarterly)
        
    - 📆 Example: Higher ice cream sales every summer
        
3. **Cyclicality**
    
    - Long-term fluctuations not of fixed length (e.g., economic cycles)
        
    - 📉 Example: Recession and recovery periods
        
4. **Irregular/Noise**
    
    - Random variation or residuals in the data
        
    - ⚠️ Not predictable
        

---

### 🔹 Types of Time Series

| Type               | Description                              | Example                         |
| ------------------ | ---------------------------------------- | ------------------------------- |
| **Univariate**     | Single variable measured over time       | Monthly temperature             |
| **Multivariate**   | Multiple variables over time             | Temperature, humidity, and wind |
| **Stationary**     | Constant mean, variance, autocorrelation | White noise                     |
| **Non-stationary** | Varying trend, seasonality, etc.         | GDP, stock prices               |

---

### 🔹 Time Series Analysis Goals

- **Understand patterns** in past data
    
- **Forecast** future values
    
- **Detect anomalies**
    
- **Model** behavior over time
    

---

### 🔹 Time Series Modeling Techniques

| Model                      | Use Case                              | Notes                                   |
| -------------------------- | ------------------------------------- | --------------------------------------- |
| **AR (AutoRegressive)**    | Uses past values of the series        | Suitable for stationary data            |
| **MA (Moving Average)**    | Uses past errors/residuals            | Smooths out noise                       |
| **ARMA**                   | Combines AR and MA                    | For stationary data                     |
| **ARIMA**                  | ARMA + differencing                   | Handles non-stationary series           |
| **SARIMA**                 | ARIMA with seasonality                | For seasonal time series                |
| **Exponential Smoothing**  | Weighted average of past values       | Simple and robust                       |
| **Prophet (by Facebook)**  | Decomposable model with holidays      | Good for business applications          |
| **LSTM (Neural Networks)** | Deep learning for sequence prediction | Complex and powerful for large datasets |

### 🔹 Steps in Time Series Forecasting

1. **Plot the data**
    
2. **Check stationarity** (use ADF test)
    
3. **Decompose components** (trend, seasonality)
    
4. **Apply transformations** (log, differencing)
    
5. **Fit a model** (ARIMA, SARIMA, etc.)
    
6. **Evaluate accuracy** (MAE, RMSE, MAPE)
    
7. **Forecast future values**
    

---

### 🔹 Time Series Evaluation Metrics

|Metric|Description|
|---|---|
|**MAE**|Mean Absolute Error|
|**RMSE**|Root Mean Squared Error|
|**MAPE**|Mean Absolute Percentage Error|
|**R²**|Goodness of fit (for regression models)|

---

### ✅ Summary

- Time series deals with data **indexed by time**
    
- Analyzing and forecasting depends on identifying **patterns and structure**
    
- Popular in fields like **finance, economics, weather, and operations**
    
