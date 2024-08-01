# Forecasting Las Vegas Visitor Volume

## Project Summary
Using publicly available time series data, I accurately modeled and forecasted monthly Las Vegas visitor volume. This project was completed as a final project for my Time Series course at UCSB in 05/24. 

## My Contribution 
This was an individual project in which I completed all of the data analysis and model generation.

## Methods Used
- Exploratory analysis
- Data transformation via differencing 
- Auto-correlation Function (ACF) and Partial Auto-correlation Function (PACF)
- Time Series Modeling: Seasonal Moving Average (SMA), Seasonal Auto-regressive integrated moving average (SARIMA)
- Akaike Information Criterion (AIC)

## Tools
- RStudio
- R Markdown

## Summary of Analysis
1. Exploratory analysis:  Visualized data to spot trends and non-stationary behavior 
- Plotted raw data to visualize trends and stationality
- Partitioned data for the purposes of training and model validation 
- Plotted Autocorrelation Function (ACF) and histogram to confirm non-stationality
2. Data processing:  Transformed non-stationary data into stationary
- Used Box-Cox to determine whether variance needed to be stabilized.
- Plotted Autocorrelation Function (ACF) to determine lag for differencing
- Differenced data by lag 12 and lag 1 and plotted ACF and histogram to confirm stationality.
3. Model Estimation & Selection: Estimated coefficients for model selection and checked model fit
- Tested MA and SARIMA models with different parameters and selected 3 models with the lowest Akaike information criterion (AIC) which indicates how well a model fits the data.  
- Plotted roots to determine whether the models were invertible and stationary. Eliminated one model since it was not invertible.
4. Model Diagnostic:  Ensured model is stationary and normal
- Plotted histogram, residuals, and Q-Q plot to determine whether two remaining models were stationary.
- Ran various test to determine normality of two remaining models: Shapiro-Wilkins, Box-Pierce, Ljung-Box, McLeod Li 
- Selected the final time series model based on results of above normality tests.
5. Forecast & Verification
- Forecasted using chosen model.
- Verified accuracy of forecast using test set.

## Data Set

The data set is publicly available at the [Las Vegas Convention and Visitors Authority](https://www.lvcva.com/research/?tab=tourism-tracker#tab-container).
