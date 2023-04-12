
[Problema](https://leetcode.com/problems/simplify-path/description/)

### Ideia
Dividir seu caminho por / em seguida para cada caminho dividido se encontrarmos .. da pop na pilha
se encontrar qualquer caso que nao e para fazer nada so vai para o caso de push no final juntamos cada elemento encontrado com / e adicionamos a / no comeco.

- Solução 
```python

class Solution:

    def simplifyPath(self, path: str) -> str:

        dir_stack = []

        path = path.split("/")

        for elem in path:

            if dir_stack and elem == "..":

                dir_stack.pop()

            elif elem not in ["", ".", ".."]:

                dir_stack.append(elem)

        return '/' + '/'.join(dir_stack)

```