#### Algorithm by Example

#### Problem 1

- Find the greatest common divisor of two non-negative integers m and n



#### 算法设计

- 要设计一个正确的算法
  - 如何定义正确



算法是为了解决问题；如果算法能解决这个问题，就叫对的

但是不利于抽象，需要规约

Specification

Input: non-negative integer m, n(所有合法的输入)

Output: gcd (m,n)（问题要求的输出）

算法必须能接受所有的合法的输入；

对每一个合法的输入，都能输出正确的值（这个可以被验证的）；

此即为算法的正确标准。



如何证明算法是对的？

测试只能证明算法是错的，但是不能证明是对的，因为合法的输入是**无穷**的。

数学归纳法。

- 弱归纳法
- 强归纳法



#### 数学归纳法

- 对什么做归纳

- Induction on n
  - Base case
    - n = 0: for any m, Euclid(m,0) = m;
    - n = 1; for any m, Euclid(m,1) = 1;
  - Assumption
    - For any n ≤ N, Euclid(m,n) is correct;
  - Induction
    - Euclid(m,N+1)=Euclid(N+1,m mod (N+1));







