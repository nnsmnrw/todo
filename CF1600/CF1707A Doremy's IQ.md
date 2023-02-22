
# Doremy's IQ题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

哆来咪·苏伊特参加了 $n$ 场比赛。 比赛 $i$ 只能在第 $i$ 天进行。比赛 $i$ 的难度为 $a_i$。最初，哆来咪的 IQ 为 $q$ 。 在第 $i$ 天，哆来咪将选择是否参加比赛 i。只有当她当前的 IQ 大于 $0$ 时，她才能参加比赛。
如果哆来咪选择在第 $i$ 天参加比赛 $i$，则会发生以下情况：

- 如果 $a_i\gtq$，哆来咪会觉得自己不够聪明，所以 $q$ 将会减 $1$；
- 否则，什么都不会改变。
    如果她选择不参加比赛，一切都不会改变。哆来咪想参加尽可能多的比赛。请给哆来咪一个解决方案。



第一行包含一个正整数 $t$ ($1\le t\le10^4$) ，表示测试数据的组数。
第二行包含两个整数 $n$ 和 $q$ ($1\le n\le10^5$, $1\le q\le10^9$)，表示比赛次数和哆来咪最开始时的 IQ。
第三行包含 $n$ 个整数 $a_1,a_2⋯a_n$($1\le a_i≤10^9$)，表示每场比赛的难度。
数据保证 $n$ 之和不超过 $10^5$。



对于每组数据，输出一个二进制字符串 $s$，如果哆来咪应该选择参加比赛 $i$，则 $s_i=1$，否则 $s_i=0$。 字符串中 $1$ 的数量应该尽可能的多，并且当她的 IQ 为 $0$ 或更低时，她不应该参加比赛。
如果有多个解决方案，你可以输出任意一个。



在第一个测试用例中，哆来咪参加了唯一的比赛。她的 IQ 没有下降。
在第二个测试用例中，哆来咪参加了两个比赛。在参加比赛 $2$ 后，她的 IQ 下降了 $1$。
在第三个测试用例中，哆来咪参加了比赛 $1$ 和比赛 $2$。她的 IQ 在参加比赛 $2$ 后降至 $0$，因此她无法参加比赛 $3$。



Doremy is asked to test $ n $ contests. Contest $ i $ can only be tested on day $ i $ . The difficulty of contest $ i $ is $ a_i $ . Initially, Doremy's IQ is $ q $ . On day $ i $ Doremy will choose whether to test contest $ i $ or not. She can only test a contest if her current IQ is strictly greater than $ 0 $ .
If Doremy chooses to test contest $ i $ on day $ i $ , the following happens:

- if $ a_i\gtq $ , Doremy will feel she is not wise enough, so $ q $ decreases by $ 1 $ ;
- otherwise, nothing changes.
    If she chooses not to test a contest, nothing changes.Doremy wants to test as many contests as possible. Please give Doremy a solution.

#### 输入格式：

The input consists of multiple test cases. The first line contains a single integer $ t $ ( $ 1\le t\le 10^4 $ ) — the number of test cases. The description of the test cases follows.
The first line contains two integers $ n $ and $ q $ ( $ 1 \le n \le 10^5 $ , $ 1 \le q \le 10^9 $ ) — the number of contests and Doremy's IQ in the beginning.
The second line contains $ n $ integers $ a_1,a_2,\cdots,a_n $ ( $ 1 \le a_i \le 10^9 $ ) — the difficulty of each contest.
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 10^5 $ .

#### 输出格式：

For each test case, you need to output a binary string $ s $ , where $ s_i=1 $ if Doremy should choose to test contest $ i $ , and $ s_i=0 $ otherwise. The number of ones in the string should be maximum possible, and she should never test a contest when her IQ is zero or less.
If there are multiple solutions, you may output any.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                           |
| ------------------------------------------------------------ | ----------------------------------- |
| 5<br/>1 1<br/>1<br/>2 1<br/>1 2<br/>3 1<br/>1 2 1<br/>4 2<br/>1 4 3 1<br/>5 2<br/>5 1 2 4 3 | 1<br/>11<br/>110<br/>1110<br/>01111 |

#### 样例解释：

In the first test case, Doremy tests the only contest. Her IQ doesn't decrease.
In the second test case, Doremy tests both contests. Her IQ decreases by $ 1 $ after testing contest $ 2 $ .
In the third test case, Doremy tests contest $ 1 $ and $ 2 $ . Her IQ decreases to $ 0 $ after testing contest $ 2 $ , so she can't test contest $ 3 $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
