# Data-Driven Stock Price Prediction and Portfolio Optimization
## Project Overview
### In this project, being part of the MSc Data Science program at the University of Hertfordshire, I have worked with advanced machine learning models to predict stock price movement and optimize a collection constituting our portfolio. It is mainly proposed a performance comparison of three models: Long Short Term Memory (LSTM), Gated Recurrent Unit (GRU), and eXtreme Gradient Boosting (XGBoost) as predictors of the price behavior on the stock exchange while also building portfolios aiming at profit maximization with controlled risk.
## Motivation
### Predicting the stock market has always been difficult as financial markets are dynamic and highly non-linear. Many traditional methods, like technical and fundamental analysis, can fail to capture these kinds of complexities, often resulting in decision-making. This project aimed to use machine learning methods to improve the accuracy of stock price predictions and ultimately help yield results from these drastic investment strategies.
## Dataset
## This project used a historical financial data dataset on companies listed in the New York Stock Exchange (NYSE) and S&P 500. It contains four primary files:
### prices.csv: Raw daily stock prices, including open, high, low, close, and volume.
### prices-split-adjusted.csv: Daily stock prices adjusted for stock splits.
### securities.csv: Descriptive information for each company, including sector classifications.
### fundamentals.csv: Financial metrics derived from SEC 10-K filings, such as earnings, margins, and financial ratios.
## Preprocessing Steps
### Data Cleaning: Merged datasets, handled missing values, resampled data to monthly frequency, and applied forward and backward fill for missing values.
### Feature Engineering: Generated technical indicators such as Moving Averages, Relative Strength Index (RSI), Bollinger Bands, and others to capture market trends and volatility.
### Normalization: Applied Min-Max Scaling to bring all feature values into a consistent range, facilitating model training.
## Models Developed
## 1. Long Short-Term Memory (LSTM)
### Architecture: Two LSTM layers with 100 units each, followed by a dense output layer. Dropout layers were added to prevent overfitting.
### Performance: Best performance achieved with a rolling window size of 5, yielding a test MAE of 5.42 and an R² value of 0.92.
## 2. Gated Recurrent Unit (GRU)
### Architecture: Similar to LSTM but with GRU layers, optimized for longer sequences.
### Performance: Best performance achieved with a rolling window size of 70, yielding a test MAE of 5.56 and an R² value of 0.93.
## 3. eXtreme Gradient Boosting (XGBoost)
### Architecture: Optimized XGBoost regressor from GridSearchCV for n_estimators, learning_rate and max_depth.
### Performance: On the performance metrics of R² and RMSE, this study found an optimal value of 0.997 for R², which means it is very good and has much less Root Mean Squared Error than other models implemented.
## Results and Discussion
### The XGBoost model achieved close to perfect R2 values and the lowest error metrics amongst all the models we tested_ compared with LSTM and GRU. The LSTM model performs better on shorter-term predictions, while the GRU has an edge on longer time scales. The results show that the model and size of the chosen window have a major effect on predictive performance, with XGBoost flagged as generally the most accurate for this dataset.
## Model Performance Comparison
## Model	MAE	RMSE	R²
### LSTM	5.42	10.48	0.92
### GRU	5.56	10.14	0.93
### XGBoost	1.72	4.15	0.997
## Portfolio Construction
### According to the model predictions, stocks were partitioned into 'UP,' 'DOWN,' and 'NEUTRAL' portfolios according to their forecast returns. All investment funds were allocated to their predicted return in those portfolios, favoring stocks with the highest expected returns. Further discussed implementing these models in simulated real-world investment strategies by showing performance assessments for these portfolios.
## Acknowledgements
### This project was implemented as part of MSc Data Science at the University of Hertfordshire under the supervision of Stephen Kane. I want to express my gratitude to the creators of the datasets and previous works and initiatives made by open-source community members who allowed this project.
