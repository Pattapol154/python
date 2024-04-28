## Input From Keyboard  
**Basic Keyboard Input**  
```python
# Getting a simple input from the user
name = input("What is your name? ")
print(f"Hello, {name}!")
```  
**Converting Input to Other Data Types**  
```python
# Converting string input to integer
age_str = input("How old are you? ")
age = int(age_str)  # Convert to integer
print(f"You are {age} years old.")
```  
**Error Handling with Input**  
```python
# Handling conversion errors
try:
    age_str = input("How old are you? ")
    age = int(age_str)
    print(f"You are {age} years old.")
except ValueError:
    print("Invalid age. Please enter a number.")
``` 
**Multiple Inputs**  
```python
# Collecting multiple inputs separately
first_name = input("Enter your first name: ")
last_name = input("Enter your last name: ")
print(f"Your full name is {first_name} {last_name}.")

# Collecting multiple inputs in one line
# Example: enter data separated by a space
data = input("Enter your age, height, and weight (separated by spaces): ")
age, height, weight = map(int, data.split())  # Splitting and converting to integers
print(f"Age: {age}, Height: {height}, Weight: {weight}")
``` 
**Handling Conditional Logic with Input**  
```python
# Using input to drive conditional logic
response = input("Do you like Python? (yes/no): ")

if response.lower() == "yes":
    print("Great! Python is awesome.")
else:
    print("Oh no! Maybe you haven't found the right project yet.")
``` 
**Ending Input with a Specific Character**  
```python
# Collecting multiple lines of input until a specific character is entered
lines = []
print("Enter text (type 'STOP' to end):")
while True:
    line = input()
    if line.upper() == "STOP":
        break
    lines.append(line)

print("You entered:")
print("\n".join(lines))
``` 
