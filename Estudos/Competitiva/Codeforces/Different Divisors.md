#math #implementation 

[Problema](https://codeforces.com/problemset/problem/1474/B)

### Explicação 

O número com 4 divisores com uma diferença de só pode ser composto por números primos ou seja eles podem ser primos distintos como p e q ou p elevado a terceira

- Solução 

```cpp
#include <iostream>

#include <vector>

  

using namespace std;

  

void solve()

{

  int x;

  cin >> x;

  vector<int> p;

  for (int i = x + 1;; i++)

  {

    int t = 1;

    for (int j = 2; j * j <= i; j++)

    {

      if (i % j == 0)

      {

        t = 0;

        break;

      }

    }

    if (t)

    {

      p.push_back(i);

      break;

    }

  }

  for (int i = p.back() + x;; i++)

  {

    int t = 1;

    for (int j = 2; j * j <= i; j++)

    {

      if (i % j == 0)

      {

        t = 0;

        break;

      }

    }

    if (t)

    {

      p.push_back(i);

      break;

    }

  }

  cout << min(1ll * p[0] * p[1], 1ll * p[0] * p[0] * p[0]) << "\n";

}

  

int main()

{

  int t;

  cin >> t;

  while (t--)

  {

    solve();

  }

}
```