## Try Except
**try Block**
```python
try:
    result = 10 / 0  # This will raise a ZeroDivisionError
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
```
**except Block**   
- Catching Specific Exceptions
```python
try:
    my_list = [1, 2, 3]
    print(my_list[5])  # IndexError
except IndexError:
    print("Error: Index is out of range.")
```
- Catching Multiple Exceptions  
```python
try:
    number = int("abc")  # This will raise a ValueError
except (ValueError, TypeError):
    print("Error: Invalid value or type.")
```
- Catching Any Exception
 ```python
try:
    unknown_variable  # This will raise a NameError
except Exception as e:
    print(f"An error occurred: {e}")  # Outputs the exception message
```
**finally Block**
 ```python
try:
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("Error: File not found.")
finally:
    if 'file' in locals() and not file.closed:
        file.close()  # Ensure the file is closed
        print("File closed.")
```
**else Block**
 ```python
try:
    number = int("10")  # No exception here
except ValueError:
    print("Error: Cannot convert to integer.")
else:
    print("Conversion successful.")  # This runs because there was no exception
```
