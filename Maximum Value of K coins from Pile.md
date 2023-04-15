#dp #dfs

[Problema](https://leetcode.com/problems/maximum-value-of-k-coins-from-piles/)

[Explicação](https://youtu.be/ZRdEd_eun8g)

- Solução 
```python

class Solution:

	def maxValueOfCoins(self, piles: List[List[int]], k: int) -> int:
		n = len(piles)
		dp = [[-1] * (k + 1) for _ in range(n)]
		def dfs(i, coins):
			if i == n:
				return 0
			if dp[i][coins] != -1:
				return dp[i][coins]
			dp[i][coins] = dfs(i+1,coins) # Next Pile dont take
			currentPile = 0
			for j in range(min(coins, len(piles[i]))):
				currentPile += piles[i][j] # Take e nextPile
				nextPile = currentPile + dfs(i+1, coins - j - 1)
				dp[i][coins] = max(dp[i][coins], nextPile)
		return dp[i][coins]
	return dfs(0, k)

```