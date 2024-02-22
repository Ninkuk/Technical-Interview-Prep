#leetcode #technical

**Link**: https://leetcode.com/problems/group-anagrams
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: 

---
## Problem
Given an array of strings `strs`, group **[[_Terms#^ac4ad9|the anagrams]]** together. You can return the answer in **any order**.

---
### Brute-Force Approach

```
groups = []

for s in str:
	for group in groups:
		if group[0] is anagram of s:
			add to group
	
	else:
		add the s to groups as a new group
```

---
## Solution

You can do this by sorting each string

**Code**:
```python
def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        if len(strs) == 0:
            return [[""]]
		
        groups = {}
		
        for s in strs:
            sortedS = ''.join(sorted(s))
			
            if sortedS in groups:
                groups[sortedS].append(s)
            else:
                groups[sortedS] = [s]
	    
        return list(groups.values())
```

**Runtime Complexity**: `O(m * n log n)`

**Space Complexity**: 

---
## Notes
