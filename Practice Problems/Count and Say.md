#leetcode #technical

**Link**: https://leetcode.com/problems/count-and-say/
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark> 
**Concepts Used**: 

---
## Problem

The **count-and-say** sequence is a sequence of digit strings defined by the recursive formula:

- `countAndSay(1) = "1"`
- `countAndSay(n)` is the way you would "say" the digit string from `countAndSay(n-1)`, which is then converted into a different digit string.

To determine how you "say" a digit string, split it into the **minimal** number of substrings such that each substring contains exactly **one** unique digit. Then for each substring, say the number of digits, then say the digit. Finally, concatenate every said digit.

For example, the saying and conversion for digit string `"3322251"`:

![](https://assets.leetcode.com/uploads/2020/10/23/countandsay.jpg)

Given a positive integer `n`, return _the_ `nth` _term of the **count-and-say** sequence_.

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def countAndSay(self, n: int) -> str:
        if n == 1:
            return "1"
        
        say = self.countAndSay(n - 1)
		
        i = 0
        j = i + 1
		
        result = ""
		
        while i < len(say):
            digit = say[i]
            count = 1
			
            while j < len(say):
                if say[j] == say[i]:
                    count += 1
                    j += 1
                else:
                    break
            
            i = j
            j = i + 1
			
            result += str(count) + digit
		
        print(result)
        return result
```

**Runtime Complexity**:

**Space Complexity**:

---
## Notes
