# 🚕 Namma Yatri & Uber Data Analysis and Prediction

This repository contains **Exploratory Data Analysis (EDA)** and **Machine Learning–based prediction** on **Yatri Sathi (Namma Yatri) ride-hailing data** from **Bangalore Open Data**.

The project focuses on understanding **ride booking behavior**, analyzing **user drop-offs across the booking funnel**, studying **ward-wise performance**, handling **outliers in rate-based features**, and building **predictive models** for key business metrics such as **completed trips and drivers’ earnings**.



## 📌 Dataset Overview

### 🔹 Namma Yatri Dataset
- **Source:** Kaggle (Namma Yatri Cab Bookings – Bangalore Open Data)
- **Granularity:** Ward-level aggregated data

### 🔹 Key Columns

| Category | Columns |
|--------|--------|
| Location | `Ward` |
| Demand Funnel | `Searches`, `Searches which got estimate`, `Searches for Quotes`, `Searches which got Quotes`, `Bookings`, `Completed Trips` |
| Rates (%) | `Search-to-estimate Rate`, `Estimate-to-search for quotes Rate`, `Quote Acceptance Rate`, `Quote-to-booking Rate`, `Booking Cancellation Rate`, `Conversion Rate` |
| Revenue | `Drivers' Earnings`, `Average Fare per Trip` |
| Distance | `Average Distance per Trip (km)`, `Distance Travelled (km)` |

---

## 🎯 Project Objectives

- Perform **end-to-end EDA** on ride-hailing data
- Understand the **ride booking funnel**
- Identify **where users drop off**
- Analyze **ward-wise demand and performance**
- Handle **outliers in rate-based columns**
- Build ML models to **predict completed trips and earnings**
- Draw **business insights** relevant to ride-hailing platforms

---

## 🔍 Exploratory Data Analysis (EDA)

### 1️⃣ Data Cleaning
- Removed commas from numeric columns
- Converted percentage columns to numeric values
- Converted currency (`₹`) columns to float
- Handled invalid and missing values

### 2️⃣ Booking Funnel Analysis

The booking funnel analyzed:



- Calculated **drop-off percentages** between each stage
- Identified critical stages where maximum users are lost

### 3️⃣ Ward-wise Performance Analysis
- Top 10 wards by **Completed Trips**
- Visualization using bar charts
- Identification of high-demand areas

### 4️⃣ Cancellation Analysis
- Relationship between:
  - Booking Cancellation Rate
  - Quote Acceptance Rate
  - Fare and Distance

### 5️⃣ Revenue & Distance Analysis
- Average Fare vs Average Distance
- Distance Travelled vs Drivers’ Earnings

### 6️⃣ Correlation Analysis
- Correlation heatmap
- Used to guide feature selection for ML

---

## 🧹 Outlier Handling

- Rate-based columns often contain extreme values
- Used **IQR (Interquartile Range) method**
- Applied **clipping instead of deleting rows**

### Why clipping?
- Preserves data
- Prevents distortion in EDA and ML models
- Improves model stability

---

## 🤖 Machine Learning

### 🔮 Prediction Tasks

- **Completed Trips (Regression)**
- **Drivers’ Earnings (Regression)**
- *(Optional)* Booking Cancellation Rate

### ⚙️ ML Workflow

1. Feature selection based on EDA
2. Train-test split
3. Model training using:
   - Linear Regression
   - Random Forest Regressor
   - Gradient Boosting (optional)
4. Model evaluation using:
   - R² Score
   - Mean Absolute Error (MAE)

---

## 📊 Key Insights

- A small number of wards contribute a large share of completed trips
- Major user drop-offs occur after quote generation
- High cancellation rates significantly reduce completed trips
- Distance and fare strongly influence driver earnings

---

## 🛠️ Tech Stack

- Python 🐍
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---
---

## 🚀 Conclusion

This project demonstrates how **data-driven analysis** can help ride-hailing platforms like **Namma Yatri and Uber**:

- Improve conversion rates
- Reduce cancellations
- Optimize driver deployment
- Increase completed trips and earnings






