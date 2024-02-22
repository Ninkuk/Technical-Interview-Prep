#leetcode #technical

**Link**: https://leetcode.com/problems/running-sum-of-1d-array/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Arrays]], [[Prefix Sum]]

---
## Problem

Given an array `nums`. We define a running sum of an array as `runningSum[i] = sum(nums[0]…nums[i])`.

Return the running sum of `nums`.

---
### Brute-Force Approach

I guess one approach would be to run a loop from `0 to i` for each `i` within the `n`, where each time you get the sum up until the current index.

```
for (i = 0; i < n; i++):
	for (j = 0; j < i; j++)
```

This approach will be `O(n^2)` in worst case.

The goal is to not repeat the calculation of the sum from index 0.

---
## Solution

**Code**:
```python
def runningSum(self, nums: List[int]) -> List[int]:
	sums = [nums[0]]
	
	for i in range(1, len(nums)):
		sums.append(sums[i - 1] + nums[i])
	
	return sums
```

**Runtime Complexity**: `O(n)`

**Space Complexity**: `O(n^2)` - we had to use an extra array to keep track of the sums

---
## Notes
