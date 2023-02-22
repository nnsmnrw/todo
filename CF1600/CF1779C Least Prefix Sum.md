
# Least Prefix Sum题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

定义长度为 $n$ 的数组 $arr$ 的前缀和数组为 $s$，对于一次操作，你可以选择一个数，变为这个数的相反数，给定一个数 $m$，请你求出最小的操作次数使序列满足：$\forall i\in[1,n], s_i\geq s_m$。

Baltic, a famous chess player who is also a mathematician, has an array $ a_1,a_2, \ldots, a_n $ , and he can perform the following operation several (possibly $ 0 $ ) times:

- Choose some index $ i $ ( $ 1 \leq i \leq n $ );
- multiply $ a_i $ with $ -1 $ , that is, set $ a_i := -a_i $ .
    Baltic's favorite number is $ m $ , and he wants $ a_1 + a_2 + \cdots + a_m $ to be the smallest of all non-empty prefix sums. More formally, for each $ k = 1,2,\ldots, n $ it should hold that $ $$$a_1 + a_2 + \cdots + a_k \geq a_1 + a_2 + \cdots + a_m. $ $ \lt/p\gt\ltp\gtPlease note that multiple smallest prefix sums may exist and that it is only required that $ a\_1 + a\_2 + \\cdots + a\_m $ is one of them.\lt/p\gt\ltp\gtHelp Baltic find the minimum number of operations required to make $ a\_1 + a\_2 + \\cdots + a\_m$$$ the least of all prefix sums. It can be shown that a valid sequence of operations always exists.

#### 输入格式：

Each test contains multiple test cases. The first line contains the number of test cases $ t $ ( $ 1 \leq t \leq 10\,000 $ ). The description of the test cases follows.
The first line of each test case contains two integers $ n $ and $ m $ ( $ 1 \leq m \leq n \leq 2\cdot 10^5 $ ) — the size of Baltic's array and his favorite number.
The second line contains $ n $ integers $ a_1,a_2, \ldots, a_n $ ( $ -10^9 \leq a_i \leq 10^9 $ ) — the array.
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2\cdot 10^5 $ .

#### 输出格式：

For each test case, print a single integer — the minimum number of required operations.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                       |
| ------------------------------------------------------------ | ------------------------------- |
| 6<br/>4 3<br/>-1 -2 -3 -4<br/>4 3<br/>1 2 3 4<br/>1 1<br/>1<br/>5 5<br/>-2 3 -5 1 -20<br/>5 2<br/>-2 3 -5 -5 -20<br/>10 4<br/>345875723 -48 384678321 -375635768 -35867853 -35863586 -358683842 -81725678 38576 -357865873 | 1<br/>1<br/>0<br/>0<br/>3<br/>4 |

#### 样例解释：

In the first example, we perform the operation $ a_4 := -a_4 $ . The array becomes $ [-1,-2,-3,4] $ and the prefix sums, $ [a_1, \ a_1+a_2, \ a_1+a_2+a_3, \ a_1+a_2+a_3+a_4] $ , are equal to $ [-1,-3,-6,-2] $ . Thus $ a_1 + a_2 + a_3=-6 $ is the smallest of all prefix sums.
In the second example, we perform the operation $ a_3 := -a_3 $ . The array becomes $ [1,2,-3,4] $ with prefix sums equal to $ [1,3,0,4] $ .
In the third and fourth examples, $ a_1 + a_2 + \cdots + a_m $ is already the smallest of the prefix sums — no operation needs to be performed.
In the fifth example, a valid sequence of operations is:

- $ a_3 := -a_3 $ ,
- $ a_2 := -a_2 $ ,
- $ a_5 := -a_5 $ .
    The array becomes $ [-2,-3,5,-5,20] $ and its prefix sums are $ [-2,-5,0,-5,15] $ . Note that $ a_1+a_2=-5 $ and $ a_1+a_2+a_3+a_4=-5 $ are both the smallest of the prefix sums (and this is a valid solution).

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
