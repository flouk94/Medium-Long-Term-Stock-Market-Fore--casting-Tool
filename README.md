# Medium-Long-Term-Stock-Market-Fore--casting-Tool
Objectives

The aim of this project is to develop an algorithm capable of predicting stock prices, currencies, and commodities over the medium and long term. The approach is based on extracting and selecting relevant data, followed by prediction models to identify the one providing the best results.

Methodology

Data Extraction

The first step involves extracting historical data on stocks, currencies, and commodities from reliable sources such as Yahoo Finance. This data typically includes opening and closing prices, traded volumes, as well as technical indicators such as moving averages.

Data Preprocessing

Once the data is extracted, it is cleaned to remove missing values and anomalies. This process also includes normalizing the data, adding new 
variables derived from technical indicators, and creating lagged variables (for example, prices shifted by several days).

Feature Selection

Selecting the most relevant features is a crucial step to improve the quality of predictions. Machine learning techniques, such as XGBoost and Random Forest, are used to evaluate the importance of each variable. These models help rank the most influential factors in price fluctuations, identifying those that contribute the most to the prediction. Insignificant variables are removed, reducing model complexity without sacrificing accuracy.

Modeling

Once the variables are selected, several prediction models are applied:
• Traditional statistical models: Linear and multivariate regressions are tested to capture linear relationships in the data. While simple, these models provide a baseline to assess the performance of more complex models.
• ForecasterAutoregMultiSeries: This multivariate autoregressive model is used to leverage temporal relationships between multiple series. It allows predicting prices by considering the interactions between different variables such as stocks, currencies, and commodities.
• ARIMA and SARIMAX models: For univariate time series, ARIMA (AutoRegressive Integrated Moving Average) and SARIMAX (Seasonal ARIMA with Exogenous Variables) models are used. These models incorporate the seasonal components of the data as well as exogenous factors (such as macroeconomic indicators or external factors influencing prices).
2
• Machine learning models: In addition to statistical models, more sophisticated approaches such as random forests (Random Forest) and gradient-based methods (XGBoost) are applied. These models are particularly effective in capturing non-linearities in the data.

Model Evaluation

Each model is evaluated based on several performance criteria, such as the coefficient of determi- nation (R2), root mean square error (RMSE), and mean absolute percentage error (MAPE). These metrics help identify the models that perform best in terms of prediction accuracy.
The goal is to choose the model that offers the best overall performance, balancing complexity, generalization capability, and forecast quality.
Medium and Long-Term Forecasting
Once the model is selected, it is applied to make medium- and long-term forecasts (7 days / 30 days / 3 months / 6 months / 1 year). The generated forecasts are compared to historical data to evaluate their accuracy, and adjustments are made as needed to improve results.

Conclusion

This project aims to provide a robust solution for predicting stock prices, currencies, and commodi- ties. By combining feature selection techniques with machine learning and time series models, the algorithm offers a versatile and effective approach to anticipating market fluctuations over time. The modular approach allows integrating new variables or adjusting models according to the specific needs of the markets or assets considered, offering a flexible tool for decision-making.
