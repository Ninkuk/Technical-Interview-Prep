#leetcode #technical

**Link**: https://leetcode.com/problems/merge-strings-alternately
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Two Pointers]]

---
## Problem

You are given two strings `word1` and `word2`. Merge the strings by adding letters in alternating order, starting with `word1`. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return _the merged string._

<u>Example:</u>
**Input:** `word1 = "abc", word2 = "pqr"`
**Output:** `"apbqcr"`

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def mergeAlternately(self, word1: str, word2: str) -> str:
        ptr1, ptr2 = 0, 0
        output = ""
        flag = True
		
		# run until one of the word ends
        while ptr1 < len(word1) and ptr2 < len(word2):
	        # alternate the words using a flag
            if flag:
                output += word1[ptr1]
                ptr1 += 1
            else:
                output += word2[ptr2]
                ptr2 += 1
			
            # switch the flag
            flag = not flag
        
        # add the remaining chars to the output
        if flag:
            output += word1[ptr1:]
        else:
            output += word2[ptr2:]
		
        return output
```

**Runtime Complexity**: `O(min(n, m))`

**Space Complexity**: `O(1)`

---
## Notes
