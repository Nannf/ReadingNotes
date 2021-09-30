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

- 抽象的机器的标准操作在实际的机器上一定有对应的实现；
- 且可以在有限步骤之内进行模拟实现

抽象的机器就是计算模型。

- 图灵机
- RAM model



#### RAM Model

##### 标准构成

- Read-only input tape
- Program
- Location counter
- Accumulator
- Memory
- Write-only output tape



##### 特性

- Each **simple operation** takes one time step
  - +/-
  - memory access
- Non-simple operations shoule be decomposed
  - Loop
  - Subroutine
- Memory
  - Memory access is simple operation
  - Unlimited memory



很简化



##### 为什么使用RAM 不用图灵机

- 模型精细->越难用，越复杂

讲授基础知识，基本内容，RAM足矣。图灵机相对而言太复杂了。









#### 小结

本节课从为什么计算机似乎能解决所有的事情出发，阐述了如果我们能把我们日常的工作编解码成0，1代码，那么这个对计算机而言就是可以实现的。但是像艺术创作，表达情感这样的无法编码或者很难编码的任务，计算机的表现就不佳。

如何进行编解码就是算法的工作。

算法就是使用cpu得提供的有限的指令集，进行无限的组合从而实现各种功能的一种计算模式。

这样说并不妥当，因为在cpu出来之前，我们就可以解决一些问题；

我们的算法应该是基于一个抽象的计算器，这个计算器能提供一些基本的简单操作，我们的算法组合的就是这样简单操作。

基于此提出了本节的最重要的概念，计算模型。

而图灵机就是一个相对比较完善的，比较复杂的计算模型。

计算模型就是这样一台虚拟的计算机。

所有的算法都是基于这样一台虚拟的计算机进行工作。

