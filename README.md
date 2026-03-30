# OnlineRetailARIMAFitting
## Project Overview
The project focuses on developing a statistical forecasting baseline for weekly revenue using ARIMA. The aim is to assess the predictability of the series and establish a benchmark for comparison with future machine learning approaches.
## Dataset
- Name: Online Retail Dataset
- Source: UCI Machine Learning Repository
- Time Period: December 2010 until December 2011
- Link: https://archive.ics.uci.edu/dataset/352/online+retail
### Description:
- InvoiceNo which is a 6 digit number assigned to each transaction if it starts with a c it represents a cancellation
- StockCode a 5 digit number unique to each distinct product
- Description which is the product name
- Quantity represents the quantity sold per invoice
- InvoiceDate is the day and time when each transaction has been generated
- UnitPrice is the price of the product per unit
- CustomerID is a 5 number unique identifier assigned to each customer
- Country is the name of the country the customer resides
## Objective
- Forecast weekly revenue
- Assess predictability of the series
- Establish a baseline forecasting model
## Methodology
- Weekly aggregation of data
- Log transformation
- First-order differencing
- ACF/PACF analysis
- ARIMA model selection (AIC/BIC)
- Static forecasting
- Walk-forward forecasting
- Naive baseline comparison
## Models Used
- ARIMA(0,1,1)
- Naive baseline
## Evaluation
Models were evaluated using Mean Absolute Error (MAE). The walk forward ARIMA has achieved the lowest MAE (0.170), followed by the naive baseline (0.216), while the static ARIMA forecasting performed worst (0.402).
## Key Findings
- ARIMA outperforms the naive baseline
- The improvement is modest
- The series exhibits short-term dependence
- The data behaves similarly to a random walk process
## Conclusion
The ARIMA(0,1,1) provides a reasonable statistical baseline by capturing the short-term dependency. However, forecasting remains challenging due to the limited dataset and weak underlying structure.
## Limitations
- Small dataset (52 observations)
- No seasonality modeling
- No external variables
## Next Steps
- Explore a machine learning models to improve forecasting performance
- Incorporate additional features
## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
