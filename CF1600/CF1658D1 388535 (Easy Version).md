
# 388535 (Easy Version)题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

**本题与 CF1658D2 的唯一区别在于 $l$ 的范围。在本题中，$l=0$。**
Marin 和 Gojou 正在玩一个和数组有关的游戏。
Gojou 会依次执行如下操作：

- 选择两个整数 $l,r$，保证 $l\leqslant r$。
- 构造出一个长度为 $r-l+1$ 的数组 $a$，保证其是数组 $[l,l+1,\cdots,r]$ 的一种排列。
- 选择一个整数 $x$，然后对于所有的 $1\leqslant i\leqslant r-l+1$，将 $a_i$ 的值替换为 $a_i\oplus x$。其中 $\oplus$ 为按位异或运算。
    然后，Gojou 会将 $l,r$ 和最终得到的数组 $a$ 告诉 Marin。Marin 需要求出能够满足要求的任意一个整数 $x$ 才能获胜。
    现在，请你帮助 Marin 求出整数 $x$。
    数据范围：
- $t$ 组数据，$1\leqslant t\leqslant 10^5$。
- $\color{red}{0=l}\color{black}\leqslant r\lt2^{17}$。
- $0\leqslant a_i\lt2^{17}$。
- $\sum(r-l+1)\leqslant 2^{17}$。
    Translated by Eason_AC

This is the easy version of the problem. The difference in the constraints between both versions is colored below in red. You can make hacks only if all versions of the problem are solved.
Marin and Gojou are playing hide-and-seek with an array.
Gojou initially performs the following steps:

- First, Gojou chooses $ 2 $ integers $ l $ and $ r $ such that $ l \leq r $ .
- Then, Gojou makes an array $ a $ of length $ r-l+1 $ which is a permutation of the array $ [l,l+1,\ldots,r] $ .
- Finally, Gojou chooses a secret integer $ x $ and sets $ a_i $ to $ a_i \oplus x $ for all $ i $ (where $ \oplus $ denotes the [bitwise XOR operation](https://en.wikipedia.org/wiki/Bitwise_operation#XOR)).
    Marin is then given the values of $ l,r $ and the final array $ a $ . She needs to find the secret integer $ x $ to win. Can you help her?
    Note that there may be multiple possible $ x $ that Gojou could have chosen. Marin can find any possible $ x $ that could have resulted in the final value of $ a $ .

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \leq t \leq 10^5 $ ) — the number of test cases.
In the first line of each test case contains two integers $ l $ and $ r $ ( $ \color{red}{\boldsymbol{0} \boldsymbol{=} \boldsymbol{l}} \le r \lt 2^{17} $ ).
The second line contains $ r - l + 1 $ integers of $ a_1,a_2,\ldots,a_{r-l+1} $ ( $ 0 \le a_i \lt 2^{17} $ ). It is guaranteed that $ a $ can be generated using the steps performed by Gojou.
It is guaranteed that the sum of $ r - l + 1 $ over all test cases does not exceed $ 2^{17} $ .

#### 输出格式：

For each test case print an integer $ x $ . If there are multiple answers, print any.

#### 样例输入输出：

| 样例1输入                                                   | 样例1输出     |
| ----------------------------------------------------------- | ------------- |
| 3<br/>0 3<br/>3 2 1 0<br/>0 3<br/>4 7 6 5<br/>0 2<br/>1 2 3 | 0<br/>4<br/>3 |

#### 样例解释：

In the first test case, the original array is $ [3, 2, 1, 0] $ .
In the second test case, the original array is $ [0, 3, 2, 1] $ .
In the third test case, the original array is $ [2, 1, 0] $ .

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
