[Problema](https://codeforces.com/problemset/problem/148/A)

- Solucao

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

  

  int k, l, m, n, d;

  cin >> k >> l >> m >> n >> d;

  

  int arr[100001] = {false};

  

  for (int i = k, j = l, x = m, y = n; i <= d || j <= d || x <= d || y <= d; i += k, j +=l, x+=m, y+=n) {

    if ( i <= d && !arr[i])

      arr[i] = true;

    if (j <= d && !arr[j])

      arr[j] = true;

    if (x <= d && !arr[x])

      arr[x] = true;

    if (y <= d && !arr[y])

      arr[y] = true;

  }

  

  int armmedDragons = 0;

  for (int i = 1; i <= d; i++){

    if (arr[i])

      armmedDragons++;

  }

  

  cout << armmedDragons << endl;

  return 0;

}
```