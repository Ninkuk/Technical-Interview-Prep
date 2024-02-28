#leetcode #technical

**Link**: https://leetcode.com/problems/additive-number/
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: [[Backtracking]]

---
## Problem

An **additive number** is a string whose digits can form an **additive sequence**.

A valid **additive sequence** should contain **at least** three numbers. Except for the first two numbers, each subsequent number in the sequence must be the sum of the preceding two.

Given a string containing only digits, return `true` if it is an **additive number** or `false` otherwise.

**Note:** Numbers in the additive sequence **cannot** have leading zeros, so sequence `1, 2, 03` or `1, 02, 3` is invalid.

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def isAdditiveNumber(self, num: str) -> bool:
	# A valid additive sequence should contain at least three numbers.
	if len(num) < 3:
		return False
	
	N = len(num)
	
	def isValid(first, second, rest):
		# Leading zero
		if first[0] == '0' and len(first) > 1:
			return False
		
		if second[0] == '0' and len(second) > 1:
			return False
		
		result = str(int(first) + int(second))
		
		if result == rest[:len(result)]:
			if len(result) == len(rest):
				return True
			
			first = str(second)
			second = rest[:len(result)]
			rest = rest[len(result):]
			
			return isValid(first, second, rest)
		else:
			return False
	
	for a in range(1, N):
		for b in range(a + 1, N):
			first = num[:a]
			second = num[a:b]
			rest = num[b:]
			
			if isValid(first, second, rest):
				return True
	
	return False
```

**Runtime Complexity**:

**Space Complexity**:

---
## Notes
