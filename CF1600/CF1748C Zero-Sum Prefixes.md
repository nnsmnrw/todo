
# Zero-Sum Prefixes题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定一个长为 $n$ 的数列 $a$，你可以将其中的每个 $0$ 分别改成任意整数。求出你最多能让多少个 $k$ 满足 $a_1+\dots+a_k=0$。



The score of an array $ v_1,v_2,\ldots,v_n $ is defined as the number of indices $ i $ ( $ 1 \le i \le n $ ) such that $ v_1+v_2+\ldots+v_i = 0 $ .
You are given an array $ a_1,a_2,\ldots,a_n $ of length $ n $ . You can perform the following operation multiple times:

- select an index $ i $ ( $ 1 \le i \le n $ ) such that $ a_i=0 $ ;
- then replace $ a_i $ by an arbitrary integer.
    What is the maximum possible score of $ a $ that can be obtained by performing a sequence of such operations?

#### 输入格式：

Each test contains multiple test cases. The first line contains a single integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases.
The first line of each test case contains one integer $ n $ ( $ 1 \le n \le 2 \cdot 10^5 $ ) — the length of the array $ a $ .
The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ( $ -10^9 \le a_i \le 10^9 $ ) — array $ a $ .
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case, print the maximum possible score of the array $ a $ after performing a sequence of operations.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                 |
| ------------------------------------------------------------ | ------------------------- |
| 5<br/>5<br/>2 0 1 -1 0<br/>3<br/>1000000000 1000000000 0<br/>4<br/>0 0 0 0<br/>8<br/>3 0 2 -10 10 -30 30 0<br/>9<br/>1 0 0 1 -1 0 1 0 -1 | 3<br/>1<br/>4<br/>4<br/>5 |

#### 样例解释：

In the first test case, it is optimal to change the value of $ a_2 $ to $ -2 $ in one operation.
The resulting array $ a $ will be $ [2,-2,1,-1,0] $ , with a score of $ 3 $ :

- $ a_1+a_2=2-2=0 $ ;
- $ a_1+a_2+a_3+a_4=2-2+1-1=0 $ ;
- $ a_1+a_2+a_3+a_4+a_5=2-2+1-1+0=0 $ .
    In the second test case, it is optimal to change the value of $ a_3 $ to $ -2\,000\,000\,000 $ , giving us an array with a score of $ 1 $ .
    In the third test case, it is not necessary to perform any operations.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
