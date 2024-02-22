#leetcode #technical

**Link**: https://leetcode.com/problems/container-with-most-water/
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: [[]]

---
## Problem

You are given an integer array `height` of length `n`. There are `n` vertical lines drawn such that the two endpoints of the `ith` line are `(i, 0)` and `(i, height[i])`.

Find two lines that together with the x-axis form a container, such that the container contains the most water.

Return _the maximum amount of water a container can store_.

**Notice** that you may not slant the container.

---
### Brute-Force Approach
Nested loop `O(N^2)` which checks each height to determine the highest volume.

---
## Solution


**Code**:
```python
def maxArea(self, height: List[int]) -> int:
		# two pointers at both ends of the array
        l, r = 0, len(height) - 1
		
		# volume to be maximized
        max_vol = 0
		
		# Iterate until two pointers pass each other
        while l < r:
			# calculate the area (volume)
            h = min(height[l], height[r])
            w = r - l
            vol = h * w
			
            max_vol = max(max_vol, vol)
			
			# move the pointers based
            if height[l] < height[r]:
                l += 1
            elif height[l] > height[r]:
                r -= 1
            else:
	            # edge case
	            # technically in this you can move either
                l += 1
        
        return max_vol
```

**Runtime Complexity**: `O(N)`

**Space Complexity**: `O(1)`

---
## Notes
