#technical 

## General Tips
- Python is very sensitive about <u>indentation</u>. Make sure your indent levels are correct, especially on a text editor!

---
## Variables

```python
# Multiple Assignments
x, y = 5, "hi" # possible to do on one line - not recommended tho -_-

# Increment
x = x + 1
x += 1
# x++ not allowed

# Null
x = None # None is Null
```

---
## Conditions

```python
# Boolean
True
False

# &&
True and False

# ||
True or False

# Multi-line conditions
((x > 2) and (x != y) or (y == 0)) # multiple conditions need paranthesis
```

---
## If statements

> [!WARNING] Check your indents

```python
if condition:
	# do something
elif condition:
	# do something
else:
	# do something
```

---
## Loops

> [!WARNING] Make sure to increment the condition variable 

```python
# While Loops
x = 0
while x < 5:
	# do something
	x += 1
```

```python
# For Loop

# Basic use
for element in array:
	# do something

# Looping over a range
## range( start, stop, step)
## start: optional, default = 0
## stop: required, specifies the stop position - not included
## step: optional, default = 1, increments (+= step)
for i in range(5):
	# do something

# Looping with index
for i, element in enumerate(x):
	# do something

# Looping parallely
for n1, n2 in zip(nums1, nums2):
	# do something with n1, n2
```

---
## Math

```python
# Division (decimal)
5 / 2 # 2.5

# Division (integer - ROUNDS DOWN - does not turncate)
5 // 2 # 2
-3 // 2 # -2 not -1
int(-3/2) # -1, this can help you turncate

# Math helpers
import math
math.floor() # round down
math.ceil() # round up
math.sqrt() # takes the sqrt
math.pow(base, exponent) # base ^ exponent

# Infinity
float("inf")
float("-inf")
```

---
## Lists (Arrays)

```python
# Lists are dynamic
lst = [1, 2, 3]

# Append - O(1)
lst.append(4)

#Pop - O(1)
lst.pop() # removes 4

# Insert - O(n)
lst.insert(index, value)

# Remove - O(n)
lst.remove(value)

# Reading and Reassigning values - O(1)
lst[0] # 1
lst[0] = 5 # [5, 2, 3]

lst[-1] # reads the last value = 3

# Init with default values
lst = [1] * 5 # [1,1,1,1,1]

# Sublists (slicing) - O(stop - start)
lst[start:stop] # stop is not included

# Length of List - O(1)
len(lst)

# Reverse - O(n)
lst.reverse()

# Sort - O(n log n)
lst.sort() # sort in ascending order
lst.sort(reverse=True) # sort in descending order

# List Comprehension
lst2 = [x+1 for x in lst] # [1,2,3] -> [2,3,4]

# Min, Max - O(n)
min(lst)
max(lst)
```

---
## 2D Arrays

```python
# [[0,0,0,0],
#  [0,0,0,0],
#  [0,0,0,0],
#  [0,0,0,0]]

# [0] * 4 => [0, 0, 0, 0]

# init
arr2d = [[0] * 4 for i in range(4)]
```

---
## Strings

> [!IMPORTANT] String are immutable and any updates result in a new string
> Space and Time: O(n)

```python
s = "abc"

# Slicing
s[start:stop] # stop is not included

# Join (using delimiter)
strings = ["abc", "def", "ghi"]
"-".join(strings) # "abc-def-ghi"
"".join(strings) # "abcdefghi"
" ".join(strings) # "abc def ghi"

# Split (using delimeter)
s = "abc,def,ghi"
s.split(",") # [abc, def, ghi]
```

---
## Queues

> [!tip] Queues in Python are double-ended by default
> You can add/remove elements from front or back

```python
from collections import deque

# init
q = deque()

# Add to the back
q.append(1)

# Add to the front
q.appendLeft(1)

# Remove from the back
q.pop()

# Remove from the front
q.popLeft()
```

---
## Hash Sets

> [!caution] Sets can not have duplicates in them

```python
# init
s = set() # {}
s = set([1,2,3]) # {1,2,3}
s = { i for i in range(5) } # {0,1,2,3,4} set comprehension

# Add
s.add(value)

# Remove
s.remove(value)

# Clear
s.clear()

# Check if element exists
value in s # True
```

---
## Hash Maps

> [!caution] Hash/Dict is UNORDERED!

```python
# init
map = {}
map = dict()
map = {"key1": val1, "key2": val2}
map = { i : 2*i for i in range(3) } # { 0:0, 1:2, 2:4 } dict comprehension
# ^ good for graph adjacency lists

# Add
map["key"] = value

# Update
map["key"] = new_value

# Remove
map.pop("key")

# Clear
map.clear()

# Iterating over keys
for key in map:
	value = map[key]

# Iterating over values
for val in map.values():
	# do something with val

# Iterating over both
for key, val in map.items():
	# do something with key and its value
```