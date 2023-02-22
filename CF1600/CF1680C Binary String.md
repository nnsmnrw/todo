
# Binary String题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

你有一个由 $1$ 和 $0$ 构成的字符串 $s$。
你需要先从 $s$ 的开头移除若干字符，然后从 $s$ 的结尾移除若干字符。（当然，你可以不移除任何字符，也可以将整个 $s$ 移除掉）
这样做的代价是从 $s$ 中移除的 $1$ 的个数和 $s$ 中剩余的 $0$ 的个数的最大值。
求代价的最小值。



第一行一个整数 $t$ 表示数据组数。$(1\le t\le 10^4)$
接下来 $t$ 行，每行一个字符串 $s$ 表示这组数据的 $s$。$(1\le |s|\le 2⋅10^5)$
$s$ 的总和不超过 $2⋅10^5$。



对于每组数据，输出一个整数表示最小代价。



样例解释：
`101110110` -\gt `(10) 111011 (0)`
`1001001001001` -\gt `(100100) 1001 (001)`
`0000111111` -\gt `(0000) 111111 ()`
`00000` -\gt `(00000)()`
`1111` -\gt `()1111()`



You are given a string $ s $ consisting of characters 0 and/or 1.
You have to remove several (possibly zero) characters from the beginning of the string, and then several (possibly zero) characters from the end of the string. The string may become empty after the removals. The cost of the removal is the maximum of the following two values:

- the number of characters 0 left in the string;
- the number of characters 1 removed from the string.
    What is the minimum cost of removal you can achieve?

#### 输入格式：

The first line contains one integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases.
Each test case consists of one line containing the string $ s $ ( $ 1 \le |s| \le 2 \cdot 10^5 $ ), consisting of characters 0 and/or 1.
The total length of strings $ s $ in all test cases does not exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case, print one integer — the minimum cost of removal you can achieve.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                 |
| ------------------------------------------------------------ | ------------------------- |
| 5<br/>101110110<br/>1001001001001<br/>0000111111<br/>00000<br/>1111 | 1<br/>3<br/>0<br/>0<br/>0 |

#### 样例解释：

Consider the test cases of the example:

1. in the first test case, it's possible to remove two characters from the beginning and one character from the end. Only one 1 is deleted, only one 0 remains, so the cost is $ 1 $ ;
2. in the second test case, it's possible to remove three characters from the beginning and six characters from the end. Two characters 0 remain, three characters 1 are deleted, so the cost is $ 3 $ ;
3. in the third test case, it's optimal to remove four characters from the beginning;
4. in the fourth test case, it's optimal to remove the whole string;
5. in the fifth test case, it's optimal to leave the string as it is.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
