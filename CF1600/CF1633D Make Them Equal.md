
# Make Them Equal题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

你有一个长度为 $n$，初始全为 $1$ 的数组 $a$，和两个长度为 $n$ 的数组 $b,c$。
你可以**最多**进行 $k$ 次如下的操作：选择两个**正整数** $i,x$，使 $a_{i}$ 变成 $ \left ( a_{i}+\left \lfloor \dfrac{a_{i}}{x} \right \rfloor \right )$。
最后，如果 $a_{i}=b_{i}$，你将会获得 $c_{i}$ 的收益。
最大化总收益。

#### 【输入格式】

**多组数据**。
第一行一个整数 $t$，表示有 $t$ 组数据。
每组数据的第一行两个整数 $n,k$，表示数组的长度和最多的操作次数。
接下来两个各 $n$ 个整数，分别表示 $b,c$。

#### 【输出格式】

一共 $t$ 行，每行一个整数表示答案。

#### 【数据范围】

- $1 \leq t \leq 100,1 \leq n \leq 1000, 1 \leq k \leq 1 \times 10^{6}$；
- $1 \leq b_{i} \leq 1000,1 \leq c_{i} \leq 1 \times 10^{6}$；
- $n$ 的总和不大于 $1000$。
    Translated by HPXXZYY.

You have an array of integers $ a $ of size $ n $ . Initially, all elements of the array are equal to $ 1 $ . You can perform the following operation: choose two integers $ i $ ( $ 1 \le i \le n $ ) and $ x $ ( $ x \gt 0 $ ), and then increase the value of $ a_i $ by $ \left\lfloor\frac{a_i}{x}\right\rfloor $ (i.e. make $ a_i = a_i + \left\lfloor\frac{a_i}{x}\right\rfloor $ ).
After performing all operations, you will receive $ c_i $ coins for all such $ i $ that $ a_i = b_i $ .
Your task is to determine the maximum number of coins that you can receive by performing no more than $ k $ operations.

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 100 $ ) — the number of test cases.
The first line of each test case contains two integers $ n $ and $ k $ ( $ 1 \le n \le 10^3; 0 \le k \le 10^6 $ ) — the size of the array and the maximum number of operations, respectively.
The second line contains $ n $ integers $ b_1, b_2, \dots, b_n $ ( $ 1 \le b_i \le 10^3 $ ).
The third line contains $ n $ integers $ c_1, c_2, \dots, c_n $ ( $ 1 \le c_i \le 10^6 $ ).
The sum of $ n $ over all test cases does not exceed $ 10^3 $ .

#### 输出格式：

For each test case, print one integer — the maximum number of coins that you can get by performing no more than $ k $ operations.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出              |
| ------------------------------------------------------------ | ---------------------- |
| 4<br/>4 4<br/>1 7 5 2<br/>2 6 5 2<br/>3 0<br/>3 5 2<br/>5 4 7<br/>5 9<br/>5 2 5 6 3<br/>5 9 1 9 7<br/>6 14<br/>11 4 6 2 8 16<br/>43 45 9 41 15 38 | 9<br/>0<br/>30<br/>167 |



<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
