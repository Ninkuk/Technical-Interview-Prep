#technical #data-structure

## Overview
An array is a collection of items of same data type stored at contiguous memory locations. 

![[Pasted image 20230723175146.png]]

---

## Time Complexity

| Operation | Runtime | Example                    |
| --------- | ------- | -------------------------- |
| Access    | O(1)    | `arr[index]`               |
| Insert    | O(n)    | `arr.insert(index, value)` |
| Append    | O(1)    | `arr.append(value)`        |
| Remove    | O(n)    | `arr.remove(value)`        |
| Pop       | O(1)    | `arr.pop()`                |

---

## Corner Cases

- Empty sequence
	- `len(arr) == 0`
- Sequence with 1 or 2 elements
	- `len(arr) == 1`
	- `len(arr) == 2`
- Sequence with repeated elements
- Duplicated values in the sequence

---
## Usage
[[Python Nuances#Lists (Arrays)|Python Lists]] - common list operations (traversal, insertion, deletion)
[[Search]] - list search implementations
[[Sorting]] - list sorting implementations

---
## Techniques

[[Sliding Window]]
[[Two Pointers]]
Traversing from the right
[[Fast and Slow Pointers]]
[[Overlapping Intervals]]
[[Cyclical Sort]]
