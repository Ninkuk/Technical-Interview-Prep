#leetcode #technical

**Link**: https://leetcode.com/problems/valid-anagram/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[HashMaps]]

---
## Problem

Given two strings `s` and `t`, return `true` _if_ `t` _is an [[_Terms#^ac4ad9|anagram]] of_ `s`_, and_ `false` _otherwise_. An **Anagram** is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

---
### Brute-Force Approach
idk tbh

---
## Solution

Fill a hashmap with character count from the first string, then with the second string decrement the counts until all are 0

**Code**:
```python
def isAnagram(self, s: str, t: str) -> bool:
	# return false right away if not same len
	if len(s) != len(t):
		return False

	# hashmap to store values
	map = {}

	# fill the hashmap with first string
	for i in s:
		if i in map:
			map[i] += 1
		else:
			map[i] = 1

	# decrement hashmap with second string
	for j in t:
		# return false if new char found
		if j not in map:
			return False
		else:
			map[j] -= 1

	# return false if there is an extra character left
	for k in map.values():
		if k != 0:
			return False

	# finally return true
	return True
```

**Runtime Complexity**: `O(n)` - separate passes on the string = `O(3n)` = `O(n)`

**Space Complexity**: `O(n)` - hashmap

---
## Notes