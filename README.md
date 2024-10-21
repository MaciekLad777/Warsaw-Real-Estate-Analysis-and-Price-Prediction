# Warsaw Real Estate Analysis and Price Prediction

![Warsaw Real Estate](./warsaw.jpeg)

**Welcome to the Warsaw Real Estate Price Prediction project! This repository contains an in-depth look at what drives apartment prices in Warsaw. We explore key factors like proximity to the city center, the condition of the flats, building materials, and distances to important services like schools, healthcare, and public transport.**

## Project Overview

The project is broken down into four main sections:

1. **Power BI Report**
   - A great introduction to the overall topic.
   - Analyzing how individual features affect apartment prices.
   - Exploring relationships and dependencies between different features.

2. **Data Preprocessing**
   - Cleaning and prepping the data.
   - Assigning apartments to districts based on geolocation.
   - Calculating distances to places like malls, train stations, etc.
   - Studying data distribution and removing outliers.

3. **Feature Correlation and Impact**
   - Investigating which features are most closely linked to price.
   - Using Lasso regression (for linear relationships) and SHAP values with XGBoost (for non-linear ones) to assess feature importance.

4. **Price Prediction Model**
   - Applying Principal Component Analysis (PCA) to similar features.
   - Building a machine learning model to predict apartment prices.
   - Combining a custom Keras model for data preprocessing with an XGBoost model for price prediction.
   - Fine-tuning the model with RandomizedSearchCV for optimal performance.

## Project Structure

- `Warsaw_real_estate_analysis.pbix`: Power BI report that visualizes the key factors affecting real estate prices.
- `Data_preprocessing.ipynb`: Jupyter notebook for data cleaning, outlier removal, and feature engineering.
- `Features_analysis.ipynb`: Jupyter notebook for feature correlation analysis using Lasso regression and SHAP values.
- `Real_estate_price_prediction.ipynb`: Jupyter notebook that contains the final machine learning model using XGBoost and Keras for preprocessing.

- `prediction_model.joblib`: The trained XGBoost model saved in Joblib format, ready for making predictions.

## Model Performance

The final model did an awesome job! It achieved a **Mean Absolute Error (MAE) of less than 16**, which is pretty impressive considering apartment prices in Warsaw range from around **10k to 30k** per square meter.

## How to Use

1. **Power BI Report**:
   - Explore the Power BI report (`Warsaw_real_estate_analysis.pbix`) to visualize and understand the factors affecting apartment prices.

2. **Jupyter Notebooks**:
   - Check out the Jupyter notebooks to see how we processed the data, analyzed features, and built a price prediction model.

3. **Predictions**:
   - If you want to predict apartment prices, you can use the trained XGBoost model (`prediction_model.joblib`).

   Here's how you can use it:

   ```python
   import joblib
   import pandas as pd

   # Load the trained model
   model = joblib.load('prediction_model.joblib')

   # Load your new data
   data = pd.read_csv('new_data.csv')

   # Make predictions
   predicted_price = model.predict(data)
   data['SquareMeterPrice']=predicted_price



**Note: The input data must be in the correct format. You can refer to the preprocessed_data.csv file to understand the required structure. The 'SquareMeterPrice' column in the input data is a placeholder and does not affect predictions but is necessary for maintaining the proper data shape.**
