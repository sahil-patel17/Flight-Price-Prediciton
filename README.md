# ✈️ Flight Price Analysis & Prediction

A complete end-to-end Data Science project that analyzes Indian flight pricing data and builds a machine learning model to predict ticket prices.

---

## 📌 Project Overview

This project explores what factors influence flight ticket prices in India — such as airline, class, number of stops, departure time, and how far in advance the ticket is booked. After a thorough exploratory data analysis (EDA), three ML models were trained and evaluated to predict flight prices.

---

## 📂 Dataset

- **Source:** Indian Flight Pricing Dataset
- **Features:** Airline, Source City, Destination City, Departure Time, Arrival Time, Class, Duration, Stops, Days Left, Price
- **Size:** ~300,000 records

---

## 🔍 Business Questions Answered

1. Which city has the highest number of departing flights?
2. How does departure time affect ticket price?
3. What is the relationship between number of stops and flight duration?
4. How does destination city affect price?
5. How does price change when tickets are bought 1–2 days before departure?
6. Which airline has the highest average ticket price?
7. What is the average price for different source–destination combinations?
8. How does arrival time affect price?

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | ML models & pipelines |
| Google Colab | Development environment |

---

**Models trained:**
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor ✅ *(Best Model)*

**Preprocessing:**
- OneHotEncoding for: `airline`, `source_city`, `destination_city`, `departure_time`, `arrival_time`
- Manual mapping for: `class` (Economy=0, Business=1), `stops` (zero=0, one=1, two_or_more=2)
- Feature engineering: `weeks` derived from `days_left`

---

## 📊 Model Results

| Model | MAE | RMSE | Test R² | Train R² |
|---|---|---|---|---|
| Linear Regression | 4590.37 | 7061.89 | 0.90 | 0.90 |
| Decision Tree | 1804.03 | 3797.73 | 0.97 | 0.98 |
| **Random Forest** | **1803.60** | **3692.01** | **0.97** | **0.98** |

**Cross-Validation (Random Forest, cv=5):**
- Mean R²: ~0.97
- Low std deviation → stable and consistent model

---

## 📈 Key Findings

- **Business class** tickets are significantly more expensive than Economy
- **Non-stop flights** are priced higher than flights with stops
- **Airline** is one of the strongest price predictors
- Tickets bought **1–2 days before departure** are the most expensive
- **Duration** and **class** are the top features by importance
