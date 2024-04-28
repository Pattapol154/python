## Understanding Oops concepts
**Classes**
```python
class Person:
    # Class constructor (initializes attributes)
    def __init__(self, name, age):
        self.name = name  # Instance attribute
        self.age = age

    # Method to describe the person
    def describe(self):
        return f"{self.name} is {self.age} years old."
```
**Objects (Instances)**
```python
# Create a Person object (instance)
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

# Accessing attributes and calling methods
print(person1.describe())  # Output: Alice is 30 years old.
print(person2.name)  # Output: Bob
```  
**Encapsulation**  
```python
class BankAccount:
    def __init__(self, balance):
        self._balance = balance  # Conventionally private (underscore)

    # Getter for balance
    def get_balance(self):
        return self._balance

    # Setter for balance
    def deposit(self, amount):
        if amount > 0:
            self._balance += amount

# Using encapsulation
account = BankAccount(100)
print(account.get_balance())  # Output: 100
account.deposit(50)
print(account.get_balance())  # Output: 150
```
**Inheritance** 
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "Some generic animal sound"

# Dog inherits from Animal
class Dog(Animal):
    def speak(self):
        return "Woof!"

dog = Dog("Buddy")
print(dog.speak())  # Output: Woof!
```
**Polymorphism** 
```python
class Cat(Animal):
    def speak(self):
        return "Meow!"

animals = [Dog("Buddy"), Cat("Whiskers")]

# Polymorphic behavior
for animal in animals:
    print(f"{animal.name} says: {animal.speak()}")
# Output:
# Buddy says: Woof!
# Whiskers says: Meow!
```
**Abstraction** 
```python
from abc import ABC, abstractmethod

# Abstract base class
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

# Concrete class implementing the abstract method
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        import math
        return math.pi * self.radius ** 2

circle = Circle(5)
print(circle.area())  # Output: 78.54 (approx.)
```
