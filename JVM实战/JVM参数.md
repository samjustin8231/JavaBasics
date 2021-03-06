# JVM参数

在JVM内存分配中，有几个参数是比较核心的，如下所示。

-Xms：Java堆内存的大小

-Xmx：Java堆内存的最大大小

-Xmn：Java堆内存中的新生代大小，扣除新生代剩下的就是老年代的内存大小了

-XX:PermSize：永久代大小

-XX:MaxPermSize：永久代最大大小

-Xss：每个线程的栈内存大小

---
下面我们对上述参数来进行一一说明。

-Xms和-Xmx，分别用于设置Java堆内存的刚开始的大小，以及允许扩张到的最大大小。

对于这对参数，通常来说，都会设置为完全一样的大小。大家先不用太过于纠结这里的细节，因为其实JVM里的各种技术细节真的太多了，不能一下子全部都搞定，要随着后续几十个案例，层层铺展开来。

但是至少大家需要清楚，这两个参数，是用来限定Java堆内存的总大小的。

---
-Xmn，这个参数也是很常见的，他用来设置Java堆内存中的新生代的大小，然后扣除新生代大小之后的剩余内存就是给老年代的内存大小，我们看下图：

---
-XX:PermSize和-XX:MaxPermSize，分别限定了永久代大小和永久代的最大大小

通常这两个数值也是设置为一样的，至于原因，请看后面结合案例的文章分析。

如果是JDK 1.8以后的版本，那么这俩参数被替换为了-XX:MetaspaceSize和-XX:MaxMetaspaceSize，但是大家至少得知道，这两个参数限定了永久代的大小。

---
-Xss，这个参数限定了每个线程的栈内存大小

大家都很清楚，每个线程都有一个自己的虚拟机栈，然后每次执行一个方法，就会将方法的栈帧压入线程的栈里，方法执行完毕，那么栈帧就会从线程的栈里出栈。





