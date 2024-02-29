#technical 

## What is Big O?
The amount of time it takes to run our algorithm based on our input size. So basically it is ==time in terms of input size==. Big O usually refers to the worst case scenario.

![](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png)


### Runtime Complexities
 - [[#O(1)]]
 - [[#O(n)]]
 - [[#O(n<sup>2</sup>)|O(n^2)]]
 - [[#O(n * m)]]
 - [[#O(n<sup>3</sup>)|O(n^3)]]
 - [[#O(logn)]]
 - [[#O(nlogn)]]
 - [[#O(2<sup>n</sup>)|O(2^n)]]

### General Tips
 - When calculating Big-O Complexity, you drop the non-dominant term
 - Nested = Multiply complexities, otherwise Add

---

## O(1)

Most efficient!

Also called constant time. No matter how big the input size is, the operation will always take place in constant time. Or in other words, the operation time does not change based on the input size.

```python
# Usually "lookups" are constant time
arr = [0, 1, 2, 3]
x = arr[1] # O(1)

map = {"key": 1}
x = map["key"] # O(1)
```

---

## O(n)

Linear Growth.

This typically happens when, in the worst case, you have to go through the entire input once.

Ex: Linear Search happens in linear time because you are searching the entire input
```python
arr = [0, 1, 2, 3]
arr.append(4) # O(n) - insertions

for i in arr: # O(n) - looping over all values
	print(i) # O(1)
```

---

## O(n<sup>2</sup>)

Usually occurs in nested loops in two ways:
 1. The nested loop iterates over the input data n times or pairs all elements
 2. The nested loop iterates over a square grid (n * n)

```python
# Iterating over input - pairing all elements
arr1D = [1,2,3,4,5]

# O(n) * O(n - i) * O(1) = O(n^2)
for i in range(len(arr1D)): # O(n)
	for j in range(i + 1, len(arr1D)): # O(n - i)
		print(arr1D[i], arr1D[j]) # pairs - O(1)


# Iterating over a square 2D array
arr2D = [[1,2,3], [4,5,6], [7,8,9]]

# O(n) * O(n) * O(1) = O(n^2)
for i in range(len(arr2D)): # O(n)
	for j in range(len(arr2D[i])): # O(n)
		print(arr2D[i][j]) # O(1)
```

---

## O(n * m)

Very similar to [[#O(n<sup>2</sup>)|O(n^2)]], except that you would either be traversing a rectangular grid (n * m) or pairing up elements from 2 separate arrays of different sizes

```python
# Iterating over input - pairing all elements
arr1, arr2 = [1,2,3], [4,5] # two arrays of different sizes

# O(n) * O(n - i) * O(1) = O(n^2)
for i in range(len(arr1)): # O(n)
	for j in range(len(arr2)): # O(n - i)
		print(arr1[i], arr2[j]) # pairs - O(1)

# Iterating over a rectangular 2D array
arr2D = [[1,2,3], [4,5,6]] # this array is 2x3

# O(n) * O(m) * O(1) = O(n^2)
for i in range(len(arr2D)): # O(n)
	for j in range(len(arr2D[i])): # O(m)
		print(arr2D[i][j]) # O(1)
```

---

## O(n<sup>3</sup>)

Triple nested loops. This can go further up to O(n<sup>4</sup>), O(n<sup>5</sup>), etc.

---

## O(logn)

Most commonly seen in binary search and binary tree (balanced). The idea here is that at each step, you cut down the size of your input (n) by half.

$$
\begin{gather}
2^x = n \\ 
log(2^x) = log(n) \\
x = log(n)
\end{gather}
$$
>[!TIP] Remember!
>At each step, if you cut down the size of your input (n) by half, then you have a run time of `log(n)`

---

## O(nlogn)

Most commonly found in sorting algorithms. Furthermore, almost all built-in sorting functions are O(nlogn), so you can assume this runtime for all if using them. Ex: Heap Sort, Merge Sort, etc.

O(nlogn) is less efficient than O(n) but more efficient than O(n<sup>2</sup>)

---

## O(2<sup>n</sup>)

This usually occurs in *recursion* where the recursion tree height is n with 2 branches at each level.

>[!DANGER] HOT HOT HOT TIP
>In `O(log n)`, you reduce your input by half everytime, but in `O(2^n)` you create two new branches for every input.

![[bigo logn vs 2_n.png]]

---

## Resources / References
 - https://www.bigocheatsheet.com/