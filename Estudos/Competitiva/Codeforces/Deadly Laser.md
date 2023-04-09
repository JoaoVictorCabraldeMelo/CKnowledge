[Problema](https://codeforces.com/problemset/problem/1721/B)

-  Solução 
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

    int n, m, sX, sY, d;

    cin >> n >> m >> sX >> sY >> d;

  

    bool touchBottomOrLeft = min(sX - 1, m - sY) <= d;

    bool touchTopOrRight = min(n - sX, sY - 1) <= d;

  

    if (!touchBottomOrLeft || !touchTopOrRight) {

      int result = n + m - 2;

      cout << result << nl;

    } else

      cout << -1 << nl;

  }

  

  return 0;

}
```