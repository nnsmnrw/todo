
# Moderate Modular Mode题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定两个**偶数** $x,y$
求一个 $n \in [1,2\times10^{18}]$ 满足 $n \bmod x = y \bmod n$
一个测试点有多组数据，数据保证有解



YouKn0wWho has two even integers $ x $ and $ y $ . Help him to find an integer $ n $ such that $ 1 \le n \le 2 \cdot 10^{18} $ and $ n \bmod x = y \bmod n $ . Here, $ a \bmod b $ denotes the remainder of $ a $ after division by $ b $ . If there are multiple such integers, output any. It can be shown that such an integer always exists under the given constraints.

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 10^5 $ ) — the number of test cases.
The first and only line of each test case contains two integers $ x $ and $ y $ ( $ 2 \le x, y \le 10^9 $ , both are even).

#### 输出格式：

For each test case, print a single integer $ n $ ( $ 1 \le n \le 2 \cdot 10^{18} $ ) that satisfies the condition mentioned in the statement. If there are multiple such integers, output any. It can be shown that such an integer always exists under the given constraints.

#### 样例输入输出：

| 样例1输入                                     | 样例1输出                    |
| --------------------------------------------- | ---------------------------- |
| 4<br/>4 8<br/>4 2<br/>420 420<br/>69420 42068 | 4<br/>10<br/>420<br/>9969128 |

#### 样例解释：

In the first test case, $ 4 \bmod 4 = 8 \bmod 4 = 0 $ .
In the second test case, $ 10 \bmod 4 = 2 \bmod 10 = 2 $ .
In the third test case, $ 420 \bmod 420 = 420 \bmod 420 = 0 $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
