
# Tree Infection题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

一个树是一个无环连通图。一个有根树有一个被称作“根结点”的结点。对于任意一个非根结点 $v$ ，其父结点是从根结点到结点 $v$ 最短路径上的前一个结点。结点 $v$ 的子结点包括所有以 $v$ 父结点为 $v$ 的结点。
给定一个有 $n$ 个结点的有根树。结点 $1$ 即为根结点。一开始，该树上所有结点均是“健康”的。
每一秒你会进行两次操作——先是传播操作，然后是注射操作，定义如下。

- 传播操作：对于每个结点 $v$ ，若该结点至少有一个子结点被“感染”，则你可以“感染”顶点 $v$ 任意一个其他的子结点。
- 注射：你可以选择任意一个“健康”的结点并使它变为“感染”状态。
    这程每秒会重复一次知道整个树的结点都处于“感染”状态。你需要找到使整个树被“感染”的最短时间（秒数）。



有多个测试数据。第一行输入整数 $t$ ，代表有 $t$ 组数据。每组数据格式如下。
第一行给定整数 $n$ ，表示整个树共有 $n$ 个结点。
第二行输入 $n-1$ 个整数 $p_{2...i-1}$ ，第 $p_i$ 个整数表示 $i$ 号结点的父节点是 $p_i$ 号结点。



共 $t$ 行，每行一个整数，即使整个树被“感染”的最短时间（秒数）。



- $ 1 \le t \le 10^4 $
- $ 2 \le n \le 2 \times 10^5 $
- $ 1 \le p_i \le n $
- $ \sum \limits_{i=1} ^t n_i \le 2 \times 10^5 $



A tree is a connected graph without cycles. A rooted tree has a special vertex called the root. The parent of a vertex $ v $ (different from root) is the previous to $ v $ vertex on the shortest path from the root to the vertex $ v $ . Children of the vertex $ v $ are all vertices for which $ v $ is the parent.
You are given a rooted tree with $ n $ vertices. The vertex $ 1 $ is the root. Initially, all vertices are healthy.
Each second you do two operations, the spreading operation and, after that, the injection operation:

1. Spreading: for each vertex $ v $ , if at least one child of $ v $ is infected, you can spread the disease by infecting at most one other child of $ v $ of your choice.
2. Injection: you can choose any healthy vertex and infect it.
    This process repeats each second until the whole tree is infected. You need to find the minimal number of seconds needed to infect the whole tree.

#### 输入格式：

The input consists of multiple test cases. The first line contains a single integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases. Description of the test cases follows.
The first line of each test case contains a single integer $ n $ ( $ 2 \le n \le 2 \cdot 10^5 $ ) — the number of the vertices in the given tree.
The second line of each test case contains $ n - 1 $ integers $ p_2, p_3, \ldots, p_n $ ( $ 1 \le p_i \le n $ ), where $ p_i $ is the ancestor of the $ i $ -th vertex in the tree.
It is guaranteed that the given graph is a tree.
It is guaranteed that the sum of $ n $ over all test cases doesn't exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case you should output a single integer — the minimal number of seconds needed to infect the whole tree.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                 |
| ------------------------------------------------------------ | ------------------------- |
| 5<br/>7<br/>1 1 1 2 2 4<br/>5<br/>5 5 1 4<br/>2<br/>1<br/>3<br/>3 1<br/>6<br/>1 1 1 1 1 | 4<br/>4<br/>2<br/>3<br/>4 |

#### 样例解释：



<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```






#### 输出格式


#### 输入输出样例
#### 输入样例 #1

#### 输出样例 #1

#### 说明
The image depicts the tree from the first test case during each second.
A vertex is black if it is not infected. A vertex is blue if it is infected by injection during the previous second. A vertex is green if it is infected by spreading during the previous second. A vertex is red if it is infected earlier than the previous second.
![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF1665C/cdb9fb6598e0de49d63d1e50d0cfca55c1b5511e.png)Note that you are able to choose which vertices are infected by spreading and by injections.
