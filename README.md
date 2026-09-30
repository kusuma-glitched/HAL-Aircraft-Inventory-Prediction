# HAL Aircraft Inventory Prediction System

A machine learning-based inventory analysis and forecasting prototype developed as a student project during an internship at Hindustan Aeronautics Limited (HAL).

## Project Overview

This project develops a prototype system for analysing aircraft inventory and forecasting future product consumption.

The system aims to:

- Forecast monthly product consumption for 2026
- Predict potential stockout risk
- Calculate reorder points
- Estimate recommended order quantities
- Identify expiry and excess-stock risks
- Generate recommended inventory actions

## Important Note

The datasets used in this project are synthetic/demo datasets created for academic and demonstration purposes.

They do not contain proprietary or confidential HAL data.

## Dataset

The project uses three datasets:

### consumption.csv

Contains historical product consumption data from January 2023 to December 2025.

Used for demand forecasting and feature engineering.

### inventory_stock.csv

Contains historical inventory information including:

- Opening stock
- Quantity received
- Quantity consumed
- Closing stock
- Reorder level
- Lead time

Used for inventory and stockout analysis.

### products.csv

Contains product master information including:

- Product name
- Category
- Manufacturing date
- Shelf life
- Expiry date
- Unit cost
- Criticality
- Supplier

## Machine Learning

### Consumption Forecasting

The primary forecasting model is:

**Random Forest Regressor**

The project also compares the forecasting approach with:

- Linear Regression
- Naive previous-year baseline
- Holt-Winters

### Stockout Prediction

A **Random Forest Classifier** is used to estimate the probability of a product experiencing a stockout in the following month.

The classification threshold was set to 0.40 to increase sensitivity to potential stockouts.

## Inventory Analysis

The system calculates:

- Safety stock
- Reorder point
- Reorder requirement
- Recommended order quantity
- Months of stock
- Inventory value
- Stockout probability
- Expiry risk
- Excess-stock risk

The system then assigns a final inventory risk category and recommended action.

## Project Workflow

```text
Historical Data
       ↓
Data Cleaning
       ↓
Feature Engineering
       ↓
Consumption Forecasting
       ↓
Stockout Prediction
       ↓
Inventory Analysis
       ↓
Risk Classification
       ↓
Recommended Action
       ↓
Final Inventory Risk Report