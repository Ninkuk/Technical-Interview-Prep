#technical #data-structure 

## Overview

Queue is a linear data structure that follows the First In First Out (FIFO) ordering.

![[Pasted image 20230723171821.png]]
>Note: This image is mirrored representation of how queues behave in python. The head is to the right and tail is to the left.

---

## Implementation

In python, you can use a list to mimic a queue. However, this it's neither efficient nor safe to use it. Instead, use `collections.deque` to implement a stack.

>[!info] Deque (double-ended queues)
>Deques are a generalization of stacks and queues. Deques support thread-safe, memory efficient appends and pops from either side of the deque with approximately the same O(1) performance in either direction.

### Init
```python
import collections.deque
q = deque()
```

### Insert (push)
```python
q.appendLeft(value) # adds to the left side (tail)
```

### Remove (pop)
```python
q.pop() # removes from the right side (head)
```

### Peek
```python
q[-1] # shows the element at right side (head)
```

### isEmpty
```python
isEmpty = len(q) == 0
```

### Size
```python
size = len(q)
```

| Operation | Runtime |
| --------- | ------- |
| Push      | O(1)    |
| Pop       | O(1)    |
| Peek      | O(1)    |
| isEmpy    | O(1)    |
| Size      | O(1)    |

