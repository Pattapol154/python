## Convert Data Type  
**Converting to Integer**  
```python
# Convert a string to an integer
num_str = "10"
num = int(num_str)  # Output: 10
print(num, type(num))

# Convert a float to an integer
float_num = 3.6
int_num = int(float_num)  # Output: 3 (truncates decimal part)
print(int_num, type(int_num))
```
**Converting to Float**  
```python
# Convert a string to a float
num_str = "3.14"
float_num = float(num_str)  # Output: 3.14
print(float_num, type(float_num))

# Convert an integer to a float
int_num = 5
float_num = float(int_num)  # Output: 5.0
print(float_num, type(float_num))
```
**Converting to String**  
```python
# Convert an integer to a string
num = 123
str_num = str(num)  # Output: "123"
print(str_num, type(str_num))

# Convert a float to a string
float_num = 3.14
str_float = str(float_num)  # Output: "3.14"
print(str_float, type(str_float))
```
**Converting to List**  
```python
# Convert a string to a list of characters
str_value = "hello"
list_value = list(str_value)  # Output: ['h', 'e', 'l', 'l', 'o']
print(list_value, type(list_value))

# Convert a tuple to a list
tuple_value = (1, 2, 3)
list_value = list(tuple_value)  # Output: [1, 2, 3]
print(list_value, type(list_value))
```
**Converting to Dictionary**   
```python
# Convert a list of tuples to a dictionary
list_of_tuples = [("name", "Alice"), ("age", 30)]
dict_value = dict(list_of_tuples)  # Output: {'name': 'Alice', 'age': 30}
print(dict_value, type(dict_value))
```
**Converting to Tuple**   
```python
# Convert a list to a tuple
list_value = [1, 2, 3]
tuple_value = tuple(list_value)  # Output: (1, 2, 3)
print(tuple_value, type(tuple_value))

# Convert a string to a tuple of characters
str_value = "python"
tuple_value = tuple(str_value)  # Output: ('p', 'y', 't', 'h', 'o', 'n')
print(tuple_value, type(tuple_value))
```
**Converting to Set**   
```python
# Convert a list with duplicates to a set
list_value = [1, 2, 2, 3, 3, 4]
set_value = set(list_value)  # Output: {1, 2, 3, 4}
print(set_value, type(set_value))

# Convert a string to a set of characters
str_value = "hello"
set_value = set(str_value)  # Output: {'h', 'e', 'l', 'o'}
print(set_value, type(set_value))
```
