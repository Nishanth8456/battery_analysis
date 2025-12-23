# Battery statistical anlysis

Statistical analysis of my laptop battery health over time using
Windows battery report data.

# OLS regression analysis.
 - Because the data are time-ordered, residuals exhibit strong positive 
autocorrelation (Durbin–Watson ≈ 0.13). This behavior is expected in 
cumulative degradation processes. Therefore, standard errors from
OLS may be underestimated.
 - The slope is interpreted primarily as an average degradation rate
rather than a strict inferential result.
 - Using the OLS estimated slope, we estimate that battery health **degrades**
over time at a rate of: 
   - a) ~0.022% per day.
   - b) ~0.155% per week.
   - c) ~0.66% per month.
   - d) ~8.1% per year.

- Using the GLS estimated slope, we estimate that battery health **degrades**
over time at a rate of:
   - a) ~0.0193% per day.
   - b) ~0.135% per week.
   - c) ~0.58% per month.
   - d) ~7.0% per year.

## Comparison of OLS and GLS degradation rates.
Under OLS, battery health was estimated to decline at approximately 
0.022% per day (≈8.1% per year). After accounting for strong positive
autocorrelation using a GLS model with AR(1) errors, the estimated 
degradation rate decreased slightly to approximately 0.019% per day 
(≈7.0% per year). While GLS yields a more conservative estimate with
larger standard errors, the magnitude and direction of the degradation
trend remain consistent across models, indicating that the observed battery
health decline is robust to autocorrelation effects.
