## File Handling ##  
**Opening Files**  
- 'r': Read mode
- 'w': Write mode (creates a new file or overwrites if the file already exists)
- 'a': Append mode (adds content to the end of the file)
- 'rb', 'wb', 'ab': Binary modes for reading, writing, or appending in binary format  
```python
# Open a file in read mode
file = open("example.txt", 'r')

# Open a file in write mode
file = open("example.txt", 'w')  # Creates if not exists, overwrites if exists

# Open a file in append mode
file = open("example.txt", 'a')  # Adds to the existing file
```
**Reading Files**  
- read(): Reads the entire file  
- readline(): Reads one line at a time  
- readlines(): Reads all lines into a list   
```python
# Reading a file entirely
file = open("example.txt", 'r')
content = file.read()  # Reads all content
print(content)
file.close()  # Always close the file after you're done

# Reading line by line
file = open("example.txt", 'r')
line = file.readline()  # Reads the first line
while line:
    print(line, end='')  # Print each line
    line = file.readline()  # Read the next line
file.close()

# Reading all lines into a list
file = open("example.txt", 'r')
lines = file.readlines()  # Returns a list of lines
print(lines)
file.close()
```
**Writing Files**   
```python
# Write to a file (overwrites if it exists)
file = open("example.txt", 'w')
file.write("Hello, World!\n")
file.write("This is a new line.\n")
file.close()

# Append to a file
file = open("example.txt", 'a')
file.write("This is appended content.\n")
file.close()
```
**Using with for File Handling**   
```python
# Using 'with' for reading
with open("example.txt", 'r') as file:
    content = file.read()
    print(content)  # File is automatically closed when exiting the 'with' block

# Using 'with' for writing
with open("example.txt", 'w') as file:
    file.write("New content\n")

# Using 'with' for appending
with open("example.txt", 'a') as file:
    file.write("Appending content.\n")
```
**Handling File Errors**   
```python
try:
    with open("nonexistent_file.txt", 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("File not found. Please check the file path.")
except IOError:
    print("An error occurred while reading the file.")
```
