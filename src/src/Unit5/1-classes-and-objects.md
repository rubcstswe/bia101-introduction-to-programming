# Classes and Objects

## Classes
a class is a **blueprint or a template for creating objects**. 

It defines the **properties** (attributes) and **behaviors** (methods) that the objects of that class will have.

Assuming you want to represent a dog in your program, a dog will have:
- **Properties**: name, breed, age, color
- **Behaviors**: bark, wag tail, eat, sleep

Representing the above information in python code:

```python
class Dog:
    # This function runs when a new Dog object is created
    # When a new object is created from this class, the __init__ function is called
    def __init__(self, name, breed, age, color):
        # self is a reference(pointer) to the object itself
        self.name = name # name is an attribute of the Dog class
        self.breed = breed # breed is an attribute of the Dog class
        self.age = age # age attribute of the Dog class
        self.color = color # color attribute of the Dog class

    # Defining a behaviour for the Dog class
    def bark(self):
        print(f"{self.name} is barking")

    # Defining a behaviour for the Dog class
    def wag_tail(self):
        print(f"{self.name} is wagging its tail")

    # Defining a behaviour for the Dog class
    def eat(self):
        print(f"{self.name} is eating")

    # Defining a behaviour for the Dog class
    def sleep(self):
        print(f"{self.name} is sleeping")
```

In simple words: 
- **Variables** that store data are called **attributes**.
- **Functions** that perform actions are called **methods**.

> **NOTE:** The `self` parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.
> For now, think of it as a rule to always include `self` as the first parameter in the method definition.

## Objects

A class definition is just a blueprint for creating objects.\
You still haven't created any dogs yet.\

To create an object, you have to call the class like a function.

```python
# Creating a Dog object
dog1 = Dog("Buddy", "Golden Retriever", 3, "Golden")
```

In the code above, you are create a `dog1` variable that stores a `Dog` object.
- The `dog1` variable is an **instance** of the `Dog` class.
- When you create the dog object, the `__init__` function is called with the arguments you passed.
- In the example above: `name="Buddy"`, `breed="Golden Retriever"`, `age=3`, `color="Golden"`

# Exercise: 

The scenario given to you is to create a Cat program that has multiple objects of the Cat class.\

The cats can:
1. Sleep
2. Eat
3. Meow

The cats have the following facts about themselves:
1. Name
2. Breed
3. Age
4. Color

**Thought Process:**

What are the attributes and behaviour of the cat to be represented in the class?
- Attributes: Name, Breed, Age, Color
- Methods: Sleep, Eat, Meow

Since Attributes are the properties of the object, they should be assigned in the `__init__` function.

```python
# Setting up attributes for the Cat
class Cat:
    def __init__(self, name, breed, age, color):
        self.name = name
        self.breed = breed
        self.age = age
        self.color = color
```

Since behaviours are just functions inside the class, they should be defined as methods.

```python
# Setting up behaviours for the Cat
def sleep(self):
    print(f"{self.name} is sleeping")

def eat(self):
    print(f"{self.name} is eating")

def meow(self):
    print(f"{self.name} is meowing")
```

Combining the attributes and behaviours in the class:

```python
class Cat:
    # Setting up attributes
    def __init__(self, name, breed, age, color):
        self.name = name
        self.breed = breed
        self.age = age
        self.color = color
    
    # Setting up behaviours
    def sleep(self):
        print(f"{self.name} is sleeping")
    
    def eat(self):
        print(f"{self.name} is eating")
    
    def meow(self):
        print(f"{self.name} is meowing")
```

Creating objects of the Cat class:

```python
# Create multiple Cat objects from the same class
cat1 = Cat("Whiskers", "Siamese", 2, "White")
cat2 = Cat("Mittens", "Persian", 4, "Grey")
cat3 = Cat("Fluffy", "Bhutanese", 1, "White")
cat4 = Cat("Snowball", "Siamese", 1, "White")
cat5 = Cat("Garfield", "Persian", 3, "Orange")

# Using the objects
cat1.sleep()
cat2.eat()
cat3.meow()

cat.name # This is how you access the attributes of the object

# array to store the cats 
cat_storage = [cat1, cat2, cat3, cat4, cat5]

# loop through the cat storage and see if cats can vote
# their voting age is more than 2
for cat in cat_storage:
    cat_age = cat.age
    if cat_age > 2:
        print(f"{cat.name} can vote")
    else:
        print(f"{cat.name} cannot vote")
```