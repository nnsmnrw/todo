
# Insert a Progression题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给你一个 $n$ 个数的序列 $a_1,a_2,...,a_n$，同时给你 $x$ 个正整数 $1,2,...,x$。
你要将这 $x$ 个数插入到序列 $a$ 中，每个数可以插在序列首位，末位以及任意两个元素中间。
设最后得到的序列为 $a'$，定义它的分数为相邻两个元素之间的绝对值之和，也就是 $\sum\limits_{i=1}^{n+x-1}|a_i'-a_{i+1}'|$。
求最小分数。



第一行输入一个整数 $t$（$1\le t\le 10^4$），表示 $t$ 组询问。
每组询问的第一行输入两个整数 $n,x$（$1\le n,x\le 2\times 10^5$），表示初始序列的长度以及你要插入的数的个数。
每组询问的第二行包含 $n$ 个整数 $a_1,a_2,...,a_n$（$1\le a_i\le 2\times 10^5$）。
保证 $\sum n\le2\times10^5$。



对于每组询问，输出一个整数，表示将 $x$ 个数插入到 $a$ 后得到序列 $a'$ 的最小分数。



样例 $4$ 组询问（构造不一定唯一）：

- $ \underline{1}, \underline{2}, \underline{3}, \underline{4}, \underline{5}, 10 $
- $ \underline{7}, 7, \underline{6}, \underline{4}, 2, \underline{2}, \underline{1}, \underline{3}, \underline{5}, \underline{8}, 10 $
- $ 6, \underline{1}, 1, \underline{2}, 5, 7, 3, 3, 9, 10, 10, 1 $
- $ 1, 3, \underline{1}, 1, 2, \underline{2}, \underline{3}, \underline{4}, \underline{5}, \underline{6}, \underline{7}, \underline{8}, \underline{9}, \underline{10} $



You are given a sequence of $ n $ integers $ a_1, a_2, \dots, a_n $ . You are also given $ x $ integers $ 1, 2, \dots, x $ .
You are asked to insert each of the extra integers into the sequence $ a $ . Each integer can be inserted at the beginning of the sequence, at the end of the sequence, or between any elements of the sequence.
The score of the resulting sequence $ a' $ is the sum of absolute differences of adjacent elements in it $ \left(\sum \limits_{i=1}^{n+x-1} |a'_i - a'_{i+1}|\right) $ .
What is the smallest possible score of the resulting sequence $ a' $ ?

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of testcases.
The first line of each testcase contains two integers $ n $ and $ x $ ( $ 1 \le n, x \le 2 \cdot 10^5 $ ) — the length of the sequence and the number of extra integers.
The second line of each testcase contains $ n $ integers $ a_1, a_2, \dots, a_n $ ( $ 1 \le a_i \le 2 \cdot 10^5 $ ).
The sum of $ n $ over all testcases doesn't exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each testcase, print a single integer — the smallest sum of absolute differences of adjacent elements of the sequence after you insert the extra integers into it.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出              |
| ------------------------------------------------------------ | ---------------------- |
| 4<br/>1 5<br/>10<br/>3 8<br/>7 2 10<br/>10 2<br/>6 1 5 7 3 3 9 10 10 1<br/>4 10<br/>1 3 1 2 | 9<br/>15<br/>31<br/>13 |

#### 样例解释：

Here are the sequences with the smallest scores for the example. The underlined elements are the extra integers. Note that there exist other sequences with this smallest score.

- $ \underline{1}, \underline{2}, \underline{3}, \underline{4}, \underline{5}, 10 $
- $ \underline{7}, 7, \underline{6}, \underline{4}, 2, \underline{2}, \underline{1}, \underline{3}, \underline{5}, \underline{8}, 10 $
- $ 6, \underline{1}, 1, \underline{2}, 5, 7, 3, 3, 9, 10, 10, 1 $
- $ 1, 3, \underline{1}, 1, 2, \underline{2}, \underline{3}, \underline{4}, \underline{5}, \underline{6}, \underline{7}, \underline{8}, \underline{9}, \underline{10} $

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
