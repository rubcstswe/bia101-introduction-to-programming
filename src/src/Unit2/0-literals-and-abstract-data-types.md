# Literals & Abstract Data Types

Literals are the raw data values that are directly assigned to variables or constants in Python. 

They are the building blocks of data manipulation in any programming language. 

Python supports various types of literals:

**Numeric Literals:**

- **Integer Literals**: Whole numbers (positive or negative), without any fractional part. Examples: 42, -7, 0

- **Floating-Point Literals**: Numbers with a fractional part, represented using a decimal point. Examples: 3.14, -0.001, 6.625

- **Complex Literals**: Numbers with a real and imaginary part, represented using j or J as the imaginary unit. Examples: 3+4j, -5.6J

```python
# Integer Literals
x = 42
y = -7
z = 0

# Floating-Point Literals
a = 3.14
b = -0.001
c = 6.625

# Complex Literals
d = 3 + 4j
e = -5.6J
```

**String Literals**

A string literal is a sequence of characters enclosed in single quotes ('), double quotes ("), or triple quotes (''' or """). Examples: 'Hello', "World", '''Multi-line string'''

```python
# Single-quoted string
message = 'Hello, World!'

# Double-quoted string
name = "Alice"

# Triple-quoted string (multi-line)
poem = '''Roses are red,
Violets are blue,
Sugar is sweet,
And so are you.'''
```

**Boolean Literals**

Boolean literals represent the truth values `True` and `False`. They are used in logical operations and conditional statements.

```python
# Boolean Literals
is_student = True
is_raining = False
```

**Special Literals**

**None**: Represents a null value or the absence of a value.

```python
# None Literal
result = None
```

# Abstract Data Types

Python provides several built-in data types that are used to store collections of values. 

These are known as Abstract Data Types (ADTs) and include the following:

**List**
A list is an ordered collection of items. Lists are mutable (changeable) and can contain elements of different data types. 

Lists are defined using square brackets `[]`.

```python
fruits = ['apple', 'banana', 'cherry']
numbers = [1, 2, 3, 4, 5]
mixed = [1, 'hello', 3.14, True]
```

**Tuple**

A tuple is an ordered, immutable (unchangeable) collection of items. 

Tuples are defined using parentheses `()`.

```python
point = (3, 4)
person = ('John', 30, 'Engineer')
coordinates = (10, 20, 30)
```

**Set**

A set is an unordered collection of unique elements. 

Sets are defined using curly braces `{}`.

```python
fruits = {'apple', 'banana', 'cherry'}
numbers = {1, 2, 3, 4, 5}
unique_chars = {'a', 'b', 'c', 'd'}
```

**Dictionary**

A dictionary is an unordered collection of key-value pairs. 

Dictionaries are defined using curly braces `{}`, with keys and values separated by colons.

```python
person = {'name': 'John', 'age': 30, 'occupation': 'Engineer'}
person1 = {'name': 'Alice', 'age': 25, 'city': 'New York'}
product = {'id': 101, 'name': 'Laptop', 'price': 999.99}
student = {'name': 'Bob', 'grades': [85, 92, 78]}
```




