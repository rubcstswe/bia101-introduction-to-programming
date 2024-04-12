# Functions

In Python, a function is a block of reusable code that performs a specific task. 

Functions are designed to take input(s) in the form of arguments, perform some operations or calculations on those inputs, and optionally return a result. 

Functions are essential for modular programming, code reusability, and organizing code into logical units.

The objective behind function is that you define a function once and then you can call it multiple times without having to rewrite the code each time.

**Python Code Examples of Functions:**

```python
# =======================================
# Defining a function
def greet():
    print("Hello!")

# If you do not write the code below, the function will not be executed (it is not called)
greet()  # Output: Hello!

# =======================================
# Function with arguments: You want to pass data while calling to the function
def greet(name): # The variable `name`'s value will be `Alice` when the function is called
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!

# =======================================
# Function with return value
def add(a, b):
    sum = a + b
    return sum # the vale of `sum` is returned to whereever the function was called from

# The function returns a value which is captured/stored in an another variable
result = add(3, 5) # Pass the values 3, 5 to the function called "add"
print(result)  # Output: 8

# =======================================
# Function with default arguments
# If you do not pass any value to the function, the default value `Human` will be used
# If you pass a value to the function, that value will be used
def greet_person(name="Human"): 
    print(f"Hello, {name}!")

greet_person()  # Output: Hello, Human!
greet_person("Alice")  # Output: Hello, Alice!

# =======================================
# Function with keyword arguments
def greet_person(name="Human", age=0):
    print(f"Hello, {name}! You are {age} years old.")

greet_person()  # Output: Hello, Human! You are 0 years old.
greet_person(age=25, name="Alice")  # Output: Hello, Alice! You are 25 years old.
# In the code above with keyword arguments, the order/sequence of the arguments does not matter

# =======================================
# Function with positional arguments
def greet_person(name, age):
    print(f"Hello, {name}! You are {age} years old.")

# The order/sequence matters here
greet_person("Alice", 25)  # Output: Hello, Alice! You are 25 years old.

# =======================================
# Function with nested functions
# Python allows you to define functions inside other functions
def outer_function():
    def inner_function():
        print("Inside inner function")
    print("Inside outer function")
    inner_function()

outer_function()
# Output:
# Inside outer function
# Inside inner function
```