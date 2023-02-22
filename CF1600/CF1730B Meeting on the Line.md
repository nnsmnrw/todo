
# Meeting on the Line题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定一个长为 $n$ 的序列 $x$ 和 $t$，请你求出一个 $x_0$，使得 $\max\limits_{i=1}^{n}\{t_i+|a_i-a_0|\}$ 最小化，输出 $x_0$。

$ n $ people live on the coordinate line, the $ i $ -th one lives at the point $ x_i $ ( $ 1 \le i \le n $ ). They want to choose a position $ x_0 $ to meet. The $ i $ -th person will spend $ |x_i - x_0| $ minutes to get to the meeting place. Also, the $ i $ -th person needs $ t_i $ minutes to get dressed, so in total he or she needs $ t_i + |x_i - x_0| $ minutes.
Here $ |y| $ denotes the absolute value of $ y $ .
These people ask you to find a position $ x_0 $ that minimizes the time in which all $ n $ people can gather at the meeting place.

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \le t \le 10^3 $ ) — the number of test cases. Then the test cases follow.
Each test case consists of three lines.
The first line contains a single integer $ n $ ( $ 1 \le n \le 10^5 $ ) — the number of people.
The second line contains $ n $ integers $ x_1, x_2, \dots, x_n $ ( $ 0 \le x_i \le 10^{8} $ ) — the positions of the people.
The third line contains $ n $ integers $ t_1, t_2, \dots, t_n $ ( $ 0 \le t_i \le 10^{8} $ ), where $ t_i $ is the time $ i $ -th person needs to get dressed.
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case, print a single real number — the optimum position $ x_0 $ . It can be shown that the optimal position $ x_0 $ is unique.
Your answer will be considered correct if its absolute or relative error does not exceed $ 10^{−6} $ . Formally, let your answer be $ a $ , the jury's answer be $ b $ . Your answer will be considered correct if $ \frac{|a−b|}{max(1,|b|)} \le 10^{−6} $ .

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                               |
| ------------------------------------------------------------ | --------------------------------------- |
| 7<br/>1<br/>0<br/>3<br/>2<br/>3 1<br/>0 0<br/>2<br/>1 4<br/>0 0<br/>3<br/>1 2 3<br/>0 0 0<br/>3<br/>1 2 3<br/>4 1 2<br/>3<br/>3 3 3<br/>5 3 3<br/>6<br/>5 4 7 2 10 4<br/>3 2 5 1 4 6 | 0<br/>2<br/>2.5<br/>2<br/>1<br/>3<br/>6 |

#### 样例解释：

- In the $ 1 $ -st test case there is one person, so it is efficient to choose his or her position for the meeting place. Then he or she will get to it in $ 3 $ minutes, that he or she need to get dressed.
- In the $ 2 $ -nd test case there are $ 2 $ people who don't need time to get dressed. Each of them needs one minute to get to position $ 2 $ .
- In the $ 5 $ -th test case the $ 1 $ -st person needs $ 4 $ minutes to get to position $ 1 $ ( $ 4 $ minutes to get dressed and $ 0 $ minutes on the way); the $ 2 $ -nd person needs $ 2 $ minutes to get to position $ 1 $ ( $ 1 $ minute to get dressed and $ 1 $ minute on the way); the $ 3 $ -rd person needs $ 4 $ minutes to get to position $ 1 $ ( $ 2 $ minutes to get dressed and $ 2 $ minutes on the way).

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
