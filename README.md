# Advanced Econometrics Homework: Exploring Econometric Tools and Concepts

This repository contains assignments from an Advanced Econometrics course, showcasing the practical application of theoretical concepts to analyze real-world economic phenomena. The focus is on using advanced econometric tools to understand complex relationships, construct robust models, and interpret results.

---

## Overview

The homework emphasizes learning and applying econometric methods to estimate relationships, test hypotheses, and evaluate model assumptions. The tasks include both parametric and non-parametric approaches, with a strong focus on understanding the underlying theory and practical implementation.

---

## Key Econometric Tools and Concepts

### 1. **Non-Parametric Estimation**
   - **Estimators**:
     - Nadaraya-Watson estimator for flexible regression modeling.
     - Local Linear estimator for smooth and stable regression fits.
   - **Kernel Functions**:
     - Epanechnikov kernel for density estimation.
     - Bandwidth selection via Leave-One-Out Cross-Validation (LOOCV) to optimize model performance.
   - **Confidence Intervals**:
     - Pointwise confidence intervals for precise estimates.
     - Uniform confidence bands constructed using Gaussian multiplier bootstrap for global inference.

### 2. **Regression Analysis**
   - **Ordinary Least Squares (OLS)**:
     - Linear regression modeling with intercept terms.
     - Model diagnostics, including R-squared and significance testing.
   - **Comparison with Non-Parametric Methods**:
     - Highlighting the advantages of non-parametric methods in capturing nonlinear relationships.

### 3. **Hypothesis Testing and Model Validation**
   - Residual diagnostics to assess model fit and assumptions.
   - Gaussian multiplier bootstrap for constructing robust confidence intervals.
   - Evaluation of nonlinearity and shifts in relationships through visual and statistical diagnostics.

### 4. **Data Visualization**
   - Graphical representation of regression estimates, including confidence intervals and bands.
   - Comparison of parametric and non-parametric fits.
   - Insights into the shape of relationships and their implications.

---

## Skills and Insights Gained

1. **Understanding Non-Parametric Methods**:
   - Flexibility of Nadaraya-Watson and Local Linear estimators in modeling complex relationships.
   - Importance of bandwidth selection in non-parametric estimation.

2. **Regression Techniques**:
   - Strengths and limitations of OLS in capturing linear relationships.
   - Practical comparison between parametric and non-parametric approaches.

3. **Constructing Confidence Intervals**:
   - Differences between pointwise and uniform intervals.
   - Using bootstrap techniques to account for variability in non-parametric estimates.

4. **Model Interpretation and Inference**:
   - Application of econometric tools to uncover relationships and test theories.
   - Visualization techniques to communicate results effectively.

---

## Installation and Usage

Clone the repository and install the required Python libraries:

```bash
git clone <repository-url>
pip install -r requirements.txt
```

Run the `HW3.ipynb` notebook to implement the econometric methods and explore the results.

---

## License

This project is open-source and licensed under the MIT License.
