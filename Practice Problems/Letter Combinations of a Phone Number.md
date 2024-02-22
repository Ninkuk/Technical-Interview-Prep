#leetcode #technical

**Link**: https://leetcode.com/problems/letter-combinations-of-a-phone-number
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark>
**Concepts Used**: [[Backtracking]]

---
## Problem

Given a string containing digits from `2-9` inclusive, return all possible letter combinations that the number could represent. Return the answer in **any order**.

A mapping of digits to letters (just like on the telephone buttons) is given below. Note that 1 does not map to any letters.

![](https://assets.leetcode.com/uploads/2022/03/15/1200px-telephone-keypad2svg.png)

---
### Brute-Force Approach


---
## Solution



**Code**:
```python
def letterCombinations(self, digits: str) -> List[str]:
        # if no digits, then just return empty list
        if len(digits) == 0:
            return []
		
        # map of alphabets for each button
        map = {
            '2': ['a', 'b', 'c'],
            '3': ['d', 'e', 'f'],
            '4': ['g', 'h', 'i'],
            '5': ['j', 'k', 'l'],
            '6': ['m', 'n', 'o'],
            '7': ['p', 'q', 'r', 's'],
            '8': ['t', 'u', 'v'],
            '9': ['w', 'x', 'y', 'z'],
            }
		
        # final output list - combinations
        output = []
		
        # recursive function
        def dfs(comb: str):
            # this means all buttons have been hit
            if len(comb) == len(digits):
                output.append(comb) # add final combination to output
                return
            
            # choices for the next button (digit)
            for d in map[digits[len(comb)]]:
                dfs(comb + d) # make choice
		
        # first button (digit)
        for c in map[digits[0]]:
            dfs(c)
        
        return output
```

**Runtime Complexity**:

**Space Complexity**:

---
## Notes
