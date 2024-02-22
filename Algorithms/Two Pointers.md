#technical #algorithm 

## What are the Two Pointers?

> The use of two different pointers to solve a problem involving indices with the benefit of saving time and space.

> **Two pointers**: one at front, one at back

![](https://miro.medium.com/max/1280/1*mQJiROyKoPVSi_459LbXMA.png)

---
## The Naive Brute-Force Approach
- Uses nested loops which leads to unnecessary iterations over elements that have already been seen
- This duplicated work could yield `O(N * K)` or `O(N^2)` time complexity

> [!question] The Goal
> Reduce the use of nested loops and replace it with a single loop, thereby reducing the time complexity.

---
## When to use?

### Recognizing the Problem
- Typically used for searching pairs in a sorted array
- Contiguity: make sure the data structure is an iterator (arrays, strings, linked lists)
- 

### Question Variants
#### Maximizing Values
- 

---
## How to use?

```python
# place pointers at each end of the array
l, r = 0 , len(arr) - 1

# iterate until pointers pass each other
while l < r:
	# move l
	# move r
```

---
## Examples
[[Valid Palindrome]]
[[Two Sum II Input Array Is Sorted]]
[[3Sum]]
[[Container With Most Water]]
[[Trapping Rain Water]]

---
## Resources

![](https://www.youtube.com/watch?v=On03HWe2tZM)
(ignore sliding window portion which they define as slow/fast pointers)
