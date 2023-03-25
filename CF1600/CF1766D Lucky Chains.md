
# 幸运链条（chains.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

当数对 $ (x, y) $ 中 $ \gcd(x, y) = 1 $ 时，我们称之为幸运数对；当 $ (x, y) $ , $ (x + 1, y + 1) $ , $ (x + 2, y + 2) $ , $ \dots $ , $ (x + k, y + k) $ 在 $ k \ge 0 $ 的情况下都是幸运数对时，我们称之为幸运链条。给定 $ n $ 对 $ (x_i, y_i) $ ，求出每个数对为起点时最长的幸运链条长度。如果 $ (x_i, y_i) $ 本身不是幸运数对，那对应的幸运链条长度为 $ 0 $ 。

#### 输入格式：

第一行输入整数 $ n $ ( $ 1 \le n \le 10^6 $ ) 表示数对个数；
以下 $ n $ 行每行包含两个整数 $ x_i $ 和 $ y_i $ ( $ 1 \le x_i \lt y_i \le 10^7 $ ) 表示数对。

#### 输出格式：

输出 $ n $ 行 $ n $ 个整数，分别表示每个数对 $ (x_i, y_i) $ 的最长幸运链条长度，如果长度为无穷则输出 $ -1 $ 。

#### 样例输入输出：

| 样例1输入                                        | 样例1输出             |
| ------------------------------------------------ | --------------------- |
| 4<br />5 15<br />13 37<br />8 9<br />10009 20000 | 0<br/>1<br/>-1<br/>79 |

<div STYLE="page-break-after: always;"/>

#### 题解：辗转相除，整除

目标是 $\gcd(x+k,y+k)>1$，那么 $\gcd(x+k,y+k)=\gcd(y-x,x+k)>1$，寻找$y-k$ 的质因数即可。

#### x 1#include<bits/stdc++.h>2using namespace std;3const int N=1e5+10,M=3.5e4+10;4int n,a[N],isp[M],pri[M],cnt,ans,num[M]; map<int,int> mp;5​6inline void preworks(){7    for(int i=2;i<M;++i){8        if(!isp[i]) pri[++cnt]=i;9        for(int j=1;j<=cnt&&i*pri[j]<M;++j){10            isp[i*pri[j]]=1;11            if(!(i%pri[j])) break;12        }13    }14}15​16signed main(){17    preworks();18    for(int T=read();T;--T){19        n=read(),mp.clear(),ans=0;20        for(int i=1;i<=n;++i) a[i]=read();21        for(int i=1;i<=n;++i){22            for(int j=1;j<=cnt&&pri[j]<=a[i];++j) // 处理 <=sqrt(V) 的因数。23                if(!(a[i]%pri[j])){24                    ++num[j];25                    while(!(a[i]%pri[j])) a[i]/=pri[j];26                }27            if(a[i]>1){28                // 剩下的就是那个大于 sqrt(V) 的因数。29                if(mp[a[i]]){ans=1;break;} mp[a[i]]=1;30            }31        }32        for(int i=1;i<=cnt;++i) ans|=(num[i]>=2),num[i]=0;33        puts(ans?"YES":"NO");34    }35    return 0;36}c++

```c++
#include<bits/stdc++.h>
using namespace std;
#define ll long long
ll gcd(ll a,ll b)
{
    if(b==0) return a;
    return gcd(b,a%b);
}
void solve()
{
    ll x,y;
    cin>>x>>y;
    if(gcd(x,y)>1) 
    {
        puts("0");
        return;
    } 
    if(x%2==1&&y%2==1)
    {
        puts("1");
        return;
    } 
    if(x>y) swap(x,y);
    ll delta=y-x;
    if(delta==1)  puts("-1");
    else 
    {
        ll g=-1;
        ll sq=sqrt(delta);
        for(int i=2;i<=delta;i++)
        {
            if(delta%i==0)
            {
                g=i;
                break;
            } 
        }
        if(g==-1) g=delta;
        cout<<(ll)(ceil(x*1.0/g))*g-x<<endl;
    }
}
int main()
{
    int t;
    cin>>t;
    while(t--) solve();
    return 0;
}
```
