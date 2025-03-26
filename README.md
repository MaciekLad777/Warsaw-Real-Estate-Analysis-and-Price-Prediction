# Warsaw Real Estate Analysis and Price Prediction

![Warsaw Real Estate](./warsaw.jpeg)

**This project explores key factors driving apartment prices in Warsaw. It analyzes location, infrastructure access, building materials, and other variables to build a reliable machine learning model for property price prediction.**

---

## Project Overview

The project consists of four main components:

1. **Power BI Report**
   - Provides a visual introduction to the dataset and key pricing factors.
   - Shows how different features impact apartment prices.
   - Highlights correlations and trends between variables.

2. **Data Preprocessing**
   - Cleans and prepares raw data for modeling.
   - Assigns apartments to districts based on GPS coordinates.
   - Calculates distances to schools, malls, hospitals, transit hubs, etc.
   - Examines data distributions and removes outliers.

3. **Feature Correlation and Importance**
   - Identifies the most influential features affecting price.
   - Applies Lasso regression for linear analysis.
   - Uses SHAP values with XGBoost to capture non-linear relationships.

4. **Price Prediction Model**
   - Applies PCA to reduce dimensionality of correlated features.
   - Combines a Keras preprocessing pipeline with an XGBoost regressor.
   - Optimizes model parameters with RandomizedSearchCV.

---

## Project Structure

- `Warsaw_real_estate_analysis.pbix`  
  Power BI dashboard exploring price trends and feature impact.

- `Data_preprocessing.ipynb`  
  Jupyter notebook for cleaning, outlier removal, and feature engineering.

- `Features_analysis.ipynb`  
  Feature importance analysis using Lasso regression and SHAP.

- `Real_estate_price_prediction.ipynb`  
  Final ML pipeline using XGBoost and Keras preprocessing.

- `prediction_model.joblib`  
  Trained XGBoost model (Joblib format) ready for prediction.

---

## Model Performance

The final model achieved a **Mean Absolute Error (MAE) below 16**, which is impressive given that apartment prices in Warsaw typically range from **10,000 to 30,000 PLN per square meter**.

---

## How to Use

1. **Power BI Dashboard**  
   Open `Warsaw_real_estate_analysis.pbix` to explore interactive visualizations and key insights.

2. **Jupyter Notebooks**  
   Walk through the preprocessing, feature analysis, and modeling steps in the provided notebooks.

3. **Making Predictions**  
   Load the trained model from `prediction_model.joblib` and use it to predict apartment prices using your own data.

---

