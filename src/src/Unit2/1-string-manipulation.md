# String Manipulation

Strings are sequences of character data. The string type in Python is called `str`

String literals may be delimited using either single or double quotes. All the characters between the opening delimiter and matching closing delimiter are part of the string:

```python
s = "I am a string"
t = 'I am a string too"

type(s) # <class str>
type(t) # <class str>
```

# String Operators

You can perform concatenation and multiplication operations on string using the symbols `+` `*`:

```python
# ================
# plus operator: String Concatenation
first_name = "Alice"
last_name = "Smith"
full_name = first_name + " " + last_name
print(full_name) # Alice Smith

s = "foo"
t = "bar"
u = "baz"

s + t # foobar
s + t + u # foobarbaz

s + u # foobaz

# ================
# Multiply Operator
s * 2 # foofoo
t * 3 # barbarbar
w = "hi."
w * 4 # hi.hi.hi.hi
```

The operator `in` and `not in` can be used to check if a string exist in another string

```python
# ================
s = "foo"
t = "bar"
u = "baz"

r = 'o' in s # True
m = 'o' in t # False
r = 'o' not in s # False
r = 'z' not in 'abc' # True
```

# String Manipulation

String methods such as `str.lower()` `str.upper()` can be used to change the string's case and slicing using `[]` can be used to extract particular string.

```python
# =================
# String Methods
# .upper()
message = "Hello, world!"
uppercase_message = message.upper()
print(uppercase_message) # HELLO, WORLD!

# .lower()
message = "Hello, world!"
lower_case = message.upper()
print(lower_case) # hello, world!

# .capitalize()
name = "emma"
capitalized_name = name.capitalize()
print(capitalized_name) # Emma
```

For a full list of available string method refer to [this article](https://www.programiz.com/python-programming/methods/string)

# String Slicing

Just like array indexing, you can access elements and slice elements from a string.

```python
# ===================
# Basic Slicing
text = "Python Programming"
# Extracts characters from index 2 (inclusive) to index 7 (exclusive).
sliced_text = text[2:8]
print(sliced_text)  # Output: thon Pro

# ===================
# Slicing from beginning
text = "Hello World"
sliced_text = text[:5]
print(sliced_text)  # Output: Hello

# ===================
# Slicing from end:
text = "Welcome Back"
sliced_text = text[-4:]
print(sliced_text)  # Output: Back

# ===================
# Reversing a string:
text = "Never say never"
sliced_text = text[::-1]
print(sliced_text)  # Output: rven ays revaN
```