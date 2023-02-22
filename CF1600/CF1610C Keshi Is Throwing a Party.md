
# Keshi Is Throwing a Party题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

蓝举办了一场宴会，她希望邀请她的朋友们赴宴，并且每个人都能开心。
她一共有 $n$ 位朋友，第 $i$ 位朋友有 $i$ 单位的钱。
若第 $i$ 位朋友赴宴，那么她会感到开心，当且仅当宴会上的人中至多有 $a_i$ 人比她富有（也就是钱严格比她多），至多有 $b_i$ 人比她贫困（也就是钱严格比她少）。
宴会当然是越热闹越好，所以蓝想要邀请尽可能多的人。你现在要帮助她算出她最多能邀请的人数。
本题多组数据，数据组数为 $t$，会在输入的开头给出。对于每组数据，蓝会依次给出 $n$ 和序列 $a,b$，其意义同题目描述所述。你需要输出她最多能邀请的人数。
题目数据满足：$1 \leq t \leq 10^4$，$1 \leq n \leq 2\times10^5$，$0 \leq a_i,b_i \lt n$，$1 \leq \sum n \leq 2\times10^5$。



Keshi is throwing a party and he wants everybody in the party to be happy.
He has $ n $ friends. His $ i $ -th friend has $ i $ dollars.
If you invite the $ i $ -th friend to the party, he will be happy only if at most $ a_i $ people in the party are strictly richer than him and at most $ b_i $ people are strictly poorer than him.
Keshi wants to invite as many people as possible. Find the maximum number of people he can invite to the party so that every invited person would be happy.

#### 输入格式：

The first line contains a single integer $ t $ $ (1\le t\le 10^4) $ — the number of test cases. The description of the test cases follows.
The first line of each test case contains a single integer $ n $ $ (1\le n\le 2 \cdot 10^5) $ — the number of Keshi's friends.
The $ i $ -th of the following $ n $ lines contains two integers $ a_i $ and $ b_i $ $ (0 \le a_i, b_i \lt n) $ .
It is guaranteed that the sum of $ n $ over all test cases doesn't exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case print the maximum number of people Keshi can invite.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出     |
| ------------------------------------------------------------ | ------------- |
| 3<br/>3<br/>1 2<br/>2 1<br/>1 1<br/>2<br/>0 0<br/>0 1<br/>2<br/>1 0<br/>0 1 | 2<br/>1<br/>2 |

#### 样例解释：

In the first test case, he invites the first and the second person. If he invites all of them, the third person won't be happy because there will be more than $ 1 $ person poorer than him.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
