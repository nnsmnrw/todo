
# Set or Decrease题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给你一个长度为 $n(1 \leq n \leq 2 \cdot 10^5)$ 的序列 $a_1,a_2,...,a_n(1 \leq a_i \leq 10^9)$ 和整数 $k(1 \leq k \leq 10^{15})$。
每一步你可以：

1. 选择一个下标 $i$ 使得 $a_i = a_i - 1$。
2. 或者选择两个下标 $i$ 和 $j$ 使得 $a_i =a_j$。
    你需要求出最少在多少步之后，$\sum\limits_{i=1}^na_i \leq k$（你可以将一些元素减成负数）。



输入的第一行包含一个整数 $t(1 \leq t \leq 10^4)$，表示样例的组数。
每组样例的第一行有两个整数 $n(1 \leq n \leq 2 \cdot 10^5)$ 和 $k(1 \leq k \leq 10^{15})$。
第二行则是数组的每一个元素。
保证所有 $n$ 的和小于等于 $2 \cdot 10^5$。



输出一个整数，表示最少需要的步数。



You are given an integer array $ a_1, a_2, \dots, a_n $ and integer $ k $ .
In one step you can

- either choose some index $ i $ and decrease $ a_i $ by one (make $ a_i = a_i - 1 $ );
- or choose two indices $ i $ and $ j $ and set $ a_i $ equal to $ a_j $ (make $ a_i = a_j $ ).
    What is the minimum number of steps you need to make the sum of array $ \sum\limits_{i=1}^{n}{a_i} \le k $ ? (You are allowed to make values of array negative).

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases.
The first line of each test case contains two integers $ n $ and $ k $ ( $ 1 \le n \le 2 \cdot 10^5 $ ; $ 1 \le k \le 10^{15} $ ) — the size of array $ a $ and upper bound on its sum.
The second line of each test case contains $ n $ integers $ a_1, a_2, \dots, a_n $ ( $ 1 \le a_i \le 10^9 $ ) — the array itself.
It's guaranteed that the sum of $ n $ over all test cases doesn't exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case, print one integer — the minimum number of steps to make $ \sum\limits_{i=1}^{n}{a_i} \le k $ .

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出            |
| ------------------------------------------------------------ | -------------------- |
| 4<br/>1 10<br/>20<br/>2 69<br/>6 9<br/>7 8<br/>1 2 1 3 1 2 1<br/>10 1<br/>1 2 3 1 2 6 1 6 8 10 | 10<br/>0<br/>2<br/>7 |

#### 样例解释：

In the first test case, you should decrease $ a_1 $ $ 10 $ times to get the sum lower or equal to $ k = 10 $ .
In the second test case, the sum of array $ a $ is already less or equal to $ 69 $ , so you don't need to change it.
In the third test case, you can, for example:

1. set $ a_4 = a_3 = 1 $ ;
2. decrease $ a_4 $ by one, and get $ a_4 = 0 $ .
    As a result, you'll get array $ [1, 2, 1, 0, 1, 2, 1] $ with sum less or equal to $ 8 $ in $ 1 + 1 = 2 $ steps.In the fourth test case, you can, for example:
3. choose $ a_7 $ and decrease in by one $ 3 $ times; you'll get $ a_7 = -2 $ ;
4. choose $ 4 $ elements $ a_6 $ , $ a_8 $ , $ a_9 $ and $ a_{10} $ and them equal to $ a_7 = -2 $ .
    As a result, you'll get array $ [1, 2, 3, 1, 2, -2, -2, -2, -2, -2] $ with sum less or equal to $ 1 $ in $ 3 + 4 = 7 $ steps.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
