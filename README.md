# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
~~~
from abc import ABC, abstractmethod
import math

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length=5, breadth=10):
        self.length = length
        self.breadth = breadth
    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    def __init__(self, radius=7):
        self.radius = radius
    def calculate_area(self):
        return math.pi * self.radius**2

rect = Rectangle()
circ = Circle()

print("Output:")
print("Rectangle area:", rect.calculate_area())
print("Circle area:", circ.calculate_area())

Result = (rect.calculate_area(), circ.calculate_area())


~~~
## Output
<img width="1617" height="987" alt="Screenshot 2025-10-20 162624" src="https://github.com/user-attachments/assets/6ca42f19-49e5-4e89-bfec-0821221dbfea" />

## Result
The program successfully creates an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.
# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
~~~
class Rectangle:
    def __init__(self, length=5, breadth=10):
        self.__length = length
        self.__breadth = breadth
        print("Output:")
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)

rect = Rectangle()
Result = (rect._Rectangle__length, rect._Rectangle__breadth)

~~~
## Output
<img width="1568" height="991" alt="Screenshot 2025-10-20 162938" src="https://github.com/user-attachments/assets/8adb008d-972c-4ba7-b9c8-a69c6c9d45f5" />

## Result
The program successfully implements Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.
