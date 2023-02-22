
# Robot on the Board 1题目（t.cpp）
时间限制 $ 1s$   |   空间限制 $ 256M$

#### 题目描述：

一个机器人在一个 $n$ 行 $m$ 列的长方形网格上，它可以移到四个相邻的格子里。
给出一个字符串指令序列 $s$，里面只会出现 `U`，`D`，`L`，`R` 四种指令，分别对应往上下左右四个方向移动。
机器人可以在任何一个格子开始移动，它会严格按照顺序执行 $s$ 中的每个字符指令。当它移出了网格的边缘，它会停止工作，所以机器人不一定能成功的执行完一个命令集。
现在需要让你求出一个使机器人在停止工作之前尽可能执行更多命令的起点。

The robot is located on a checkered rectangular board of size $ n \times m $ ( $ n $ rows, $ m $ columns). The rows in the board are numbered from $ 1 $ to $ n $ from top to bottom, and the columns — from $ 1 $ to $ m $ from left to right.
The robot is able to move from the current cell to one of the four cells adjacent by side.
The sequence of commands $ s $ executed by the robot is given. Each command is denoted by one of the symbols 'L', 'R', 'D' or 'U', and triggers the movement to left, right, down or up, respectively.
The robot can start its movement in any cell. The robot executes the commands starting from the first one, strictly in the order in which they are listed in $ s $ . If the robot moves beyond the edge of the board, it falls and breaks. A command that causes the robot to break is not considered successfully executed.
The robot's task is to execute as many commands as possible without falling off the board. For example, on board $ 3 \times 3 $ , if the robot starts a sequence of actions $ s= $ "RRDLUU" ("right", "right", "down", "left", "up", "up") from the central cell, the robot will perform one command, then the next command will force him to cross the edge. If the robot starts moving from the cell $ (2, 1) $ (second row, first column) then all commands will be executed successfully and the robot will stop at the cell $ (1, 2) $ (first row, second column).
![](https://cdn.luogu.com.cn/upload/vjudge_pic/CF1607E/e9041329204b86a5b243e3524c9fedaa23a2383e.png)The robot starts from cell $ (2, 1) $ (second row, first column). It moves right, right, down, left, up, and up. In this case it ends in the cell $ (1, 2) $ (first row, second column).Determine the cell from which the robot should start its movement in order to execute as many commands as possible.

#### 输入格式：

The first line contains an integer $ t $ ( $ 1 \leq t \leq 10^4 $ ) — the number of test cases.
The next $ 2t $ lines contain descriptions of the test cases.
In the description of each test case, the first line contains two integers $ n $ and $ m $ ( $ 1 \leq n, m \leq 10^6 $ ) — the height and width of the field that the robot is located on. The second line of the description is a string $ s $ consisting solely of characters 'L', 'R', 'D' and 'U' — the sequence of commands the robot executes. The string has a length from $ 1 $ to $ 10^6 $ commands.
It is guaranteed that the total length of $ s $ over all test cases does not exceed $ 10^6 $ .

#### 输出格式：

Print $ t $ lines, each of which contains the answer to the corresponding test case. The answer to the test case are two integers $ r $ ( $ 1 \leq r \leq n $ ) and $ c $ ( $ 1 \leq c \leq m $ ), separated by a space — the coordinates of the cell (row number and column number) from which the robot should start moving to perform as many commands as possible.
If there are several such cells, you may output any of them.

#### 样例输入输出：

| 样例1输入                                                    | 样例1输出                   |
| ------------------------------------------------------------ | --------------------------- |
| 4<br/>1 1<br/>L<br/>1 2<br/>L<br/>3 3<br/>RRDLUU<br/>4 3<br/>LUURRDDLLLUU | 1 1<br/>1 2<br/>2 1<br/>3 2 |

<div STYLE="page-break-after: always;"/>

#### 题解：



#### 参考代码：

```c++

```
