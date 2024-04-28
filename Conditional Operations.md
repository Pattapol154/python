## Conditional Operations
**Basic if Statement**
```python
x = 10
if x > 5:
    print("x is greater than 5")
```  
**if-else Statement**  
```python
x = 3
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```  
**if-elif-else Statement** 
```python
x = 5
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is exactly 5")
else:
    print("x is less than 5")
```  
**Nested if Statements**  
```python
x = 8
if x > 5:
    if x > 7:
        print("x is greater than 7")
    else:
        print("x is greater than 5 but not greater than 7")
else:
    print("x is not greater than 5")
```  
**Ternary Operator (Conditional Expression)**     
```python
x = 3
result = "greater than 5" if x > 5 else "not greater than 5"
print(result)
```  
**and, or, and not Operators**   
```python
x = 6
y = 10

if x > 5 and y > 5:
    print("Both x and y are greater than 5")

if x > 5 or y > 5:
    print("Either x or y is greater than 5")

if not x > 5:
    print("x is not greater than 5")
```  
