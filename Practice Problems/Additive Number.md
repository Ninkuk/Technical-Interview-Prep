#leetcode #technical

**Link**: 
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: 

---
## Problem

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
