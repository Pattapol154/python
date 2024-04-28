## For Loop
**Looping Over a List**  
```python
fruits = ["apple", "banana", "orange"]

for fruit in fruits:
    print(fruit)
```  
**Looping Over a Range**  
```python
# Looping over a range of numbers
for i in range(5):  # i goes from 0 to 4
    print(i)

# Looping with a specific start, stop, and step
for i in range(1, 10, 2):  # i goes from 1 to 9 with a step of 2
    print(i)  # Output: 1, 3, 5, 7, 9
```  
**Looping Over a Dictionary**  
```python
person = {"name": "Alice", "age": 30, "city": "New York"}

# Looping over dictionary keys
for key in person:
    print(key, person[key])  # Output: name Alice, age 30, city New York

# Looping over dictionary items (key-value pairs)
for key, value in person.items():
    print(f"{key}: {value}")  # Same output as above
```  
**Nested for Loops**  
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9],
]

# Looping over a matrix
for row in matrix:
    for value in row:
        print(value, end=" ")  # Output: 1 2 3 4 5 6 7 8 9
    print()  # New line after each row
```  
**break and continue in for Loops**  
```python
# Breaking out of a loop
for i in range(10):
    if i == 5:
        break  # Exit the loop when i is 5
    print(i)  # Output: 0 1 2 3 4

# Skipping an iteration with continue
for i in range(10):
    if i == 5:
        continue  # Skip when i is 5
    print(i)  # Output: 0 1 2 3 4 6 7 8 9
```  
**Using else with for Loops**  
```python
# Using else to indicate normal loop completion
for i in range(10):
    if i == 5:
        break  # This triggers an early exit
else:
    print("Completed without break.")  # This does not execute

# Without break, else block executes
for i in range(5):
    print(i)
else:
    print("Completed without break.")  # This executes
```  
