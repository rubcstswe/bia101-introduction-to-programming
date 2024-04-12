# Logical & Conditional Expression

# Conditional Expression

Conditional expressions in Python are used to execute different blocks of code based on certain conditions. 

They are formed using conditional statements like if, elif (else if), and else.

## `if` statement
The if statement executes a block of code if a specified condition is `True`

```python
x = 10

if x > 5:
    print("x is greater than 5")  # This line will be executed
```

## `if-else` statement

The if-else statement executes one block of code if a specified condition is `True`, and another block if the condition is `False`

```python
x = 3

if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")  # This line will be executed
```

## `if-elif-else` statement

The if-elif-else statement allows you to check multiple conditions and execute different blocks of code **based on the first condition that evaluates to True.**

```python
x = 10

if x < 5:
    print("x is less than 5")
elif x < 10:
    print("x is less than 10")
else:
    print("x is greater than or equal to 10")  # This line will be executed
```

## Nesting
Conditional expressions can be nested and combined with logical expressions to create more complex decision-making structures in your Python code.

```python
age = 25
is_student = True

if age < 18:
    print("You are a minor")
elif age >= 18 and is_student:
    print("You are a student")
else:
    print("You are an adult")  # This line will be executed
```

# Logical Operators

Logical expressions in Python are used to combine or negate conditions. 

They are formed using logical operators and operands (which can be variables, values, or other expressions). 

**The result of a logical expression is either True or False.**

Python provides the following logical operators:

`and`: Returns True if **both** operands are True, otherwise False.
`or`: Returns True if **at least one** of the operands is True, otherwise False.
`not`: Returns the **opposite boolean value** of the operand (True if the operand is False, and False if the operand is True).

**Example:**
```python
x = 5
y = 10

# and operator
result = x < 10 and y > 5  # True

# or operator
result = x > 10 or y > 5  # True

# not operator
result = not (x == 5)  # False
```

# More Examples

```python
# =================
# Example 1
x = 5
y = 10

if x > 5 and y < 15:
    print("Both conditions are True")  
else:
    print("At least one condition is False") # This line will be executed

# =================
# Example 2 - Nested if-else
age = 25
is_student = True

if age < 18:
    print("You are a minor")
elif age >= 18 and is_student:
    print("You are a student")
else:
    print("You are an adult")  # This line will be executed

# =================
# Example 3 - If inside a if block
x = 5
y = 10

if x > 5:
    if y > 5:
        print("Both x and y are greater than 5")  
    else:
        print("x is greater than 5, but y is not")
else:
    print("x is not greater than 5") # This line will be executed

# =================
# More if inside if example
x = 6
y = 10
if x > 5:
    if y < 5:
        print("Both x and y are greater than 5")  
    else:
        print("x is greater than 5, but y is not") # This line will be executed
else:
    print("x is not greater than 5")

# =================
# Example 4 - Using not operator
x = 5
a = 10
if not x == a:
    print("x is not equal to a")  # This line will be executed
else:
    print("x is equal to a")

# =================
# Example 5 - Using or operator
x = 4
y = 10
if x > 5 or y > 5:
    print("At least one of the conditions is True")  # This line will be executed
else:
    print("Both conditions are False")

# =================
# Example 6 - Using not operator
x = 6
y = 10
# x == 6 will be false
# y == 10 will be true
# The operations insdie the brackets() will be False as both are not True in the `and` operation

# Therefore, `not False` will evaluate to True
if not (x == 5 and y == 10):
    print("x is not equal to 5 and y is not equal to 10")  # This line will be executed
else:
    print("x is equal to 5 and y is equal to 10")

# =================
# Example 7 - Triple nested if statement
x = 6
y = 10

if x > 5:
    if y > 5:
        if x + y > 15:
            print("x, y, and their sum are greater than 5") # This line will be executed
        else:
            print("x, y are greater than 5, but their sum is not greater than 15") 
    else:
        print("x is greater than 5, but y is not")
else:
    print("x is not greater than 5")
```