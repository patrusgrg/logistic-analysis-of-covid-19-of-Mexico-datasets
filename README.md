# Logistic Analysis of COVID-19 Mexico Datasets

This repository contains a statistical analysis of COVID-19 data from Mexico using logistic regression techniques.

## Mathematical Background

### Logistic Regression Model

The logistic regression model estimates the probability of a binary outcome. For COVID-19 analysis, we model the probability of a positive case based on various features.

The logistic function (sigmoid) is defined as:

$$ \sigma(z) = \frac{1}{1 + e^{-z}} $$

where $z = \beta_0 + \beta_1x_1 + \beta_2x_2 + ... + \beta_nx_n$

### Model Components

- $\sigma(z)$: Probability of the outcome (0 to 1)
- $\beta_0$: Intercept term
- $\beta_i$: Coefficient for feature $x_i$
- $x_i$: Input features (e.g., age, comorbidities, etc.)

### Log-Likelihood Function

The model is trained by maximizing the log-likelihood function:

$$ \mathcal{L}(\beta) = \sum_{i=1}^{n} [y_i \log(\sigma(z_i)) + (1-y_i)\log(1-\sigma(z_i))] $$

where:
- $y_i$ is the actual outcome (0 or 1)
- $n$ is the number of observations

### Model Evaluation

The model's performance is evaluated using the following metrics:

| Metric | Formula |
|--------|---------|
| Accuracy | `(TP + TN) / (TP + TN + FP + FN)` |
| Precision | `TP / (TP + FP)` |
| Recall | `TP / (TP + FN)` |
| F1 Score | `2 * (Precision * Recall) / (Precision + Recall)` |

Where:
- `TP`: True Positives (correctly predicted positive cases)
- `TN`: True Negatives (correctly predicted negative cases)
- `FP`: False Positives (incorrectly predicted positive cases)
- `FN`: False Negatives (incorrectly predicted negative cases)

#### Visual Representation:

```
Accuracy = (True Positives + True Negatives) / Total Cases
         = (TP + TN) / (TP + TN + FP + FN)

Precision = True Positives / Predicted Positives
         = TP / (TP + FP)

Recall = True Positives / Actual Positives
       = TP / (TP + FN)

F1 Score = 2 * (Precision * Recall) / (Precision + Recall)
```

## Implementation

The analysis is implemented using Python with the following key libraries:
- pandas: For data manipulation
- scikit-learn: For logistic regression implementation
- numpy: For numerical computations
- matplotlib/seaborn: For visualization

## License

This project is licensed under the MIT License - see the LICENSE file for details.