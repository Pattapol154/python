## Functions ##
**Defining a Basic Function**
```python
# Function to add two numbers
def add(x, y):
    return x + y

result = add(3, 5)
print(result)  # Output: 8

```  
**Parameters and Arguments**  
```python
# Function with default parameter values
def greet(name="Guest"):
    return f"Hello, {name}!"

# Calling with a specific argument
print(greet("Alice"))  # Output: Hello, Alice!

# Calling without an argument (uses the default value)
print(greet())  # Output: Hello, Guest!
```
**Positional and Keyword Arguments**   
```python
# Function with multiple arguments
def describe_person(name, age, city):
    return f"{name} is {age} years old and lives in {city}."

# Positional arguments
print(describe_person("Alice", 30, "New York"))  # Correct order

# Keyword arguments
print(describe_person(age=30, city="New York", name="Alice"))  # Order doesn't matter
```
**Variable-Length Arguments**   
```python
# Function with *args for variable positional arguments
def sum_numbers(*args):
    return sum(args)

print(sum_numbers(1, 2, 3, 4, 5))  # Output: 15

# Function with **kwargs for variable keyword arguments
def print_details(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_details(name="Alice", age=30, city="New York")
# Output:
# name: Alice
# age: 30
# city: New York
```
**Function Scope and Closures**   
```python
def outer_function(x):
    def inner_function(y):
        return x + y  # 'x' is from the outer scope
    return inner_function

# Create a closure
add_with_5 = outer_function(5)
print(add_with_5(3))  # Output: 8
```
**Lambda Functions (Anonymous Functions)**   
```python
# Lambda to square a number
square = lambda x: x ** 2

print(square(4))  # Output: 16

# Using lambda with map to apply a function to a list
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]
```
**Decorators**    
```python
# A simple decorator that logs function execution
def log_decorator(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args} and {kwargs}")
        result = func(*args, **kwargs)
        print(f"Finished {func.__name__}")
        return result
    return wrapper

@log_decorator
def add(x, y):
    return x + y

print(add(3, 5))
# Output:
# Calling add with (3, 5) and {}
# Finished add
# 8
```

