#leetcode #technical

**Link**: https://leetcode.com/problems/diameter-of-binary-tree/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark> 
**Concepts Used**: [[Binary Trees]], [[Depth First Search]]

---
## Problem

Given the `root` of a binary tree, return _the length of the **diameter** of the tree_.

The **diameter** of a binary tree is the **length** of the longest path between any two nodes in a tree. This path may or may not pass through the `root`.

The **length** of a path between two nodes is represented by the number of edges between them.

**Example 1:**
![](https://assets.leetcode.com/uploads/2021/03/06/diamtree.jpg)

**Input:** root = `[1,2,3,4,5]`
**Output:** 3
**Explanation:** 3 is the length of the path `[4,2,1,3]` or `[5,2,1,3]`.

**Example 2:**

**Input:** root = `[1,2]`
**Output:** 1

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
class Solution:
    # Declare a max height outside scope
    def __init__(self):
        self.maxD = 0
	
    # dfs recursion
    def height(self, root) -> int:
        # base case - return 0 on null
        if not root:
            return 0
		
        # calculate the height of left and right nodes
        dL = self.height(root.left)
        dR = self.height(root.right)
        
        # calculate the diameter of current node
        self.maxD = max(self.maxD, (dL + dR))
        
        # return the depth of current node
        return max(dL, dR) + 1
    
    def heightOfBinaryTree(self, root: Optional[TreeNode]) -> int:
        # run dfs
        self.height(root)
		
        # return the max diameter found
        return self.maxD
```

**Runtime Complexity**: 

**Space Complexity**:

---
## Notes
