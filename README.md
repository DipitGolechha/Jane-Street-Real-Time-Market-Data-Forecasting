# Jane Street Real-Time Market Data Forecasting

### Kaggle Competition Project  
By **Dipit Golechha** and **Devesh Shah**

---

## Overview
This repository contains the code, models, and experiments developed for the **Kaggle competition “Jane Street Real-Time Market Data Forecasting”**.  
The objective of this challenge was to **predict responders (returns on trades)** from **anonymized real-time financial market data** provided by Jane Street.  
The project explores multiple machine learning techniques — from traditional regression models to advanced deep learning architectures — to design a high-performance trading signal prediction system.

---

## Competition Context
The competition involves **modeling complex, real-world financial market data** with the goal of determining whether a trade should be executed or passed based on expected outcomes.  
Due to **non-stationary time series**, **high dimensionality**, and **anonymized features**, the task requires robust, adaptive models that generalize to unseen market conditions.

Dataset link:  
[Jane Street Real-Time Market Data Forecasting (Kaggle)](https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting)

---

## Team Members
- **Dipit Golechha**  
- **Devesh Shah**

---

## Project Highlights
This repository includes:
- Multiple predictive modeling approaches  
- Feature engineering experiments  
- Model ensemble and online learning strategies  
- Real-time model evaluation workflows  

---

## Models Implemented
The following models were explored and benchmarked:

1. **Linear Regression**
2. **Linear Regression with Online Learning**
3. **Linear Regression with Lagged Features**
4. **XGBoost**
5. **LightGBM**
6. **CatBoost**
7. **Long Short-Term Memory (LSTM)**
8. **XGBoost Regressor (Ensemble Version)**
9. **AutoEncoder**
10. **Ensemble version of these models**

Each model was designed to capture different aspects of time-dependence, feature correlation, and temporal drift in the dataset.

---

## Key Insights

### Effective Strategies
- **Lagged Feature Engineering:** Helped improve responsiveness to temporal patterns.  
- **Online Learning:** Enabled the model to adapt to changing market dynamics.  
- **Model Ensembling:** Improved predictive stability and reduced variance.  

### Performance Takeaways
- Tree-based models (LightGBM and XGBoost) achieved superior performance on structured tabular features.  
- Recurrent architectures (LSTM) better captured temporal dependencies, though sensitive to noise.
- While linear regression with selected features, online learning and lagged features achieved the best results, suggesting us that sometimes understanding the data is more important than understanding complex models.

---

## Dataset Description
The competition dataset comprises a set of timeseries with 79 features and 9 responders, anonymized but representing real market data. The goal of the competition is to forecast one of these responders, i.e., responder_6, for up to six months in the future.

For more information: https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting/data
---

## Modeling Workflow
1. **Data Preprocessing**  
   - Handling missing values  
   - Feature normalization  
   - Weight and resp scaling  

2. **Feature Engineering**  
   - Lagged features and rolling window statistics  
   - Online update of weights  
   - Construction of meta-features for time-based trends  

3. **Model Training & Validation**  
   - K-fold cross-validation with temporal splits  
   - Early stopping based on validation metrics  
   - Hyperparameter tuning for gradient boosting methods  

4. **Evaluation Metrics**  
   - **Utility Score (competition metric)**  
     - Balances profitability and risk  
   - **Mean Squared Error (MSE)**
   - **Root Mean Squared Error (RMSE)**
   - **Cross validation score**
  

---
