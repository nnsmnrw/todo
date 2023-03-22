# 不互质序列（number.cpp）

时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定长度为 $n$ 的数列 $a_i$，判断数列中是否存在不互质的两个数，存在输出 "YES"，否则输出 "NO"。

#### 输入格式：

第一行输入整数 $ t $ ( $ 1 \le t \le 10^5 $ ) 表示样例组数；
每组样例第一行输入整数 $ n $ ( $ 2 \le n \le 10^5 $ ) 表示数列长度，第二行依次输入数列中的每个数 $ a_1, a_2, \dots, a_n $ ( $ 1 \le a_i \le 10^9 $ )；
保证每组样例中所有 $ n $ 的和不超过 $ 10^5 $ 。

#### 输出格式：

对于每组样例，输出"YES"或者"NO"。

#### 样例输入输出：

| 样例1输入                            | 样例1输出  |
| ------------------------------------ | ---------- |
| 2<br/>3<br/>32 48 7<br/>3<br/>14 5 9 | YES<br/>NO |

<div STYLE="page-break-after: always;"/>

#### 题解：筛法的灵活运用，质数个数

类似筛法，每一轮筛的时候如果遇到数列中的两个数，则输出YES，如果不出现这样的情况则输出NO，注意质数只选 $sqrt(V)$ 以内的数， $V$ 是值域。

#### 参考代码：

```c++
#include<bits/stdc++.h>
using namespace std;
const int N=1e5+10,M=3.5e4+10;
int n,a[N],isp[M],pri[M],cnt,ans,num[M]; map<int,int> mp;

inline void preworks(){
    for(int i=2;i<M;++i){
        if(!isp[i]) pri[++cnt]=i;
        for(int j=1;j<=cnt&&i*pri[j]<M;++j){
            isp[i*pri[j]]=1;
            if(!(i%pri[j])) break;
        }
    }
}

signed main(){
    preworks();
    for(int T=read();T;--T){
        n=read(),mp.clear(),ans=0;
        for(int i=1;i<=n;++i) a[i]=read();
        for(int i=1;i<=n;++i){
            for(int j=1;j<=cnt&&pri[j]<=a[i];++j) // 处理 <=sqrt(V) 的因数。
                if(!(a[i]%pri[j])){
                    ++num[j];
                    while(!(a[i]%pri[j])) a[i]/=pri[j];
                }
            if(a[i]>1){
                // 剩下的就是那个大于 sqrt(V) 的因数。
                if(mp[a[i]]){ans=1;break;} mp[a[i]]=1;
            }
        }
        for(int i=1;i<=cnt;++i) ans|=(num[i]>=2),num[i]=0;
        puts(ans?"YES":"NO");
    }
    return 0;
}
```
