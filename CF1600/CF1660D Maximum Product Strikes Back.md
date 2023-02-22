
# Maximum Product Strikes Back题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

你有一个长度为 $n$ 的数组，每一个元素都在 $-2$ 和 $2$ 之间，当从数组首删去 $x$ 个元素，从数组末删去 $y$ 个元素时，数组剩下的乘积最大，输出 $x$ 和 $y$ 。
特别地，当存在多种情况时，输出任意一种即可； 当数组为空时，这个数组的乘积被认为是 $1$ 。

You are given an array $ a $ consisting of $ n $ integers. For each $ i $ ( $ 1 \le i \le n $ ) the following inequality is true: $ -2 \le a_i \le 2 $ .
You can remove any number (possibly $ 0 $ ) of elements from the beginning of the array and any number (possibly $ 0 $ ) of elements from the end of the array. You are allowed to delete the whole array.
You need to answer the question: how many elements should be removed from the beginning of the array, and how many elements should be removed from the end of the array, so that the result will be an array whose product (multiplication) of elements is maximal. If there is more than one way to get an array with the maximum product of elements on it, you are allowed to output any of them.
The product of elements of an empty array (array of length $ 0 $ ) should be assumed to be $ 1 $ .

#### 输入格式：

The first line of input data contains an integer $ t $ ( $ 1 \le t \le 10^4 $ ) —the number of test cases in the test.
Then the descriptions of the input test cases follow.
The first line of each test case description contains an integer $ n $ ( $ 1 \le n \le 2 \cdot 10^5 $ ) —the length of array $ a $ .
The next line contains $ n $ integers $ a_1, a_2, \dots, a_n $ ( $ |a_i| \le 2 $ ) — elements of array $ a $ .
It is guaranteed that the sum of $ n $ over all test cases does not exceed $ 2 \cdot 10^5 $ .

#### 输出格式：

For each test case, output two non-negative numbers $ x $ and $ y $ ( $ 0 \le x + y \le n $ ) — such that the product (multiplication) of the array numbers, after removing $ x $ elements from the beginning and $ y $ elements from the end, is maximal.
If there is more than one way to get the maximal product, it is allowed to output any of them. Consider the product of numbers on empty array to be $ 1 $ .

#### 样例输入输出：

| 样例1输入输出                                                | 样例2输入输出                       |
| ------------------------------------------------------------ | ----------------------------------- |
| 5<br/>4<br/>1 2 -1 2<br/>3<br/>1 1 -2<br/>5<br/>2 0 -2 2 -1<br/>3<br/>-2 -1 -1<br/>3<br/>-1 -2 -2 | 0 2<br/>3 0<br/>2 0<br/>0 1<br/>1 0 |

#### 样例解释：

In the first case, the maximal value of the product is $ 2 $ . Thus, we can either delete the first three elements (obtain array $ [2] $ ), or the last two and one first element (also obtain array $ [2] $ ), or the last two elements (obtain array $ [1, 2] $ ). Thus, in the first case, the answers fit: "3 0", or "1 2", or "0 2".
In the second case, the maximum value of the product is $ 1 $ . Then we can remove all elements from the array because the value of the product on the empty array will be $ 1 $ . So the answer is "3 0", but there are other possible answers.
In the third case, we can remove the first two elements of the array. Then we get the array: $ [-2, 2, -1] $ . The product of the elements of the resulting array is $ (-2) \cdot 2 \cdot (-1) = 4 $ . This value is the maximum possible value that can be obtained. Thus, for this case the answer is: "2 0".

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
