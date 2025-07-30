
# 🚗 Predicting Used Car Sale Prices

*A Machine Learning Project*

This repository contains a complete solution for a Kaggle-style forecasting project focused on **predicting used car prices** using machine learning regression models. The project was developed as part of the **BUSA8001 Group Project**.

---

## 📌 Overview

The project aims to accurately forecast used car prices based on various car features provided in a dataset. This is a **supervised regression problem**, where the target variable is **`price`**.

### 🎯 Why Accurate Price Prediction Matters

| Stakeholder           | Benefit                                                   |
| --------------------- | --------------------------------------------------------- |
| 🚘 **Buyers**         | Smarter purchasing decisions & price comparison           |
| 🏷️ **Sellers**       | Optimized pricing strategies for faster, profitable sales |
| 🏦 **Lenders**        | Better collateral estimation for car loans                |
| 📉 **Insurers**       | Fair premium calculations & claims management             |
| 🌍 **Import Dealers** | Competitive local market pricing for imported vehicles    |

---

## 📁 Project Structure

```
├── S1_2024_BUSA8001.ipynb     # Main notebook with code and analysis
├── train.csv                  # Training dataset
├── test.csv                   # Test dataset
├── submission.csv             # Final predictions
```

---

## 📊 Dataset Summary

The dataset consists of various **numerical**, **categorical**, and **boolean** features:

| Type        | Features                                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| **Numeric** | `latitude`, `longitude`, `mileage`, `price`, `horsepower`, `engine_displacement`, `year`, `dealer_zip`, etc. |
| **Nominal** | `make_name`, `model_name`, `fuel_type`, `body_type`, `transmission`, `interior_color`, `engine_type`, etc.   |
| **Boolean** | `is_new`                                                                                                     |
| **Target**  | `price` (car sale price)                                                                                     |

Missing values were found in features like `interior_color`, `mileage`, `torque`, `fuel_economy`, etc., and were handled accordingly.

---

## 🔍 Key Steps

### 1. **Data Preprocessing**

* 🧼 Handling missing values
* 🔁 Converting text-based numerics to float (e.g., `torque`, `height`)
* 🏷️ Encoding categorical features
* 📊 Outlier treatment in variables like `mileage` and `price`

### 2. **Exploratory Data Analysis (EDA)**

* Distribution plots and histograms
* Correlation heatmaps to identify influential predictors
* Visualizing feature relationships with the target (`price`)

### 3. **Modeling**

* Trained multiple models (e.g., Linear Regression, Random Forest, XGBoost, LightGBM)
* Evaluation based on **MAPE** (Mean Absolute Percentage Error)
  $\text{MAPE} = \frac{1}{n} \sum_{i=1}^{n} \left| \frac{y_i - \hat{y}_i}{y_i} \right| \times 100$
* Other metrics considered: **RMSE** and **R²**

### 4. **Prediction & Submission**

* Final model used for test data predictions
* Results saved to `submission.csv`

---

## 📌 Notable Findings

* 📈 Features like `year`, `make_name`, `model_name`, `mileage`, and `engine_displacement` were strong predictors.
* 🛠️ Handling missing values (especially in `torque` and `fuel_economy`) significantly improved model performance.
* 🌍 Geographic features (`latitude`, `longitude`) hinted at region-based price variations.
* 🏁 Performance metrics indicated solid forecasting capability with low MAPE and competitive RMSE.

---

## 🛠️ How to Run

1. **Set up environment**

   ```bash
   pip install pandas seaborn matplotlib missingno scikit-learn
   ```

2. **Update dataset paths in the notebook if needed:**

   ```python
   train_df = pd.read_csv('/your/path/train.csv')
   test_df = pd.read_csv('/your/path/test.csv')
   ```

3. **Run the notebook:**
   Open `S1_2024_BUSA8001.ipynb` in Jupyter and run cells sequentially.

---

## 🧠 Future Improvements

* Hyperparameter tuning with cross-validation
* Using stacked or ensemble models
* Incorporating geospatial clustering features
* Deploying as a web app with Streamlit or Flask

---

## 📎 License

This project is for educational purposes under the BUSA8001 unit at Macquarie University.
📚 Not intended for commercial use.
