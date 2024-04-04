# Sorting Algorithms

Imagine you own an e-commerce company that sells a wide range of products. Your online store has a vast inventory, and customers can search for products based on various criteria, such as price, popularity, or ratings. 

Without an efficient way to sort the products based on these criteria, it would be challenging for your customers to find what they're looking for, leading to a poor user experience and potentially lost sales.

# Bubble Sort

**Time Complexity:** O(n^2) in the worst case, O(n) in the best case\
**Space Complexity:** O(1)

Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. 

The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted.

**Let's use a real-life example to understand the intuition behind bubble sort:**

Imagine you have a group of friends standing in a line, but they are not arranged in order of height. You want to rearrange them from shortest to tallest (or vice versa). 

Here's how you could use the bubble sort approach:
- Start from the beginning of the line.
- Compare the heights of the first two people. If the person on the right is shorter than the person on the left, swap their positions.
- Move to the next pair of adjacent people and repeat step 2.
- Continue this process, moving along the line and swapping adjacent people if they are in the wrong order.
- After reaching the end of the line, you will have bubbled up (or down) the tallest (or shortest) person to the correct position.
- Repeat steps 2-5 for the remaining unsorted portion of the line until the entire line is sorted.

**Visualization:** 

```plaintext
# Imagine the following heights represent your friend's height in a line:
Initial line: [68, 62, 72, 65, 70, 61]

Iteration 1:
[62, 68, 65, 70, 61, 72]  (Swapped 68 and 62, 72 bubbled to the end)
  ^   ^

Iteration 2:
[62, 65, 68, 61, 70, 72]  (Swapped 68 and 65, 70 bubbled up)
      ^  ^

Iteration 3:
[62, 65, 61, 68, 70, 72]  (Swapped 68 and 61)
          ^  ^

Iteration 4:
[62, 61, 65, 68, 70, 72]  (Swapped 65 and 61)
      ^  ^

Iteration 5:
[61, 62, 65, 68, 70, 72]  (Swapped 62 and 61)
 ^  ^

Sorted line: [61, 62, 65, 68, 70, 72]
```

**Python Implementation:**

```python
def bubble_sort(arr):
    """
    Sorts the given list 'arr' in ascending order using the bubble sort algorithm.
    """
    n = len(arr)

    # Iterate through the list n-1 times
    for i in range(n-1):
        # Last i elements are already sorted
        for j in range(n-i-1):
            # Traverse the list from 0 to n-i-1
            # Swap if the element is greater than the next element
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

    return arr

my_list = [64, 34, 25, 12, 22, 11, 90]

sorted_list = bubble_sort(my_list)
print("Sorted list:", sorted_list)

# Output: Sorted list: [11, 12, 22, 25, 34, 64, 90]
```

**Video:**\
NOTE: No need to watch the Java Implementation

<iframe width="560" height="315" src="https://www.youtube.com/embed/Dv4qLJcxus8?si=xk-kmP2GzOqKGZ_U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Insertion Sort

**Time Complexity:** O(n^2) in the worst case, O(n) in the best case\
**Space Complexity:** O(1)

The insertion sort algorithm is a simple and intuitive sorting algorithm that works by building a sorted array (or list) one element at a time.

**Let's use a real-life example to understand the intuition behind insertion sort:**

Imagine you are a card player, and you have a hand of cards that is initially unsorted. You want to sort your cards in ascending order (for example, from Ace to King)

Here's how you could use the insertion sort approach:
- Start by considering the first card as your sorted "hand" (a single card is already sorted).
- Take the next card from the unsorted portion of your hand.
- Insert the new card into the correct position in your sorted "hand" by shifting the cards that are greater than the new card to the right.
- Repeat steps 2 and 3 for each remaining card in the unsorted portion until all cards are inserted into the sorted "hand".

**Visualization:**

```plaintext
Initial hand (unsorted): [5, 2, 9, 1, 7]

Iteration 1:
Sorted hand: [5]
Unsorted cards: [2, 9, 1, 7]
Insert 2 into the sorted hand:
Sorted hand: [2, 5]
Unsorted cards: [9, 1, 7]

Iteration 2:
Sorted hand: [2, 5]
Unsorted cards: [9, 1, 7]
Insert 9 into the sorted hand:
Sorted hand: [2, 5, 9]
Unsorted cards: [1, 7]

Iteration 3:
Sorted hand: [2, 5, 9]
Unsorted cards: [1, 7]
Insert 1 into the sorted hand:
Sorted hand: [1, 2, 5, 9]
Unsorted cards: [7]

Iteration 4:
Sorted hand: [1, 2, 5, 9]
Unsorted cards: [7]
Insert 7 into the sorted hand:
Sorted hand: [1, 2, 5, 7, 9]
Unsorted cards: []

Final sorted hand: [1, 2, 5, 7, 9]
```

**Video:**\
NOTE: No need to watch the Java Implementation

<iframe width="560" height="315" src="https://www.youtube.com/embed/8mJ-OhcfpYg?si=PFud3Q3IzUeYy_XE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Python Implementation:**

```python
def insertion_sort(arr):
    """
    Sorts the given list 'arr' in ascending order using the insertion sort algorithm.
    """
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1

        # Shift elements greater than 'key' to the right
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1

        # Insert 'key' at the correct position
        arr[j + 1] = key

    return arr

my_list = [5, 2, 9, 1, 7]

sorted_list = insertion_sort(my_list)
print("Sorted list:", sorted_list)

# Output: Sorted list: [1, 2, 5, 7, 9]
```