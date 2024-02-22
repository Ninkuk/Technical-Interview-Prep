#leetcode #technical

**Link**: https://leetcode.com/problems/reverse-linked-list/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Linked Lists]]

---
## Problem

Given the `head` of a singly linked list, reverse the list, and return _the reversed list_.

![](https://assets.leetcode.com/uploads/2021/02/19/rev1ex1.jpg)

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
	if head == None:
		return head
	
	prev_node = None
	curr_node = head
	next_node = head.next
	
	while True:
		# reverse the connection of current node
		curr_node.next = prev_node
		
		# move the nodes forward
		if next_node == None:
			break
		else:
			prev_node = curr_node
			curr_node = next_node
			next_node = next_node.next
	
	return curr_node
```

**Runtime Complexity**: `O(N)`

**Space Complexity**: `O(N)`

---
## Notes
