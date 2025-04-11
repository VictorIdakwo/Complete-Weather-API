# 🌦️ Nigerian States Weather & Air Quality Data Pipeline

This project collects real-time **weather** and **air quality** data for all 36 Nigerian states and the FCT using the [OpenWeather API](https://openweathermap.org/api). It processes the data using **Pandas** and **Apache Spark**, and stores the results in a **Delta Lake table** for scalable analytics.

---

## 🔁 2-Hourly Automated Ingestion

A scheduled job orchestrates the data ingestion pipeline **every 2 hours**, ensuring that the Delta table is continuously updated with the most recent weather and air quality data for each Nigerian state.

- ✅ Scheduled with: **[insert orchestration tool — e.g., Databricks Jobs]**
- ⏱ Frequency: **Every 2 hours**
- 📌 Output: Appends data to the Delta Table `nigeria_weather.complete_weather_data`

---

## 📦 Features

- Retrieves:
  - Weather (temperature, humidity, wind, cloudiness, precipitation)
  - Air Quality (AQI, PM2.5, PM10, CO, NO₂, SO₂, O₃)
- Parallel API calls using `ThreadPoolExecutor` for efficiency
- Converts data to Pandas and Spark DataFrames
- Stores data in a Delta Lake table
- Optionally saves a local CSV snapshot

---

## 🛠️ Tech Stack

- Python
- OpenWeatherMap API
- Pandas
- Apache Spark
- Delta Lake
- Threading
- [Job Scheduler Tool]

---

## 📁 Project Structure

