#technical #algorithm

## What is the Sliding Window?

> Approach that involves iterating over a collection of items with a fixed-size window, where the window slides over the collection from left to right.

![](https://i.stack.imgur.com/F6087.png)

---
## The Naive Brute-Force Approach
- Same brute-force as the Two Pointers
- Uses nested loops which leads to unnecessary iterations over elements that have already been seen
- This duplicated work could yield `O(N * K)` or `O(N^2)` time complexity

Brute force vs Sliding Window
<img src="https://i.stack.imgur.com/2Dneo.png" width="200"> <img src="https://i.stack.imgur.com/zsGl7.png" width="200">

> [!question] The Goal
> Reduce the use of nested loops and replace it with a single loop, thereby reducing the time complexity.

---
## When to use?

### Recognizing the Problem
- Contiguity: make sure the data structure is an iterator (arrays, strings, linked lists)
- Asking for a *min, max, longest, shortest, contained*
- Subarray problems where you have to limit your field of view within an array
- Comparing subarrays

### Question Variants

#### Fixed Length Window
- We are given the window size (subarray size)
- ex: [[Maximum Subarray]] *(of size k)*
#### Dynamic Length Window
- We have to determine the sizes ourselves
- It can grow and shrink - like a caterpillar
- ex: [[Best Time to Buy and Sell Stock]]

---
## How to use?
```python
l, r = 0,0
```

---
## Examples
[[Best Time to Buy and Sell Stock]]
[[Longest Substring Without Repeating Characters]]
[[Longest Repeating Character Replacement]]
[[Permutation In String]]
[[Minimum Window Substring]]
[[Sliding Window Maximum]]

---
## Resources
[Maximum Subarrray Problem - Wikipedia](https://en.wikipedia.org/wiki/Maximum_subarray_problem)
[NeetCode - Sliding Window](https://www.youtube.com/playlist?list=PLot-Xpze53leOBgcVsJBEGrHPd_7x_koV)

![](https://www.youtube.com/watch?v=MK-NZ4hN7rs)