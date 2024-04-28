## While Loop
**Example: Basic while Loop**  
```python
counter = 1

while counter <= 5:
    print(counter)
    counter += 1  # Increment the counter to avoid infinite loop
```  
**Example: Looping with User Input**  
```python
response = ""

while response.lower() not in ["yes", "no"]:
    response = input("Do you want to continue? (yes/no): ")

print(f"You answered: {response}")
```  
**Example: Accumulating Results**  
```python
n = 10
sum_total = 0
counter = 1

while counter <= n:
    sum_total += counter
    counter += 1

print(f"The sum of numbers from 1 to {n} is {sum_total}")
```  
**break Statement**  
```python
while True:
    command = input("Enter a command (type 'exit' to quit): ")
    if command.lower() == "exit":
        break  # Exit the loop
    print(f"You entered: {command}")
```  
**continue Statement**  
```python
counter = 0

while counter < 10:
    counter += 1
    if counter % 2 == 0:  # Skip even numbers
        continue  # Move to the next iteration
    print(counter)  # This prints only odd numbers
```  
**Infinite Loops**  
```python
# Example of an infinite loop
# This loop will continue indefinitely because the condition is always True
while True:
    print("This will run forever, unless there's a break or exit condition.")
    # To exit, you can use 'break' or some external condition (like a keyboard interrupt)
```  
