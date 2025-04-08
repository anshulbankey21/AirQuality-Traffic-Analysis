# 🚦 Air Quality & Traffic Delay Prediction Using Machine Learning & Tableau

This project explores the relationship between **air pollution**, **traffic patterns**, and **weather conditions** to build a predictive system that forecasts AQI (Air Quality Index). It combines data cleaning, EDA, predictive modeling, and an interactive Tableau dashboard.

---

## 📌 Project Highlights

- 🧹 **Cleaned 50,000+ records** with missing values in AQI, weather, and traffic data.
- 📊 **Performed EDA**: Univariate, bivariate, and time-based visualizations.
- 🧠 **Built predictive models** (Linear Regression, Random Forest, Gradient Boosting) to estimate AQI using weather & traffic features.
- 🌐 **Created a Tableau dashboard** for intuitive visualization of AQI trends, delays, and pollutants.

---

## 🗂️ Project Structure
```
AirQuality-Traffic-Analysis/
├── data/                  # Cleaned datasets
│   └── cleaned_air_quality_data.csv
├── notebooks/             # Jupyter Notebooks
│   └── cleaning_data.ipynb
|   └── EDA.ipynb
|   └── feature_engineering.ipynb
|   └── model.ipynb
├── models/                # Trained ML model
│   └── aqi_predictor_model.pkl
│   └── aqi_predictor_model2.pkl
├── dashboard/             
│   └── dashboard_app.py
├── README.md              # Project overview (this file)
└── Requirements.txt       # Python dependencies
```

---

## 🧹 Data Cleaning Summary

- Filled missing weather values (`Humidity`, `Wind Speed`) using city-wise means.
- Imputed traffic-related columns (`Duration`, `Distance`) using grouped medians.
- Converted columns to proper data types for analysis.

---

## 🔎 Exploratory Data Analysis (EDA)

### ✅ Univariate Analysis
- Histograms for AQI, Temperature, Traffic Delay.

### ✅ Bivariate Analysis
- Correlation matrix
- Scatter plots: AQI vs Delay, PM2.5 vs PM10

### ✅ Time-Based Trends
- AQI variation by hour of day
- Delay patterns: Weekdays vs Weekends

---

## 🔮 Predictive Modeling

### Models Used:
- **Linear Regression**
- **Random Forest**
- **Gradient Boosting Regressor**

### Target Variable:
- `AQI (Air Quality Index)`

### Features:
- `Duration`, `Temperature`, `Humidity`, `Wind Speed`, `PM2.5`, `PM10`

### Model Export:
```python
import joblib
joblib.dump(rf_model, 'aqi_predictor_model.pkl')

# 📈 Prediction Function

def predict_aqi(duration, temp, humidity, wind, pm25, pm10):
    input_data = np.array([[duration, temp, humidity, wind, pm25, pm10]])
    return rf_model.predict(input_data)[0]
```

📊 Tableau Dashboard
📍 Interactive visualization showing:

AQI trends across cities

PM2.5 vs PM10 analysis

Delay vs AQI heatmaps

Time-based filters

💻 Tech Stack
Python: pandas, numpy, sklearn, seaborn, matplotlib, joblib

Jupyter Notebook: Data analysis & modeling

Tableau: Interactive dashboard

GitHub: Project hosting and version control

📥 How to Run Locally
Clone this repo:
```
git clone https://github.com/anshulbankey21/AirQuality-Traffic-Analysis.git
cd AirQuality-Traffic-Analysis
```
Install dependencies:
pip install -r requirements.txt

Open the notebook:
jupyter notebook notebooks/AQI_EDA_and_Modeling.ipynb

🙋‍♂️ Author
Anshul Bankey
📧 [anshulbankey21@gmail.com]
🔗 LinkedIn -- `linkedin.com/in/anshul-bankey/`

⭐ Show Some Love!
If you found this project useful, consider giving it a ⭐ and sharing it!
Feedback and collaborations are welcome!
