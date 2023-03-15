
# 阻断病毒（vertices.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定一棵以$1$ 号节点为根的二叉树，总节点个数为 $n$。
现在 $1$ 号节点感染了病毒，病毒每一回合都会去感染与该节点直接相连的节点，而你在这一回合里可以选择删除任意一个没有被病毒感染（尚未被删除）的点，这样就断开了它与其直接相连的点得关系.
询问最多可以有多少不被病毒感染的点，被删除的点不算做不被病毒感染的点。

#### 输入格式：

第一行输入整数 $ t $ ( $ 1\leq t\leq 5000 $ ) 表示样例组数；
每组样例第一行输入整数 $ n $ ( $ 2\leq n\leq 3\cdot 10^5 $ ) 表示结点数；以下 $ n-1 $ 行每行两个整数 $ u_i $ 和 $ v_i $ ( $ 1 \leq u_i, v_i \leq n $ )，表示两点之间有一条边。保证树根为 $ 1 $ 号结点，并且一组输入中所有 $ n $ 的和不超过 $ 3\cdot 10^5 $ 。

#### 输出格式：

对于每组样例，输出一个整数表示不被感染的最多结点数。

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出            |
| ------------------------------------------------------------ | -------------------- |
| 4<br/>2<br/>1 2<br/>4<br/>1 2<br/>2 3<br/>2 4<br/>7<br/>1 2<br/>1 5<br/>2 3<br/>2 4<br/>5 6<br/>5 7<br/>15<br/>1 2<br/>2 3<br/>3 4<br/>4 5<br/>4 6<br/>3 7<br/>2 8<br/>1 9<br/>9 10<br/>9 11<br/>10 12<br/>10 13<br/>11 14<br/>11 15 | 0<br/>2<br/>2<br/>10 |

<div STYLE="page-break-after: always;"/>

#### 题解：

病毒必须走到叶子结点或者只有一个子结点时才能截断，所以从上往下搜索这样的结点即可。

#### 参考代码：

```c++
#include<bits/stdc++.h>
using namespace std;
vector<int> head[300005];
int deep[300005];
void solve()
{
    int n,u,v;
    cin>>n;
    for(int i=1;i<n;i++)
    {
        cin>>u>>v;
        head[u].push_back(v);
        head[v].push_back(u);
    }
    queue<int> q;
    q.push(1);
    deep[1]=1;
    int pre=1,out=2,flag=1;
    while(q.size())
    {
        int u=q.front();q.pop();
        if(deep[u]!=pre&&out<2)    // 新的一层
        {
            if(out==1)
            {     
                
                flag=0;  
                cout<<n-pre*2<<endl;
                break;
            }
            else if(out==0)
            {
                flag=0;
                cout<<n-pre*2+1<<endl;
                break;
            }
        }
        pre=deep[u];
        int uo=head[u].size();
        if(u!=1) uo--;
        out=min(uo,out);
        for(int i=0;i<head[u].size();i++)
        {
            int v=head[u][i];
            if(deep[v]) continue;
            deep[v]=deep[u]+1;
            q.push(v);
        }
    }
    if(flag) cout<<n-pre*2+1<<endl;
    while(q.size()) q.pop();
    for(int i=1;i<=n;i++) 
    {
        vector<int> temp;
        head[i].swap(temp);
    }
    memset(deep,0,sizeof(deep));
}
int main()
{
    int t;
    cin>>t;
    while(t--) solve();
    return 0;
}
```
