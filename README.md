# Real-Time Financial Market Anomaly Detection System

An end-to-end ML pipeline that detects anomalies in financial 
market data using a dual-model ensemble approach.

## Models Used
- Isolation Forest — detects single-day statistical outliers
- LSTM Autoencoder — detects pattern breaks over 30-day windows
- Ensemble scoring — combines both models (40% ISO + 60% LSTM)

## Tech Stack
Python, TensorFlow, scikit-learn, MySQL, SQLAlchemy, pandas, numpy

## Key Results (AAPL — 5 years of data)
- Correctly flagged September 2024 iPhone launch / options expiry
- Detected April 2025 market crash (-9% single day)
- Severity classification: LOW / MEDIUM / HIGH alerts

## Project Structure
- market_anomaly_detection.ipynb — full project notebook
- AAPL_final_dashboard.png       — anomaly detection dashboard
- AAPL_anomaly_results.csv       — full results export

## Setup
1. Clone the repo
2. Create a .env file with your MySQL credentials:
   DB_USER=root
   DB_PASSWORD=your_password
   DB_HOST=localhost
   DB_PORT=3306
   DB_NAME=market_anomaly_db
3. Install dependencies: pip install -r requirements.txt
4. Run the notebook top to bottom
