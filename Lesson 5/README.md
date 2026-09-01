## 🚀 Usage
```python
import requests

url = "https://raw.githubusercontent.com/daniel-nguyen123/INFO450/refs/heads/main/Lesson%205/soccer.json"
response = requests.get(url)
response.status_code          # check the HTTP status
response.raise_for_status()   # raise an error if the request failed

data = response.json()        # parse JSON response into a dict
data.keys()                   # inspect top-level keys
data['matches'][64]           # view a specific match record
```

## 🔍 What This Does
1. Sends a GET request to the raw JSON file on GitHub
2. Verifies the request succeeded (`status_code`, `raise_for_status()`)
3. Parses the JSON response into a Python dictionary
4. Inspects the dictionary's structure (`data.keys()`)
5. Accesses an individual match record from the `matches` list (index 64)

## 📌 Notes
- `raise_for_status()` will throw an `HTTPError` if the request fails (e.g., 404), which is useful for catching broken links early.
- `data['matches']` is a list, so individual matches are accessed by index.

## 📬 Contact
[Your Name] — INFO 450
