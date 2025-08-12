# Seattle Weather Time Series Analysis

## Project Overview
This project explores time series data of Seattle’s climate variables — precipitation, temperature, and wind — alongside the recorded weather type for each day. The main objectives are to analyze feature interactions that define weather patterns, predict future climate variables, and classify upcoming weather conditions using historical data.

Understanding and predicting weather patterns is vital for various sectors including agriculture, transportation, and urban planning. This project leverages both classical time series models and machine learning techniques to provide insights and predictive capabilities for Seattle's weather.

## Dataset Source and Credits
The dataset used in this project was obtained from Kaggle:  
[Seattle Weather Prediction Dataset](https://www.kaggle.com/datasets/petalme/seattle-weather-prediction-dataset)  
Credit to the original dataset authors for making this data publicly available.

## Key Tasks

1. Analyze interactions among climate features to identify those that best separate weather clusters.  
2. Predict future climate variables (precipitation, temperature, wind) using historical time series data.  
3. Classify future weather types based on climate variables and date information.

## Dataset Description

The dataset includes:

- **Precipitation:** Water falling to earth (inches) — rain, snow, drizzle, etc.  
- **Temperature:** Air temperature measured in Fahrenheit.  
- **Wind:** Wind speed in miles per hour.  
- **Weather:** Weather conditions categorized as drizzle, rain, sun, snow, and fog.

## Tools and Models Used

- **Time Series Models:**  
  - Autoregressive Models (AutoReg)  
  - Autoregressive Moving Average Models (ARIMA)  
- **Machine Learning Models:**  
  - Gradient Boosting Regressors (XGBRegressor) for climate variable prediction  
  - Gradient Boosting Classifiers (XGBClassifier) for weather classification  
- **Validation Techniques:**  
  - Walk-Forward Validation to simulate real-world forecasting scenarios and iteratively update models  
- **Visualization:**  
  - Boxplots, pairplots, and other exploratory data analysis techniques to study feature interactions and distributions

## Observations and Insights

### Feature Interaction and Clustering

- Precipitation is the strongest feature distinguishing weather types, with rain and snow showing the highest precipitation values.  
- Temperature helps differentiate sunny and snowy days, with sun showing higher temperature values and snow showing the lowest.  
- Wind speeds tend to be higher during rain and snow but can vary independently of weather.

### Predicting Climate Variables

- Walk-forward validation improved prediction accuracy by continuously updating models with observed data.  
- Autoregressive models with walk-forward validation performed better than gradient boosting regressors for time series forecasting in this context.  
- Achieved mean absolute errors (MAE):  
  - Precipitation: ~4.04  
  - Temperature: ~2.24  
  - Wind: ~0.91  
  - ARIMA with walk-forward validation: ~1.4  

### Weather Classification

- Using the XGBClassifier, the model classified weather types based on climate variables and date features.  
- The final classifier achieved approximately 84% accuracy in predicting weather categories.

## Final Remarks

- Temperature and precipitation are key drivers of weather classification.  
- Effective feature engineering combined with models like XGBRegressor, AutoReg, and ARIMA enables accurate prediction of climate variables.  
- Walk-forward validation is essential for realistic forecasting with time series data.  
- Assumptions made about feature units may affect outlier detection and model performance. Addressing outliers, especially in precipitation, may improve accuracy further.

## Additional Notes

For more detailed insights, exploratory analysis, and additional observations, feel free to explore the Jupyter notebook included in this repository.

## Questions and Suggestions

Feedback and suggestions are welcome. Please reach out if you notice any errors or have ideas for enhancing this analysis. Thanks to the Kaggle community for providing valuable resources and inspiration through their shared notebooks.
