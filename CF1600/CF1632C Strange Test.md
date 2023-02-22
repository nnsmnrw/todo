
# Strange Test题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给定两个整数 $a,b$。你可以执行若干次操作，每次操作分为如下三种：

- $a\leftarrow a+1$。
- $b\leftarrow b+1$。
- $a\leftarrow a\operatorname{or} b$。
    其中 $x\leftarrow y$ 表示将 $x$ 的值替换为 $y$，即赋值操作。$\operatorname{or}$ 表示按位或操作。
    请求出使得 $a$ 变为 $b$ 的最少操作次数。
    数据范围：
- $t$ 组数据，$1\leqslant t\leqslant 10^4$。
- $1\leqslant a\ltb\leqslant 10^6$。
- $\bf\sum b\leqslant 10^6$。
    

Igor is in 11th grade. Tomorrow he will have to write an informatics test by the strictest teacher in the school, Pavel Denisovich.
Igor knows how the test will be conducted: first of all, the teacher will give each student two positive integers $ a $ and $ b $ ( $ a \lt b $ ). After that, the student can apply any of the following operations any number of times:

- $ a := a + 1 $ (increase $ a $ by $ 1 $ ),
- $ b := b + 1 $ (increase $ b $ by $ 1 $ ),
- $ a := a \ | \ b $ (replace $ a $ with the [bitwise OR](https://en.wikipedia.org/wiki/Bitwise_operation#OR) of $ a $ and $ b $ ).
    To get full marks on the test, the student has to tell the teacher the minimum required number of operations to make $ a $ and $ b $ equal.
    Igor already knows which numbers the teacher will give him. Help him figure out what is the minimum number of operations needed to make $ a $ equal to $ b $ .

#### 输入格式：

Each test contains multiple test cases. The first line contains the number of test cases $ t $ ( $ 1 \le t \le 10^4 $ ). Description of the test cases follows.
The only line for each test case contains two integers $ a $ and $ b $ ( $ 1 \le a \lt b \le 10^6 $ ).
It is guaranteed that the sum of $ b $ over all test cases does not exceed $ 10^6 $ .

#### 输出格式：

For each test case print one integer — the minimum required number of operations to make $ a $ and $ b $ equal.

#### 样例输入输出：

| 样例1输入                                           | 样例1输出                     |
| --------------------------------------------------- | ----------------------------- |
| 5<br/>1 3<br/>5 8<br/>2 5<br/>3 19<br/>56678 164422 | 1<br/>3<br/>2<br/>1<br/>23329 |

#### 样例解释：

In the first test case, it is optimal to apply the third operation.
In the second test case, it is optimal to apply the first operation three times.
In the third test case, it is optimal to apply the second operation and then the third operation.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```

