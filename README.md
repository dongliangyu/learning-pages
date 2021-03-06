## 学习笔记 - 深入理解Java虚拟机

### 一、 java虚拟机内存模型

#### 1. 程序计数器
   * 程序计数器是线程私有的。
   * 存储线程需要执行的字节码指令地址，如果正在执行的是Native方法，计数器为undefined。
   * 记录线程切换，线程恢复、分支、循环、跳转、异常等信息。
   * 唯一在《Java虚拟机规范》中没有规定任何OutOfMemoryError情况的区域。
   
#### 2. Java虚拟机栈
   * Java虚拟机栈是线程私有的。
   * 存储局部变量表、操作数栈、动态连接、方法出口等信息。
   * 线程请求的栈深度大于虚拟机所允许的深度，将抛出StackOverflowError。
   * Java虚拟机栈容量可以动态扩展，当栈扩展时无法申请到足够的内存会抛出OutOfMemoryError。


