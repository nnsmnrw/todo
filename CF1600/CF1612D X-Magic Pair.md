
# X-Magic Pair题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

给一个数对 $(a,b)$ ，每次可以进行操作 $(a,b) \to (|a-b|,b)$ 或 $(a,|a-b|)$ 。问最后能否令 $a=x$ 或 $b=x$ 。$a,b,x \le 10^{18}$



You are given a pair of integers $ (a, b) $ and an integer $ x $ .
You can change the pair in two different ways:

- set (assign) $ a := |a - b| $ ;
- set (assign) $ b := |a - b| $ ,
    where $ |a - b| $ is the absolute difference between $ a $ and $ b $ .The pair $ (a, b) $ is called $ x $ -magic if $ x $ is obtainable either as $ a $ or as $ b $ using only the given operations (i.e. the pair $ (a, b) $ is $ x $ -magic if $ a = x $ or $ b = x $ after some number of operations applied). You can apply the operations any number of times (even zero).
    Your task is to find out if the pair $ (a, b) $ is $ x $ -magic or not.
    You have to answer $ t $ independent test cases.

#### 输入格式：

The first line of the input contains one integer $ t $ ( $ 1 \le t \le 10^4 $ ) — the number of test cases. The next $ t $ lines describe test cases.
The only line of the test case contains three integers $ a $ , $ b $ and $ x $ ( $ 1 \le a, b, x \le 10^{18} $ ).

#### 输出格式：

For the $ i $ -th test case, print YES if the corresponding pair $ (a, b) $ is $ x $ -magic and NO otherwise.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                                                  |
| ------------------------------------------------------------ | ---------------------------------------------------------- |
| 8<br/>6 9 3<br/>15 38 7<br/>18 8 8<br/>30 30 30<br/>40 50 90<br/>24 28 20<br/>365 216 52<br/>537037812705867558 338887693834423551 3199921013340 | YES<br/>YES<br/>YES<br/>YES<br/>NO<br/>YES<br/>YES<br/>YES |

#### 样例解释：



<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
