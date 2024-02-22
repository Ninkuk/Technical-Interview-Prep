#leetcode #technical

**Link**: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
**Difficulty**: <mark style="background: #BBFABBA6;">Easy</mark>
**Concepts Used**: [[Sliding Window]]

---
## Problem
You are given an array `prices` where `prices[i]` is the price of a given stock on the `ith` day.

You want to maximize your profit by choosing a **single day** to buy one stock and choosing a **different day in the future** to sell that stock.

Return _the maximum profit you can achieve from this transaction_. If you cannot achieve any profit, return `0`.

---
### Brute-Force Approach
#todo

---
## Solution

**Code**:
```python
def maxProfit(self, prices: List[int]) -> int:
	# brute force: pair all values (in nested for) and return the highest diff
	# O(n^2)
	l, r = 0, 1
	max_profit = 0

	while r < len(prices):
		# see if there's a profit
		if prices[l] < prices[r]:
			diff = prices[r] - prices[l]
			max_profit = max(diff, max_profit)
		else:
			l = r
		r += 1
	
	return max_profit
```

**Runtime Complexity**: `O(n)`

**Space Complexity**: `O(1)`

---
## Notes

