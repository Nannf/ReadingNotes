#### Model of Computation

- 计算模型



##### 如何组织主线

- 问题
  - 排序
  - 选择
  - 图遍历
- 策略
  - 动态规划
  - 分治

正交的维度。



#### 问题

##### Order

比大小

- 排序
- 查找



##### Graph

- DFS
- BFS



##### 策略

- 蛮力
  - 一个一个找
  - 大智若愚
- 分治策略
  - 排序
  - 选择
  - 查找

蛮力->分治策略的提升



- 贪心
- 动态规划



##### 抽象

- 与机器无关
- 与机器语言无关

什么是计算？

核心含义

计算模型-> 算法设计与分析

有了计算模型之后才能进行抽象的算法设计与分析

抽象指的是与机器无关，与程序语言无关。





#### 问题

##### 为什么计算机似乎无所不能

- 聊天
- 电影
- 看论文
- 写代码
- ...

##### 为什么计算机有时候比较厉害，有时候比较不行

- 百万量级的歌曲内容查找，计算机比较擅长
- 普一段曲子，计算机似乎不太擅长

由此引出：计算是什么



#### 计算的要素

- 计算机无所不能的原因是0，1的编解码（使能技术）
  - 编码
  - 处理
  - 解码
- 图灵机
  - An abstract/logical computer



计算就是对一串0，1编码，用一系列不多的指令集进行处理。



#### 计算的类比

- 积木
  - 积木块的种类是有限的
  - 假设积木块的个数是无限的话，可以搭配成无穷多的形状
- 谱曲
  - 音符的种类是有限的
  - 音符的组合是无限的
- 文字创作

本质的相像。

- cpu的指令集是有限的
- 但是cpu可以做无穷多的事情（几乎是无所不能的）



Rebuild the world with 0s and 1s.



#### Algorithm

- To solve a specific problem(so called an algorithmic problem)
- Combination of basic operations
  - in a precise(精确) and elegant(优美) way
  - the art of computer programming



### Model of Computation

- Problems
  - Why the algorithms we learn can run almost everywhere?
  - Why the algorithms we learn can be implemented in any language?
- Machine-and language-independent algorthms, running on an **abstract** machine
  - Turing machine: over-qualify
  - RAM model: simple but powerful



抽象

- 与具体的机器无关
- 与具体的语言无关

抽象的算法，抽象的道理。

机器能做种类不多的事情（指令集是有限的）；

但是种类不多的事情的组合是无穷的；

计算机做的就是把有限种类的操作进行无限次的组合达到似乎无所不能的感觉。

抽象的算法基于抽象的机器才能运行。

抽象的机器就是计算模型。

- 图灵机
- RAM model





