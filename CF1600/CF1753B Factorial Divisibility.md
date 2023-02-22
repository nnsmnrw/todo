
# Factorial Divisibility题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定两个正整数 $n$ 和 $x$ 和一个正整数序列 $a_1 \sim a_n$。
请问 $\sum_{i = 1}^n a_i!$ 是否能被 $x!$ 整除。如果能则输出一个字符串 $\texttt{Yes}$，不能则输出字符串 $\texttt{No}$。



第一行两个正整数 $n$ 和 $x$。
第二行 $n$ 个正整数 $a_1 \sim a_n$。



一行一个字符串，输出 $\texttt{Yes}$ 或 $\texttt{No}$。



You are given an integer $ x $ and an array of integers $ a_1, a_2, \ldots, a_n $ . You have to determine if the number $ a_1! + a_2! + \ldots + a_n! $ is divisible by $ x! $ .
Here $ k! $ is a factorial of $ k $ — the product of all positive integers less than or equal to $ k $ . For example, $ 3! = 1 \cdot 2 \cdot 3 = 6 $ , and $ 5! = 1 \cdot 2 \cdot 3 \cdot 4 \cdot 5 = 120 $ .

#### 输入格式：

The first line contains two integers $ n $ and $ x $ ( $ 1 \le n \le 500\,000 $ , $ 1 \le x \le 500\,000 $ ).
The second line contains $ n $ integers $ a_1, a_2, \ldots, a_n $ ( $ 1 \le a_i \le x $ ) — elements of given array.

#### 输出格式：

In the only line print "Yes" (without quotes) if $ a_1! + a_2! + \ldots + a_n! $ is divisible by $ x! $ , and "No" (without quotes) otherwise.

#### 样例输入输出：

| 样例1输入输出       | 样例2输入输出           | 样例3输入输出         | 样例4输入输出                | 样例5输入输出              |
| ------------------- | ----------------------- | --------------------- | ---------------------------- | -------------------------- |
| 6 4<br/>3 2 2 2 3 3 | 8 3<br/>3 2 2 2 2 2 1 1 | 7 8<br/>7 7 7 7 7 7 7 | 10 5<br/>4 3 2 1 4 3 2 4 3 4 | 2 500000<br/>499999 499999 |
| Yes                 | Yes                     | No                    | No                           | No                         |

#### 样例解释：

In the first example $ 3! + 2! + 2! + 2! + 3! + 3! = 6 + 2 + 2 + 2 + 6 + 6 = 24 $ . Number $ 24 $ is divisible by $ 4! = 24 $ .
In the second example $ 3! + 2! + 2! + 2! + 2! + 2! + 1! + 1! = 18 $ , is divisible by $ 3! = 6 $ .
In the third example $ 7! + 7! + 7! + 7! + 7! + 7! + 7! = 7 \cdot 7! $ . It is easy to prove that this number is not divisible by $ 8! $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
