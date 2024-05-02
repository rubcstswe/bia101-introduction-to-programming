# Why Object Oriented Programming

Till now, you have been working with functions and data structures like lists and dictionaries, the next step is to understand Object-Oriented Programming (OOP). 

OOP is a programming paradigm that revolves around the concept of objects, which are instances of classes.


In OOP: you write functions that take **inputs and produce outputs.**

These functions operate on data structures like lists and dictionaries.

However, in OOP, you create objects that encapsulate both **data** (attributes) and **behavior** (methods) within a single unit.

## Scenario:

Imagine you are building a program that deals with Car ownership.

How would you represent a car in your program using just functions and data structures?

You could use a dictionary to represent a car:

```python
car = {
    "make": "Toyota",
    "model": "Corolla",
    "year": 2019,
    "color": "Red",
    "mileage": 5000
}
```

You could also write functions that operate on this dictionary:

```python
def drive(car, miles):
    car["mileage"] += miles

def paint(car, color):
    car["color"] = color

def sell(car):
    print(f"Sold the {car['make']} {car['model']} for ${car['price']}")
```

This approach works, but it has some limitations:
- The functions are separate from the data structure, which can make the **code harder to understand and maintain**.

**Using OOP Concepts:**

In OOP, you would define a `Car` class that encapsulates both the data and behavior of a car:

```python
class Car:
    def __init__(self, make, model, year, color, mileage):
        self.make = make
        self.model = model
        self.year = year
        self.color = color
        self.mileage = mileage

    def drive(self, miles):
        self.mileage += miles

    def paint(self, color):
        self.color = color

    def sell(self, price):
        print(f"Sold the {self.make} {self.model} for ${price}")
```

You can then create instances of the `Car` class and call its methods:

```python
my_car = Car("Toyota", "Corolla", 2019, "Red", 5000)
my_car.drive(100)
my_car.paint("Blue")
my_car.sell(15000)
```

You can also create multiple instances of the `Car` class, each with **its own data and behavior**:

```python
# create multiple instances of the Car class --> Car Objects
my_car = Car("Toyota", "Corolla", 2019, "Red", 5000)
friends_car = Car("Honda", "Civic", 2020, "Black", 3000)
car_to_sell = Car("Ford", "Fiesta", 2018, "White", 10000)
```

In the code above you can see that the `Car` class encapsulates both the data and behavior of a car, making the **code easier to understand and maintain**.

