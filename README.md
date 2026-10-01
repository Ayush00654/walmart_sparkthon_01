# walmart_sparkathon_009

# Smart Inventory Forecasting & Sustainability System

A machine-learning-powered retail inventory management system designed to forecast product demand, recommend inventory orders, and track the estimated environmental impact of inventory decisions.

## Overview

This project combines demand forecasting with inventory planning and sustainability tracking. Users can enter a **store ID, product ID, and forecast date** to generate an expected demand forecast and recommended order quantity.

The system uses historical sales data, product selling prices, calendar events, and time-based features to predict future product demand using a trained **LightGBM regression model**.

In addition to demand forecasting, the application estimates the CO₂ impact associated with the recommended order quantity and maintains a sustainability leaderboard for comparing stores based on their estimated monthly carbon footprint.

## Key Features

* **Demand Forecasting** – Predicts expected product demand for a specific store and date.
* **Machine Learning Model** – Uses a trained LightGBM model for demand prediction.
* **Feature Engineering** – Incorporates:

  * 7-day lag sales
  * 7-day rolling average sales
  * Selling price
  * Calendar events
  * Day, month and year
  * Week of the year
* **Inventory Recommendation** – Converts predicted demand into a recommended order quantity.
* **Sustainability Tracking** – Estimates CO₂ emissions associated with inventory orders.
* **Store Sustainability Leaderboard** – Tracks monthly CO₂ estimates and compares them with the previous month.
* **Web Interface** – Provides an interactive Flask-based interface for generating forecasts and viewing sustainability metrics.

## Technology Stack

* **Python**
* **Pandas**
* **NumPy**
* **LightGBM**
* **Scikit-learn Label Encoding**
* **Flask**
* **SQLAlchemy**
* **SQLite**
* **HTML / CSS / JavaScript**

## System Workflow

```text
Historical Sales Data
        +
Calendar & Event Data
        +
Selling Price Data
        ↓
Feature Engineering
        ↓
LightGBM Demand Forecasting Model
        ↓
Expected Product Demand
        ↓
Recommended Order Quantity
        ↓
CO₂ Impact Estimation
        ↓
Sustainability Tracking & Store Leaderboard
```

## Application Output

For each forecast request, the application provides:

* Store ID
* Product ID
* Forecast date
* Expected demand
* Recommended order quantity
* Unit price
* Estimated CO₂ emissions

The application also provides a sustainability leaderboard showing monthly estimated CO₂ emissions and the percentage change compared with the previous month.

## Project Structure

```text
├── data/
│   ├── calendar.csv
│   └── sell_prices.csv
│
├── models/
│   ├── inventory_forecast_model.pkl
│   └── label_encoders.pkl
│
├── static/
│   ├── style.css
│   └── walmart.png
│
├── templates/
│   └── index.html
│
├── utils/
│   └── forecast.py
│
├── app.py
├── sustainability.csv
└── README.md
```

## Objective

The objective of the project is to demonstrate how machine learning can support **retail demand forecasting and inventory planning** while incorporating sustainability metrics into operational decision-making.

By forecasting demand before placing inventory orders, the system aims to support more informed purchasing decisions and provide visibility into the estimated environmental impact of those decisions.
