
# Tokitsukaze and Strange Inequality题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给一个长度为 $n$ 的排列，求有多少个四元组 $(a,b,c,d)$ 满足 $a\ltb\ltc\ltd$ 和 $p_a\ltp_c$、$p_b\gtp_d$。
$n\le 5000$

Tokitsukaze has a permutation $ p $ of length $ n $ . Recall that a permutation $ p $ of length $ n $ is a sequence $ p_1, p_2, \ldots, p_n $ consisting of $ n $ distinct integers, each of which from $ 1 $ to $ n $ ( $ 1 \leq p_i \leq n $ ).
She wants to know how many different indices tuples $ [a,b,c,d] $ ( $ 1 \leq a \lt b \lt c \lt d \leq n $ ) in this permutation satisfy the following two inequalities:
$ p_a \lt p_c $ and $ p_b \gt p_d $ . Note that two tuples $ [a_1,b_1,c_1,d_1] $ and $ [a_2,b_2,c_2,d_2] $ are considered to be different if $ a_1 \ne a_2 $ or $ b_1 \ne b_2 $ or $ c_1 \ne c_2 $ or $ d_1 \ne d_2 $ .

#### 输入格式：

The first line contains one integer $ t $ ( $ 1 \leq t \leq 1000 $ ) — the number of test cases. Each test case consists of two lines.
The first line contains a single integer $ n $ ( $ 4 \leq n \leq 5000 $ ) — the length of permutation $ p $ .
The second line contains $ n $ integers $ p_1, p_2, \ldots, p_n $ ( $ 1 \leq p_i \leq n $ ) — the permutation $ p $ .
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 5000 $ .

#### 输出格式：

For each test case, print a single integer — the number of different $ [a,b,c,d] $ tuples.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出      |
| ------------------------------------------------------------ | -------------- |
| 3<br/>6<br/>5 3 6 1 4 2<br/>4<br/>1 2 3 4<br/>10<br/>5 1 6 2 8 3 4 10 9 7 | 3<br/>0<br/>28 |

#### 样例解释：

In the first test case, there are $ 3 $ different $ [a,b,c,d] $ tuples.
$ p_1 = 5 $ , $ p_2 = 3 $ , $ p_3 = 6 $ , $ p_4 = 1 $ , where $ p_1 \lt p_3 $ and $ p_2 \gt p_4 $ satisfies the inequality, so one of $ [a,b,c,d] $ tuples is $ [1,2,3,4] $ .
Similarly, other two tuples are $ [1,2,3,6] $ , $ [2,3,5,6] $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
