
#array 

[Problema](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/description/)

- Solução

```python

class Solution:

def kidsWithCandies(self, candies: List[int], extraCandies: int) -> List[bool]:
	ordList = candies.copy()
	ordList.sort()
	gtCandie = ordList[-1]
	result = [False] * len(candies)
	for i in range(len(candies)):
		if candies[i] + extraCandies >= gtCandie:
			result[i] = True
	return result
```

```javascript
/**
 * @param {number[]} candies
 * @param {number} extraCandies
 * @return {boolean[]}
 */
var kidsWithCandies = function(candies, extraCandies) {
    let ordList = [...candies];
    ordList.sort((x,y) => x - y);
    let maxCandie = ordList.pop();
    let result = Array(candies.length).fill(false);
    for (let i = 0; i < candies.length; i++) {
        if (candies[i] + extraCandies >= maxCandie) 
            result[i] = true;
    }
    return result;
};
```