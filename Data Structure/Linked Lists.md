#technical #data-structure 

## Overview

A linked list is a linear data structure, in which the elements are not stored at contiguous memory locations. The elements in a linked list are linked using pointers.

![[Pasted image 20230724100802.png]]

### Types of Linked Lists
 - <u>Single-linked list</u>: each node contains a reference to the next node in the sequence
 - <u>Double-linked list</u>: each node contains references to both the next and previous nodes
 - <u>Circular linked list</u>: last node points back to the head node, creating a circular structure
---

## Implementation

### Node Class
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        # self.prev = prev - for double linked list
```

### Linked List Class
```python
class LinkedList:
	def __init__(self, data):
		self.head = None
```

### Traversing
```python
temp = head
while temp is not None:
	# do something
	temp = temp.next
```

### Insert
```python
# inserting at head - O(1)
new_node = Node(data) # create new node
new_node.next = head # set head as the next element to it
head = new_node # set new node as the head

# inserting in the middle - O(n)
temp = head
while temp is not None:
	

```

### Reverse a Linked List