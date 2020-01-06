# JVM参数

在JVM内存分配中，有几个参数是比较核心的，如下所示。

-Xms：Java堆内存的大小

-Xmx：Java堆内存的最大大小

-Xmn：Java堆内存中的新生代大小，扣除新生代剩下的就是老年代的内存大小了

-XX:PermSize：永久代大小

-XX:MaxPermSize：永久代最大大小

-Xss：每个线程的栈内存大小

---
-Xms和-Xmx，分别用于设置Java堆内存的刚开始的大小，以及允许扩张到的最大大小。

