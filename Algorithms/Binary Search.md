#technical #algorithm 

>[!danger] Remember
>The most important requirement for Binary Search is that the array must be **SORTED**!

## What is the Binary Search?

> Algorithm for finding an item from a *sorted list* of items. It works by repeatedly dividing in half the portion of the list that could contain the item, until you've narrowed down the possible locations to just one.

![](https://tutswiki.com/images/DSA/binary-search-divide-flow.png)

---
## The Naive Brute-Force Approach
- [[Linear Search]] - `O(N)`

> [!question] The Goal
> Make Linear Search faster if the array is already sorted

---
## When to use?

### Recognizing the Problem
- You are given a sorted array

### Question Variants
- 

---
## How to use?

### Iterative Method
```python
def binarySearch(array, x, low, high):
    # Repeat until the pointers low and high meet each other
    while low <= high:
        mid = low + (high - low)//2
        # If found at mid, then return it
        if array[mid] == x:
            return mid
        # Move pointers
        elif array[mid] < x:
            low = mid + 1
        else:
            high = mid - 1
    return -1
```

### Recursive Method
This uses the [[Divide and Conquer]] approach
```python
def binarySearch(array, x, low, high):
    if high >= low:
        mid = low + (high - low)//2
        # If found at mid, then return it
        if array[mid] == x:
            return mid
        # Search the left half
        elif array[mid] > x:
            return binarySearch(array, x, low, mid-1)
        # Search the right half
        else:
            return binarySearch(array, x, mid + 1, high)
    else:
        return -1
```

---
## Examples
[[Binary Search - Leetcode]]
[[Search a 2D Matrix]]
[[Koko Eating Bananas]]
[[Find Minimum In Rotated Sorted Array]]
[[Search In Rotated Sorted Array]]
[[Time Based Key Value Store]]
[[Median of Two Sorted Arrays]]

---
## Resources
[Binary Search - Programiz](https://www.programiz.com/dsa/binary-search)

![]()