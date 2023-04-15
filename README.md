# SC1015 B126 Group 3 Mini-Project

Done by: Wang Yangming, Wang Anqi, Yang Ziyu

================================

**Our Motivation:**
- Cryptocurrency is a decentralized digital currency designed to work as a medium of exchange through a computer network that is not reliant on any central authority, such as a government or bank, to uphold or maintain it. While the working mechanism of cryptocurrency differs from traditional currencies, its stock prices are still determined by the combination of supply, demand, competition, regulations, etc.
- As prices of cryptocurrencies **fluctuate strongly with time**, it is interesting to know whether ML models can identify some hidden patterns in the prices time series and use them to **predict future prices with decent accuracy**.

## Project Goal:
- This project aims to evaluate and compare different ML models on their performence of predicting future Bitcoin prices by fitting them to the past Bitcoin prices time series.

## Dataset Used:
We used the Bitcoin time series dataset from [Yahoo Finance Crypto](https://finance.yahoo.com/quote/BTC-USD/history?p=BTC-USD) to obtain Bitcoin prices from 2014 to 2023, cleaned and processed it for Exploratory Data Analysis and Machine Learning.
- [Dataset Folder](./data/Bitcoin/)

**Note:** Some datasets of other cryptocurrencies are scraped but are not included in the final project 

## Jupyter Notebooks:
- [Data Collection](./src/1.EDA.ipynb)
- [Data Cleaning and Preprocessing](./src/1.EDA.ipynb)
- [Exploratory Data Analysis & Visualization](./src/1.EDA.ipynb)
- [ARIMA Model - Machine Learning](./src/2.ARIMA.ipynb)
- [LSTM and GRU Models - Machine Learning](./src/3.LSTM%26GRU.ipynb)

**Note:** Some Jupyter Notebooks are used but are not included in the final project (e.g. XGBoost Model)

## Slide Deck:
- [Presentation Slides](./presentation/Slides.pdf)

<br>

---

# Overview of DataScience Pipeline
### [1. Data Collection](./src/1.EDA.ipynb)
Used Bitcoin price time series data from [Yahoo Finance Cryptocurrency](https://finance.yahoo.com/crypto/) from 2014 to 2023 (a total of 3108 days)

### [2. Data Cleaning and Preprocessing](./src/1.EDA.ipynb)
- Removing useless features, handling missing values
- Export data as csv
- Generating time-series data

### [3. EDA & Visualization](./src/1.EDA.ipynb)
Explored, visualized, and generated insights for the following:
- 'close' price time series over the last 8 years, the last 1 year and the last 1 month 
- 'close' price 50-day and 200-day moving average

### 4. Machine Learning
##### 4.1 [SARIMAX](./src/2.ARIMA.ipynb)
`Metrics:`
- Augmented Dickey-Fullet Test Score
- Akaike Information Criterion
- Root Mean Squared Error (RMSE)
##### 4.2 [LSTM and GRU](./src/3.LSTM%26GRU.ipynb)
`Metrics:`
- Root Mean Squared Error (RMSE)

### 5. Data-driven Insights
Conclusions:
- **LSTM** and **GRU** have better performance on the Bitcoin time series forecasting than *ARIMA*
- **LSTM** and **GRU** are less dependent on the stability of the time series
- **ARIMA** is only restricted to cases where the time series follow some seasonality or stable temporal patterns
- There still a considerable amount of **error** in the prediction solely with ML models

Market traders should:
- Be **vigilant** when using ML models in predicting stock prices
- Conduct also the **fundamental analysis** considering the updates from regulatory departments, mass media and authoritative market agencies
- Reasonably predict the fast-changing stock prices of cryptocurrencies

<br>

---

# What we learnt from this project:
**Data Collection:**
- Collecting data from Yahoo Finance Website or from third-apart agent API calls

**Data cleaning and preprocessing:**
- Removing useless features, handling missing values
- Generating time-series data

**EDA & Visualization:**
- Visualization plots with fluctuating values
- 'close' price time series EDA

**Machine Learning:**
- Machine Learning Models:
    - SARIMAX, LSTM, GRU
- Performance Metrics:
    - Root Mean Squared Error (RMSE)

<br>

---

# Contributions
**Data Collection:** `Wang Anqi` and `Yang Ziyu` <br>
**Data Cleaning and Preprocesing:** `Wang Anqi` and `Yang  Ziyu` <br>
**EDA and Visualization:** `Wang Anqi` and `Yang Ziyu` <br>
**ARIMA:** `Wang Anqi` and `Yang Ziyu` <br>
**LSTM and GRU:** `Wang Yangming` <br>
**Presentation Script:** `Wang Yangming` <br>
**Presentation Voice Over + Editing:** `Wang Yangming` <br>
**Slides Deck:** `Wang Yangming`, `Wang Anqi`, and `Yang Ziyu` <br>
**GitHub ReadMe:** `Wang Yangming`

Did but not included in the final product: <br>
**XGBoost:** `Wang Yangming` <br>

# References
- Wikipedia contributors. (2023). Cryptocurrency. Wikipedia. https://en.wikipedia.org/wiki/Cryptocurrency
- Wikipedia contributors. (2023a). Bitcoin. Wikipedia. https://en.wikipedia.org/wiki/Bitcoin
- pandas - Python Data Analysis Library. (n.d.). https://pandas.pydata.org/
- Nguyen, B. (2021, December 29). End-to-End Time Series Analysis and Forecasting: a Trio of SARIMAX, LSTM and Prophet (Part 1). Medium. https://towardsdatascience.com/end-to-end-time-series-analysis-and-forecasting-a-trio-of-sarimax-lstm-and-prophet-part-1-306367e57db8
- statsmodels.tsa.arima.model.ARIMA — statsmodels. (n.d.). https://www.statsmodels.org/dev/generated/statsmodels.tsa.arima.model.ARIMA.html
- Wikipedia contributors. (2023a). Power transform. Wikipedia. https://en.wikipedia.org/wiki/Power_transform#Example
- Wikipedia contributors. (2022). Augmented Dickey–Fuller test. Wikipedia. https://en.wikipedia.org/wiki/Augmented_Dickey%E2%80%93Fuller_test
- LSTM — PyTorch 2.0 documentation. (n.d.). https://pytorch.org/docs/stable/generated/torch.nn.LSTM.html
- GRU — PyTorch 2.0 documentation. (n.d.). https://pytorch.org/docs/stable/generated/torch.nn.GRU.html
- Phi, M. (2020, June 28). Illustrated Guide to LSTM’s and GRU’s: A step by step explanation. Medium. https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21
- sklearn.preprocessing.MinMaxScaler. (n.d.). Scikit-learn. https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html