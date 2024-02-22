#leetcode #technical

**Link**: https://leetcode.com/problems/two-sum/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Arrays]], [[HashMaps]]

---
## Problem

Given an array of integers `nums` and an integer `target`, return _indices of the two numbers such that they add up to `target`_.

You may assume that each input would have **_exactly_ one solution**, and you may not use the _same_ element twice.

You can return the answer in any order.

---
### Brute-Force Approach
Nested loop that checks each possible solution in `O(N^2)`

---
## Solution

Keep the target sum complement and their index `{(target - value): index}` in the hashmap and return when you find a complement.

**Code**:
```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
	map = {}
	
	for i, val in enumerate(nums):
		diff = target - val
		
		if diff in map:
			return [i, map[diff]]
		else:
			map[val] = i
```

**Runtime Complexity**: `O(n)` - array traversal

**Space Complexity**: `O(n)` - hashmap

---
## Notes