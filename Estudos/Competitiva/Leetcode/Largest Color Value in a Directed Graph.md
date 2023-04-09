#grap #topologicaSorting #dfs


[Problema](https://leetcode.com/problems/largest-color-value-in-a-directed-graph/description/)

[Explicação](https://www.youtube.com/watch?v=_DgjY4HvMto)

### Ordenação topológica é boa para encontra ciclos 

-> Pseudocódigo:

_L_ ← Empty list that will contain the sorted nodes
**while** exists nodes without a permanent mark **do**
    select an unmarked node _n_
    visit(_n_)

**function** visit(node _n_)
    **if** _n_ has a permanent mark **then**
        **return**
    **if** _n_ has a temporary mark **then**
        **stop**   _(graph has at least one cycle)_
	mark _n_ with a temporary mark
    **for each** node _m_ with an edge from _n_ to _m_ **do**
        visit(_m_)
    remove temporary mark from _n_
    mark _n_ with a permanent mark
    add _n_ to head of _L_


## Código

````python

class Solution:

    def largestPathValue(self, colors: str, edges: List[List[int]]) -> int:

        graph = [[] for _ in range(len(colors))] #cria sua lista de adjancencia

        states = [0] * len(colors) # cria array de estado nao-visitado =  0, visitado = 1, terminado = 2

        colorsNode = [[0] * 26 for _ in range(len(colors))] # criar um array para cada no sendo tamanho do alfabeto

  

        for u,v in edges:

            graph[u].append(v)

        """Topological sorting porem com dfs """

        def dfs(u):

            if states[u] == 2: # se for um terminado ta ok

                return True

            if states[u] == 1: # se for um visitado tem ciclo

                return False

            states[u] = 1 # coloca esse no como visitado

  

            for v in graph[u]:

                if not dfs(v): return False

                for color in range(26): # o cor maxima de cor possivel do no

                    colorsNode[u][color] = max(colorsNode[u][color], colorsNode[v][color])

            states[u] = 2 # coloca como terminado

            colorsNode[u][ord(colors[u]) - ord('a')] += 1 # atualiza a cor

            return True

        for node in range(len(colors)): #faco o dfs para cada no

            if not dfs(node):

                return -1

        return max(max(color) for color in colorsNode) # retorne o maximo de cada no
```
