#### Exception & Error

- 都是Throwable的子类
- Error比较严重，一般发生这种情况时，程序无法恢复到正常
  - OOM
- Exception按照编译器是否需要被捕获可分为检测性和非检测型
  - 检测型包括IO异常
  - 非检测型包括RuntimeException,运行时异常，比如数组越界；



![img](https://static001.geekbang.org/resource/image/ac/00/accba531a365e6ae39614ebfa3273900.png)

其实这里作者也说出了一个我的疑问，因为检测型异常的初衷是加上我们可以对其进行处理，实际上我们处理不了，而且再处理异常的过程中，还可能会接着出现异常；

但是另一个地方考虑，像网络io这种具有波动性的，是可以进行尝试成功的；



try-catch在生成堆栈信息的时候，需要生成当前函数栈的一个快照，然后打印出异常信息；

这个比较耗时；

