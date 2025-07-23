Raw files still to be adjusted, following my own learning journey, perfrormed using books (time series and ML), internet forums, scientific papers, ChatGPT (to implement after studying).

Below you can find an overview of the path:
0. Extract financial data (data provider is YahooFinance; for better quality data, a lot of API exist, e.g. AlphaVantage, Vanguard,.. with limited number of call per day)
1. Time Series:
    AR model -> after computing ACF/PACF
    MA model  -> after computing ACF/PACF
    ARMA model -> one single feature, one stock AAPL, feature is log performance
    VARMA model (multivariate ARMA) -> on two stocks, AAPL and MSFT, features are log performances of both assets
                                      (this is extendible at N features or stocks easily, N>=2)
    ARCH model -> one single stock
    GARCH model -> one single stock
2. ML:
    Hidden Markov Model (HMM) -> using candlesticks data (OHCL) + VIX index; features and lag adjusted with OPTUNA
    LSTM -> using one stock + features + computed indices/signal (MACD, signal line,..) ; tuned with OPTUNA
                           
                           
                           
