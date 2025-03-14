# Projects
# Real-Time U.S. Temperature Monitoring System

## 📌 Project Overview

This project is a **real-time temperature monitoring system** that:

- Fetches **real-time temperature data** for all U.S. states using the Open-Meteo API.
- Stores the data in an **SQLite database**.
- Detects **anomalous temperatures** based on historical data.
- Sends **alerts** when temperatures exceed verified historical limits.
- Utilizes **machine learning** to predict future temperatures.
- Provides a **Flask-based dashboard** for visualization.
- Exports data to **CSV files for Power BI integration**.

## 🎯 Why This Project?

The project was developed to:

- Automate **temperature anomaly detection** for better climate monitoring.
- Integrate **real-time data streaming** with storage solutions.
- Develop a **machine learning pipeline** for temperature prediction.
- Build an **interactive dashboard** for data visualization.
- Provide **actionable alerts** for extreme weather conditions.

---

## 🛠️ Technologies & Tools Used

| Component            | Technology/Tool       |
| -------------------- | --------------------- |
| Programming Language | Python 3.12           |
| Web Framework        | Flask                 |
| Database             | SQLite                |
| API                  | Open-Meteo            |
| Machine Learning     | Scikit-learn, XGBoost |
| Data Processing      | Pandas, NumPy         |
| Visualization        | Matplotlib, Power BI  |
| Messaging            | Email SMTP            |
| Task Scheduling      | Cron, Time.sleep      |

---

## 📦 Project Structure

```
📂 data-quality-firewall
│── venv/                   # Python Virtual Environment
│── __pycache__/            # Cached Python files
│── weather_monitoring.db   # SQLite database
│── main.py                 # Core script for fetching, storing, and alerting
│── ml_anomaly_detection.py # Machine learning model for predictions
│── alert_notifier.py       # Sends alerts via email
│── dashboard.py            # Flask web dashboard for visualization
│── temperature_data.csv    # CSV file storing temperature records
│── alerts_data.csv         # CSV file storing temperature alerts
│── static/                 # Contains static files for the dashboard
│── templates/              # Contains HTML templates for Flask UI
```

---

## 📜 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-repo/data-quality-firewall.git
cd data-quality-firewall
```

### 2️⃣ Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # For Mac/Linux
venv\Scripts\activate     # For Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Set Up the Database

```bash
python main.py  # This will initialize the database tables
```

---

## 🚀 Running the System

### 1️⃣ Start the Temperature Monitoring Script

```bash
python main.py
```

### 2️⃣ Start the Machine Learning Model (for anomaly detection)

```bash
python ml_anomaly_detection.py
```

### 3️⃣ Start the Flask Dashboard

```bash
python dashboard.py
```

Then, open [**http://127.0.0.1:5000/**](http://127.0.0.1:5000/) in your browser.

---

## 📊 Data Flow & Working

1. **Fetching Data:**
   - `main.py` fetches **real-time temperature** for U.S. states.
   - Compares against **historical records** from Open-Meteo.
2. **Storing Data:**
   - Saves real-time readings into `weather_monitoring.db`.
   - **Exports data to CSV** for Power BI.
3. **Detecting Anomalies:**
   - If temperature crosses normal min/max, it triggers an **alert**.
4. **Sending Alerts:**
   - `alert_notifier.py` sends email alerts for extreme temperatures.
5. **Predicting Future Temperatures:**
   - `ml_anomaly_detection.py` uses **XGBoost** to predict future temperatures.
6. **Visualizing Data:**
   - `dashboard.py` provides an **interactive web dashboard** with **matplotlib** plots.

---

## 🔮 Future Enhancements

- **Integrate Kafka for real-time streaming.**
- **Deploy the Flask dashboard on the cloud (AWS/GCP).**
- **Use a NoSQL database like MongoDB for scalability.**
- **Enhance ML model with deep learning (LSTMs for time series).**
- **Use a cloud-based messaging system (Twilio, Telegram Bot) for alerts.**
---

### ⭐ Like this project? Give it a star on GitHub! 🚀

