
# 🏠 House Price Prediction App

A machine learning project that predicts house prices based on property features. It involves data cleaning, exploratory data analysis (EDA), model training, and a Streamlit web app for interactive predictions.

---

## 📌 Project Objectives

* Preprocess and clean the house price dataset
* Identify key property features influencing price
* Train a regression model to predict property value
* Deploy a Streamlit app for user-friendly price predictions

---

## 📊 Dataset Overview

* **Target Variable**: `Price` (numeric – predicted house price)
* **Dataset File**: `House Price Prediction Dataset (1).csv`

### ✅ Features Used:

| Column Name | Description                                       |
| ----------- | ------------------------------------------------- |
| `Id`        | Unique identifier for each property               |
| `Area`      | Total area in square feet                         |
| `Bedrooms`  | Number of bedrooms                                |
| `Bathrooms` | Number of bathrooms                               |
| `Floors`    | Number of floors                                  |
| `YearBuilt` | Year the house was built                          |
| `Location`  | Location of the house                             |
| `Condition` | Condition of the property (e.g., Excellent, Fair) |
| `Garage`    | Garage availability (Yes/No or numeric)           |
| `Price`     | Selling price (Target Variable)                   |

---

## 🧹 Data Cleaning

📄 **File**: `Data_Cleaning (2).ipynb`

### Cleaning Steps:

* Handled missing and inconsistent values
* Encoded categorical features like `Location`, `Condition`, and `Garage`
* Converted `YearBuilt` into age-based feature if applicable
* Scaled/normalized numerical features
* Exported cleaned dataset as:
  ✅ `Cleaned_House_Price_Data.csv`

---

## 📊 Exploratory Data Analysis (EDA)

📄 **File**: `EDA_2 (2).ipynb`

### Key Insights:

* **Area** and **Location** are the strongest predictors of price
* Houses with **more bedrooms, bathrooms, and garages** tend to be more expensive
* Newer houses (higher `YearBuilt`) generally fetch higher prices
* Outliers were detected in `Price` and `Area` features

---

## 🤖 Model Training & Selection

📄 **File**: (Model Training inside Data Cleaning or separate)

* Used **regression models** to predict `Price`

  * Linear Regression
  * Random Forest Regressor ✅ *(Best Performance)*
  * Gradient Boosting Regressor

Final trained model saved as:
✅ `House_Price_Prediction_Project (1).pkl`

---

## 🌐 Streamlit Web App

📄 **File**: `app.py` (assumed structure)

### 🔍 Features:

* User inputs property details (area, bedrooms, location, etc.)
* Predicts expected **house price** using saved model
* Displays predicted price in currency format

---

## 🚀 How to Run

```bash
# 1. Install dependencies
pip install pandas numpy scikit-learn streamlit

# 2. (Optional) Retrain model
# Run notebook: Data_Cleaning (2).ipynb or your model training script

# 3. Launch the app
streamlit run app.py
```

---

## 🧪 Example Inputs & Outputs

| Area (sqft) | Bedrooms | Location | Condition | Garage | Predicted Price |
| ----------- | -------- | -------- | --------- | ------ | --------------- |
| 1800        | 3        | Downtown | Good      | Yes    | \$250,000       |
| 3200        | 4        | Suburban | Excellent | Yes    | \$425,000       |

---

## 💾 Files in This Project

| Filename                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- |
| `House Price Prediction Dataset (1).csv` | Raw housing data                         |
| `Data_Cleaning (2).ipynb`                | Data preprocessing & feature engineering |
| `EDA_2 (2).ipynb`                        | Visual analysis and feature insights     |
| `Cleaned_House_Price_Data.csv`           | Cleaned dataset used for modeling        |
| `House_Price_Prediction_Project (1).pkl` | Trained regression model (serialized)    |
| `app.py` *(optional/assumed)*            | Streamlit web app                        |

---
## Output:


---<img width="581" height="756" alt="image" src="https://github.com/user-attachments/assets/32878950-c204-494e-a071-4208715e41f7" />


## 🧠 Future Enhancements

* Add **model explainability** (e.g., SHAP plots)
* Support **map-based location selection**
* Include **historical price trends** per location
* Deploy online via **Streamlit Cloud** or **Render**

