## Api example
**Install the requests Library**  
```python
pip install requests
```
**Make a Request to the APOD API**  
```python
import requests

# Your NASA API key
api_key = "YOUR_NASA_API_KEY"  # Replace with your actual API key

# Base URL for the APOD API
url = "https://api.nasa.gov/planetary/apod"

# Parameters for the request (with your API key)
params = {
    "api_key": api_key,  # Required parameter
    "hd": "True"  # Optional: request the high-definition image
}

# Making a GET request to the APOD API
response = requests.get(url, params=params)

# Check if the request was successful
if response.status_code == 200:
    # Get the JSON response data
    apod_data = response.json()
    
    # Display the relevant information
    print("Title:", apod_data["title"])
    print("Date:", apod_data["date"])
    print("Explanation:", apod_data["explanation"])
    print("Image URL:", apod_data["url"])  # URL to the image
else:
    print("Failed to retrieve data:", response.status_code)
```
**Additional Features**
```python
# Example: Fetching APOD from a specific date
params = {
    "api_key": api_key,
    "date": "2021-10-01",  # Example date
    "hd": "True"
}

response = requests.get(url, params=params)

if response.status_code == 200:
    apod_data = response.json()
    print("Title:", apod_data["title"])
    print("Date:", apod_data["date"])
    print("Explanation:", apod_data["explanation"])
    print("Image URL:", apod_data["url"]) 
else:
    print("Failed to retrieve data:", response.status_code)
```  
