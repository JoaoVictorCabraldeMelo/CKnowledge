
#stack #string 

[Problema](https://leetcode.com/problems/valid-parentheses/description/)

- Solução

```python

class Solution:

	def isValid(self, s: str) -> bool:
		stack = []
		for c in s:
			if c == '(' or c == '[' or c == '{':
				stack.append(c)
			elif c == ')' or c == ']' or c == '}':
				if len(stack) == 0:
					return False
			else:
				top = stack.pop()
				if top == '(' and c != ')':
					return False
				elif top == '[' and c != ']':
					return False
				elif top == '{' and c != '}':
					return False
		if len(stack) > 0: return False
		return True

```