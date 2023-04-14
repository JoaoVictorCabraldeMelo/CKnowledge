#dp #string 

[Problema](https://leetcode.com/problems/longest-palindromic-subsequence/description/)

[Descrição da solução](https://www.youtube.com/watch?v=TLaGwTnd3HY)

- Solução 
```python

class Solution:

def longestPalindromeSubseq(self, s: str) -> int:

	n = len(s)

	dp = [[0 for x in range(n)] for y in range(n)]

	def lps(s:str):
		for i in range(len(s)):
			dp[i][i] = 1
		for d in range(2, len(s)+1):
			for i in range(len(s)-d+1):
				j = i+d-1
				if s[i] == s[j] and d == 2:
					dp[i][j] = 2
				elif s[i] == s[j]:
					dp[i][j] = dp[i+1][j-1] + 2
				else:
					dp[i][j] = max(dp[i][j-1],dp[i+1][j])
	lps(s)
	return dp[0][n-1]

```