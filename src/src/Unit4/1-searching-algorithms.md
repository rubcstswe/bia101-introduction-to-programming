# Searching Algorithms

Searching algorithms are crucial in computing because they help businesses and organizations efficiently manage and retrieve information from large datasets.

Imagine you run a large retail company with thousands of products in your inventory. Your customers want to quickly find and purchase the products they need. 

If you didn't have an efficient way to search through your inventory, it would be incredibly time-consuming and frustrating for your customers to locate the items they're looking for, leading to potential lost sales and dissatisfied customers.

Searching algorithms provide a systematic and efficient way to locate specific data or information within a large collection, similar to how you might use an index or table of contents in a book to quickly find a particular topic or chapter.

The two most common searching algorithms are:
1. Linear Search
2. Binary Search

# Linear Search

**Time Complexity:** O(n) - Linear\
**Space Complexity:** O(1) - Constant

It works by sequentially checking each element in the list until the desired element is found or the end of the list is reached.

**Real life example:**\
You can think of linear search as similar to how you might search for a specific book in a library by checking each bookshelf one by one from the start until you find the book you're looking for.

**NOTE:** The input list does not need to be sorted for linear search to work.

```python
def linear_search(arr, target):
    # The triple quote is a python string to specify what a function does
    """
    Performs a linear search on the given list 'arr' to find the 'target' element.
    Returns the index of the target element if found, otherwise returns -1.
    """
    for i in range(len(arr)):
        if arr[i] == target:
            return i # Return the index of the target element: 
            # Just like break statement, return statement will immediately exit the function itself
    return -1

# Usage of linear search
my_list = [5, 2, 9, 1, 7]
target = 9

index = linear_search(my_list, target)
if index == -1:
    print(f"Target {target} not found in the list")
else:
    print(f"Target {target} found at index {index}")
````

# Binary Search

**Time Complexity:** O(log n) - Logarithmic\
**Space Complexity:** O(1) - Constant

The binary search algorithm is an efficient way to find a target element in a **sorted list** or array.

It works by **repeatedly dividing the search interval in half** until the target element is found or it is determined that the element is not present in the list.

**Real life example:**\

Imagine you have a large dictionary (a book containing words and their definitions in alphabetical order), and you want to find the definition of a specific word. Instead of going through the dictionary page by page from the beginning (linear search), you can utilize the binary search approach.

Steps to perform binary search for the example above:
- Open the dictionary in the middle.

- Compare the word you're looking for with the word on the currently opened page.

- If the word you're looking for comes before the word on the current page, you know the word must be in the first half of the dictionary, so you can discard the second half.

- If the word you're looking for comes after the word on the current page, you know the word must be in the second half of the dictionary, so you can discard the first half.

- Repeat steps 1-4, but this time, open the dictionary in the middle of the remaining half.

```python
def binary_search(arr, target):
    """
    Performs a binary search on the sorted list 'arr' to find the 'target' element.
    Returns the index of the target element if found, otherwise returns -1.
    """
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

my_list = [1, 3, 5, 7, 9]
target = 7

index = binary_search(my_list, target)
if index != -1:
    print(f"Target {target} found at index {index}")
else:
    print(f"Target {target} not found in the list")
```

**Visualization:**

```plaintext
Initial list: [1, 3, 5, 7, 9]
               0  1  2  3  4
               low        high

Iteration 1:
mid = (0 + 4) // 2 = 2 (index of 5)
5 < 7, so we update low = mid + 1 = 3

List: [1, 3, 5, 7, 9]
          low      high

Iteration 2:
mid = (3 + 4) // 2 = 3 (index of 7)
7 == 7, target found at index 3

# ================================================
Visualization:

Initial list: [1, 3, 5, 7, 9]

                    mid
                     |
                     v
              [1, 3, 5, 7, 9]
               ^           ^
               |           |
              low         high
                       

After Iteration 1:
              [1, 3, 5, 7, 9]
                        ^  ^
                        |  |
                       low high

After Iteration 2 (Target Found):
              [1, 3, 5, 7, 9]
                        ^
                        |
                       mid
```
