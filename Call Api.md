## Call Api
**Consuming APIs with Python**  
- Installing the requests Library
```python
pip install requests
```
**Making a Basic API Request**  
```python
import requests

# Sending a GET request to a public API
response = requests.get("https://jsonplaceholder.typicode.com/posts/1")

# Checking if the request was successful
if response.status_code == 200:
    # Parse JSON response
    data = response.json()  # Converts the JSON string into a Python dictionary
    print(data)
else:
    print("Failed to fetch data")
```
- Sending Data with POST   
```python
# Data to send
post_data = {
    "title": "My New Post",
    "body": "This is the content of the post.",
    "userId": 1
}

# Sending a POST request
response = requests.post("https://jsonplaceholder.typicode.com/posts", json=post_data)

if response.status_code == 201:
    # Created successfully
    print("Post created:", response.json())
else:
    print("Failed to create post")
```
- Using Headers and Authentication
```python
# Sending a request with headers
headers = {
    "Authorization": "Bearer YOUR_ACCESS_TOKEN",
    "Content-Type": "application/json"
}

response = requests.get("https://api.example.com/protected", headers=headers)

if response.status_code == 200:
    print("Authorized access:", response.json())
else:
    print("Access denied")
```
**Building Your Own API in Python**  
```python
pip install Flask
```
- Building a Basic Flask API  
```python
from flask import Flask, jsonify

# Create a Flask application
app = Flask(__name__)

# Define a route for the API
@app.route('/api/hello', methods=['GET'])
def hello():
    # Returning JSON data
    return jsonify(message="Hello, World!")

# Start the Flask server
if __name__ == '__main__':
    app.run(debug=True)
```
- Creating a RESTful API with Flask
```python
from flask import Flask, request, jsonify

# Create a Flask application
app = Flask(__name__)

# In-memory data storage (for demonstration purposes)
posts = []

# Define a route for getting all posts
@app.route('/api/posts', methods=['GET'])
def get_posts():
    return jsonify(posts)  # Return the list of posts

# Define a route for creating a new post
@app.route('/api/posts', methods=['POST'])
def create_post():
    # Get data from the request
    new_post = request.json
    posts.append(new_post)
    return jsonify(new_post), 201  # Return the created post with status code 201

# Start the Flask server
if __name__ == '__main__':
    app.run(debug=True)
```  
