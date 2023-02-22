# 相同频率（Equal.cpp）

时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给出长度为 $n$ 的只包含小写字母的字符串 $s$，请修改尽量少的字符，使得每种出现过的字符出现次数相同。给出最优的修改次数和一种方案。

#### 输入格式：

第一行输入一个整数 $ t $ ( $ 1 \le t \le 10^4 $ ) 表示数据组数；每组数据有两行：第一行输入整数 $ n $ ( $ 1 \le n \le 10^5 $ ) 表示字符串 $ s $ 的长度，第二行输入仅由小写字母组成的字符串 $ s $。数据保证单个样例所有字符串的长度之和不超过 $ 10^5 $ 。

#### 输出格式：

每组数据输出两行，分别表示最优修改次数和修改方案，如果方案有多种，输出一种即可。保证数据有解。

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 4<br/>5<br/>hello<br/>10<br/>codeforces<br/>5<br/>eevee<br/>6<br/>appall | 1<br/>helno<br/>2<br/>codefofced<br/>1<br/>eeeee<br/>0<br/>appall |

<div STYLE="page-break-after: always;"/>

#### 题解：排序、整除、验证法

出现次数相同，那么出现次数和字母个数一定是字符串长度的因数，枚举因数找最优解即可。

#### 参考代码：

```c++
#include <bits/stdc++.h>
using namespace std;
#define int long long
int n;
string s;
int cnt[26];
struct Node
{
    int id, cnt;
} v[26];
bool cmp(Node a, Node b)
{
    return a.cnt > b.cnt;
}
signed main()
{
    int t;
    ios::sync_with_stdio(false);
    cin.tie(0);
    cout.tie(0);
    cin >> t;
    while (t--)
    {
        cin >> n >> s;
        fill(cnt, cnt + 26, 0);
        for (int i = 0; i < s.length(); ++i)
            ++cnt[s[i] - 'a'];
        int ans = 0x3f3f3f3f3f3f3f3fll, ansid = 0;
        for (int i = 0; i < 26; ++i)
            v[i] = {i, cnt[i]}; // 记录出现次数
        sort(v, v + 26, cmp); // 排序
        for (int used = 1; used <= 26; ++used)
        { // 枚举使用的字母个数 k
            if (n % used != 0)
                continue;
            int m = n / used; // n / k
            int now = 0;
            for (int i = 0; i < used; ++i)
                now += abs(v[i].cnt - m); // 前 k 个字母的目标为 n / k
            for (int i = used; i < 26; ++i)
                now += v[i].cnt; // 剩余字母的目标为 0
            now /= 2; // 每次修改可以改变 2 个出现次数
            ans = min(ans, now);
            if (ans == now)
                ansid = used;
        }
        cout << ans << '\n'; // 先输出修改次数，下面进行构造
        for (int i = 0; i < ansid; ++i)
            cnt[v[i].id] = n / ansid;
        for (int i = ansid; i < 26; ++i)
            cnt[v[i].id] = 0; // 保存目标出现次数
        for (int i = 0; i < s.length(); ++i)
        {
            bool vis = false;
            for (int j = 0; j < ansid; ++j)
                if (v[j].id == s[i] - 'a')
                {
                    vis = true;
                    break;
                } // 判断当前字母可不可以保留
            if (!vis)
                s[i] = '\0'; // 因为当前字母不在前 k 种里，所以不能保留
            else if (cnt[s[i] - 'a'])
                --cnt[s[i] - 'a'];
            else
                s[i] = '\0'; // 因为当前字母出现次数过多，所以不能保留
        }
        for (int i = 0; i < s.length(); ++i)
        {
            if (s[i] != '\0')
                continue; // 对不能保留的字母重新分配
            int vis = -1;
            for (int j = 0; j < ansid; ++j)
                if (cnt[v[j].id])
                {
                    vis = v[j].id; // 找到还有空余的字母
                    break;
                }
            s[i] = vis + 'a'; // 进行分配
            --cnt[vis];
        }
        cout << s << '\n';
    }
    cout.flush();
    return 0;
}
```

