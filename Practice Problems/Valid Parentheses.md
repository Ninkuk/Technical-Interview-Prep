#leetcode #technical

**Link**: https://leetcode.com/problems/valid-parentheses/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Stacks]]

---
## Problem

Given a string `s` containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['` and `']'`, determine if the input string is valid.

An input string is valid if:

1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

---
### Brute-Force Approach
No brute force - just use a stack

---
## Solution

**Code**:
```python
def isValid(self, s: str) -> bool:
    map = {"(": ")", "{": "}", "[": "]"}
    stack = []
	
	for c in s:
		if c in map:
			stack.append(map[c])
		else:
			if not stack or stack.pop() != c:
				return False
	
	return False if stack else return True
```

**Runtime Complexity**: `O(N)`

**Space Complexity**: `O(N)`

---
## Notes
