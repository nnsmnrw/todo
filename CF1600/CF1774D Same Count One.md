
# Same Count One题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定 $n$ 个长度为 $m$ 的，只包含 $0$ 和 $1$ 的数组，选择任意两个数组交换位置 $pos$ 上的数。在经过最少的操作后使得每个数组中的 $1$ 数量相等，并输出操作过程。



第一行一个整数 $t$ $( 1 \leq t \leq 2\cdot 10^4 )$ 表示有 $t$ 组测试数据。
每组测试数据：第一行两个整数 $ n $ 和 $ m $ 。 $( 2 \leq n \leq 10^5 $ , $ 2 \leq m \leq 10^5 , \sum n\times m \le 10^6)$
接下来 $ n $ 行，每行 $ m $ 个整数（ $ 0 $ 或 $ 1 $ ）。



对于每一组测试样例，若无法满足要求，输出 $ -1 $ .
否则, 第一行输出一个整数 $ k $ $ (0 \le k \le mn) $ ，即最小的操作数量。
接下来输出 $ k $ 行，每行 $ 3 $ 个整数, $ x, y, z $ $ (1 \le x, y \le n, 1 \le z \le m) $ , 表示交换 $ a_{x, z}, a_{y, z} $ : 即交换第 $ x $ 和第 $ y $ 行的第 $ z $ 个数。

ChthollyNotaSeniorious received a special gift from AquaMoon: $ n $ binary arrays of length $ m $ . AquaMoon tells him that in one operation, he can choose any two arrays and any position $ pos $ from $ 1 $ to $ m $ , and swap the elements at positions $ pos $ in these arrays.
He is fascinated with this game, and he wants to find the minimum number of operations needed to make the numbers of $ 1 $ s in all arrays the same. He has invited you to participate in this interesting game, so please try to find it!
If it is possible, please output specific exchange steps in the format described in the output section. Otherwise, please output $ -1 $ .

#### 输入格式：

The first line of the input contains a single integer $ t $ ( $ 1 \leq t \leq 2\cdot 10^4 $ ) — the number of test cases. The description of test cases follows.
The first line of each test case contains two integers $ n $ and $ m $ ( $ 2 \leq n \leq 10^5 $ , $ 2 \leq m \leq 10^5 $ ).
The $ i $ -th of the following $ n $ lines contains $ m $ integers $ a_{i, 1}, a_{i, 2}, \ldots, a_{i, m} $ $ (0 \le a_{i, j} \le 1) $ — the elements of the $ i $ -th array.
It is guaranteed that the sum of $ n \cdot m $ over all test cases does not exceed $ 10^6 $ .

#### 输出格式：

For each test case, if the objective is not achievable, output $ -1 $ .
Otherwise, in the first line output $ k $ $ (0 \le k \le mn) $ — the minimum number of operations required.
The $ i $ -th of the following $ k $ lines should contain $ 3 $ integers, $ x_i, y_i, z_i $ $ (1 \le x_i, y_i \le n, 1 \le z_i \le m) $ , which describe an operation that swap $ a_{x_i, z_i}, a_{y_i, z_i} $ : swap the $ z_i $ -th number of the $ x_i $ -th and $ y_i $ -th arrays.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                          |
| ------------------------------------------------------------ | ---------------------------------- |
| 3<br/>3 4<br/>1 1 1 0<br/>0 0 1 0<br/>1 0 0 1<br/>4 3<br/>1 0 0<br/>0 1 1<br/>0 0 1<br/>0 0 0<br/>2 2<br/>0 0<br/>0 1 | 1<br/>2 1 1<br/>1<br/>4 2 2<br/>-1 |

#### 样例解释：

In the first test case, it's enough to do a single operation: to swap the first element in the second and the first rows. The arrays will become $ [0, 1, 1, 0], [1, 0, 1, 0], [1, 0, 0, 1] $ , each of them contains exactly two $ 1 $ s.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```

