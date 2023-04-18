
[Problema](https://leetcode.com/problems/merge-strings-alternately/submissions/)

- Solução
```python
class Solution:
	def mergeAlternately(self, word1: str, word2: str) -> str:
		maxLen = max(len(word1), len(word2))
		mergedString = []
		for i in range(maxLen):
			if i < len(word1):
				mergedString.append(word1[i])
			if i < len(word2):
				mergedString.append(word2[i])

return "".join(mergedString)
```


```js
/**
* @param {string} word1
* @param {string} word2
* @return {string}
*/
var mergeAlternately = function(word1, word2) {
	let mergedString = []
	maxLen = Math.max(word1.length, word2.length);
	for (let i = 0; i < maxLen; i++) {
		if (i < word1.length) mergedString.push(word1[i]);
		if (i < word2.length) mergedString.push(word2[i]);
	}
	return mergedString.join("");
};
```