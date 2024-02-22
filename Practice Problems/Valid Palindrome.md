#leetcode #technical

**Link**: https://leetcode.com/problems/valid-palindrome/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Two Pointers]]

---
## Problem
A phrase is a **palindrome** if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Given a string `s`, return `true` _if it is a **palindrome**, or_ `false` _otherwise_.

Example: `s = "racecar"`

---
### Brute-Force Approach

I don't even know tbh

---
## Solution

Place one pointer at the head and one at the back of the string.
Iterate until nonidentical char found or if the two pointers pass each other.

**Code**:
```python
def isPalindrome(self, s: str) -> bool:
	# Not shown: to lower and remove non alphanumeric
	
	l = 0
	r = len(s) - 1
	
	# Iterate until two pointers pass each other
	while l < r:
		# if the character at two pointers are not equal
		if s[l] != s[r]:
			return False
		# if same, continue and move pointers
		else:
			l += 1
			r -= 1
	
	return True
```

**Runtime Complexity**: `O(n)`

**Space Complexity**: `O(1)`

---
## Notes
