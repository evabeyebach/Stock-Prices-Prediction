# Stock Prices & Risk Prediction (Dow Jones Index)
Built models to predict stock prices and evaluate risks of stocks (Dow Jones Index)

## Background
The research at hand addresses the challenge of financial forecasting by focusing on the prediction of weekly stock returns using historical data. The central aim is to build 
a predictive model that can accurately forecast the highest rate of return for the following week, emphasizing the metric percent_change_next_weeks_price. To establish the model's efficacy,
the available data is segmented into two quarters: the first quarter's data is utilized for model training, while the second quarter's data is employed to validate the model's 
predictive prowess.

## Introduction
We used quarter 1 (Jan-Mar) data for training and quarter 2 (Apr-Jun) data for testing.
We built models to predict stock prices and evaluate risks of stocks in the Daw Jones Index. We tried different models (LM, Decision Trees/SVR) to test for accuracy. We analyzed 
appropriateness of model and insights from findings as well as prediction accuracy. We also used CAPM to get the risk of stocks.

## Data

• quarter: the yearly quarter (1 = Jan-Mar; 2 = Apr=Jun).

• stock: the stock symbol.

• date: the last business day of the work (this is typically a Friday)

• open: the price of the stock at the beginning of the week

• high: the highest price of the stock during the week

• low: the lowest price of the stock during the week

• close: the price of the stock at the end of the week

• volume: the number of shares of stock that traded hands in the week

• percent_change_price: the percentage change in price throughout the week

• percent_chagne_volume_over_last_wek: the percentage change in the number of shares of

• stock that traded hands for this week compared to the previous week

• previous_weeks_volume: the number of shares of stock that traded hands in the previous week

• next_weeks_open: the opening price of the stock in the following week

• next_weeks_close: the closing price of the stock in the following week

• percent_change_next_weeks_price: the percentage change in price of the stock in the

• following week days_to_next_dividend: the number of days until the next dividend

• percent_return_next_dividend: the percentage of return on the next dividend

## Analysis
After clenaning and exploring the data "Dow Jones Index case," we employ a methodological approach that leans heavily on predictive analytics,
using a blend of **Linear Models**, **Linear Regression**, **Support Vector Regression (SVR)**, **Decision Trees**, and the **Capital Asset Pricing Model (CAPM)**.
Each of these methods brings a unique lens to the study of financial time-series data.
We predict on traing and evaluate on testing. We aim to choose the model that is best predictor of `percent_change_next_weeks_price` and we evaluate the stocks that have less risk.


## Conclusion
After cleaning and exploring the data, we performed three different models (linear regression, SVR, and Decision Trees) and the aim was to get the best model in predicting
`percent_change_next_weeks_price` based on the independent variables. The Linear Regression model exhibited the most precise predictions with an RMSE of 3.29, 
marginally outperforming the SVM and Decision Tree models, which recorded RMSEs of 3.38 and 3.47, respectively. The Linear Model also helped eliminate collinearity 
issues between independent variables and helped us determine the inputs for generating the final three models. Even though the RMSE for the linear model was the lowest,
we decided to choose the SVM model. The model itself does a better job of considering the categorical and continuous variables and the computing power of SVMs is much greater.
CAPM was also utilized in this case study to assess the given stocks' risk compared to the market and get the best return for each stock. After getting all beta and return results, 
we chose KO, MCD, and MRK to be the best stocks. They all had a beta lower than 1 (less risky than the market) and better returns than the other stocks.






