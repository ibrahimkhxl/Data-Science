# \# 🛒 Sales Prediction with LightGBM
# This project builds a machine learning pipeline to predict product-level daily sales for a retail business. It includes feature engineering, model training, hyperparameter tuning, and evaluation with LightGBM.
# ---
# \## 📊 Dataset Overview
# \*\*Historical data columns:\*\*

# \- `Date`
# \- `Product`
# \- `Quantity`
# \- `DayOfWeek`
# \- `Month`
# \- `Year`
# \- `IsWeekend`
# \- `High\_season`
# \- `lag\_1`, `lag\_7`, `lag\_30`
# \- `roll\_mean\_7`, `roll\_mean\_30`

# \- `volume\_category`

# 

# \*\*One-hot encoded columns:\*\*  

# E.g. `Product\_27in\_4K\_Gaming\_Monitor`, `Product\_iPhone`, etc.

# 

# ---

# 

# \## 🔨 Key Steps

# 

# \### ✅ Data Preparation

# 

# \- Cleaned missing or inconsistent entries.

# \- Converted dates to datetime.

# \- Created time-series features:

# &nbsp; - Rolling means (7, 30 days)

# &nbsp; - Lags (1, 7, 30 days)

# \- One-hot encoded products for modeling.

# 

# ---

# 

# \### ✅ Baseline Model

# 

# Used LightGBM with default parameters:

# 

# \- \*\*MAE:\*\* ~6.99

# \- \*\*RMSE:\*\* ~9.29

# \- \*\*R²:\*\* ~0.90

# 

# Model performed well on historical data.

# 

# ---

# 

# \### ✅ Hyperparameter Tuning

# 

# \- Conducted RandomizedSearchCV and GridSearchCV.

# \- Best tuned MAE around ~6.65.

# \- Tuning improved metrics only slightly over baseline.

# 

# ---

# 

# \### ✅ Model Evaluation

# 

# \- Visualized predictions vs. actuals.

# \- Smoothed curves over 7 days for trend clarity.

# \- Baseline model tracked historical data well.

# 

# 

# ---

# 

# \## 🤔 Observations \& Learnings

# 

# \- Good historical fit but challenges predicting unseen future trends.

# \- Rolling means help smooth fluctuations but cannot fully predict market shifts.

# \- Performance highly depends on how representative training data is for future periods.

# 

# ---

# 

# \## 🚀 Future Improvements

# 

# \- Integrate external data (promotions, holidays, economic indicators).

# \- Explore deep learning time-series models (LSTM, GRU).

# \- Implement probabilistic forecasting to produce prediction intervals.

# 

# ---

# 

# \## 📈 Predicting Future Sales

# 

# We built a function to predict future sales:

# 

# \- Accepts product name.

# \- Accepts prediction window (e.g. 7 or 30 days).

# \- Generates time-series features automatically.

# \- Outputs future sales forecast.

# 

# 

# ---



# 







