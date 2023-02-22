
# Hossam and Trainees题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

有 $T$ 组数据，每组数据给出 $n$ 和长度为 $n$ 的数列 $a_i$，判断有没有两个数不互质，如果有输出 "YES"，没有输出 "NO"

Hossam has $ n $ trainees. He assigned a number $ a_i $ for the $ i $ -th trainee.
A pair of the $ i $ -th and $ j $ -th ( $ i \neq j $ ) trainees is called successful if there is an integer $ x $ ( $ x \geq 2 $ ), such that $ x $ divides $ a_i $ , and $ x $ divides $ a_j $ .
Hossam wants to know if there is a successful pair of trainees.
Hossam is very tired now, so he asks you for your help!

#### 输入格式：

The input consists of multiple test cases. The first line contains a single integer $ t $ ( $ 1 \le t \le 10^5 $ ), the number of test cases. Description of the test cases follows.
The first line of each test case contains an integer number $ n $ ( $ 2 \le n \le 10^5 $ ).
The second line of each test case contains $ n $ integers, the number of each trainee $ a_1, a_2, \dots, a_n $ ( $ 1 \le a_i \le 10^9 $ ).
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 10^5 $ .

#### 输出格式：

Print the answer — "YES" (without quotes) if there is a successful pair of trainees and "NO" otherwise. You can print each letter in any case.

#### 样例输入输出：

| 样例1输入                            | 样例1输出  |
| ------------------------------------ | ---------- |
| 2<br/>3<br/>32 48 7<br/>3<br/>14 5 9 | YES<br/>NO |

#### 样例解释：

In the first example, the first trainee and the second trainee make up a successful pair:
$ a_1 = 32, a_2 = 48 $ , you can choose $ x = 4 $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
