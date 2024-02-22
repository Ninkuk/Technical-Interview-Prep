#leetcode #technical

**Link**: https://leetcode.com/problems/longest-substring-without-repeating-characters/
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: [[Sliding Window]]

---
## Problem
Given a string `s`, find the length of the [[_Terms#^2d3de1|longest substring]] without repeating characters.

---
### Brute-Force Approach
#todo

---
## Solution

![](LSWRC.png)

**Code**:
```python
def lengthOfLongestSubstring(self, s: str) -> int:
	l, r = 0, 0
	max_sub = 0
	char_set = set()
	
	while r < len(s):
		# check if char exists in set
		if s[r] not in char_set:
			char_set.add(s[r])
			max_sub = max(max_sub, len(char_set))
			r += 1
		# if exists then reset window
		else:
			# empty set
			char_set.clear()
			l += 1
			r = l
			
	return max_sub
```

**Runtime Complexity**:

**Space Complexity**:

---
## Notes
