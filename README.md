# 🍔 Food Delivery Time Estimation using Machine Learning

## 📌 Project Overview

This project predicts the estimated food delivery time based on various factors such as delivery partner details, restaurant location, customer location, weather conditions, traffic density, vehicle type, city, and festival information.

The project follows a complete Machine Learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction.

---

## 📂 Dataset

The dataset consists of two files:

* **Train Dataset:** 45,593 records
* **Test Dataset:** 11,399 records

### Features

* Delivery Person Age
* Delivery Person Ratings
* Restaurant Latitude & Longitude
* Delivery Location Latitude & Longitude
* Order Date
* Time Ordered
* Time Picked
* Weather Conditions
* Road Traffic Density
* Vehicle Condition
* Type of Order
* Type of Vehicle
* Multiple Deliveries
* Festival
* City

### Target Variable

* **Time_taken(min)**

---

## 🚀 Project Workflow

### 1. Data Understanding

* Loaded training and testing datasets
* Explored dataset structure
* Checked data types
* Examined missing values
* Identified duplicate records

### 2. Data Cleaning

* Replaced invalid missing values
* Converted data types
* Handled missing values
* Cleaned the target variable
* Removed unnecessary columns

### 3. Exploratory Data Analysis (EDA)

* Delivery Time Distribution
* Delivery Person Age Distribution
* Delivery Ratings Distribution
* Weather Conditions Analysis
* Road Traffic Density Analysis
* Vehicle Type Analysis
* City Distribution
* Boxplots for Outlier Detection
* Correlation Heatmap

### 4. Feature Engineering

Created new features to improve model performance:

* Delivery Distance (Haversine Formula)
* Order Month
* Order Day
* Weekday
* Weekend Indicator

### 5. Data Preprocessing

* Label Encoding
* Feature Selection
* Train-Test Split

### 6. Machine Learning Models

The following regression models were trained and evaluated:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* XGBoost Regressor

### 7. Model Evaluation

Models were evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

---

# 📊 Model Performance

| Model             |      MAE |     RMSE |  R² Score |
| ----------------- | -------: | -------: | --------: |
| Linear Regression |     5.67 |     7.09 |     0.427 |
| Decision Tree     |     4.24 |     5.62 |     0.639 |
| Random Forest     |     3.21 |     4.05 |     0.813 |
| **XGBoost**       | **3.18** | **3.99** | **0.819** |

**Best Performing Model:** XGBoost Regressor

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

---

# 📁 Project Structure

```
Food-Delivery-Time-Estimation/
│
├── train.csv
├── test.csv
├── model.ipynb
├── README.md
├── requirements.txt
└── images/
```

---

# 📈 Key Insights

* Delivery distance significantly affects delivery time.
* Heavy traffic leads to longer delivery durations.
* Weather conditions also influence delivery performance.
* Feature engineering improved model accuracy.
* Ensemble models outperformed the basic Linear Regression model.
* XGBoost achieved the highest prediction performance.

---

# 🎯 Future Improvements

* Hyperparameter optimization using Optuna.
* Advanced feature engineering with time-based features.
* Deployment using Flask or FastAPI.
* Interactive dashboard using Streamlit.
* Real-time delivery time prediction.

---

# ✅ Conclusion

This project demonstrates a complete Machine Learning pipeline for predicting food delivery time. The workflow includes data cleaning, exploratory data analysis, feature engineering, model training, evaluation, and prediction. Among all the models tested, **XGBoost Regressor** achieved the best performance with an **R² Score of 0.819**, making it the most effective model for this dataset.
