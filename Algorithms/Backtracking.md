#technical #algorithm 

## What is the Backtracking?

> Backtracking can be defined as a general algorithmic technique that considers searching every possible combination in order to solve a computational problem.

> Backtracking is like trying different paths, and when you hit a dead end, you backtrack to the last choice and try a different route.

### "Brute-Force" approach
The **Brute force approach** tries out all the possible solutions and chooses the desired/best solutions

> [!question] Backtracking vs DP
> Backtracking = All possible valid solutions
> DP = most efficient solution

### Basic Terminologies
- **Candidate:** A candidate is a potential choice or element that can be added to the current solution.
- **Solution:** The solution is a valid and complete configuration that satisfies all problem constraints.
- **Partial Solution:** A partial solution is an intermediate or incomplete configuration being constructed during the backtracking process.
- **Decision Space:** The decision space is the set of all possible candidates or choices at each decision point.
- **Decision Point:** A decision point is a specific step in the algorithm where a candidate is chosen and added to the partial solution.
- **Feasible Solution:** A feasible solution is a partial or complete solution that adheres to all constraints.
- **Dead End:** A dead end occurs when a partial solution cannot be extended without violating constraints.
- **Backtrack:** Backtracking involves undoing previous decisions and returning to a prior decision point.
- **Search Space:** The search space includes all possible combinations of candidates and choices.
- **Optimal Solution:** In optimization problems, the optimal solution is the best possible solution.


![](https://ibpublicimages.s3-us-west-2.amazonaws.com/tutorial/backtracking1.png)

---
## State Space Tree

> A space state tree is a tree representing all the possible states (solution or nonsolution) of the problem from the root as an initial state to the leaf as a terminal state.

![](https://cdn.programiz.com/sites/tutorial2program/files/ba-state-space-tree.png)

---
## The Algorithm

```python
def backtracking(result, args):
	if (GOAL REACHED):
		add solution to result
		return

	# go through all available choices
	for choice in choices:
		if choice is valid:
			make choice
			Backtrack(res, args) # DFS - keep going ahead
			undo choice # backtrack
```

### Permutation

### Combination