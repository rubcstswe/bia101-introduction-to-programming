# Introductory Python

Before diving into writing actual code, it's essential to understand some fundamental programming concepts that are common across most programming languages:

- **Variables**: Variables are used to store data values, such as numbers, strings, or more complex data types, for later use or manipulation.

- **Data Types**: Programming languages support various data types, including integers, floating-point numbers, characters, strings, booleans, and more complex structures like arrays and objects.

- **Control Structures**: These structures allow programs to make decisions and execute different blocks of code based on certain conditions. Examples include if-else statements, loops (for, while), and switch statements.

- **Functions**: Functions are reusable blocks of code that perform specific tasks. They can accept input parameters and return output values, promoting code modularity and reusability.

- **Object-Oriented Programming (OOP)**: Many modern programming languages support object-oriented programming, which revolves around the concept of objects containing data (properties) and code (methods). OOP promotes code organization, reusability, and maintainability.

# Namespace

A namespace is a mapping of names (identifiers) to objects (variables, functions, classes, etc.) in Python. 

It helps to prevent naming conflicts by allowing the same name to be used for different objects in different namespaces. 

For example you cannot use `for` as a variable name because it is a reserved keyword in Python that is used to define a loop.\
Similarly, you cannot use `def` as a variable name because it is a reserved keyword used to define a function.

```python
for = "Hello World" # SyntaxError: can't assign to keyword
print(for) # cannot execute
def = 0 # error as def word is reserved
```

# Identifiers

An identifier is a name given to a variable, function, class, or any other object in Python.\
It is the rules in how you can name your variables, functions, classes, etc.

Identifiers must follow certain rules:
- They must start with a letter (a-z or A-Z) or an underscore (_).
- After the first character, they can contain letters, digits (0-9), and underscores.
- Identifiers are case-sensitive (e.g., myVar and myvar are different identifiers).
- Keywords (reserved words in Python) cannot be used as identifiers.

# Variables

A variable is a named storage location in memory that holds a value. In Python, variables are created when you assign a value to them, and they can store different types of data, such as numbers, strings, lists, or objects. Variables are dynamically typed, meaning their type is determined by the value they hold.



```python
x = 5       # Integer variable
name = "Alice"  # String variable
my_list = [1, 2, 3]  # List variable
```

# Arithmetic Operators
Python provides several arithmetic operators for performing mathematical operations on numerical values. 

Here are some commonly used arithmetic operators:

- `+` (Addition): Adds two values together.
- `-` (Subtraction): Subtracts one value from another.
- `*` (Multiplication): Multiplies two values.
- `/` (Division): Divides one value by another and returns a floating-point result.
- `//` (Floor Division): Divides one value by another and returns the integer part of the result (rounded down).
- `%` (Modulus): Returns the remainder when one value is divided by another.
- `**` (Exponentiation): Raises one value to the power of another.

```python
# Example for arithmetic operators
a = 10
b = 3

result = a + b  # Addition: result = 13
result = a - b  # Subtraction: result = 7
result = a * b  # Multiplication: result = 30
result = a / b  # Division: result = 3.3333333333333335
result = a // b  # Floor Division: result = 3
result = a % b  # Modulus: result = 1
result = a ** b  # Exponentiation: result = 1000
```

These terms are fundamental concepts in Python programming and are essential for understanding how variables, identifiers, and arithmetic operations work in the language.


