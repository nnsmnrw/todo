
# Matrix and Shifts题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

你有一个 $n\times n$ 的二进制矩阵 $A$，将其行从上到下分别编号 $1$ 至 $n$，其列从左到右分别编号 $1$ 至 $n$，因此位于第 $i$ 行和第 $j$ 列交叉处的元素为 $A_{ij}$。
给出如下 $4$ 种操作，你可以无限次无代价地使用：

1. 循环地将所有行向上移动。这样，现在的第 $i$ 行为原来的第 $i + 1$ 行 $(1 \leq i \lt n)$，而现在的第 $n$ 行为原来的第 $1$ 行。
1. 循环地将所有行向下移动。这样，现在的第 $i$ 行为原来的第 $i - 1$ 行 $(1 \lt i \leq n)$，而现在的第 $1$ 行为原来的第 $n$ 行。
1. 循环地将所有列向左移动。这样，现在的第 $j$ 列为原来的第 $j + 1$ 列 $(1 \leq j \lt n)$，而现在的第 $n$ 列为原来的第 $1$ 列。
1. 循环地将所有列向右移动。这样，现在的第 $j$ 列为原来的第 $j - 1$ 列 $(1 \lt j \leq n)$，而现在的第 $1$ 列为原来的第 $n$ 列。
    在这四种操作均完成后，你想要把 $A$ 变成单位矩阵（即 即 $\forall\ i,j \in [1,n] \cap \Z,\ A_{ij} = [i = j]$）。所以你会使出最后一种操作：将 $A$ 中与目标矩阵（即单位矩阵）不相同的位置异或 $1$（也就是说，$0$ 变成 $1$，而 $1$ 变成 $0$），这会产生 $1$ 的代价。
    **使用异或操作后，你不能再使用上述的 $4$ 种操作。** 求你最少应付多少代价。



You are given a binary matrix $ A $ of size $ n \times n $ . Rows are numbered from top to bottom from $ 1 $ to $ n $ , columns are numbered from left to right from $ 1 $ to $ n $ . The element located at the intersection of row $ i $ and column $ j $ is called $ A_{ij} $ . Consider a set of $ 4 $ operations:

1. Cyclically shift all rows up. The row with index $ i $ will be written in place of the row $ i-1 $ ( $ 2 \le i \le n $ ), the row with index $ 1 $ will be written in place of the row $ n $ .
2. Cyclically shift all rows down. The row with index $ i $ will be written in place of the row $ i+1 $ ( $ 1 \le i \le n - 1 $ ), the row with index $ n $ will be written in place of the row $ 1 $ .
3. Cyclically shift all columns to the left. The column with index $ j $ will be written in place of the column $ j-1 $ ( $ 2 \le j \le n $ ), the column with index $ 1 $ will be written in place of the column $ n $ .
4. Cyclically shift all columns to the right. The column with index $ j $ will be written in place of the column $ j+1 $ ( $ 1 \le j \le n - 1 $ ), the column with index $ n $ will be written in place of the column $ 1 $ .
    ![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF1660E/12668e041dd8d5dbd1e7d6bac1040ded6cc9fc28.png)The $ 3 \times 3 $ matrix is shown on the left before the $ 3 $ -rd operation is applied to it, on the right — after.You can perform an arbitrary (possibly zero) number of operations on the matrix; the operations can be performed in any order.
    After that, you can perform an arbitrary (possibly zero) number of new xor-operations:

- Select any element $ A_{ij} $ and assign it with new value $ A_{ij} \oplus 1 $ . In other words, the value of $ (A_{ij} + 1) \bmod 2 $ will have to be written into element $ A_{ij} $ .
    Each application of this xor-operation costs one burl. Note that the $ 4 $ shift operations — are free. These $ 4 $ operations can only be performed before xor-operations are performed.
    Output the minimum number of burles you would have to pay to make the $ A $ matrix unitary. A unitary matrix is a matrix with ones on the main diagonal and the rest of its elements are zeros (that is, $ A_{ij} = 1 $ if $ i = j $ and $ A_{ij} = 0 $ otherwise).

#### 输入格式：

The first line of the input contains an integer $ t $ ( $ 1 \le t \le 10^4 $ ) —the number of test cases in the test.
The descriptions of the test cases follow. Before each test case, an empty line is written in the input.
The first line of each test case contains a single number $ n $ ( $ 1 \le n \le 2000 $ )
This is followed by $ n $ lines, each containing exactly $ n $ characters and consisting only of zeros and ones. These lines describe the values in the elements of the matrix.
It is guaranteed that the sum of $ n^2 $ values over all test cases does not exceed $ 4 \cdot 10^6 $ .

#### 输出格式：

For each test case, output the minimum number of burles you would have to pay to make the $ A $ matrix unitary. In other words, print the minimum number of xor-operations it will take after applying cyclic shifts to the matrix for the $ A $ matrix to become unitary.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出            |
| ------------------------------------------------------------ | -------------------- |
| 4<br/>3<br/>010<br/>011<br/>100<br/>5<br/>00010<br/>00001<br/>10000<br/>01000<br/>00100<br/>2<br/>10<br/>10<br/>4<br/>1111<br/>1011<br/>1111<br/>1111 | 1<br/>0<br/>2<br/>11 |

#### 样例解释：

In the first test case, you can do the following: first, shift all the rows down cyclically, then the main diagonal of the matrix will contain only "1". Then it will be necessary to apply xor-operation to the only "1" that is not on the main diagonal.
In the second test case, you can make a unitary matrix by applying the operation $ 2 $ — cyclic shift of rows upward twice to the matrix.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
