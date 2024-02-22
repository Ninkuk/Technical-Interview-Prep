#leetcode #technical

**Link**: https://leetcode.com/problems/merge-two-sorted-lists/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Linked Lists]]

---
## Problem

You are given the heads of two sorted linked lists `list1` and `list2`.

Merge the two lists into one **sorted** list. The list should be made by splicing together the nodes of the first two lists.

Return _the head of the merged linked list_.

![](https://assets.leetcode.com/uploads/2020/10/03/merge_ex1.jpg)

---
### Brute-Force Approach


---
## Solution

**Code**:
```python
def mergeTwoLists(self, list1, list2):
	# return the non-empty list
	if list1 == None:
		return list2
	elif list2 == None:
		return list1
	
	# create a new node
	curr_node = ListNode()
	head = curr_node
	
	while True:
		if list1.val < list2.val:
			curr_node.next = list1
			list1 = list1.next
		else:
			curr_node.next = list2
			list2 = list2.next
	
		curr_node = curr_node.next
		
		# check if one of the lists is over
		if list1 == None:
			curr_node.next = list2
			break
		elif list2 == None:
			curr_node.next = list1
			break
	
	# return the actual head
	return head.next
```

**Runtime Complexity**: `O(min(N1,N2))`

**Space Complexity**: ???

---
## Notes
