# Stock Price Prediction and Backtesting API

This Django application fetches historical stock price data, performs backtesting using moving averages, predicts future stock prices, and generates PDF reports. The application integrates with the Alpha Vantage API for financial data and uses PostgreSQL as the database.

## Features

- Fetch historical stock prices for a given symbol.
- Perform backtesting based on 50-day and 200-day moving averages.
- Predict future stock prices using a pre-trained linear regression model.
- Generate PDF reports comparing actual vs predicted prices.

## Prerequisites

Ensure you have the following installed:

- Python 3.x
- PostgreSQL
- Docker and Docker Compose (optional for local development)
- Alpha Vantage API key (for fetching stock data)

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/yourusername/stock-prediction-api.git
cd stock-prediction-api
```


## Installation

To install the required Python packages, run:

```bash
pip install -r requirements.txt
```

## Configure the Environment Variables
#### Create a .env file in the root directory with the following content:
```
# ===================== Database configurations =====================
POSTGRES_DB='postgres'
POSTGRES_USER='postgres'
POSTGRES_PASSWORD='postgres'
DB_HOST='db'
DB_PORT=5432

SECRET_KEY='"django-insecure-e1!&6zk&+m^=)7ai_=i61j&qv5lb4jbr$0+3bw1+sk7+b-w_7q"'

ALPHA_VANTAGE_API_KEY="ODIKOA2YE96209XN"
```

## Database Setup
#### If you're using Docker for local development, run the following command to set up PostgreSQL:
```
docker-compose up -d
```