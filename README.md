# 🌦️ Localised Precipitation Forecasting in Brazzaville 🇨🇬

This repository contains my solution for the [Zindi Localised Precipitation Forecasting Challenge](https://zindi.africa/competitions/localised-precipitation-forecasting-in-brazzaville-in-republic-of-congo-using-ai), where the goal was to **predict future precipitation levels** in Brazzaville, Republic of Congo, using historical weather data.

📌 **Result:**  
🏅 **Position:** 7th out of all competitors  
📊 **Scores:**  
- Public Leaderboard: **6.9640 RMSE**  
- Private Leaderboard: **9.5191 RMSE**

---

## 📂 Repository Contents

```
📁 precipitation-forecasting/
├── Precipitation_Forecasting.ipynb   # Main solution notebook
├── train.csv                         # Training dataset (to be uploaded)
├── test.csv                          # Test dataset (to be uploaded)
├── submission.csv                    # My final submission file
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation
```

---

## 📜 Competition Overview

The challenge was to develop a model capable of **forecasting daily precipitation** in Brazzaville given weather and environmental variables.  
The main difficulties included:
- **Localised data** — unique patterns specific to Brazzaville’s microclimate.
- **Limited dataset size** — requiring careful feature engineering.
- **Non-linear relationships** — making simple models insufficient.

---

## 🛠️ My Approach

### **1. Data Exploration & Cleaning**
- Handled missing values and outliers in rainfall measurements.
- Conducted time-series checks for seasonality and trends.
- Visualised precipitation patterns over months and years.

### **2. Feature Engineering**
I created **rich temporal and statistical features**:
- Rolling averages (7, 14, and 30-day windows)
- Lag features to capture recent weather patterns
- Seasonal indicators (month, day of year)
- Interaction terms between temperature, humidity, and wind speed

### **3. Model Selection**
- Chose **LightGBM** as the primary model for its speed and handling of non-linear data.
- Tuned hyperparameters using **cross-validation** to avoid overfitting.
- Applied early stopping to prevent unnecessary iterations.

### **4. Evaluation**
- Used **Root Mean Squared Error (RMSE)** as per the competition metric.
- Validated on a custom time-based split to simulate real forecasting scenarios.

---

## 📈 Performance

| Leaderboard | RMSE Score |
|-------------|-----------|
| Public      | **6.9640** |
| Private     | **9.5191** |

---

## 📌 Key Takeaways
- **Feature engineering** was the biggest driver of performance improvements.
- **Tree-based models** like LightGBM are highly effective for weather forecasting with tabular data.
- Understanding **domain context** (Brazzaville’s local climate) helped in feature selection.

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/keystats/Localised-Precipitation-Forecasting-in-Brazzaville-Using-AI.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Add `train.csv` and `test.csv` to the project directory.

4. Run the notebook:
   - Open `Precipitation_Forecasting.ipynb` in Jupyter or Google Colab.
   - Execute all cells to train the model and generate predictions.

---

## 🔮 Future Work
- Incorporate **external datasets** (e.g., satellite imagery, ENSO indexes).
- Experiment with **deep learning architectures** for time-series.
- Try **stacked ensembles** combining LightGBM, CatBoost, and XGBoost.

---

## 👨‍💻 Author
**Jackson Kahungu Njeri**  
Data Scientist   
📊 Focus: Data-driven forecasting, machine learning, and reasoning-based AI.

---

⭐ If you found this repo helpful, give it a star!
