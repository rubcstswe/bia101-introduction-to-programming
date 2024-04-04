# Space & Time Complexity; Asymptotic Notation

Space and time complexity are concepts used to measure the efficiency of an algorithm or a program. 

They help us understand how an algorithm or program behaves **as the input size grows**, allowing us to make informed decisions about which approach is better suited for a particular problem.

![Space and Time Complexity](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*5ZLci3SuR0zM_QlZOADv8Q.jpeg)

# Time Complexity

Time complexity refers to the amount of time an algorithm or program takes to complete its execution relative to the input size. 

It is typically expressed using **Big O notation**, which describes the worst-case scenario or the upper bound of the algorithm's running time.

Big O notation is a mathematical way of expressing the growth rate of an algorithm's running time relative to the input size.
- In other words, it describes how long the algorithm will take to run as the input size grows (as the input size tends to infinity).

The following table shows the most common time complexities in order of increasing efficiency:

| Notation | Name | Description |
| --- | --- | --- |
| O(1) | Constant | The algorithm's running time is constant and does not depend on the input size - `The time required to run an algorithm is same no matter the input (be it input size of 10 or 1 million)` |
| O(log n) | Logarithmic | The algorithm's running time grows logarithmically with the input size. |
| O(n) | Linear | The algorithm's running time grows linearly with the input size. |
| O(n log n) | Linearithmic | The algorithm's running time grows in proportion to n log n, where n is the input size. |
| O(n^2) | Quadratic | The algorithm's running time grows quadratically with the input size. |
| O(2^n) | Exponential | The algorithm's running time doubles with each addition to the input size. |
| O(n!) | Factorial | The algorithm's running time grows factorially with the input size. |

# Space Complexity

Space complexity refers to the amount of memory an algorithm or program uses relative to the input size.
- In other words, it describes how much space/memory of a computer will be used by the algorithm as the input size grows.

Similar to time complexity, space complexity is also expressed using Big O notation, which describes the worst-case scenario or the upper bound of the algorithm's memory usage.

The following table shows the most common space complexities in order of increasing efficiency:

| Notation | Name | Description |
| --- | --- | --- |
| O(1) | Constant | The algorithm uses a constant amount of memory regardless of the input size - `The space required to run an algorithm is same no matter the input (be it input size of 10 or 1 million)`. |
| O(log n) | Logarithmic | The algorithm's memory usage grows logarithmically with the input size. |
| O(n) | Linear | The algorithm's memory usage grows linearly with the input size. |
| O(n log n) | Linearithmic | The algorithm's memory usage grows in proportion to n log n, where n is the input size. |
| O(n^2) | Quadratic | The algorithm's memory usage grows quadratically with the input size. |
| O(2^n) | Exponential | The algorithm's memory usage doubles with each addition to the input size. |
| O(n!) | Factorial | The algorithm's memory usage grows factorially with the input size. |

# Code Examples

Let's look at some code examples to understand how time and space complexity are calculated.

## Space-Time Example

Consider the following Python function that calculates the sum of the first `n` numbers:

```python
def sum_of_n_numbers(n):
    total = 0
    for i in range(1, n+1):
        total += i
    return total
```

The time complexity of this function is `O(n)` because the loop runs `n` times, where `n` is the input size.

- The loop runs `n` times, so the time complexity is `O(n)`.

- The space complexity of this function is `O(1)` because it uses a constant amount of memory regardless of the input size - It uses the same amount of variable.

- **NOTE**: If you were using an array and adding elements to it, the space complexity would be `O(n)` because the array would grow in proportion to the input size. 

**More Examples:**

```python
# ==============================
# Time complexity: O(n): Linear
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

# ==============================
# Time complexity: O(1): Constant
# Space complexity: O(1): Constant
def access_element(arr, index):
    if index >= len(arr):
        return "Index out of range"
    return arr[index]

# ==============================
# Time complexity: O(n^2): Quadratic
# Space complexity: O(1): Constant
def nested_loops(arr):
    for i in range(len(arr)):
        for j in range(len(arr)):
            print(arr[i], arr[j])

# ==============================
# Time complexity: O(log n): Logarithmic
# Space complexity: O(1): Constant
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1

# ==============================
# Time complexity: O(n log n): Linearithmic
# Space complexity: O(n): Linear
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)
# In the above example the merge function is not shown, but it is a helper function that merges two sorted arrays.
# The space complexity of merge sort is O(n) because it uses additional memory (new `left` and `right` arrays whose values gets added ) to store the sorted subarrays.

```

# Exercises 

```python
# ==============================
def sum_of_squares(n):
    total = 0
    for i in range(1, n+1):
        total += i**2
    return total

# Time: O(n)
# Space: O(1)

# ==============================
input = [1,2,3]
for i in range(1, len(input)):
    print(i)

# Time: O(n)
# Space: O(1)

# ==============================
arr = []
input = [1,2,3]
for i in range(1, len(input)):
    arr.append(i)
    print(i)

# Time: O(n)
# Space: O(n)

# ==============================
input = [1,2,3]
for i in range(1, len(input)):
    break
    print(i)

# Time: O(1)
# Space: O(1)

# ==============================
input = [1,2,3]
for i in range (1, len(input)):
    for j in range(1, 10):
        print(j)

# Time: O(n^2)
# Space: O(1)

# ==============================
input = [1,2,3]
a = []
for i in range (1, len(input)):
    for j in range(1, len(input)):
        a.append(j)
        print(j)

# Time: O(n^2)
# Space: O(n^2) # because the amount of values stored in the array `a` grows quadratically with the input size. (for input size 2 -> 4 elements will be added to the array a)

# ==============================
input = [1,2,3]
a = []
for i in range (1, len(input)):
    for j in range(1, len(input)):
        break
        a.append(j)
        print(j)

# Time: O(n) # the inside for loop is not executed because of the for loop
# Space: O(1) # The append function is never executed

# ==============================
input = [1,2,3]
a = []
for i in range (1, len(input)):
    for j in range(1, len(input)):
        if j == 2:
            continue 
        print(j)

# Time: O(n^2) # Actually it's (n^2 - 1) because of the continue statement
    # but as n tends to infinity, the -1 becomes insignificant, therefore the time complexity is O(n^2)
# Space: O(1) 
```