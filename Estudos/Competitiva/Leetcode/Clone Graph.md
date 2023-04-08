
#graph #bfs 
Solução usando algoritmo de busca em largura:

## Python

[Problema](https://leetcode.com/problems/clone-graph/)


```
class Solution:

    def cloneGraph(self, node: 'Node') -> 'Node':

        if not node: return node

  

        q, clones = deque([node]), {node.val: Node(node.val, [])}

  

        while q:

            curr = q.popleft()

            curr_clone = clones[curr.val]

            for neighbor in curr.neighbors:

                if neighbor.val not in clones:

                    clones[neighbor.val] = Node(neighbor.val, [])

                    q.append(neighbor)

                curr_clone.neighbors.append(clones[neighbor.val])

  

        return clones[node.val]
```