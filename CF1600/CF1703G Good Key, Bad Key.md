
# Good Key, Bad Key题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

你有 $n$ 个箱子。第 $i$ 个箱子中有 $a_i$ 个硬币。你需要按照从箱子 $1$ 号到箱子 $n$ 号的顺序打开所有 $n$ 个箱子。
你可以用以下两种钥匙之一打开一个箱子：

- 好钥匙：使用一次消耗 $k$ 个硬币。
- 坏钥匙：使用时不消耗硬币，但会使所有未打开的箱子中的硬币数减半（包括正要打开的这个箱子）。硬币减半时向下取整。比如，用坏钥匙打开箱子 $i$ 号时，$a_i=a_i/2$，$a_{i+1}=a_{i+1}/2$，$......$，$a_n=a_n/2$。
    所有钥匙用过一次就会断掉（别想着买一把好钥匙开完所有箱子了），好钥匙需要重复付费，坏钥匙效果会重复计算。
    也就是说，你总共需要使用 $n$ 把钥匙，每个箱子用一把。开始时，你没有硬币和钥匙，如果想用好钥匙，你就得去买。值得注意的是，在这个过程中你可以赊账买钥匙；例如，如果你只有 $1$ 个硬币，你也可以购买价值 $k=3$ 个硬币的好钥匙，你的余额会变成 $-2$ 个硬币。
    你需要求出开完所有箱子之后你能获得的最大硬币数量（显然大于等于 $0$ ）。



第一行包含一个整数 $t$（$1 \leq t \leq 10
^4$），表示测试数据的组数。

- 每组测试数据的第一行包含两个整数 $n$ 和 $k$（$1 \leq n \leq 10^5$，$0 \leq k \leq 10^9$），分别表示箱子的个数和每把好钥匙的花费。
- 每组测试数据的第二行包含 $n$ 个整数 $a_i$（$0 \leq a_i \leq 10^9$），表示每个箱子中硬币的数量。
    所有测试数据中 $n$ 的总和不超过 $10^5$ 。



对于每组测试数据，输出对应的可获得的最大硬币数量。
提示（题面中给出）：开 $long$ $long$



There are $ n $ chests. The $ i $ -th chest contains $ a_i $ coins. You need to open all $ n $ chests in order from chest $ 1 $ to chest $ n $ .
There are two types of keys you can use to open a chest:

- a good key, which costs $ k $ coins to use;
- a bad key, which does not cost any coins, but will halve all the coins in each unopened chest, including the chest it is about to open. The halving operation will round down to the nearest integer for each chest halved. In other words using a bad key to open chest $ i $ will do $ a_i = \lfloor{\frac{a_i}{2}\rfloor} $ , $ a_{i+1} = \lfloor\frac{a_{i+1}}{2}\rfloor, \dots, a_n = \lfloor \frac{a_n}{2}\rfloor $ ;
- any key (both good and bad) breaks after a usage, that is, it is a one-time use.
    You need to use in total $ n $ keys, one for each chest. Initially, you have no coins and no keys. If you want to use a good key, then you need to buy it.
    During the process, you are allowed to go into debt; for example, if you have $ 1 $ coin, you are allowed to buy a good key worth $ k=3 $ coins, and your balance will become $ -2 $ coins.
    Find the maximum number of coins you can have after opening all $ n $ chests in order from chest $ 1 $ to chest $ n $ .

#### 输入格式：

The first line contains a single integer $ t $ ( $ 1 \leq t \leq 10^4 $ ) — the number of test cases.
The first line of each test case contains two integers $ n $ and $ k $ ( $ 1 \leq n \leq 10^5 $ ; $ 0 \leq k \leq 10^9 $ ) — the number of chests and the cost of a good key respectively.
The second line of each test case contains $ n $ integers $ a_i $ ( $ 0 \leq a_i \leq 10^9 $ ) — the amount of coins in each chest.
The sum of $ n $ over all test cases does not exceed $ 10^5 $ .

#### 输出格式：

For each test case output a single integer — the maximum number of coins you can obtain after opening the chests in order from chest $ 1 $ to chest $ n $ .
Please note, that the answer for some test cases won't fit into 32-bit integer type, so you should use at least 64-bit integer type in your programming language (like long long for C++).

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                     |
| ------------------------------------------------------------ | ----------------------------- |
| 5<br/>4 5<br/>10 10 3 1<br/>1 2<br/>1<br/>3 12<br/>10 10 29<br/>12 51<br/>5 74 89 45 18 69 67 67 11 96 23 59<br/>2 57<br/>85 60 | 11<br/>0<br/>13<br/>60<br/>58 |

#### 样例解释：

xxxxxxxxxx1 1​c++

- Buy a good key for $ 5 $ coins, and open chest $ 1 $ , receiving $ 10 $ coins. Your current balance is $ 0 + 10 - 5 = 5 $ coins.
- Buy a good key for $ 5 $ coins, and open chest $ 2 $ , receiving $ 10 $ coins. Your current balance is $ 5 + 10 - 5 = 10 $ coins.
- Use a bad key and open chest $ 3 $ . As a result of using a bad key, the number of coins in chest $ 3 $ becomes $ \left\lfloor \frac{3}{2} \right\rfloor = 1 $ , and the number of coins in chest $ 4 $ becomes $ \left\lfloor \frac{1}{2} \right\rfloor = 0 $ . Your current balance is $ 10 + 1 = 11 $ .
- Use a bad key and open chest $ 4 $ . As a result of using a bad key, the number of coins in chest $ 4 $ becomes $ \left\lfloor \frac{0}{2} \right\rfloor = 0 $ . Your current balance is $ 11 + 0 = 11 $ .
    At the end of the process, you have $ 11 $ coins, which can be proven to be maximal.

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
