#implementation #math 

[Problema](https://codeforces.com/contest/1714/problem/A)

## C++

```
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

    int n, H, M;

    cin >> n >> H >> M;

    int sleepTime = 60 * H + M;

    int minAlarm = INT_MAX;

    int resultMin = 0;

    for (int i = 0; i < n; i++)

    {

      int x, y;

      cin >> x >> y;

      int alarm = x * 60 + y;

      resultMin = alarm - sleepTime;

      if (resultMin < 0)

        resultMin += 24 * 60;

      minAlarm = min(minAlarm, resultMin);

    }

    int totalH = minAlarm / 60;

    int totalM = minAlarm % 60;

    cout << totalH << " " << totalM << endl;

  }
  return 0;

}
```

