# Function Call Stack

In the previous section, we learned about functions and how they work. 

In this section, we will learn about the function call stack: what happens when multiple functions are called, and how the computer keeps track of them.

A function call stack is created when one function is called inside another function.

The function call stack behaves like a stack data structure.

**Simple Case Example:**

```python
def greet():
    print("Hello, World!")

def main():
    greet()
    print('This is the main function')

main()

# Output:
# Hello, World!
# This is the main function
```

In the above code, the `main()` function calls the `greet()` function. 

When you run this code, the following happens:
- The interpreter starts executing the `main()` function.

- `main()` calls the `greet()` function.\
**NOTE:** The `greet()` function need to finish executing before the `main()` function can continue executing: Cannot print ("This is the main function") until `greet()` is done executing.

- A new stack frame for `greet()` is created and pushed onto the call stack.

- `greet()` executes and prints "Hello, World!".

- The stack frame for `greet()` is popped off the call stack, and execution returns to `main()`.

- `main()` completes execution, and its stack frame is popped off the call stack.

**Another Example:**

```python
def greet(name):
    print(f"Hello, {name}!")
    print('greet done')

def welcome(age, occupation):
    greet(f"{occupation} of age {age}")
    print('welcome done')

def main():
    welcome(30, "Developer")
    print('main done')

main()

# Output:
# Hello, Developer of age 30!
# greet done
# welcome done
# main done
# No call stack: Stops Executing
```

When you run this code, the following happens:\
- The interpreter starts executing the `main()` function.

- `main()` calls the `welcome()` function with arguments 30 and "Developer".

- A new stack frame for `welcome()` is created and pushed onto the call stack.

- Inside `welcome()`, the `greet()` function is called with the argument "Developer of age 30".

- A new stack frame for `greet()` is created and pushed onto the call stack.

- `greet()`executes and prints "Hello, Developer of age 30!".

- The stack frame for `greet()` is popped off the call stack, and execution returns to `welcome()`.

- `welcome()` completes execution, and its stack frame is popped off the call stack.

- `main()` completes execution, and its stack frame is popped off the call stack.
