#Deadlock
##一、运行结果
实验运行结果为：

![img1](http://oficjb2g0.bkt.clouddn.com/lock.png)

可以看到跑到第11次的时候从产生了死锁
##二、产生死锁的解释
程序的运行框架为：

![img2](http://oficjb2g0.bkt.clouddn.com/thread.png)

当t.start()之后，线程t被插入到调度队列里，当调度到它的时候就运行run()里的代码（b.methodB(a)，而在start函数之前，定义了count，当数到count的时候，运行a.methodA(b)。 

methodA、methodB及它们调用的函数都是用关键字synchronized，当线程访问object的一个synchronized同步代码块或同步方法时，其他线程对object中所有其他synchronized同步代码块或同步方法的访问将被阻塞。而代码中可能出现同时调用A类的methodA和last函数，导致资源都被阻塞，造成死锁。

![img3](http://oficjb2g0.bkt.clouddn.com/classab.png)
##三、产生死锁的四个必要条件
1. **互斥**：至少有一个资源必须处于非共享模式，即一次只有一个进程使用。如果另一进程申请该资源，那么申请进程必须等到该资源被释放为止。
1.  **占有并等待**：一个进程必须占有至少一个资源，并等待另一资源，而该资源被其他进程所占有。
1.   **非抢占**：资源不能被抢占，即资源只能在进程完成任务后自动释放。
1.   **循环等待**：有一组等待进程{P0，P1，... ,Pn}，P0等待的资源为P1所有，P1等待的资源为P2所有，......，Pn-1等待的资源为Pn所占有，Pn等待的资源为P0所占有。
  
  四个条件必须同时满足才会出现死锁。
