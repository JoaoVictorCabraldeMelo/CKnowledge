
[Problema](https://codeforces.com/problemset/problem/1374/C)

- Solução
```cpp
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

  

  int t;

  cin >> t;

  

  while(t--) {

    int n;

    cin >> n;

    stack<char> brackets;

    int count = 0;

    for (int i = 0; i < n; i++)

    {

      char bracket;

      cin >> bracket;

      if (bracket == ')' && brackets.empty())

        count++;

      else if (bracket == '(')

        brackets.push(bracket);

      else if (bracket == ')' && !brackets.empty())

        brackets.pop();

    }

    cout << count << endl;

  }

  return 0;

}
```