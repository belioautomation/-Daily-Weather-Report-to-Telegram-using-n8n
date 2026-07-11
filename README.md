# 🌤 Daily Weather Report to Telegram using n8n

An automated weather notification workflow built with **n8n** and the **Open-Meteo API**. This workflow retrieves the latest weather information, formats the data into a readable report, and sends a daily weather update directly to Telegram.

Built as part of my **30-Day n8n Automation Portfolio**, this project demonstrates scheduled automation, REST API integration, data transformation, and Telegram notifications using free services.

---

## 📌 Features

- 🌤 Retrieves real-time weather data from the Open-Meteo API
- ⏰ Runs automatically on a scheduled interval
- 🌡 Reports temperature, humidity, and wind speed
- ☁️ Converts weather codes into readable conditions
- 📲 Sends formatted weather reports to Telegram
- 🆓 Uses the free Open-Meteo API (No API key required)
- ⚡ Fully automated workflow

---

## 🛠️ Technologies Used

- n8n
- Schedule Trigger
- HTTP Request
- Edit Fields (Set)
- JavaScript (Code Node)
- Open-Meteo API
- Telegram Bot API

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
Code (JavaScript)
        │
        ▼
Telegram
```

---

## ⚙️ Workflow Explanation

### 1. Schedule Trigger

Starts the workflow automatically at a scheduled time.

---

### 2. HTTP Request

Retrieves the latest weather data from the Open-Meteo API.

Configuration:

- Method: GET
- Authentication: None

---

### 3. Edit Fields (Set)

Extracts only the required weather information.

Fields:

- Temperature
- Relative Humidity
- Wind Speed
- Weather Code

---

### 4. Code Node

Transforms weather codes into human-readable weather conditions and formats the Telegram message.

Example Weather Codes:

| Weather Code | Description |
|--------------|-------------|
| ☀️ | Clear Sky |
| 🌤 | Mainly Clear |
| ⛅ | Partly Cloudy |
| ☁️ | Overcast |
| 🌧 | Rain |
| ⛈ | Thunderstorm |

---

### 5. Telegram

Sends the formatted weather report directly to Telegram.

Example:

```text
🌤 Daily Weather Report

📍 Cebu City

🌡 Temperature: 29°C
💧 Humidity: 76%
🌬 Wind Speed: 11 km/h
☁️ Weather: ⛅ Partly Cloudy

Have a wonderful day!

🤖 Generated automatically using n8n.
```

---

## 📁 Repository Structure

```text
Daily-Weather-Report-to-Telegram/
│
├── README.md
├── workflow.json
│
├── screenshots/
│   └── workflow.png
```

---

## 📷 Screenshots

Include the following screenshots:

- Complete Workflow
- HTTP Request Node
- Edit Fields Node
- Code Node
- Telegram Output
- Workflow Execution

---

## 🎯 Learning Objectives

This project demonstrates:

- Scheduled Workflow Automation
- REST API Integration
- HTTP Requests
- JSON Data Processing
- JavaScript in n8n
- Data Transformation
- Telegram Bot Integration
- API-Based Automation

---

## 🚀 Future Improvements

- Support multiple cities
- 7-day weather forecast
- Rain and storm alerts
- Google Sheets weather history
- Email notifications
- Discord integration
- AI-generated weather summaries
- Weather analytics dashboard

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student  
Cebu Technological University (CTU)

**GitHub:** https://github.com/belioautomation

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical workflow automation using **n8n**, **REST APIs**, and **Telegram integrations**.
