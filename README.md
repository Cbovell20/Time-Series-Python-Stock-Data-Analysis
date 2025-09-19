# Python Stock Data Analysis and Monte Carlo Simulation  
*SPX, MSFT, UNH Empirical Returns - Curtis Bovell*

---

## Project Summary  

This project analyzes daily stock data for SPX, MSFT, and UNH from 2010 to 2023 using Python. Key steps include:  
- Importing and cleaning historical price and volume data from CSV files.  
- Calculating log returns and summary statistics (mean, std dev, skewness, kurtosis).  
- Plotting histograms and autocorrelation functions (ACF) of prices, returns, and squared returns.  
- Computing correlations between returns and volume.  
- Estimating conditional probabilities for price and volume changes based on previous day movements.  
- Running Monte Carlo simulations by regressing empirical returns on simulated normal variables and assessing statistical significance over 1000 runs.

## Return Calculation

Returns (r_t) are computed as the percentage log difference of adjusted prices:
rt = 100[log(pt) − log(pt−1)]

where ( p_t) is the adjusted closing price at time (t)

## Findings  

- Return distributions show negative skewness and heavy tails (high kurtosis), deviating from normality.  
- Low correlation between returns and volume.  
- Price and volume conditional probabilities exhibit some persistence in movement direction.  
- Monte Carlo results illustrate expected rates of false positives in regressions with random data (intercept significant ~24.6%, slope ~5.6%).

## Usage  

1. Place CSV files in `data/` directory.  
2. Run `analysis.py` to reproduce results and plots.  

## Requirements  

- Python 3.8+ with pandas, numpy, matplotlib, statsmodels, scipy. 
