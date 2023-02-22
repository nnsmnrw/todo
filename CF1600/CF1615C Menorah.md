
# Menorah题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

有两个长度为 $n$ 且仅由 $0$ 和 $1$ 组成的字符串$a$、$b$，要求通过以下的操作将字符串 $a$ 变成字符串 $b$
对于一次操作：选择字符串 $a$ 中的一个 **$1$** ，并将字符串 $a$ 中除了所选择的 $1$ 之外的所有 $0$ 变成 $1$、所有 $1$ 变成 $0$。
若可以由字符串 $a$ 变成字符串 $b$ 则输出最小操作次数，若不能则输出`-1`



There are $ n $ candles on a Hanukkah menorah, and some of its candles are initially lit. We can describe which candles are lit with a binary string $ s $ , where the $ i $ -th candle is lit if and only if $ s_i=1 $ .
![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF1615C/23095c0b536d5c6c64ebf4ef5c8e358f51d36118.png)Initially, the candle lights are described by a string $ a $ . In an operation, you select a candle that is currently lit. By doing so, the candle you selected will remain lit, and every other candle will change (if it was lit, it will become unlit and if it was unlit, it will become lit).
You would like to make the candles look the same as string $ b $ . Your task is to determine if it is possible, and if it is, find the minimum number of operations required.

#### 输入格式：

The first line contains an integer $ t $ ( $ 1\le t\le 10^4 $ ) — the number of test cases. Then $ t $ cases follow.
The first line of each test case contains a single integer $ n $ ( $ 1\le n\le 10^5 $ ) — the number of candles.
The second line contains a string $ a $ of length $ n $ consisting of symbols 0 and 1 — the initial pattern of lights.
The third line contains a string $ b $ of length $ n $ consisting of symbols 0 and 1 — the desired pattern of lights.
It is guaranteed that the sum of $ n $ does not exceed $ 10^5 $ .

#### 输出格式：

For each test case, output the minimum number of operations required to transform $ a $ to $ b $ , or $ -1 $ if it's impossible.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                  |
| ------------------------------------------------------------ | -------------------------- |
| 5<br/>5<br/>11010<br/>11010<br/>2<br/>01<br/>11<br/>3<br/>000<br/>101<br/>9<br/>100010111<br/>101101100<br/>9<br/>001011011<br/>011010101 | 0<br/>1<br/>-1<br/>3<br/>4 |

#### 样例解释：

In the first test case, the two strings are already equal, so we don't have to perform any operations.
In the second test case, we can perform a single operation selecting the second candle to transform $ 01 $ into $ 11 $ .
In the third test case, it's impossible to perform any operations because there are no lit candles to select.
In the fourth test case, we can perform the following operations to transform $ a $ into $ b $ :

1. Select the $ 7 $ -th candle: $ 100010{\color{red}1}11\to 011101{\color{red} 1}00 $ .
2. Select the $ 2 $ -nd candle: $ 0{\color{red} 1}1101100\to 1{\color{red} 1}0010011 $ .
3. Select the $ 1 $ -st candle: $ {\color{red}1}10010011\to {\color{red}1}01101100 $ .
    In the fifth test case, we can perform the following operations to transform $ a $ into $ b $ :
4. Select the $ 6 $ -th candle: $ 00101{\color{red}1}011\to 11010{\color{red}1}100 $
5. Select the $ 2 $ -nd candle: $ 1{\color{red}1}0101100\to 0{\color{red}1}1010011 $
6. Select the $ 8 $ -th candle: $ 0110100{\color{red}1}1\to 1001011{\color{red}1}0 $
7. Select the $ 7 $ -th candle: $ 100101{\color{red}1}10\to 011010{\color{red}1}01 $

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
