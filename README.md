# 🌤 Daily Weather Report to Telegram using n8n

An automated **n8n workflow** that retrieves the latest weather information from the **Open-Meteo API** and sends a beautifully formatted daily weather report directly to a **Telegram chat**.

This project demonstrates how to build a fully automated workflow using free services without requiring an API key.

---

# 📌 Project Overview

This workflow automatically:

* ⏰ Runs on a scheduled time every day
* 🌐 Retrieves real-time weather data from the Open-Meteo API
* 🔄 Extracts and formats the required weather information
* 🧠 Converts weather codes into human-readable conditions
* 📲 Sends a formatted weather report to Telegram

---

# ✨ Features

* Daily scheduled automation
* Real-time weather information
* Temperature reporting
* Humidity reporting
* Wind speed reporting
* Weather condition translation
* Telegram Bot integration
* Free Open-Meteo API
* No API key required
* Fully automated workflow

---

# 🛠 Tech Stack

* **n8n**
* **Open-Meteo API**
* **HTTP Request Node**
* **Edit Fields (Set) Node**
* **Code Node (JavaScript)**
* **Telegram Bot API**

---

# 📂 Repository Structure

```
.
├── Daily Weather Report to Telegram.json
├── README.md
└── workflow-image/
```

---

# 🔄 Workflow

```
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

# ⚙️ Workflow Explanation

## 1. Schedule Trigger

Starts the workflow automatically at the configured schedule.

---

## 2. HTTP Request

Retrieves the latest weather data from the Open-Meteo API.

**Method**

```
GET
```

**Authentication**

```
None
```

---

## 3. Edit Fields (Set)

Extracts only the required fields from the API response:

* Temperature
* Relative Humidity
* Wind Speed
* Weather Code

---

## 4. Code Node

Transforms weather codes into readable weather descriptions.

Examples include:

| Weather Code | Description   |
| ------------ | ------------- |
| ☀️           | Clear Sky     |
| 🌤           | Mainly Clear  |
| ⛅            | Partly Cloudy |
| ☁️           | Overcast      |
| 🌧           | Rain          |
| ⛈            | Thunderstorm  |

The node also formats the final Telegram message.

---

## 5. Telegram

Delivers the formatted weather report directly to your Telegram chat.

---

# 📱 Example Output

```
🌤 Daily Weather Report

📍 Cebu City

🌡 Temperature: 29°C
💧 Humidity: 76%
🌬 Wind Speed: 11 km/h
☁️ Weather: ⛅ Partly Cloudy

Have a wonderful day!

🤖 Generated automatically with n8n.
```

---

# 📸 Workflow Screenshot

The repository includes a screenshot of the workflow inside the **workflow-image** folder.

---

# 💡 Use Cases

* Daily weather updates
* Morning notifications
* Travel planning
* Outdoor activity planning
* Learning API integration
* Learning workflow automation with n8n
* Portfolio project

---

# 📈 Future Improvements

* Support multiple cities
* 7-day weather forecast
* Rain and storm alerts
* Google Sheets weather history
* Email notifications
* Discord notifications
* AI-generated weather summaries
* Weather charts and analytics

---

# 📚 What I Learned

Building this project improved my understanding of:

* Workflow Automation
* n8n Fundamentals
* REST API Integration
* HTTP Requests
* JSON Data Processing
* JavaScript in n8n
* Telegram Bot Integration
* Scheduled Automations
* Data Transformation

---

# 🏷 Skills Demonstrated

* n8n
* Workflow Automation
* REST APIs
* HTTP Request
* JavaScript
* JSON Parsing
* Data Transformation
* Telegram Bot API
* API Integration
* No-Code / Low-Code Development

---

# 🚀 Getting Started

## Prerequisites

* n8n installed locally or self-hosted
* Telegram Bot Token
* Telegram Chat ID

## Import Workflow

1. Download **Daily Weather Report to Telegram.json**
2. Open n8n.
3. Click **Import Workflow**.
4. Configure your Telegram credentials.
5. Activate the workflow.

---

# 📄 License

This project is licensed under the **MIT License**.

---

## ⭐ Support

If you found this project useful, consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and supports my learning journey in workflow automation.
