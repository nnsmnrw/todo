
# 零前缀和（sum.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定长为 $n$ 的数列 $a$，每次操作你可以将数列中为 $0$ 的项改成任意整数。求最多能让多少个前缀和序列 $a_1+\dots+a_k$ 为 $0$，即 $a_1+\dots+a_k=0$。

#### 输入格式：

第一行输入整数 $ t $ ( $ 1 \le t \le 10^4 $ ) 表示样例组数；
每组样例第一行输入整数 $ n $ ( $ 1 \le n \le 2 \cdot 10^5 $ ) 表示数列 $ a $ 的长度；第二行依次输入序列中的每个数 $ a_1,a_2,\ldots,a_n $ ( $ -10^9 \le a_i \le 10^9 $ ) 。

#### 输出格式：

对于每组样例，输出最多的满足要求的前缀和数量。

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                 |
| ------------------------------------------------------------ | ------------------------- |
| 5<br/>5<br/>2 0 1 -1 0<br/>3<br/>1000000000 1000000000 0<br/>4<br/>0 0 0 0<br/>8<br/>3 0 2 -10 10 -30 30 0<br/>9<br/>1 0 0 1 -1 0 1 0 -1 | 3<br/>1<br/>4<br/>4<br/>5 |

<div STYLE="page-break-after: always;"/>

#### 题解：前缀和、众数

改变一个 $0$ 可以使它后面多个位置的前缀和变为 $0$ ，为了让变为 $0$ 的位置尽可能多，我们在修改的时候选择众数进行修改，即把 $0$ 修改为众数的相反数。那么可以影响多少个数呢？每个 $0$ 的影响范围在它和它后面一个 $0$ 之间。  

#### 参考代码：

```c++
#include<bits/stdc++.h>
#define fi first
#define se second
#define pii pair<int, int> 
#define pb push_back
#define IOS ios::sync_with_stdio(0), cin.tie(0), cout.tie(0);
#define int long long
using namespace std;

const int mod = 998244353;

void solve()
{
	int n, ans = 0;
	cin >> n;
	vector<int> a(n + 1), b(n + 1);
	for (int i = 1;i <= n;i++)
	{
		cin >> a[i];
		b[i] = a[i];
		b[i] += b[i - 1];
	}
	int i = 1;
	while (a[i] && i <= n) i++;
	for (int _ = 1;_ < i;_++)
	if (!b[_])
	ans++;
	for (;i <= n;)
	{
		int j = i + 1, Max = 1;
		map<int, int> mp;
		while (a[j] && j <= n) j++;
		for (int k = i ;k < j;k++)
		{
			mp[b[k]]++;
			Max = max(Max, mp[b[k]]);
		}
		i = j;
		ans += Max;
	}
	cout << ans << '\n';
}

signed main()
{
	IOS;
	int t;
	cin >> t;
	while (t--)
	{
		solve();
	}
}
```
