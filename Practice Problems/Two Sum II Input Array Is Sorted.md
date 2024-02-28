#leetcode #technical

**Link**: https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: [[Two Pointers]]

---
## Problem

Given a **1-indexed** array of integers `numbers` that is already **_sorted in non-decreasing order_**, find two numbers such that they add up to a specific `target` number. Let these two numbers be `numbers[index1]` and `numbers[index2]` where `1 <= index1 < index2 < numbers.length`.

Return _the indices of the two numbers,_ `index1` _and_ `index2`_, **added by one** as an integer array_ `[index1, index2]` _of length 2._

The tests are generated such that there is **exactly one solution**. You **may not** use the same element twice.

Your solution must use only constant extra space.

---
### Brute-Force Approach

Just like the brute force for Two Sum, you can use nested loop to check each possible solution in `O(N^2)`

---
## Solution

Place one pointer at the head and one at the back of the array.
Move the pointers based on their sum
- Increase the left pointer if the sum is lower than the target
- Decrease the right pointer if the sum is higher than the target

**Code**:
```python
def twoSum(self, numbers: List[int], target: int) -> List[int]:
	l = 0
	r = len(numbers) - 1
	
	# iterate until pointers pass each other
	while l < r:
		# sum
		s = numbers[l] + numbers[r]
		
		# check if target is high, lower or equal
		if s == target:
			return [l + 1, r + 1]
		elif s > target:
			r -= 1
		elif s < target:
			l += 1
```

**Runtime Complexity**: `O(n)`

**Space Complexity**: `O(n)`

---
## Notes
Notice that the array is sorted - this is not a coincidence!
