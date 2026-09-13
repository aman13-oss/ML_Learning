# Day 17 — API to DataFrame

## 📌 Topics Covered

### 1. API Basics
- What is an API?
- How APIs provide data
- Understanding API endpoints
- `requests` library
- `requests.get()`
- Understanding the `response` object
- HTTP status codes
- `response.json()`

### 2. JSON → DataFrame

Learned how to convert API JSON data into a Pandas DataFrame.

```python
import pandas as pd
import requests

response = requests.get("API_URL")

data = response.json()

df = pd.DataFrame(data)