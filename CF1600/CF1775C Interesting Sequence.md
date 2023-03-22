
## 序列按位与（sequence.cpp）—CF1775C—1600
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给两个数，$n$ 和 $x$，问是否存在 $m$，使得 $n \&n+1 \&…… \&m = x$，如果存在求出最小的 $m$，否则输出 $-1$。

#### 输入格式：

第一行输入整数 $ t $ ( $ 1 \le t \le 2000 $ ) 表示样例组数；
每组样例包含两个整数 $ n $ , $ x $ ( $ 0\le n, x \le 10^{18} $ )，见题目描述。

#### 输出格式：

对于每组样例根据情况输出 $ m $ 或者 $ -1 $ ；如果 $ m $ 存在，保证其不超过 $ 5 \cdot 10^{18} $ 。

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                                       |
| ------------------------------------------------------------ | ----------------------------------------------- |
| 5<br/>10 8<br/>10 10<br/>10 42<br/>20 16<br/>1000000000000000000 0 | 12<br/>10<br/>-1<br/>24<br/>1152921504606846976 |

#### 样例解释：

样例1： $ 10\ \&\ 11 = 10 $ 但是 $ 10\ \&\ 11\ \&\ 12 = 8 $ ，所以答案是 $ 12 $ ；
样例2： $ 10 = 10 $ ，所以答案是 $ 10 $ ；
样例3：我们可以知道答案不存在，所以输出 $ -1 $ 。

<div STYLE="page-break-after: always;"/>

#### 题解：考察二进制运算的综合运用

如果 $n\& x \not= x $，则答案一定不存在；否则从低到高枚举 $n$ 的每一位，如果 $n$ 的这一位为 $0$，$x$ 的这一位为 $1$ ，则答案不存在，如果 $n$ 的这一位为 $1$，$x$ 的这一位为 $0$ ，则存在 $n+k$ 的这一位为  $0$，如果 $n$ 和 $x$ 的这一位均为 $1$，则 $n+k$ 不存在更高位的新的 $0$ （对应 $n$ 的这一位为 $1$） 。

####  参考代码：

```c++
#include<bits/stdc++.h>
#define ll long long
#define pb push_back
#define ld long double
#define f first
#define s second
using namespace std;
const ll inf = (1ll << 62);
int main() {
    ios_base::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);
    ll t;
    cin >> t;
    while(t--) {
        ll n, x;
        cin >> n >> x;
        ll ma = n, mi = inf;
        ll mask = 0;
        for(ll i = 0; i < 61; i++) {
            if(!((n >> i) & 1)) { // n的这一位是 0
                if((x >> i) & 1) {// x的这一位是 1
                    mi = -1;	  // -1
                    break;
                }
            } else {			// n的这一位是 1
                ll now = n + (1ll << i) - (n & mask);
                if((x >> i) & 1) {
                    mi = min(mi, now);
                } else {
                    ma = max(ma, now);
                }
            }
            mask += (1ll << i);
        }
        if(ma < mi) cout << ma << '\n';
        else cout << "-1\n";
    }
	return 0;
}
```
