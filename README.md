# Titanic Dataset: Feature Engineering & Logistic Regression

This project analyzes the historical Titanic passenger dataset using a Logistic Regression model. The main goal was to optimize model performance by applying advanced data cleaning and categorical encoding techniques.

## Project Structure
* `feature_engineering.ipynb` - The primary Jupyter Notebook containing the data pipeline, imputation logic, and modeling steps.

## Workflow Overview

1. **Data Inspection:** Explored the structural footprint and baseline shape of the raw Titanic dataset using pandas.
2. **Custom Missing Value Imputation:**
   * **Embarked & Fare:** Researched historical records on Encyclopedia Titanica to manually fix missing embarkation and fare values for specific passengers by name.
   * **Age:** Built a conditional subpopulation lookup loop that dynamically filled missing age values based on a passenger's specific title (e.g Master, Miss, Mr, Mrs) instead of a flat dataset average.
3. **Model Comparison:** Evaluated model classification accuracy across two different categorical data approaches using a standard 80/20 train-test split.

## Key Performance Results

* **Label Encoded Baseline Accuracy:** **84.73%** 
* **One-Hot Encoded Optimization Accuracy:** **85.11%**

By transitioning from simple ordinal label encoding to One-Hot Encoding for multi-category nominal values, we removed artificial numerical hierarchies and pushed the model to its peak performance score of 85.11%.
