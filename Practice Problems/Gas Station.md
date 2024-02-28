#leetcode #technical

**Link**: https://leetcode.com/problems/gas-station
**Difficulty**: <mark style="background: #FFF3A3A6;">Medium</mark> 
**Concepts Used**: [[Arrays]], [[Greedy Algorithm]]

---
## Problem

There are `n` gas stations along a circular route, where the amount of gas at the `ith` station is `gas[i]`.

You have a car with an unlimited gas tank and it costs `cost[i]` of gas to travel from the `ith` station to its next `(i + 1)th` station. You begin the journey with an empty tank at one of the gas stations.

Given two integer arrays `gas` and `cost`, return _the starting gas station's index if you can travel around the circuit once in the clockwise direction, otherwise return_ `-1`. If there exists a solution, it is **guaranteed** to be **unique**

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def canCompleteCircuit(self, gas: List[int], cost: List[int]) -> int:
        gasInTank = 0
		
        exploration = True
        start = -1
		
        i = 0
        while True:
            # end of array - either exit or loop around
            if i == len(gas):
                if start == -1:
                    # exit if you have been through the entire array and have not found a start
                    return -1
                else:
                    # otherwise if start has been found then loop around
                    exploration = False
                    i = 0
            
            # exit if loop is successfully complete
            if i == start:
                return i
			
            if gasInTank + gas[i] >= cost[i]:
                # you can move to the next stop
                if start == -1:
                    start = i
                gasInTank = gasInTank + gas[i] - cost[i]
                i += 1    
            else:
                # you can not move - either explore or quit
                if exploration:
                    start = -1
                    gasInTank = 0
                    i += 1
                else:
                    return -1
```

**Runtime Complexity**: 

**Space Complexity**:

---
## Notes
