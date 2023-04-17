
[Problema](https://codeforces.com/contest/499/problem/B)

- Solução
```python

import sys
input = sys.stdin.readline

  
n, m = list(map(int, input().split()))
d = {}
for i in range(m):
	a,b = list(map(str, input().split()))
	if len(a) <= len(b):
		d[a] = a;
	else:
		d[a] = b;
lecture = list(map(str, input().split()))
for i in range(len(lecture)):
	if i != len(lecture) - 1:
	print(d[lecture[i]], end=' ')
else:
	print(d[lecture[i]])
```