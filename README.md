# 🌤 Daily Weather Report to Telegram using n8n

An automated **n8n workflow** that retrieves the latest weather information from the **Open-Meteo API** and delivers a daily weather report directly to a Telegram chat.

This project is designed for beginners learning workflow automation with **n8n** while using **100% free services**—no paid APIs or subscriptions required.

---

## 📌 Features

* ⏰ Runs automatically every day using a Schedule Trigger
* 🌤 Retrieves live weather data from the Open-Meteo API
* 🌡 Displays temperature, humidity, wind speed, and weather conditions
* 📩 Sends a formatted weather report to Telegram
* 💸 No API key required
* 🆓 Completely free to build and use

---

## 🛠 Technologies Used

* n8n
* Open-Meteo API
* Telegram Bot API
* BotFather

---

## 📂 Workflow

```text
Schedule Trigger
        │
        ▼
HTTP Request
        │
        ▼
Edit Fields (Set)
        │
        ▼
Code
        │
        ▼
Telegram
```

---

## 📋 Prerequisites

Before importing this workflow, ensure you have:

* n8n installed (Cloud or Self-hosted)
* A Telegram account
* A Telegram Bot created with BotFather
* Your Telegram Chat ID

No paid services are required.

---

## ⚙️ Workflow Overview

### 1. Schedule Trigger

Runs the workflow automatically every day at a specified time (e.g., 7:00 AM).

### 2. HTTP Request

Fetches the latest weather data from the Open-Meteo API.

Example endpoint:

```
https://api.open-meteo.com/v1/forecast
```

### 3. Edit Fields (Set)

Extracts only the required weather values:

* Temperature
* Humidity
* Wind Speed
* Weather Code

### 4. Code

Converts the weather code into a human-readable description such as:

* ☀️ Clear Sky
* 🌤 Mainly Clear
* ⛅ Partly Cloudy
* ☁️ Overcast
* 🌧 Rain
* ⛈ Thunderstorm

### 5. Telegram

Sends the formatted weather report to the specified Telegram chat.

---

## 📱 Example Output

```
🌤 Daily Weather Report

📍 Cebu City

🌡 Temperature: 29°C
💧 Humidity: 76%
🌬 Wind Speed: 11 km/h
☁ Weather: ⛅ Partly Cloudy

Have a wonderful day!
```

---

## 📚 Learning Objectives

This project helps you learn:

* Workflow automation
* Schedule-based execution
* REST API integration
* HTTP Request node
* JSON data processing
* Expressions in n8n
* Data transformation
* Telegram automation

---

## 🚀 Future Improvements

Possible enhancements include:

* 7-day weather forecast
* Rain alerts
* Multiple locations
* Weather charts
* Google Sheets integration
* Email notifications
* Discord notifications
* Daily weather logs
* AI-generated weather summaries using a local LLM (e.g., Ollama)

---

## 📄 License

This project is available under the MIT License.

---

## 🙌 Acknowledgements

* Open-Meteo for providing a free weather API
* The n8n team for the automation platform
* Telegram for the Bot API
