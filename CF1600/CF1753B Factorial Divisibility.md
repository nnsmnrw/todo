
# 阶乘整除（factorial.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定两个正整数 $n$ 和 $x$ 和一个正整数序列 $ a_1, a_2, \ldots, a_n $ 。
请问 $\sum_{i = 1}^n a_i!$ 是否能被 $x!$ 整除。如果能则输出一个字符串 $\texttt{Yes}$，不能则输出字符串 $\texttt{No}$。

#### 输入格式：

第一行输入两个整数 $ n $ 和 $ x $ ( $ 1 \le n \le 500\,000 $ , $ 1 \le x \le 500\,000 $ )；
第二行依次输入 $ n $ 个整数 $ a_1, a_2, \ldots, a_n $ ( $ 1 \le a_i \le x $ ) 。

#### 输出格式：

如果可以整除输出 $\texttt{Yes}$，否则输出 $\texttt{No}$。

#### 样例输入输出：

| 样例1输入输出       | 样例2输入输出           | 样例3输入输出         | 样例4输入输出                  | 样例5输入输出              |
| ------------------- | ----------------------- | --------------------- | ------------------------------ | -------------------------- |
| 6 4<br/>3 2 2 2 3 3 | 8 3<br/>3 2 2 2 2 2 1 1 | 7 8<br/>7 7 7 7 7 7 7 | 10 5<br /> 4 3 2 1 4 3 2 4 3 4 | 2 500000<br/>499999 499999 |
| Yes                 | Yes                     | No                    | No                             | No                         |

<div STYLE="page-break-after: always;"/>

#### 题解：阶乘、整除

$(n+1)*n!=(n+1)!$  ，统计每个阶乘出现的次数，从小到大处理进位即可。

#### 参考代码：

```c++
#include <bits/stdc++.h>
using namespace std;
int cnt[500005];
int main()
{
	ios::sync_with_stdio(false);
	int n, x;
	cin >> n >> x;
	for (int i = 1; i <= n; i++)
	{
		int a;
		cin >> a;
		cnt[a]++; //统计
	}
	for (int i = 1; i < x; i++) cnt[i + 1] += (cnt[i] / (i + 1)), cnt[i] %= (i + 1); //"进位"
	for (int i = 1; i < x; i++)
		if (cnt[i])
		{
			cout << "No";
			return 0;
		}
	if (cnt[x]) cout << "Yes";
	else cout << "No";
	return 0;
}
```
