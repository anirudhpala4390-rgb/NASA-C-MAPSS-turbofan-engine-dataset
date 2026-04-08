# ✈️ Aircraft Engine Predictive Maintenance (NASA C-MAPSS)

## 📌 Project Overview

This project focuses on **predicting the Remaining Useful Life (RUL)** of aircraft engines using the NASA C-MAPSS turbofan engine dataset. The goal is to identify potential failures **before they occur**, enabling predictive maintenance and reducing operational risks.

---

## 🚀 Problem Statement

Aircraft engines generate large amounts of sensor data during operation.
The challenge is to:

> Predict how many cycles an engine can operate before failure.

This helps in:

* Preventing unexpected breakdowns
* Reducing maintenance costs
* Improving safety and efficiency

---

## 📊 Dataset Information

* **Source:** NASA Prognostics Center of Excellence
* **Dataset:** C-MAPSS Turbofan Engine Degradation Simulation
* **File Used:** `train_FD001.txt`

### Dataset Structure:

* `engine_id` → Unique engine identifier
* `cycle` → Time step (engine life progression)
* `op_setting_1 to 3` → Operational conditions
* `sensor_1 to 21` → Sensor measurements

---

## 🧠 Target Variable

The dataset does not provide the target directly.

### 🔹 RUL (Remaining Useful Life)

Calculated as:

```python
RUL = max_cycle - current_cycle
```

👉 Represents how many cycles are left before engine failure.

---

## ⚙️ Project Workflow

### 1. Data Loading

* Loaded dataset using Pandas
* Handled missing values (removed extra NaN columns)

### 2. Data Preprocessing

* Assigned meaningful column names
* Created RUL (target variable)
* Selected relevant sensor features

### 3. Feature Engineering

* Extracted sensor columns
* Normalized data using MinMaxScaler

### 4. Exploratory Data Analysis

* Visualized sensor trends over time
* Observed degradation patterns

### 5. Model Building

* Model Used: **Random Forest Regressor**
* Train-Test Split: 80-20

### 6. Model Evaluation

* Metric Used: **RMSE (Root Mean Squared Error)**
* RMSE achieved: ~41

---

## 📈 Results

* Successfully predicted Remaining Useful Life (RUL)
* Model captured degradation trends from sensor data
* Visualization showed correlation between actual and predicted values

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## 🔥 Key Learnings

* Handling real-world noisy data
* Feature selection and normalization
* Understanding time-series degradation patterns
* Building regression models for predictive maintenance

---

## 💡 Future Improvements

* Use advanced models (LSTM for time-series)
* Hyperparameter tuning
* Feature importance analysis
* Deployment as a dashboard

---

## 🎯 Conclusion

This project demonstrates how machine learning can be used for **predictive maintenance in aerospace systems**, helping detect failures early and improve reliability.

---

## 👤 Author

Anirudh Pala
B.Tech ECE | Data Analyst | Machine Learning Enthusiast

---
