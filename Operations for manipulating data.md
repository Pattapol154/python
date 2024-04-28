## Operations for manipulating data ##
**Arithmetic Operations**
```python
a = 10
b = 3
print(a + b)  # Addition
print(a - b)  # Subtraction
print(a * b)  # Multiplication
print(a / b)  # Division (float result)
```
**String Manipulation**  
```python
s = "hello world"
print(s.upper())  # Converts to uppercase
print(s.lower())  # Converts to lowercase
print(s.replace("world", "Python"))  # Replaces part of the string
print(s.split())  # Splits a string into a list of words
```
**List Manipulation**   
```python
my_list = [1, 2, 3, 4, 5]
my_list.append(6)  # Adds an item at the end
my_list.pop()  # Removes and returns the last item
my_list.insert(1, "a")  # Inserts at a specific index
my_list.extend([7, 8, 9])  # Adds multiple items
print(my_list)  # Output: [1, 'a', 2, 3, 4, 5, 6, 7, 8, 9]

# List comprehensions
squared = [x**2 for x in my_list if isinstance(x, int)]
print(squared)  # Output: [1, 4, 9, 16, 25, 36, 49, 64, 81]
```
**Dictionary Manipulation**   
```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}
print(my_dict["name"])  # Accesses a value by key
my_dict["age"] = 31  # Updates a value
my_dict["country"] = "USA"  # Adds a new key-value pair
del my_dict["city"]  # Deletes a key-value pair
print(my_dict)  # Output: {'name': 'Alice', 'age': 31, 'country': 'USA'}
```
**DataFrame Manipulation with Pandas** 
```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [30, 25, 35],
    "City": ["New York", "Los Angeles", "Chicago"]
})

# Selecting a column
print(df["Name"])  # Output: column 'Name'

# Selecting rows based on a condition
print(df[df["Age"] > 25])

# Adding a new column
df["Country"] = ["USA", "USA", "USA"]

# Grouping and aggregating
grouped = df.groupby("City").mean()  # Gets the mean age per city

# Dropping a column
df.drop("Country", axis=1, inplace=True)

# Resetting index
df.reset_index(drop=True, inplace=True)
```
