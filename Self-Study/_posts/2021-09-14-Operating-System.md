---
layout: post
title: 【OS】Operating System
---



1. **操作系统的特征**

操作系统的特征包括：并发，共享，虚拟，异步。
其中，并发和共享互为存在条件。举个例子：当两个进程正在并发执行的时候，需要共享的访问硬盘资源。如果失去并发性，则系统中只有一个程序正在运行，则共享性失去存在的意义。
![并发共享.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/并发共享.png)

2. **操作系统的发展过程**

![OS的发展与分类.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/OS的发展与分类.png)

3. **操作系统的运行机制和体系结构**

![OS的运行机制和体系结构.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/OS的运行机制和体系结构.png)
当处理器状态是用户态时，cpu只能执行非特权指令，当是核心态时，特权指令，非特权指令都可执行。

操作系统的内核程序是系统的管理者，既可执行特权指令，也可执行非特权指令，运行在核心态。
为了保证系统能安全运行，普通应用程序只能执行非特权指令，运行在用户态。

![计算机系统的层次结构.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/计算机系统的层次结构.png)

大内核：企业初创时体量不大，管理层的人会负责大部分的事情。
微内核：随着企业体量越来越大，管理层只负责最核心的一些工作。

3. **中断和异常**

![中断的分类.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/中断的分类.png)
用户态到核心态是通过终端实现的，并且中断是唯一途径。
核心态到用户态的切换是通过执行一个特权指令，将程序状态字(PSW)的标志位设置为用户态。

![中断和异常.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/中断和异常.png)

4. **系统调用**

![中断和异常.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/中断和异常.png)

![中断的分类.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/中断的分类.png)

5. **进程**
PCB 存放操作系统用于管理程序的各种各样的信息。
程序段，数据段，PCB三部分组成了进程实体(进程映像)。一般情况下，我们把进程实体就简称炜进程，例如，所谓创建进程，实质上是创建进程实体中的PCB；而撤销进程，实质上是撤销进程实体中的PCB。注意：PCB是进程存在的唯一标志。

从不同的角度，进程可以有不同的定义，比较传统的典型定义有：
1. 进程是程序的一次执行过程。
2. 进程是一个程序及其数据在处理机上顺序执行时所发生的活动。
3. 进程是具有独立功能的程序在数据集合上运行的过程，它是系统进行资源分配和调度的一个独立单位。

引入进程实体的概念后，可把进程定义为：
进程是进程实体的运行过程，是系统进行资源分配和调度的一个独立单位。进程实体和进程不一样，进程实体是静态的，进程则是动态的。
![PCB.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/PCB.png)

![进程的组成.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/进程的组成.png)

PCB是操作系统对各个进程进行管理的数据所存放的地方。

![进程的特征.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/进程的特征.png)
动态性是进程最基本的特征。

进程有三种基本状态，运行态，就绪态，阻塞态。运行态即占有cpu，并在cpu上运行。就绪态指已经具备运行条件，但由于没有空闲的cpu，而暂时不能运行。阻塞态指因等待某一件事而暂时不能运行。

![进程状态的转换.png](https://gitee.com/junyang-chen/daily_photo/raw/master/img/进程状态的转换.png)