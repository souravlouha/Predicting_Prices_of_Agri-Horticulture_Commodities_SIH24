# 🌾 Predicting Prices of Agri-Horticulture Commodities

## 📘 Project Title: Crop_Prediction

**Crop_Prediction** is a comprehensive machine learning-powered web application designed to forecast the prices of agricultural and horticultural commodities in India. The platform helps farmers, agri-businesses, and policymakers by delivering accurate crop price predictions, supporting data-driven decision-making, and reducing financial risk due to unpredictable market fluctuations.

Developed with a focus on accessibility, scalability, and real-world utility, this system uses real datasets from [data.gov.in](https://data.gov.in), including historical crop prices, rainfall data, and wholesale price index (WPI) statistics. Using this multi-faceted data, a **Decision Tree Regression** model is trained to predict the prices of various crops for up to **12 future months** with an accuracy ranging between **93% and 95%**.

---

## 🎯 Project Objective

The Indian agricultural market is highly dynamic. Farmers often face a dilemma regarding the right time to sell their produce due to lack of reliable price forecasts. The primary objectives of this project include:

- 📈 Predicting future crop prices based on historical data  
- 📊 Identifying top gainers and losers among various crops  
- 🧠 Enabling farmers to make informed decisions  
- 💡 Helping policymakers to track food inflation and plan procurement  
- 🤝 Bridging the data gap in India's agricultural ecosystem  

---

## 🧠 Our Approach

### 1. Data Collection & Curation

We use authenticated datasets from [data.gov.in](https://data.gov.in):
- Historical monthly crop price data for 23 key commodities  
- Rainfall data which influences crop yield  
- Wholesale Price Index (WPI) values that reflect market trends  

These datasets are cleaned, normalized, and aligned based on temporal factors to ensure consistency across different sources.

### 2. Feature Engineering

For each crop entry, we generate features like:
- Month index (seasonality factor)  
- Average rainfall for the region  
- Corresponding WPI for that commodity type  
- Historical moving average of crop price trends  

### 3. Model Training

We use **Decision Tree Regressors**, a supervised learning technique from **scikit-learn**, known for its interpretability and ability to model non-linear patterns. The model is trained on preprocessed data, then evaluated on hold-out test sets. Accuracy reaches **93–95%**, and outliers are handled using smoothing techniques.

### 4. Forecasting

For each commodity selected by the user, the model forecasts the prices for the **next 12 months**. Forecasts are displayed using **interactive graphs** (Chart.js) and data tables, highlighting key price fluctuations.

### 5. Visualization

All forecast results are presented through:
- 📈 Dynamic line graphs  
- 📉 Tabular data comparisons  
- 🔼 Top Gainers & 🔽 Top Losers based on projected changes  

---

## 👨‍🌾 Why This Matters for Farmers & Stakeholders

- ✅ **Farmers**: Can plan sowing and selling schedules based on projected price trends, reducing risk and increasing profit  
- ✅ **Traders & Retailers**: Helps optimize inventory purchases and investments  
- ✅ **Government Bodies**: Use the tool to predict inflation-sensitive crops, plan imports, or issue Minimum Support Price (MSP) advisories  
- ✅ **NGOs/Agri Startups**: Build value-added services around this forecasting engine  

**Impact**:  
> With accurate insights into market behavior, this system can significantly enhance rural economic resilience and productivity.

---

## 💻 Technology Stack

| Component         | Technology Used                             |
|------------------|---------------------------------------------|
| Language          | Python 3                                    |
| Backend           | Flask Web Framework                         |
| Machine Learning  | scikit-learn (DecisionTreeRegressor)        |
| Frontend          | HTML, CSS (MaterializeCSS), JavaScript      |
| Charts            | Chart.js                                     |
| Deployment        | Streamlit (alternate live deployment)       |

---

## 🚀 Features

- 📌 23 Crops Supported: Cereals, fruits, vegetables, spices, etc.  
- 📈 12-Month Prediction Window  
- 🔍 Top Gainers & Losers Tracker  
- 📉 Side-by-side Historical vs Predicted Graphs  
- 🧠 Model built with Decision Tree Regression  
- 🌦️ Uses Rainfall and WPI data as auxiliary predictors  
- 🖥️ Fully Interactive Interface  
- 📡 Accessible from any browser  

---

## 🔧 How to Run Locally

```bash
# Step 1: Clone the repository
git clone https://github.com/souravlouha/Crop_Prediction.git
cd Crop_Prediction

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Start the Flask server
python app.py

# Step 4: Open in browser
# Go to: http://127.0.0.1:5000

```

----------

### 📷 Screenshots
(Embed your screenshots here using this format)

<img src="static/Screenshot%20(23).png" width="700"/>
<img src="static/Screenshot%20(24).png" width="700"/>
<img src="static/Screenshot%20(25).png" width="700"/>
<img src="static/Screenshot%20(26).png" width="700"/>
<img src="static/Screenshot%20(27).png" width="700"/>

----------

### 📁 Directory Structure
```
Crop_Prediction/
├── app.py               # Flask backend logic
├── crops.py             # Data parser & prediction logic
├── templates/           # Jinja2 HTML templates
├── static/              # CSS, JS, and images
├── requirements.txt     # Python dependencies
├── README.md            # Documentation

```


-----------

### 🔮 Future Work
- 🔄 Use LSTM/RNN models for time-series analysis
- 🧭 Add district-wise and geo-tagged price trends
- 🌍 Multi-language interface for regional accessibility
- 📱 Convert to a Progressive Web App (PWA) or Android app
- 📊 Add real-time data ingestion from market APIs
- 📩 SMS or Email alerts for predicted price spikes
- 🛰️ Integration with satellite imagery to correlate weather impact

  ------

  ### ✨ Contributors
- Sourav Louha – Full-stack development, model design
- Debajyoti Chowdhury – Full-stack development, Data handling, frontend support

  ---

  ### 📑 Acknowledgements & License
- 📊 Data Source: https://data.gov.in
- 📄 This project is released under the MIT License and intended for educational and research purposes.

----------
--------

## 🌾 Theoretical Background of Crop_Prediction – A Machine Learning Based Commodity Price Forecasting System
 **Introduction -**  Agriculture is the cornerstone of the Indian economy, employing more than 50% of the country’s workforce. However, the agricultural market in India is characterized by high volatility in the prices of commodities such as rice, wheat, tomato, and onion. This volatility, combined with a lack of reliable forecasting tools, often leads to farmer distress, post-harvest losses, and inefficient market behavior.
To tackle these challenges, the Crop_Prediction project introduces a data-driven approach for forecasting crop prices using machine learning algorithms, specifically Decision Tree Regression, with the aim of enhancing profitability for farmers and providing strategic insights for stakeholders such as agri-businesses and policymakers.

**Problem Statement -**  Farmers face the problem of price unpredictability, which hampers their ability to make informed decisions regarding crop production and marketing. Traditional forecasting methods are either non-transparent or unavailable at the grassroots level. This project proposes a technological solution using AI and ML to forecast prices in advance based on historical and environmental data.

**Theoretical Foundations -** The Crop_Prediction project leverages principles from machine learning, data mining, and time series analysis to model the nonlinear relationships between commodity prices and various factors such as rainfall and economic indices. The model aims to learn from past trends and generalize them for future prediction.

**Data Collection and Sources -** The project uses publicly available data from the Government of India:

- Historical Crop Price Data: Monthly commodity prices from data.gov.in for over 23 commodities.
- Rainfall Data: Annual and seasonal rainfall data, critical to understanding crop yield impact.
- Wholesale Price Index (WPI): Macro-economic indicator that reflects the price level of goods including agri-products.

**Data Preprocessing -** Preprocessing is a critical step in any ML pipeline. In this project, it includes:

- Handling Missing Values: Filling in gaps in rainfall or price data.
- Temporal Alignment: Ensuring rainfall and WPI data are synchronized with crop price data month-wise.
- Normalization: Standardizing features like WPI and rainfall for uniform scale.
- Encoding: Encoding categorical variables such as crop name or category for model input.

**Feature Engineering -** The model’s ability to forecast accurately is heavily dependent on meaningful features. Key features include:
- Month Index: Accounts for seasonal price variation.
- Moving Averages: To capture temporal price trends.
- Rainfall Index: Normalized value for corresponding months/regions.
- WPI Index: Economic pressure on commodity prices.
These features are then fed into the model as predictors (independent variables).

**Machine Learning Model: Decision Tree Regression**
The core ML algorithm used is the Decision Tree Regressor from the scikit-learn library. Decision Trees are a form of supervised learning suitable for both classification and regression tasks.

**Key characteristics of this model:**
- Non-linear modeling: Capable of modeling sudden price spikes or drops.
- Interpretability: Each decision path can be visualized and interpreted.
- Robustness: Handles missing and noisy data better than linear models.
- Low Bias, High Variance: Managed through pruning and hyperparameter tuning.
- The dataset is split into training (80%) and testing (20%) sets, and metrics such as R² score and Mean Squared Error (MSE) are used to evaluate model accuracy.

**Forecasting Pipeline**
Once trained, the model forecasts the crop prices for the next 12 months based on the most recent available data. The output includes:
-Month-wise predicted price
-Trend charts
- Comparison with historical prices
- Identification of Top Gainers and Losers

**Visualization and User Interface**
The front-end is designed using HTML, MaterializeCSS, and Chart.js to provide:
- Dynamic interactive charts
- Tabular summaries of forecasted prices
- User-friendly selection interface for crops and time periods
- A Flask web server handles the back-end logic, and the system can also be hosted via Streamlit for instant online access.

**Real-World Impact**
- For Farmers: Helps plan sowing and selling to maximize profit.
- For Traders: Offers insights for smart buying/selling strategies.
- For Policymakers: Provides macro-level insights into price stability and inflation.
- For Researchers: Acts as a testbed for developing agri-economic forecasting systems.

**Limitations and Future Work**
Although the model provides a strong baseline prediction, it may not account for real-time market shocks (e.g., sudden pest outbreaks, war, policy changes). Future enhancements include:
- Use of LSTM or RNN for deep time-series modeling
- Incorporation of satellite imagery for yield estimation
- Real-time API integrations with market data
- Support for local languages and mobile access
- SMS/WhatsApp alerts for price thresholds

**Conclusion**
Crop_Prediction is a scalable, cost-effective solution that leverages publicly available data to offer valuable insights into crop market behavior. By integrating economic and environmental factors into a prediction model, this system provides a much-needed support tool for India’s agricultural community. It stands as a demonstration of how AI/ML can be applied in real-world domains like agritech for sustainable development and rural empowerment.



