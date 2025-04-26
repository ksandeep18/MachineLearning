# Types of Errors in Supervised Machine Learning

Supervised machine learning involves predicting an output variable based on labeled input data. The performance of these models is assessed using error metrics, which differ for regression and classification tasks.

---

## 📈 Regression Errors

In regression, the goal is to predict a continuous value. Errors are the differences between predicted and actual values.

### 1. **Mean Absolute Error (MAE)**
- **Definition**: Average of the absolute differences between predicted and actual values.
- **Formula**:
  ```
  MAE = (1/n) * Σ|yᵢ - ŷᵢ|
  ```

### 2. **Mean Squared Error (MSE)**
- **Definition**: Average of the squared differences between predicted and actual values.
- **Formula**:
  ```
  MSE = (1/n) * Σ(yᵢ - ŷᵢ)²
  ```

### 3. **Root Mean Squared Error (RMSE)**
- **Definition**: Square root of MSE, brings error metric back to the original scale.
- **Formula**:
  ```
  RMSE = sqrt(MSE)
  ```

### 4. **R-squared (R²) / Coefficient of Determination**
- **Definition**: Proportion of the variance in the dependent variable that is predictable.
- **Formula**:
  ```
  R² = 1 - (SS_res / SS_tot)
  ```

---

## 📊 Classification Errors

In classification, the model predicts a category label. Errors are evaluated based on the number of correct and incorrect predictions.

### 1. **Accuracy**
- **Definition**: Ratio of correctly predicted observations to the total observations.
- **Formula**:
  ```
  Accuracy = (TP + TN) / (TP + TN + FP + FN)
  ```

### 2. **Precision**
- **Definition**: Ratio of true positives to all predicted positives.
- **Formula**:
  ```
  Precision = TP / (TP + FP)
  ```

### 3. **Recall (Sensitivity or True Positive Rate)**
- **Definition**: Ratio of true positives to all actual positives.
- **Formula**:
  ```
  Recall = TP / (TP + FN)
  ```

### 4. **F1 Score**
- **Definition**: Harmonic mean of precision and recall.
- **Formula**:
  ```
  F1 = 2 * (Precision * Recall) / (Precision + Recall)
  ```

### 5. **Confusion Matrix**
- **Definition**: A matrix showing TP, TN, FP, and FN to evaluate classification performance.

  |                    | Predicted Positive | Predicted Negative |
  |--------------------|--------------------|--------------------|
  | **Actual Positive**| TP                 | FN                 |
  | **Actual Negative**| FP                 | TN                 |

### 6. **Log Loss / Cross-Entropy Loss**
- **Definition**: Measures the performance of a classification model with probability outputs.
- **Formula**:
  ```
  Log Loss = - (1/n) * Σ [yᵢ * log(pᵢ) + (1 - yᵢ) * log(1 - pᵢ)]
  ```

---

## ⚠️ Common Error Sources

### 1. **Bias Error**
- **Definition**: Error from wrong assumptions in the learning algorithm.
- **Effect**: Leads to underfitting.

### 2. **Variance Error**
- **Definition**: Error from sensitivity to small fluctuations in the training set.
- **Effect**: Leads to overfitting.

### 3. **Irreducible Error**
- **Definition**: Error caused by noise or unknown factors in data.
- **Effect**: Cannot be eliminated regardless of model used.

---

## 🎯 Bias-Variance Tradeoff

- **Goal**: Find a balance between bias and variance to minimize total error.
- **High Bias**:
  - Oversimplified model.
  - Fails to capture patterns.
  - High training and test error.

- **High Variance**:
  - Overcomplicated model.
  - Captures noise in training data.
  - Low training error, high test error.

- **Tradeoff**:
  - Reducing bias increases variance, and vice versa.
  - Ideal model has low bias and low variance.

**Total Error = Bias² + Variance + Irreducible Error**

---

## ✅ Summary Table

| Error Type            | Regression       | Classification      |
|----------------------|------------------|----------------------|
| Absolute Error        | MAE              | –                    |
| Squared Error         | MSE, RMSE        | –                    |
| Relative Score        | R²               | Accuracy, F1 Score   |
| Probabilistic Error   | –                | Log Loss             |
| Confusion-Based       | –                | Confusion Matrix     |
| Fundamental Sources   | Bias, Variance   | Bias, Variance       |
