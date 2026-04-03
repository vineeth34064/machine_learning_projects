# Gold Price Prediction using Random Forest Regressor

This notebook demonstrates the process of predicting gold prices using a Random Forest Regressor model. The project involves data loading, exploratory data analysis (EDA), model training, and evaluation.

## Dataset
The dataset `gld_price_data.csv` contains historical data for various financial instruments including Gold (GLD), S&P 500 (SPX), Crude Oil (USO), Silver (SLV), and EUR/USD exchange rate.

## Steps Performed

1.  **Data Loading and Initial Inspection**: The `gld_price_data.csv` file was loaded into a pandas DataFrame. Basic information about the dataset, such as its shape (`2290 rows, 6 columns`), data types, and missing values, was checked.

2.  **Statistical Measures**: Descriptive statistics of the dataset were generated to understand the distribution and central tendencies of the numerical features.

3.  **Correlation Analysis**: A correlation matrix was computed for the numerical features (excluding the 'Date' column) and visualized using a heatmap. This helped in understanding the relationships between Gold prices and other assets.

4.  **Target Variable Distribution**: A distribution plot (histogram with KDE) was created for the 'GLD' (Gold Price) column to visualize its distribution.

5.  **Feature and Target Splitting**: The dataset was split into features (`x`) and target (`y`), where 'GLD' was the target variable, and 'Date' was excluded from features.

6.  **Train-Test Split**: The data was further divided into training and testing sets (80% training, 20% testing) to prepare for model training and evaluation.

7.  **Model Training**: A Random Forest Regressor model with 100 estimators was initialized and trained using the `x_train` and `y_train` datasets.

8.  **Prediction**: The trained model was used to make predictions on the `x_test` dataset.

9.  **Model Evaluation**: The R-squared error was calculated to evaluate the model's performance. The R-squared score obtained was approximately **0.9887**, indicating a very high correlation between predicted and actual values.

10. **Visualization of Predictions**: A plot comparing the actual gold prices (`y_test`) with the predicted gold prices (`test_data_pred`) was generated to visually assess the model's accuracy.
