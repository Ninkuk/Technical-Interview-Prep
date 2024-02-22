#leetcode #technical

**Link**: https://leetcode.com/problems/contains-duplicate/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Arrays]], [[HashSets]]

---
## Problem

Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

---
### Brute-Force Approach
idk tbh

---
## Solution

Use a hashset `set()` in which you add found integers. If an int already exists, return `True` (duplicate found), else at the end return `False`

**Code**:
```python
def containsDuplicate(self, nums: List[int]) -> bool:
	found = set()
	
	for i in nums:
		if i in found:
			return True
		else:
			found.add(i)

	return False
```

**Runtime Complexity**: `O(n)` - iterating through the array once

**Space Complexity**: `O(n)` - set when no duplicates

---
## Notes