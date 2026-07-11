# 🌤 Daily Weather Report to Telegram — n8n Automation

![n8n](https://img.shields.io/badge/n8n-Automation-orange)
![API](https://img.shields.io/badge/API-Open--Meteo-blue)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-yellow)
![Telegram](https://img.shields.io/badge/Notification-Telegram-blue)
![License](https://img.shields.io/badge/license-MIT-green)

An automated weather notification workflow built using **n8n**, **Open-Meteo API**, **JavaScript**, and **Telegram Bot API**.

This system automatically retrieves real-time weather information, processes weather data, converts weather codes into readable conditions, generates a formatted weather report, and delivers daily updates directly through Telegram.

**Stack:**  
n8n · Open-Meteo API · HTTP Request · JavaScript · Telegram Bot · REST API Automation


---

# 🎯 Project Overview


## Problem

Checking weather conditions manually every day can be inconvenient and time-consuming.

Common challenges include:

- Manually opening weather applications
- Forgetting daily weather checks
- Difficulty accessing weather information quickly
- Lack of automated notifications
- Repetitive manual tasks


Common scenarios:

- Daily commute preparation
- Travel planning
- Outdoor activities
- Personal productivity


---

## Solution

This project creates an automated weather notification system by:


1. Running a scheduled workflow
2. Requesting weather data from Open-Meteo API
3. Extracting important weather information
4. Transforming raw API responses
5. Converting weather codes into readable conditions
6. Formatting a weather report
7. Sending updates through Telegram


The workflow acts as a personal AI-free weather assistant that automatically delivers daily weather information.


---

# ✨ Features


## Weather Data Processing

✅ Real-time weather retrieval  
✅ Temperature monitoring  
✅ Humidity tracking  
✅ Wind speed monitoring  
✅ Weather condition detection  


## Automation

✅ Scheduled workflow execution  
✅ Fully automated weather reports  
✅ No manual checking required  
✅ Free API integration  


## Data Transformation

✅ JSON data processing  
✅ Weather code conversion  
✅ Custom message formatting  
✅ JavaScript data manipulation  


## Notifications

✅ Telegram weather alerts  
✅ Readable weather reports  
✅ Instant delivery  


---

# 🗺️ System Architecture


```mermaid
flowchart TD

A["⏰ Schedule Trigger"]

--> B["🌐 Open-Meteo API"]


B --> C["📥 HTTP Request"]


C --> D["⚙️ Edit Fields"]


D --> E["💻 JavaScript Code Node"]


E --> F["📱 Telegram Notification"]

````

---

# 🏗️ Workflow Implementation

# Workflow 1: Daily Weather Notification Pipeline

## Node 1 — Schedule Trigger

### Purpose

Automatically starts the weather workflow at a scheduled time.

Example Configuration:

```text
Trigger:

Every Day

Time:

7:00 AM
```

Execution Flow:

```text
Scheduled Time

      ↓

Request Weather Data

      ↓

Generate Weather Report
```

---

# Node 2 — HTTP Request

### Purpose

Retrieves current weather information from the Open-Meteo API.

Configuration:

```text
Method:

GET


Authentication:

None
```

API Example:

```text
Open-Meteo Weather API
```

Captured Data:

| Field        | Description                  |
| ------------ | ---------------------------- |
| Temperature  | Current temperature          |
| Humidity     | Relative humidity            |
| Wind Speed   | Current wind speed           |
| Weather Code | Weather condition identifier |

Example API Response:

```json
{
"temperature":29,

"humidity":76,

"windspeed":11,

"weathercode":2
}
```

---

# Node 3 — Edit Fields (Set)

### Purpose

Extract only the required weather information from the API response.

Extracted Fields:

| Field        | Description            |
| ------------ | ---------------------- |
| Temperature  | Current temperature    |
| Humidity     | Air moisture level     |
| Wind Speed   | Wind measurement       |
| Weather Code | Weather condition code |

Processing:

```text
Raw API Response

        ↓

Selected Weather Data

        ↓

JavaScript Processing
```

---

# Node 4 — Code Node (JavaScript)

### Purpose

Transform weather data into a user-friendly Telegram message.

Functions:

* Convert weather codes
* Add weather emojis
* Format final report
* Prepare Telegram message

Example Weather Mapping:

| Code  | Condition       |
| ----- | --------------- |
| 0     | ☀️ Clear Sky    |
| 1-3   | ⛅ Partly Cloudy |
| 45-48 | 🌫 Fog          |
| 51-67 | 🌧 Rain         |
| 80-82 | 🌦 Rain Showers |
| 95    | ⛈ Thunderstorm  |

Example Output:

```javascript
{
"message":

"🌤 Daily Weather Report

📍 Cebu City

🌡 Temperature: 29°C

💧 Humidity: 76%

🌬 Wind Speed: 11 km/h

☁️ Weather: Partly Cloudy"
}
```

---

# Node 5 — Telegram Notification

### Purpose

Send the generated weather report directly to Telegram.

Example:

```text
🌤 Daily Weather Report


📍 Cebu City


🌡 Temperature:

29°C


💧 Humidity:

76%


🌬 Wind Speed:

11 km/h


☁️ Weather:

⛅ Partly Cloudy


Have a wonderful day!


🤖 Generated automatically using n8n.
```

---

# 🔐 Credentials Required

| Service          | Purpose                    |
| ---------------- | -------------------------- |
| Telegram Bot API | Send weather notifications |
| n8n Instance     | Workflow execution         |

Note:

Open-Meteo API does not require an API key.

---

# ⚙️ Setup Guide

## 1. Configure Schedule Trigger

Set your preferred notification schedule.

Example:

```text
Every Day

07:00 AM
```

---

## 2. Configure Open-Meteo API

Add weather API endpoint.

Required:

```text
Location Coordinates

API Endpoint
```

Example:

```text
Latitude:

10.3157


Longitude:

123.8854
```

---

## 3. Configure JavaScript Code Node

Add weather code conversion logic.

Required:

```text
Weather Mapping

Message Formatting
```

---

## 4. Configure Telegram Bot

Steps:

1. Create bot using BotFather
2. Copy bot token
3. Add Telegram credentials in n8n
4. Configure chat ID

---

## 5. Import Workflow

Import:

```text
workflow.json
```

Configure:

* Location coordinates
* Telegram credentials
* Schedule time

Activate workflow.

---

# 🧪 Testing Checklist

| Test Case            | Expected Result         |
| -------------------- | ----------------------- |
| Schedule executes    | Workflow starts         |
| API request runs     | Weather data retrieved  |
| Edit Fields executes | Required data extracted |
| Code Node runs       | Message formatted       |
| Telegram executes    | Weather report received |

---

# 📁 Repository Structure

```text
Daily-Weather-Report-to-Telegram-n8n/

│
├── README.md
│
├── workflow.json
│
├── screenshots/
│
│   ├── workflow.png
│   ├── schedule-trigger.png
│   ├── http-request.png
│   ├── edit-fields.png
│   ├── code-node.png
│   ├── telegram-output.png
│   └── execution-result.png
│
└── LICENSE
```

---

# 📸 Screenshots

Recommended screenshots:

* Complete workflow
* Schedule Trigger configuration
* HTTP Request API response
* Edit Fields output
* JavaScript Code Node
* Telegram weather message
* Workflow execution result

---

# 🚀 Future Improvements

| Feature             | Implementation                    |
| ------------------- | --------------------------------- |
| Multiple Cities     | Monitor different locations       |
| Weather Forecast    | Add 7-day forecast                |
| Storm Alerts        | Detect severe weather             |
| Weather History     | Save data to Google Sheets        |
| AI Weather Summary  | Generate natural language reports |
| Email Notifications | Send weather emails               |
| Discord Integration | Add community alerts              |
| Analytics Dashboard | Visualize weather trends          |

---

# 🎓 Skills Applied

## Automation

* n8n Workflow Automation
* Scheduled workflows
* Automated notifications

## APIs

* REST API Integration
* HTTP Requests
* JSON API Processing

## Programming

* JavaScript
* Data transformation
* Conditional logic
* Message formatting

## Integrations

* Open-Meteo API
* Telegram Bot API

## Business Automation

* Productivity automation
* Information delivery systems
* Real-time notification workflows

---

# 📚 Learning Objectives

This project demonstrates:

* Building API-powered automation workflows
* Working with external REST APIs
* Processing JSON responses
* Creating scheduled automation systems
* Integrating Telegram notifications
* Transforming raw data into useful information

---

# 🙌 Acknowledgements

* n8n
* Open-Meteo API
* Telegram Bot API

---

# 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student
Cebu Technological University (CTU)

GitHub:

[https://github.com/belioautomation](https://github.com/belioautomation)

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical automation solutions using **n8n, REST APIs, JavaScript, and workflow automation**.

---

# 📄 License

MIT License

```
```
