# 📊 Retail Sales Prediction using Machine Learning  

## 📌 Project Overview  
This project focuses on predicting **weekly retail sales** using historical sales data from **45 stores** across different regions.  
The dataset includes information on:  
- Store characteristics  
- External economic indicators  
- Promotional markdowns  
- Holiday events  

By leveraging **machine learning**, this project aims to build an effective predictive model to assist in **sales forecasting**.  

---

## 📂 Dataset Description  
The dataset consists of **three** key components:  

### 🏢 Stores Dataset  
Contains anonymized information about 45 stores, including **store type** and **size**.  

### 📋 Features Dataset  
Includes external factors that might influence sales, such as:  
- **Temperature:** Average temperature in the store’s region  
- **Fuel Price:** Cost of fuel in the region  
- **Markdown1-5:** Promotional markdown data (available only after **November 2011**)  
- **CPI:** Consumer Price Index  
- **Unemployment:** Regional unemployment rate  
- **IsHoliday:** Boolean indicator for holiday weeks  

### 💰 Sales Dataset  
Contains weekly sales records from **February 2010 to November 2012**, including:  
- **Store Number**  
- **Department Number**  
- **Weekly Sales** figures  
- **Holiday Indicators**  

---

## 🛠 Data Preprocessing  
### ✅ Handling Missing Values  
- **Markdown Features (MarkDown1-5):** Missing values were **filled with 0**.  
- **CPI & Unemployment:** Missing values were imputed using their **mean values**.  

### 🔗 Merging Datasets  
The `Stores`, `Features`, and `Sales` datasets were merged based on the **Store** and **Date** columns to create a unified dataset for model training.  

---

## 📊 Exploratory Data Analysis (EDA)  
Conducted **detailed EDA** to understand feature relationships and their impact on sales, including:  
✔ The effect of **holiday weeks** on sales trends  
✔ Correlation between **promotional markdowns** and sales  
✔ Impact of **external factors** (CPI, Unemployment, Fuel Price, Temperature) on weekly sales  

---

## 🤖 Modeling Approach  
### 📌 Model Used  
- **XGBRegressor** (Extreme Gradient Boosting) was selected for its efficiency and ability to handle non-linear relationships in sales data.  

### 🎯 Training and Evaluation  
- The model was trained on the merged dataset to predict **Weekly Sales**.  
- Performance was measured using **Mean Absolute Error (MAE)**:  
  ```yaml
  MAE: 3333
