#stack 

[Problema](https://leetcode.com/problems/validate-stack-sequences/description/)

- Solução
```python

class Solution:

    def validateStackSequences(self, pushed: List[int], popped: List[int]) -> bool:

        stack = []

        for i in range(len(pushed)):

            stack.append(pushed[i])    

            while stack != [] and stack[-1] == popped[0]:

                    stack.pop()

                    popped.pop(0)

  

        return True if stack == [] else False
```