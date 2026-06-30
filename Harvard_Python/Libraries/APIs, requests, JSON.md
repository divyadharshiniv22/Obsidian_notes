
# What is API, requests, and JSON in Python?

These three are connected and heavily used in:


- backend development
- AI/ML
- web applications
- data engineering
- automation
- enterprise software

---

# 1. What is an API?

API stands for:

```
Application Programming Interface
```

---

# Simple Meaning

An API allows two applications to communicate with each other.

---

# Real-Life Analogy

```
API = waiter in restaurant
```

### Example

- You → customer
- Kitchen → server/database
- Waiter → API

You tell waiter what you want.

Waiter takes request to kitchen and brings response back.

---

# Real Example

Suppose weather app shows Chennai weather.

How?

```
Weather App    
↓Weather API   
↓Weather Server
```

The API sends request and receives weather data.

---

# APIs Are Used For

|Use Case|Example|
|---|---|
|Weather apps|Weather API|
|Payment systems|Razorpay API|
|Maps|Google Maps API|
|AI tools|OpenAI API|
|Social media login|Google/Facebook API|
|Backend communication|microservices|

---

# API Request and Response

## Request

Application asks for data.

Example:

```
Give user details
```

---

## Response

Server sends data back.

Example:

```
User name, email, age
```

---

# Common HTTP Methods

|Method|Purpose|
|---|---|
|GET|Fetch data|
|POST|Send data|
|PUT|Update data|
|DELETE|Delete data|

---

# Example

```
GET /users
```

means:

```
Fetch all users
```

---

# 2. What is `requests` in Python?

`requests` is a Python library used to call APIs.

---

# Why We Use `requests`

Without requests:

❌ API communication becomes difficult

With requests:

✅ easy API calls

---

# Install requests

```
pip install requests
```

---

# Import requests

```
import requests
```

---

# Example — GET Request

```
import requestsresponse = requests.get("https://api.github.com")print(response.status_code)
```

---

# Explanation

## Step 1

```
requests.get()
```

sends GET request to API.

---

## Step 2

```
response.status_code
```

shows whether request succeeded.

---

# Common Status Codes

|Code|Meaning|
|---|---|
|200|Success|
|404|Not found|
|500|Server error|
|401|Unauthorized|

---

# Example Output

```
200
```

means request successful.

---

# 3. What is JSON?

JSON stands for:

```
JavaScript Object Notation
```

---

# Simple Meaning

JSON is a data format used to exchange information between applications.

Most APIs send data in JSON format.

---

# Example JSON

```
{    "name": "Divya",    "age": 25,    "city": "Chennai"}
```

---

# JSON Looks Like Python Dictionary

```
{    "name": "Divya",    "age": 25}
```

---

# Why JSON Is Used

Because JSON is:

✅ lightweight  
✅ readable  
✅ language-independent  
✅ easy to transfer over internet

---

# API + requests + JSON Together

This is the most important part.

---

# Full Example

```
import requestsresponse = requests.get("https://api.github.com")data = response.json()print(data)
```

---

# Step-by-Step Flow

---

# Step 1 — Send API Request

```
response = requests.get("https://api.github.com")
```

Python sends request to GitHub API.

---

# Step 2 — API Sends JSON Response

Server returns data like:

```
{    "current_user_url": "https://api.github.com/user"}
```

---

# Step 3 — Convert JSON to Python Dictionary

```
data = response.json()
```

Now JSON becomes Python dictionary.

---

# Step 4 — Access Data

```
print(data["current_user_url"])
```

---

# Real Flow Diagram

```
Python Program      ↓requests library      ↓API call      ↓Server      ↓JSON response      ↓Python dictionary
```

---

# Example — Weather API

```
import requestsurl = "https://api.weatherapi.com"response = requests.get(url)data = response.json()print(data)
```

---

# Example — POST Request

POST is used to send data.

```
import requestsuser = {    "name": "Divya",    "age": 25}response = requests.post(    "https://example.com/api",    json=user)print(response.status_code)
```

---

# Real Job Usage

These concepts are used everywhere.

---

# Backend Development

```
Frontend ↔ API ↔ Database
```

---

# AI/ML

```
LLM APIsOpenAI APIsModel serving
```

---

# Data Engineering

```
Fetch data from APIs
```

---

# Automation

```
Send notificationsIntegrate systems
```

---

# Enterprise Applications

```
Payment APIsBank APIsCRM systems
```

---

# Very Important Interview Understanding

|Concept|Meaning|
|---|---|
|API|communication bridge|
|requests|sends HTTP requests|
|JSON|data format|
|GET|fetch data|
|POST|send data|

---

# Complete Real Example

```
import requestsresponse = requests.get("https://api.github.com")if response.status_code == 200:    data = response.json()    print(data["current_user_url"])else:    print("Request failed")
```

---

# Final Simple Understanding

```
API → service/providerrequests → sends request to APIJSON → format of returned data
```

---

# One-Line Definitions

```
API → allows applications to communicate
```

```
requests → Python library used to call APIs
```

```
JSON → data format used to exchange information
```

**How to get the data in readable form ?**

To get API data in a readable form, we usually use:

```
json.dumps()
```

with:

```
indent
```

---
# Readable Format Method

```
import jsonprint(json.dumps(data, indent=2))
```

---

# Full Example

```
import requestsimport jsonresponse = requests.get(    "https://jsonplaceholder.typicode.com/users")data = response.json()print(json.dumps(data, indent=2))
```


| Method         | Purpose              |
| -------------- | -------------------- |
| `json.dumps()` | Python → JSON string |
| `json.loads()` | JSON string → Python |
