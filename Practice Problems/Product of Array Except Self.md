#leetcode #technical

**Link**: https://leetcode.com/problems/product-of-array-except-self
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark> 
**Concepts Used**: 

---
## Problem

Given an integer array `nums`, return _an array_ `answer` _such that_ `answer[i]` _is equal to the product of all the elements of_ `nums` _except_ `nums[i]`.

The product of any prefix or suffix of `nums` is **guaranteed** to fit in a **32-bit** integer.

You must write an algorithm that runs in `O(n)` time and without using the division operation.

---
### Brute-Force Approach
Nested for loop `O(n^2)`

---
## Solution

**Code**:
```python
def productExceptSelf(self, nums: List[int]) -> List[int]:
	prefix = [1] * len(nums)
	suffix = [1] * len(nums)
	
	# fill prefix
	for i in range(len(nums)):
		if i == 0:
			continue
		
		prefix[i] = prefix[i - 1] * nums[i - 1]
	
	# fill suffix
	for i in range(len(nums) - 1, -1, -1):
		if i == len(nums) - 1:
			continue
		
		suffix[i] = suffix[i + 1] * nums[i + 1]
	
	results = []
	for i, j in zip(prefix, suffix):
		results.append(i * j)

	return results
```

**Runtime Complexity**: `O(3n) = O(n)`

**Space Complexity**:

---
## Notes
