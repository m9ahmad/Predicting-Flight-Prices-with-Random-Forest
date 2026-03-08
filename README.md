# Flight Price Prediction & Regression Analysis

An end-to-end machine learning project to predict airline ticket prices using a dataset of over 300,000 flight records. This project explores the impact of flight duration, booking windows, and cabin class on pricing, achieving high predictive accuracy through ensemble methods.

## 🚀 Performance Summary
* **Best Model:** Tuned Random Forest Regressor
* **$R^2$ Score:** 0.98 (Explains 98% of price variance)
* **Mean Absolute Error (MAE):** ~1,813 units
* **Data Size:** 300,153 records

## Dataset Overview
The dataset contains 11 features including:
* **Categorical:** Airline, Source City, Destination City, Departure Time, Arrival Time, Stops, and Class.
* **Numerical:** Duration (hours), Days Left (until departure), and Price (Target).

## 🛠️ Tech Stack
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebooks
* **Libraries:** * **Data Manipulation:** Pandas, NumPy
    * **Visualization:** Matplotlib, Seaborn
    * **Machine Learning:** Scikit-Learn, XGBoost

## Methodology
1. **Exploratory Data Analysis (EDA):** Analyzed price distributions and identified a strong correlation between ticket class (Business vs. Economy) and price.
2. **Feature Engineering:** Applied One-Hot Encoding for categorical cities/airlines and Label Encoding for ordinal features.
3. **Model Selection:** Compared **XGBoost** and **Random Forest** architectures.
4. **Hyperparameter Tuning:** Addressed initial overfitting (where Training $R^2$ was 1.0) by adjusting `max_depth` and `min_samples_leaf` to create a more generalized, robust model.

## Key Insights
* **The Class Factor:** The distinction between Economy and Business class is the most significant predictor of price.
* **Booking Window:** Prices show a significant "spike" as the `days_left` variable approaches zero, confirming the necessity of early booking for cost-efficiency.
* **Model Reliability:** By closing the gap between Training and Test MAE, the model demonstrates high reliability for unseen data.

##  Project Structure
```text
├── Flight_Price_Prediction.ipynb  # Main Google Colab Notebook
├── README.md                      # Project documentation
