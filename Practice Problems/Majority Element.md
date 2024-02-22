#leetcode #technical

**Link**: https://leetcode.com/problems/majority-element
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Arrays]], [[HashMaps]]

---
## Problem

Given an array `nums` of size `n`, return _the majority element_.

The majority element is the element that appears more than `⌊n / 2⌋` times. You may assume that the majority element always exists in the array.

---
### Brute-Force Approach

```
maxFreq = 0
majorEl = 0

for i = 0; i < nums.length; i++
	counter = 0
	for j = i; j < nums.length; j++
		if nums[j] == nums[i]
			counter++
	
	if counter > maxFreq
		majorEl = i
```

---
## Solution

**Code**:
```python
def majorityElement(self, nums: List[int]) -> int:
	hashmap = {}
	
	for i in nums:
		if i in hashmap:
			hashmap[i] += 1
		else:
			hashmap[i] = 1
	
	maxFreq = 0
	maxEl = 0
	
	for key in hashmap:
		if hashmap[key] > maxFreq:
			maxFreq = hashmap[key]
			maxEl = key
	
	return maxEl
```

**Runtime Complexity**: `O(n)`

**Space Complexity**: `O(n/2) = O(n)`

---
## Notes
