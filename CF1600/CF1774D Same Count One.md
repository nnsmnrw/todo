
# 相似数组（same.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

​	给定 $n$ 个长度为 $m$ 且只包含 $0$ 和 $1$ 的数组，每次操作可以交换任意两个数组对应位置 $pos$ 上的数。目标是使每个数组中的 $1$ 数量相等，求最小操作次数并输出操作过程。如果答案不存在则输出 $ -1 $ 。

#### 输入格式：

第一行输入整数 $ t $ ( $ 1 \leq t \leq 2\cdot 10^4 $ ) 表示样例组数；
每组样例第一行输入两个整数 $ n $ 和 $ m $ ( $ 2 \leq n \leq 10^5 $ , $ 2 \leq m \leq 10^5 $ )，以下 $ n $ 行每行包含 $ m $ 个整数 $ a_{i, 1}, a_{i, 2}, \ldots, a_{i, m} $ $ (0 \le a_{i, j} \le 1) $ ，分别表示每个数组的元素。保证每组输入中 $ n \cdot m $ 不超过 $ 10^6 $ 。

#### 输出格式：

对于每组样例，如果无法满足要求输出 $ -1 $ ；否则第一行输出一个整数 $ k $ $ (0 \le k \le mn) $ 表示最少操作次数，以下 $ k $ 行每行输出 $ 3 $ 个整数 $ x_i, y_i, z_i $ $ (1 \le x_i, y_i \le n, 1 \le z_i \le m) $ ，表示该次操作交换了 $ a_{x_i, z_i}, a_{y_i, z_i} $ 两个整数，即第 $ x_i $ 个数组和第 $ y_i $ 个数组中的第 $ z_i $ 个元素。

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                          |
| ------------------------------------------------------------ | ---------------------------------- |
| 3<br/>3 4<br/>1 1 1 0<br/>0 0 1 0<br/>1 0 0 1<br/>4 3<br/>1 0 0<br/>0 1 1<br/>0 0 1<br/>0 0 0<br/>2 2<br/>0 0<br/>0 1 | 1<br/>2 1 1<br/>1<br/>4 2 2<br/>-1 |

<div STYLE="page-break-after: always;"/>

#### 题解：考察代码实现
首先当 $1$ 的数量不是 $n$ 的倍数时，答案不存在；
否则，超过平均数的数组中，每个多出来的 $1$ 至少要操作一次，我们将超过平均数的数组和低于平均数的数组分成两类，显然，每次选择一个超过平均数的数组和一个低于平均数的数组，可以通过若干次操作至少让其中一个数组中 $1$ 的个数变为平均数，并且这些操作中， $1$ 和  $0$ 的变化一定是单向（从超过平均数的数组到低于平均数的数组）的。所以通过这种策略，可以使操作次数最少。

#### 参考核心代码：

```c++
void solve(){
    scanf("%d%d",&n,&m);
    init();
    for(int i=0;i<n;i++){
        int tmp=0;
        for(int j=0;j<m;j++){
            int x;scanf("%d",&x);
            a[i].push_back(x);
            sum+=x,tmp+=x;
        }
        cnt.push_back(tmp);
    }
    if(sum%n!=0){
        puts("-1");
        return;
    }
    sum/=n;
    for(int i=0;i<m;i++){
        locmore.clear(),locless.clear();
        for(int j=0;j<n;j++){
            if(cnt[j]>sum&&a[j][i])locmore.push_back(j);
            if(cnt[j]<sum&&!a[j][i])locless.push_back(j);
        }
        int len=min(locmore.size(),locless.size());
        for(int j=0;j<len;j++){
            ans[++tot]=(node){locless[j],locmore[j],i};
            cnt[locmore[j]]--,cnt[locless[j]]++;
        }
    }
    printf("%d\n",tot);
    for(int i=1;i<=tot;i++)printf("%d %d %d\n",ans[i].x+1,ans[i].y+1,ans[i].z+1);
}
 
```

