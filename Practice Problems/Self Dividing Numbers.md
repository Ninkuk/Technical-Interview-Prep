#leetcode #technical

**Link**: https://leetcode.com/problems/self-dividing-numbers
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark> 
**Concepts Used**: [[]]

---
## Problem

A **self-dividing number** is a number that is divisible by every digit it contains.

- For example, `128` is **a self-dividing number** because `128 % 1 == 0`, `128 % 2 == 0`, and `128 % 8 == 0`.

A **self-dividing number** is not allowed to contain the digit zero.

Given two integers `left` and `right`, return _a list of all the **self-dividing numbers** in the range_ `[left, right]`.

**Example 1:**
**Input:** `left = 1, right = 22`
**Output:** `[1,2,3,4,5,6,7,8,9,11,12,15,22]`

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def selfDividingNumbers(self, left: int, right: int) -> List[int]:
	output = []
	
	for n in range(left, right + 1):
		addToList = True
		
		for digit in str(n):
			if digit == '0':
				addToList = False
				break
			
			if n % int(digit) != 0:
				addToList = False
				break
			
		if addToList:
			output.append(n)
	
	return output
```

**Runtime Complexity**:

**Space Complexity**:

---
## Notes
