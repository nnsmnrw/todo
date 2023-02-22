
# Interesting Sequence题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给两个数，$n$ 和 $x$，问是否存在 $m$，使得 $n \&amp; n+1 \&amp; …… \&amp; m = x$，如果存在求出最小的 $m$，否则输出 $-1$。

Petya and his friend, robot Petya++, like to solve exciting math problems.
One day Petya++ came up with the numbers $ n $ and $ x $ and wrote the following equality on the board: $ $$$n\ \&amp;\ (n+1)\ \&amp;\ \dots\ \&amp;\ m = x, $ $ where $ \\&amp;amp; $ denotes the \lta href="https://en.wikipedia.org/wiki/Bitwise_operation#AND"\gtbitwise AND operation\lt/a\gt. Then he suggested his friend Petya find such a minimal $ m $ ( $ m \\ge n$$$) that the equality on the board holds.
Unfortunately, Petya couldn't solve this problem in his head and decided to ask for computer help. He quickly wrote a program and found the answer.
Can you solve this difficult problem?
![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF1775C/3708862555546ebb5c352c2d2207eacbd490398b.png)

#### 输入格式：

Each test contains multiple test cases. The first line contains the number of test cases $ t $ ( $ 1 \le t \le 2000 $ ). The description of the test cases follows.
The only line of each test case contains two integers $ n $ , $ x $ ( $ 0\le n, x \le 10^{18} $ ).

#### 输出格式：

For every test case, output the smallest possible value of $ m $ such that equality holds.
If the equality does not hold for any $ m $ , print $ -1 $ instead.
We can show that if the required $ m $ exists, it does not exceed $ 5 \cdot 10^{18} $ .

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                                       |
| ------------------------------------------------------------ | ----------------------------------------------- |
| 5<br/>10 8<br/>10 10<br/>10 42<br/>20 16<br/>1000000000000000000 0 | 12<br/>10<br/>-1<br/>24<br/>1152921504606846976 |

#### 样例解释：

In the first example, $ 10\ \&amp;\ 11 = 10 $ , but $ 10\ \&amp;\ 11\ \&amp;\ 12 = 8 $ , so the answer is $ 12 $ .
In the second example, $ 10 = 10 $ , so the answer is $ 10 $ .
In the third example, we can see that the required $ m $ does not exist, so we have to print $ -1 $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
