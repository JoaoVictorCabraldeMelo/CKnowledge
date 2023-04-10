
#string #implementation 

[Problema](https://codeforces.com/problemset/problem/131/A)

- Solução 

```c++

#include <bits/stdc++.h>
using namespace std;

#define vi vector<int>
#define ll long long
#define pb push_back
#define mp make_pair
#define ii pair<int, int>
#define nl "\n"

  

int main() {

	ios_base::sync_with_stdio(false);
	cin.tie(NULL);
	string s;
	cin >> s;
	bool allLettersUpperCase = true;

	for (int i = 1; i < (int)s.size(); i++) {
		if (s[i] >= 97 && s[i] <= 122)
			allLettersUpperCase = false;
	}

	if (allLettersUpperCase) {
		if (s[0] >= 97 && s[0] <= 122){
			s[0] -= 32;
			for (int i = 1; i < (int)s.size(); i++)
				s[i] += 32;
		} else {
			for (int i = 0; i < (int)s.size(); i++)
				s[i] += 32;
		}
	}
	cout << s << endl;
	return 0;
}
```