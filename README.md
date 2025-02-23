Project Overview:
This project focuses on predicting weekly retail sales using historical sales data from 45 stores across different regions. The dataset includes information on store characteristics, external economic indicators, promotional markdowns, and holiday events. By leveraging machine learning techniques, this project aims to build an effective predictive model to assist in sales forecasting.

Dataset Description:
The dataset consists of three key components:

Stores Dataset:

Contains anonymized information about 45 stores, including store type and size.
Features Dataset:

Includes external factors that might influence sales, such as:
Temperature: Average temperature in the store’s region.
Fuel Price: Cost of fuel in the region.
Markdown1-5: Promotional markdown data (available only after November 2011, with missing values).
CPI: Consumer Price Index.
Unemployment: Regional unemployment rate.
IsHoliday: Boolean indicator for holiday weeks.
Sales Dataset:

Contains weekly sales records from February 2010 to November 2012.
Includes store number, department number, sales figures, and holiday indicators.
Data Preprocessing
Handling Missing Values:
Markdown features (MarkDown1-5) were missing in several entries and were filled with 0.
Missing values in CPI and Unemployment were imputed using their respective mean values.
Merging Datasets:
The Stores, Features, and Sales datasets were merged based on the Store and Date columns to create a unified dataset for model training.
Exploratory Data Analysis (EDA)
Conducted a detailed EDA to understand feature relationships and their impact on sales, including:

The effect of holiday weeks on sales trends.
The correlation between promotional markdowns and sales.
The impact of external factors (CPI, Unemployment, Fuel Price, Temperature) on weekly sales.
Modeling Approach
Model Used:
XGBRegressor (Extreme Gradient Boosting) was selected due to its efficiency and ability to handle non-linear relationships in sales data.
Training and Evaluation:
The model was trained on the merged dataset to predict Weekly Sales.
Performance was measured using Mean Absolute Error (MAE), which resulted in 3333.
Given the wide range of sales values (-4000 to 700000), this error suggests a reasonable predictive capability.
Results and Future Improvements
The XGBRegressor model demonstrated good performance but can be further optimized through:
Feature engineering to capture seasonality, store-specific trends, and demand patterns.
Hyperparameter tuning to refine model accuracy.
Testing alternative models such as Random Forest, LSTM (for time-series forecasting), or ensemble techniques.
