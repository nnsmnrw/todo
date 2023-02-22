
# Split Into Two Sets题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给你 $n$ （$n$ 为偶数，$2 \le 2 \cdot 10^5$）个，数对。数对中的每个数字都是从 $1$ 到 $n$ 的。
现在问你是否能将这些数对分到两个集合中。使得每个集合中没有任何一个重复的数字。
比如有下面这四个数对：$\{1, 4\}, \{1, 3\}, \{3, 2\}, \{4, 2\}$。
那么可以这样分配这些数对：

- 第一个集合包含数对 $\{1, 4\}$ 和 $\{3, 2\}$。第二个包含 $\{1, 3\}$ 和 $\{4, 2\}$。

Polycarp was recently given a set of $ n $ (number $ n $ — even) dominoes. Each domino contains two integers from $ 1 $ to $ n $ .
Can he divide all the dominoes into two sets so that all the numbers on the dominoes of each set are different? Each domino must go into exactly one of the two sets.
For example, if he has $ 4 $ dominoes: $ \{1, 4\} $ , $ \{1, 3\} $ , $ \{3, 2\} $ and $ \{4, 2\} $ , then Polycarp will be able to divide them into two sets in the required way. The first set can include the first and third dominoes ( $ \{1, 4\} $ and $ \{3, 2\} $ ), and the second set — the second and fourth ones ( $ \{1, 3\} $ and $ \{4, 2\} $ ).

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases.
The descriptions of the test cases follow.
The first line of each test case contains a single even integer $ n $ ( $ 2 \le n \le 2 \cdot 10^5 $ ) — the number of dominoes.
The next $ n $ lines contain pairs of numbers $ a_i $ and $ b_i $ ( $ 1 \le a_i, b_i \le n $ ) describing the numbers on the $ i $ -th domino.
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case print:

- YES, if it is possible to divide $ n $ dominoes into two sets so that the numbers on the dominoes of each set are different;
- NO if this is not possible.
    You can print YES and NO in any case (for example, the strings yEs, yes, Yes and YES will be recognized as a positive answer).

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                                |
| ------------------------------------------------------------ | ---------------------------------------- |
| 6<br/>4<br/>1 2<br/>4 3<br/>2 1<br/>3 4<br/>6<br/>1 2<br/>4 5<br/>1 3<br/>4 6<br/>2 3<br/>5 6<br/>2<br/>1 1<br/>2 2<br/>2<br/>1 2<br/>2 1<br/>8<br/>2 1<br/>1 2<br/>4 3<br/>4 3<br/>5 6<br/>5 7<br/>8 6<br/>7 8<br/>8<br/>1 2<br/>2 1<br/>4 3<br/>5 3<br/>5 4<br/>6 7<br/>8 6<br/>7 8 | YES<br/>NO<br/>NO<br/>YES<br/>YES<br/>NO |

#### 样例解释：

In the first test case, the dominoes can be divided as follows:

- First set of dominoes: $ [\{1, 2\}, \{4, 3\}] $
- Second set of dominoes: $ [\{2, 1\}, \{3, 4\}] $
    In other words, in the first set we take dominoes with numbers $ 1 $ and $ 2 $ , and in the second set we take dominoes with numbers $ 3 $ and $ 4 $ .In the second test case, there's no way to divide dominoes into $ 2 $ sets, at least one of them will contain repeated number.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
