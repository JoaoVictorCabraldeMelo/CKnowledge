
[Problema](https://codeforces.com/contest/1293/problem/B)

- Solução 
```python

T = 1
for test_no in range(T):
	n = int(input())
	ans = sum([1.0 / i for i in range(1, n+1)])
print(ans)

```