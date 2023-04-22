
#dp #string 

- [Referencia](https://www.youtube.com/watch?v=O5h3pTEEfr0)

# Solucao

```python
class Solution:

    def minInsertions(self, s: str) -> int:
        n = len(s)
        dp =[[sys.maxsize] * (n+1) for _ in range(n+1)] # Cria uma dp para fazer calculo entre substrings sub(i a j)

        for i in range(n-1, -1, -1):
            for j in range(n):
                if s[i] == s[j]:
                    if j - i < 2:
                        dp[i][j] = 0 # eh a ou aa
                    else:
                        dp[i][j] = dp[i+1][j-1] # eh igual continua
                else:
                    dp[i][j] = 1 + min(dp[i][j-1], dp[i+1][j]) #procura o min entre inserir no comeco e inserir no final
        return dp[0][n-1] #retorna o string inteira 
```