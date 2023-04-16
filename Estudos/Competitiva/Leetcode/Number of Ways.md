
[Explicacao](https://www.youtube.com/watch?v=_GF-0T-YjW8)

[Problema](https://leetcode.com/problems/number-of-ways-to-form-a-target-string-given-a-dictionary/)

Fazer como array 2d.

- Solucao 

```python
class Solution:

    def numWays(self, words: List[str], target: str) -> int:

        mod = 10 ** 9 + 7

  

        cnt = defaultdict(int)

        dp = {}

        for word in words:

            for i, c in enumerate(word):

                cnt[(i,c)] += 1

  

        def recur(i, k):

            if i == len(target):

                return 1

            if k == len(words[0]):

                return 0

            if (i,k) in dp:

                return dp[(i,k)]

            c = target[i]

            dp[(i, k)] = recur(i, k+1)

            dp[(i, k)] += cnt[(k, c)] * recur(i+1, k+1)

            return dp[(i, k)] % mod

  

        return recur(0, 0)
```