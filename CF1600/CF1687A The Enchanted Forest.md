
# The Enchanted Forest题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

其实这里被称为魔法森林，基本上就是因为这些有幻觉效果的蘑菇。光是接近这些蘑菇，就好像被施了魔法而产生幻觉。——《东方求闻史纪》
魔理沙来到了魔法森林采摘蘑菇。
魔法森林可以被抽象成一条有着 $n$ 个节点，从 $1$ 到 $n$ 标号的数轴。在魔理沙出发之前，她的好友帕秋莉运用魔法去侦测了每个节点上的蘑菇数量，分别为 $a_1,a_2,\dots,a_n$。
在第 $0$ 分钟的时候，魔理沙可以从任意一个节点出发。在每一分钟的时候，她将会做以下事情：

- 她将从节点 $x$ 移动到节点 $y$（$|x-y| \leq 1$，即 $y$ 可能等于 $x$）
- 她将会收集节点 $y$ 上的所有蘑菇。
- 魔法森林中每个节点会再生长出一个蘑菇。
    注意，她不能在第 $0$ 分钟的时候收集蘑菇。
    现在魔理沙希望知道她在前 $k$ 分钟的时候，最多能收集到多少个蘑菇。请你帮帮她。
    **输入格式**
    第一行输入一个正整数 $t(1 \leq t \leq 10^4)$，表示输入数据组数。
    对于每一组测试数据，第一行输入两个正整数 $n,k(1 \leq n \leq 2\times 10^5, 1\leq k \leq 10^9)$，含义如题目所述。
    第二行输入 $n$ 个正整数 $a_i$，表示每个节点上起初有的蘑菇数量。
    **输出格式**
    对于每组测试数据输出一行，表示魔理沙最多能收集到多少个蘑菇。

The enchanted forest got its name from the magical mushrooms growing here. They may cause illusions and generally should not be approached.
—Perfect Memento in Strict Sense
Marisa comes to pick mushrooms in the Enchanted Forest.
The Enchanted forest can be represented by $ n $ points on the $ X $ -axis numbered $ 1 $ through $ n $ . Before Marisa started, her friend, Patchouli, used magic to detect the initial number of mushroom on each point, represented by $ a_1,a_2,\ldots,a_n $ .
Marisa can start out at any point in the forest on minute $ 0 $ . Each minute, the followings happen in order:

- She moves from point $ x $ to $ y $ ( $ |x-y|\le 1 $ , possibly $ y=x $ ).
- She collects all mushrooms on point $ y $ .
- A new mushroom appears on each point in the forest.
    Note that she cannot collect mushrooms on minute $ 0 $ .
    Now, Marisa wants to know the maximum number of mushrooms she can pick after $ k $ minutes.

#### 输入格式：

Each test contains multiple test cases. The first line contains a single integer $ t $ ( $ 1 \leq t \leq 10^4 $ ) — the number of test cases. The description of the test cases follows.
The first line of each test case contains two integers $ n $ , $ k $ ( $ 1 \le n \le 2 \cdot 10 ^ 5 $ , $ 1\le k \le 10^9 $ ) — the number of positions with mushrooms and the time Marisa has, respectively.
The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ( $ 1 \le a_i \le 10^9 $ ) — the initial number of mushrooms on point $ 1,2,\ldots,n $ .
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2 \cdot 10 ^ 5 $ .

#### 输出格式：

For each test case, print the maximum number of mushrooms Marisa can pick after $ k $ minutes.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                            |
| ------------------------------------------------------------ | ------------------------------------ |
| 4<br/>5 2<br/>5 6 1 2 3<br/>5 7<br/>5 6 1 2 3<br/>1 2<br/>999999<br/>5 70000<br/>1000000000 1000000000 1000000000 1000000000 1000000000 | 12<br/>37<br/>1000000<br/>5000349985 |

#### 样例解释：

Test case 1:
Marisa can start at $ x=2 $ . In the first minute, she moves to $ x=1 $ and collect $ 5 $ mushrooms. The number of mushrooms will be $ [1,7,2,3,4] $ . In the second minute, she moves to $ x=2 $ and collects $ 7 $ mushrooms. The numbers of mushrooms will be $ [2,1,3,4,5] $ . After $ 2 $ minutes, Marisa collects $ 12 $ mushrooms.
It can be shown that it is impossible to collect more than $ 12 $ mushrooms.
Test case 2:
This is one of her possible moving path:
$ 2 \rightarrow 3 \rightarrow 2 \rightarrow 1 \rightarrow 2 \rightarrow 3 \rightarrow 4 \rightarrow 5 $
It can be shown that it is impossible to collect more than $ 37 $ mushrooms.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
