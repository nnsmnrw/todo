
# 阶乘整除（factorial .cpp）
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

| 样例1输入输出       | 样例2输入输出           | 样例3输入输出         | 样例4输入输出                                                | 样例5输入输出              |
| ------------------- | ----------------------- | --------------------- | ------------------------------------------------------------ | -------------------------- |
| 6 4<br/>3 2 2 2 3 3 | 8 3<br/>3 2 2 2 2 2 1 1 | 7 8<br/>7 7 7 7 7 7 7 | xxxxxxxxxx40 1#include<bits/stdc++.h>2using namespace std;3#define int long long4int a[200005];5int t,n,m,i,k,s;6signed main()7{8    scanf("%lld",&t);9    while(t--)10    {11        scanf("%lld%lld",&n,&m);k=s=0;12        priority_queue<int> q1;//大根优先队列13        priority_queue<int,vector<int>,greater<int> > q2;//小根优先队列14        for(i=1;i<=n;i++) scanf("%lld",&a[i]);15        if(n==1) puts("0");continue;16        for(i=m;i>1;i--)//不能为017        {18            k+=a[i];19            q1.push(a[i]);20            if(k>0)//需要修改21            {22                k-=q1.top()*2ll;//最大值 x 取反后对 k 的贡献减小 2*x23                q1.pop();s++;24            }25        }26        k=0;27        for(i=m+1;i<=n;i++)28        {29            k+=a[i];30            q2.push(a[i]);31            if(k<0)//需要修改32            {33                k-=q2.top()*2ll;34                q2.pop();s++;35            }36        }37        printf("%lld\n",s);38    }39    return 0;40}c++ | 2 500000<br/>499999 499999 |
| Yes                 | Yes                     | No                    | No                                                           | No                         |

<div STYLE="page-break-after: always;"/>

#### 题解：阶乘、整除



#### 参考代码：

```c++

```
