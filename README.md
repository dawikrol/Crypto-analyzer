# Crypto-analyser-dashboard

My training project. I want to learn how use external API and how create full interactive dashboards in jupyter notebook.
Maybe, in the future I will develop this project into desktop application to full Technical Analysis.

## Table of contents
* [Technologies](#Technologies)
* [API](#API)
* [Database](#Database)
* [Dashboard](#Dashboard)


## Technologies

JupyterNotebook (Python 3.9)

  Main libraries: Plotly, ipywidgets, Pandas, SQLAlchemy
  
Database: MySQL


## API

The historical and real time data regarding crypto currencies come from www.binance.com

The API key is required. It is free, and here you find manual how to get it: https://www.binance.com/en/support/faq/360002502072

When you get your own key modify this line: 
```
binance_api_key = os.environ.get('binance_api_key')
binance_api_secret = os.environ.get('binance_api_secret')
```


## Database

This project use MySQL database to store data. 
You have to config your database connection by modify:
```
MYSQL_HOSTNAME = 'localhost'
MYSQL_USER = os.environ.get('DB_USER')
MYSQL_PASSWORD = os.environ.get('DB_PASS')
MYSQL_DATABASE = 'cranalyserDB'
```
If you use on line notebook be sure to configure your fierwall. 


## Dashboard

A fully interactive dashboard with widgets and interactive charts allows you to analyse one of the most popular crypto currency.
Adding additional currency is really simple. You need add cryptocurrency to dictionary according to the pattern:
```
cryptocurrencies = {
    'Bitcoin': 'btcusdt',
    'BinanceCoin': 'bnbusdt',
    'Ethereum': 'ethusdt',
    'Litecoin': 'ltcusdt',
    'XRP': 'xrpusdt'
    }
```
User need to select currency, period of time and date interval. After click the button they get: dataframe with selected data, time series plot and candlestick plot. 

![image](https://user-images.githubusercontent.com/63808220/114439352-2bc51480-9bc9-11eb-89f6-8ff032186226.png)





