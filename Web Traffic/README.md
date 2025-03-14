<img align='right' src="https://visitor-badge.laobi.icu/badge?page_id=rrxzyy.ARIMA-Web-Traffic"/>

# What is ARIMA

ARIMA (Auto-Regressive Integrated Moving Average) is a general class of statistical models for time series analysis forecasting
ARIMA uses a time series' past values and/or forecast errors to predict its future values
ARIMA model assumption - stationary: the time series has its statistical properties remain constant across time

Three components/parameters: AR + I + MA (p, d, q)

- AR (Auto-Regressive): the time series is linearly regressed on its own past values
  p : the number of past values included in the AR model

- I (Integrated): if not stationary, the time series can be differenced to become stationary, i.e., compute the differences between consecutive observations
  d : the number of times the time series is differenced

- MA (Moving Average): the time series is 'regressed' on the past forecast errors
  q : the number of past forecast errors included in the MA model

AR: ARIMA (p, 0, 0) = AR(p)
MA: ARIMA (0, 0, q) = MA(q)
ARMA: ARIMA (p, 0, q)

# ACF plot and PACF plot

- ACF (autocorrelation function) is the correlation of the time series with its lags, e.g., y, and yt-k for k = 1, 2, ...

Question: assume y and y1-1 are correlated, yt-1 and yt-2 are correlated.
How can we measure if there is new information in yt-2 to predict yt, besides their
relationships with yt-1?

- PACF (partial autocorrelation function) is the partial correlation of the time series with its lags, after removing the effects of lower-order-lags between them
  e.g, the partial autocorrelation of y, and y kis the correlation that is not explained by their relationships with the lags yt-1, Yt-2, ... , Yt-k+1

# ADF (Augmented Dickey-Fuller)

ADF used to test the null hypothesis that the time series is non-stationary. If p-value > 0.05, the data needs differencing, because is non-stationary.
