# S&P 500 Log Returns Analysis

This project, developed as part of an Advanced Econometrics course, analyzes the log returns of the S&P 500 index to evaluate the distribution characteristics of financial data. It includes empirical distribution analysis, density estimation, confidence intervals, and normality tests.

## Project Structure

1. **Dataset**: Download the S&P 500 adjusted closing prices.
2. **Log Returns Calculation**: Compute log returns, \( r_t = \log(P_t / P_{t-1}) \).
3. **Empirical Cumulative Distribution Function (ECDF)**: Calculate and visualize the ECDF of the log returns.
4. **Confidence Bands for CDF**: Construct pointwise and uniform 95% confidence bands.
5. **Kolmogorov-Smirnov Test**: Perform a KS test for normality of log returns.
6. **Kernel Density Estimation (KDE)**: Implement Epanechnikov kernel density estimation with plug-in bandwidth selection.
7. **Density Comparison**: Compare the KDE with a normal density estimation.
8. **Confidence Intervals for KDE**: Calculate pointwise confidence intervals for KDE estimates.
9. **Additional Normality Tests**: Test for stationarity, autocorrelation, and normality using statistical tests.

## Installation

Clone this repository and install the required libraries:
```bash
git clone <repository-url>
pip install -r requirements.txt
```

## Data

The dataset used is the S&P 500 (^GSPC) historical data (2010-01-01 to 2020-01-01), which is retrieved using the `yfinance` library and saved as `SP500.csv`.

## Analysis

### 1. Load and Prepare Data

```python
import yfinance as yf
data = yf.download('^GSPC', '2010-01-01', '2020-01-01')
data.to_csv('SP500.csv')
```

### 2. Calculate Log Returns

Load the data and compute log returns:
```python
import pandas as pd
import numpy as np
sp500_data = pd.read_csv('SP500.csv')
adjusted_closing_prices = sp500_data['Adj Close']
log_returns = np.log(adjusted_closing_prices / adjusted_closing_prices.shift(1)).dropna()
```

### 3. Empirical CDF and Confidence Bands

- **ECDF**: Visualize the cumulative distribution of log returns.
- **Pointwise Confidence Bands**: Construct 95% pointwise confidence intervals.
- **Uniform Confidence Bands**: Use Kolmogorov-Smirnov distribution to build uniform bands.

### 4. Kolmogorov-Smirnov Test for Normality

Conduct a KS test to check if log returns follow a normal distribution:
```python
from scipy.stats import kstest
ks_stat, p_value = kstest(log_returns, 'norm', args=(mean, std_dev))
```

### 5. Kernel Density Estimation (Epanechnikov Kernel)

Estimate density with Epanechnikov kernel, determine plug-in bandwidth, and compare with normal distribution density.

### 6. Confidence Intervals for KDE

Construct 95% confidence intervals for KDE to assess the estimated density of log returns.

## Results Summary

- **Normality Tests**: Log returns deviate from normality as shown by KS and Shapiro-Wilk tests.
- **KDE Insights**: Financial data demonstrates heavier tails and peakedness around the mean, captured well by KDE but not by normal distribution.
- **Confidence Bands**: Highlight the high probability of extreme returns, showcasing limitations of normal distribution in financial data.

## Conclusion

The analysis reveals that S&P 500 log returns are not normally distributed, exhibit autocorrelation, and have heavier tails and a sharper peak, typical in financial returns. This supports the use of non-parametric approaches like KDE over assuming normality for risk and return assessments.

## License

This project is open-source and licensed under the MIT License.

---
