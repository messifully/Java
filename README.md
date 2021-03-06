- [Java基础](#java基础)
  - [基础问题](#基础问题)
  - [Java集合](#java集合)
    - [HashMap](#hashmap)
    - [ArrayList](#arraylist)
    - [LinkedList](#linkedlist)
    - [堆Heap](#堆heap)
  - [ConcurrentHashMap](#concurrenthashmap)
  - [容器](#容器)
    - [同步容器](#同步容器)
    - [并发容器](#并发容器)
  - [枚举Enum](#枚举enum)
- [Redis](#redis)
  - [基础](#基础)
      - [Redis数据结构](#redis数据结构)
        - [引入及配置](#引入及配置)
        - [Redis使用](#redis使用)
        - [Redis问题](#redis问题)
        - [Redis问答](#redis问答)
        - [Redis主从复制、哨兵、Cluster三种集群模式](#redis主从复制哨兵cluster三种集群模式)
          - [主从复制模式](#主从复制模式)
          - [Sentinel（哨兵）模式](#sentinel哨兵模式)
          - [Cluster模式](#cluster模式)
      - [Redis持久化](#redis持久化)
      - [Redis应用场景](#redis应用场景)
      - [Redis设计思想](#redis设计思想)
- [Kafka](#kafka)
  - [**Kafka群集部署**](#kafka群集部署)
  - [**Kakfa的设计思想**](#kakfa的设计思想)
        - [如何保证百万级写入速度：](#如何保证百万级写入速度)
          - [页缓存技术 + 磁盘顺序写 +零拷贝技术](#页缓存技术--磁盘顺序写-零拷贝技术)
        - [Kafka如何做到不丢失不重复消费](#kafka如何做到不丢失不重复消费)
          - [**kafka的消息传递机制**](#kafka的消息传递机制)
        - [幂等的producer](#幂等的producer)
- [多线程](#多线程)
  - [锁](#锁)
    - [锁原理](#锁原理)
      - [volatile](#volatile)
        - [JMM（JavaMemoryModel）](#jmmjavamemorymodel)
        - [可见性的解决方案](#可见性的解决方案)
          - [加锁](#加锁)
          - [Volatile修饰共享变量](#volatile修饰共享变量)
          - [应用](#应用)
      - [**AQS**](#aqs)
      - [**CAS**](#cas)
      - [synchronized](#synchronized)
        - [对象内存分布](#对象内存分布)
        - [锁升级](#锁升级)
          - [偏向锁](#偏向锁)
          - [轻量级锁](#轻量级锁)
          - [自旋锁](#自旋锁)
      - [Lock](#lock)
      - [ThreadLocal](#threadlocal)
    - [锁类型](#锁类型)
        - [乐观锁、悲观锁<a name = "乐观锁、悲观锁-头"></a>](#乐观锁悲观锁)
        - [**自旋锁、适应性自旋锁**<a name = "自旋锁、适应性自旋锁-头"></a>](#自旋锁适应性自旋锁)
        - [无锁、偏向锁、轻量级锁、重量级锁<a name ="无锁、偏向锁、轻量级锁、重量级锁"></a>](#无锁偏向锁轻量级锁重量级锁)
        - [公平锁、非公平锁<a name ="公平锁、非公平锁-头"></a>](#公平锁非公平锁)
        - [可重入锁、非可重入锁<a name = "可重入锁、非可重入锁-头"></a>](#可重入锁非可重入锁)
        - [独享锁、共享锁<a name = "独享锁、共享锁-头"></a>](#独享锁共享锁)
        - [互斥锁、自旋锁](#互斥锁自旋锁)
        - [读写锁](#读写锁)
    - [**锁优化**](#锁优化)
  - [java.util.concurrent](#javautilconcurrent)
    - [包基本内容](#包基本内容)
    - [**atomic**](#atomic)
    - [**locks**](#locks)
        - [**ThreadPoolExecutor**<a name ="ThreadPoolExecutor-tail"></a>](#threadpoolexecutor)
          - [**workQueue任务队列**](#workqueue任务队列)
          - [RejectedExecutionHandler拒绝策略](#rejectedexecutionhandler拒绝策略)
          - [预定义线程池](#预定义线程池)
    - [**collections**](#collections)
    - [**tools**](#tools)
      - [**CountDownLatch**<a name = "CountDownLatch-tail"></a>](#countdownlatch)
      - [**CyclicBarrier**<a name = "CyclicBarrier-tail"></a>](#cyclicbarrier)
      - [Semaphore<a name = "Semaphore-tail"></a>](#semaphore)
    - [多线程使用示例](#多线程使用示例)
      - [**实现ABC交叉打印**](#实现abc交叉打印)
        - [Synchronized同步法](#synchronized同步法)
        - [Lock锁方法](#lock锁方法)
        - [ReentrantLock结合Condition](#reentrantlock结合condition)
        - [Semaphore信号量方式](#semaphore信号量方式)
- [**Linux**](#linux)
    - [Java开发环境](#java开发环境)
      - [**JDK**](#jdk)
      - [**Tomcat**](#tomcat)
      - [Mysql](#mysql)
      - [apt更换源](#apt更换源)
    - [常用命令](#常用命令)
      - [文件管理](#文件管理)
      - [服务篇](#服务篇)
        - [ip](#ip)
        - [mysql](#mysql-1)
        - [tomcat](#tomcat-1)
      - [工具](#工具)
        - [vim](#vim)
    - [运维问题](#运维问题)
    - [Mysql调优](#mysql调优)
- [Spring](#spring)
  - [IOC容器](#ioc容器)
  - [**AOP**](#aop)
- [SpringMVC](#springmvc)
- [SpringBoot](#springboot)
    - [整合其他框架](#整合其他框架)
      - [ElasticSearch](#elasticsearch)
    - [Spring Data JPA](#spring-data-jpa)
      - [Repository 接口](#repository-接口)
- [MyBatis](#mybatis)
- [MySql](#mysql-2)
  - [存储引擎](#存储引擎)
    - [InnoDB](#innodb)
      - [InnoDB 内存架构](#innodb-内存架构)
      - [InnoDB 磁盘架构](#innodb-磁盘架构)
    - [MyISAM](#myisam)
    - [InnoDB 和 MyISAM 的比较](#innodb-和-myisam-的比较)
  - [日志系统](#日志系统)
    - [**重做日志（redo log）**](#重做日志redo-log)
      - [**脏数据刷盘**](#脏数据刷盘)
      - [**脏日志刷盘**](#脏日志刷盘)
      - [日志刷盘的规则](#日志刷盘的规则)
      - [数据页刷盘的规则及checkpoint](#数据页刷盘的规则及checkpoint)
    - [**二进制日志（`binlog`）**](#二进制日志binlog)
    - [**回滚日志（```undo log```）**](#回滚日志undo-log)
  - [索引](#索引)
    - [背景](#背景)
      - [磁盘IO和预读](#磁盘io和预读)
      - [索引是什么？](#索引是什么)
    - [BTree索引](#btree索引)
    - [B+Tree索引](#btree索引-1)
    - [B+ Tree 原理](#b-tree-原理)
      - [数据结构](#数据结构)
      - [操作](#操作)
      - [树的常见特性](#树的常见特性)
      - [B + 树与红黑树的比较](#b--树与红黑树的比较)
      - [B + 树与 B 树的比较](#b--树与-b-树的比较)
    - [MySQL 索引](#mysql-索引)
      - [B+ Tree 索引](#b-tree-索引)
      - [哈希索引](#哈希索引)
      - [全文索引](#全文索引)
      - [空间数据索引](#空间数据索引)
    - [索引的优点](#索引的优点)
    - [索引的使用条件](#索引的使用条件)
    - [如何合理创建索引](#如何合理创建索引)
      - [索引不生效的原因](#索引不生效的原因)
      - [无法避免对索引列使用函数，怎么使用索引](#无法避免对索引列使用函数怎么使用索引)
        - [前缀索引与索引选择性](#前缀索引与索引选择性)
      - [索引设计准则：三星索引](#索引设计准则三星索引)
  - [Mysql调优](#mysql调优-1)
    - [**Explain**](#explain)
        - [**排除缓存干扰**](#排除缓存干扰)
        - [**Explain**](#explain-1)
        - [**覆盖索引**](#覆盖索引)
        - [联合索引](#联合索引)
        - [最左匹配原则](#最左匹配原则)
        - [索引下推](#索引下推)
        - [唯一索引普通索引选择难题](#唯一索引普通索引选择难题)
        - [前缀索引](#前缀索引)
        - [条件字段函数操作](#条件字段函数操作)
        - [隐式类型转换](#隐式类型转换)
        - [隐式字符编码转换](#隐式字符编码转换)
        - [总结](#总结)
    - [查询性能优化](#查询性能优化)
      - [合理创建索引](#合理创建索引)
        - [独立的列](#独立的列)
        - [多列索引](#多列索引)
        - [索引列的顺序](#索引列的顺序)
      - [使用 explain 分析 select 查询语句](#使用-explain-分析-select-查询语句)
      - [优化数据访问](#优化数据访问)
        - [减少请求的数据量](#减少请求的数据量)
        - [减少服务器端扫描的行数](#减少服务器端扫描的行数)
      - [重构查询方式](#重构查询方式)
        - [切分大查询](#切分大查询)
        - [分解大连接查询](#分解大连接查询)
  - [事务](#事务)
    - [ACID](#acid)
    - [ACID 之间的关系](#acid-之间的关系)
    - [隔离问题](#隔离问题)
    - [隔离级别](#隔离级别)
    - [Mysql事务的实现](#mysql事务的实现)
      - [**多版本并发控制（MVCC）**](#多版本并发控制mvcc)
      - [InnoDB的MVCC实现逻辑](#innodb的mvcc实现逻辑)
        - [**InnoDB存储引擎保存的MVCC的数据**](#innodb存储引擎保存的mvcc的数据)
          - [**`undo log`**](#undo-log)
          - [`ReadView`](#readview)
        - [`READ COMMITTED` 隔离级别下的``ReadView``](#read-committed-隔离级别下的readview)
        - [`REPEATABLE READ` 隔离级别下的`ReadView`](#repeatable-read-隔离级别下的readview)
        - [MVCC总结](#mvcc总结)
  - [锁](#锁-1)
    - [锁类型](#锁类型-1)
    - [**粒度锁**](#粒度锁)
    - [**InnoDB行级锁和表级锁**](#innodb行级锁和表级锁)
      - [**InnoDB锁模式**](#innodb锁模式)
      - [**InnoDB加锁方法**](#innodb加锁方法)
      - [InnoDB 行锁实现方式](#innodb-行锁实现方式)
      - [**InnoDB的间隙锁**](#innodb的间隙锁)
      - [**InnoDB 在不同隔离级别下的一致性读及锁的差异：**](#innodb-在不同隔离级别下的一致性读及锁的差异)
      - [获取 InnoDB 行锁争用情况：](#获取-innodb-行锁争用情况)
      - [**LOCK TABLES 和 UNLOCK TABLES**](#lock-tables-和-unlock-tables)
      - [**LOCK TABLES语法**](#lock-tables语法)
      - [使用LOCK TABLES的场景](#使用lock-tables的场景)
    - [MVCC](#mvcc)
      - [基础概念](#基础概念)
      - [实现过程](#实现过程)
      - [快照读与当前读](#快照读与当前读)
    - [锁算法](#锁算法)
      - [Record Lock](#record-lock)
      - [Gap Lock](#gap-lock)
      - [Next-Key Lock](#next-key-lock)
  - [分库分表数据切分](#分库分表数据切分)
    - [水平切分](#水平切分)
    - [垂直切分](#垂直切分)
    - [Sharding 策略](#sharding-策略)
    - [Sharding 存在的问题](#sharding-存在的问题)
  - [复制](#复制)
    - [主从复制](#主从复制)
    - [读写分离](#读写分离)
  - [关系数据库设计理论](#关系数据库设计理论)
    - [函数依赖](#函数依赖)
    - [异常](#异常)
    - [范式](#范式)
      - [第一范式 (1NF)](#第一范式-1nf)
      - [第二范式 (2NF)](#第二范式-2nf)
      - [第三范式 (3NF)](#第三范式-3nf)
    - [ER 图](#er-图)
    - [实体的三种联系](#实体的三种联系)
    - [表示出现多次的关系](#表示出现多次的关系)
    - [联系的多向性](#联系的多向性)
    - [表示子类](#表示子类)
  - [其他使用相关](#其他使用相关)
    - [JSON](#json)
      - [JSON_CONTAINS](#json_contains)
      - [JSON_CONTAINS_PATH](#json_contains_path)
      - [column->path、column->>path](#column-pathcolumn-path)
- [ElasticSearch](#elasticsearch-1)
      - [安装](#安装)
        - [windows](#windows)
- [Zookeeper](#zookeeper)
      - [集群搭建](#集群搭建)
      - [Zookeeper启动](#zookeeper启动)
- [Mongodb](#mongodb)
- [RabbitMQ](#rabbitmq)
- [SpringCloud](#springcloud)
- [Hadoop/Spark](#hadoopspark)
- [互联网工具](#互联网工具)
      - [Jenkins](#jenkins)
      - [Git](#git)
      - [Maven](#maven)
      - [Nginx](#nginx)
      - [Docker](#docker)
- [事务](#事务-1)
  - [事务的特性（ACID）](#事务的特性acid)
- [JVM](#jvm)
  - [JVM整体架构](#jvm整体架构)
    - [类加载器子系统](#类加载器子系统)
      - [**类加载器ClassLoader加载**](#类加载器classloader加载)
      - [**链接**](#链接)
      - [**初始化**](#初始化)
    - [Java运行时数据区](#java运行时数据区)
    - [执行引擎](#执行引擎)
    - [常见问题](#常见问题)
  - [**JMM Java内存模型**](#jmm-java内存模型)
  - [**GC垃圾回收**](#gc垃圾回收)
    - [GC参数](#gc参数)
  - [常用JVM配置参数](#常用jvm配置参数)
  - [性能监控工具](#性能监控工具)
    - [命令](#命令)
- [分布式](#分布式)
  - [分布式锁与分布式事务](#分布式锁与分布式事务)
    - [分布式锁](#分布式锁)
        - [基于缓存实现分布式锁](#基于缓存实现分布式锁)
          - [Redis](#redis-1)
- [数据结构和算法](#数据结构和算法)
  - [排序](#排序)
    - [冒泡排序](#冒泡排序)
    - [快速排序](#快速排序)
    - [归并排序](#归并排序)
    - [插入排序](#插入排序)
    - [希尔排序](#希尔排序)
    - [堆排序](#堆排序)
    - [桶排序](#桶排序)
    - [基数排序](#基数排序)
  - [算法](#算法)
- [计算机网络](#计算机网络)
- [IDEA](#idea)
  - [快捷键](#快捷键)
- [实用工具](#实用工具)
  - [文档编辑](#文档编辑)
    - [Typora](#typora)
- [技能](#技能)

# Java基础

## 基础问题

**[1.java项目中的classpath到底是什么](https://segmentfault.com/a/1190000015802324)**

![clipboard.png](https://segmentfault.com/img/bVbes4j?w=1006&h=994)

compareTo()

Ps：（快速记忆法）当前对象与后一个对象进行比较，如果比较结果为1进行交换，其他不进行交换。

当后一个对象比当前对象大，返回结果值为1时，前后交换，说明是倒序排列。

当后一个对象比当前对象小，返回结果值为1时，前后交换，说明是升序排列。



## Java集合

![img](https://img2018.cnblogs.com/blog/1362965/201901/1362965-20190118094735724-2129767713.png)

 

![img](https://img2018.cnblogs.com/blog/1362965/201901/1362965-20190118095106326-273814633.png)

 

。

![img](https://www.runoob.com/wp-content/uploads/2014/01/2243690-9cd9c896e0d512ed.gif)

**常用集合的分类：**

**Collection** 接口的接口 对象的集合（单列集合） 
 ├——-**List** 接口：元素按进入先后有序保存，可重复 
 │—————-├ **LinkedList** 接口实现类， 链表， 插入删除， 没有同步， 线程不安全 
 │—————-├ **ArrayList** 接口实现类， 数组， 随机访问， 没有同步， 线程不安全 
 │—————-└ **Vector** 接口实现类 数组， 同步， 线程安全 
 │ ———————-└ **Stack** 是Vector类的实现类 
 └——-**Set** 接口： 仅接收一次，不可重复，并做内部排序 
 ├—————-└**HashSet** 使用hash表（数组）存储元素 
 │————————└ **LinkedHashSet** 链表维护元素的插入次序 
 └ —————-**TreeSet** 底层实现为二叉树，元素排好序

**Map** 接口 键值对的集合 （双列集合） 
 ├———**Hashtable** 接口实现类， 同步， 线程安全 
 ├———**HashMap** 接口实现类 ，没有同步， 线程不安全- 
 │—————–├ **LinkedHashMap** 双向链表和哈希表实现 
 │—————–└ **WeakHashMap** 
 ├ ——–**TreeMap** 红黑树对所有的key进行排序 
 └———**IdentifyHashMap**



### HashMap

**原理**：通过计算key的hash值，对数组长度取余后得到下标，找到table数组对应下标，如果此槽为null，则放入；否则，进行比较：如果此时槽内hash值与key的hash相等并且key值相等（==或equals）,则替换；否则放入链表或者红黑树。

jdk1.7采用数组+链表；jdk1.8采用数组+链表/红黑树



> 为何要有链表？

数组本身是有限的，在有限的长度里使用Hash，因为Hash本身存在概率性，不同的key Hash后对数组取模后可能会落到同一个槽上；



> 链表插入方式？

​		java8之前是**头插法**，java8后改为**尾插**。为何改用尾插？因为在并发的情况下会造成死循环。具体来说，若map容量为2，有2个线程AB插入了3和7，这时元素已经插入链表中，链表结构为`3`->`7`，还未完成resize()，这时A线程在resize()过程中在处理`3`时挂起，而B线程完成了resize()，因为链表头插方式插入的元素会放在链表的头部（也就是让下一节点的指针指向上一节点），所以此时`7`的next指针指向了`3`，链表变为`7`->`3`，**链表顺序被倒置了**。这时A线程被调度回来，继续处理，发现`7`的next元素为`3`，继续处理`3`，将`3`的next指针指向`7`，这时**链表就形成了环**（Infinite Loop）。[参考1](https://mp.weixin.qq.com/s/VtIpj-uuxFj5Bf6TmTJMTw).[参考2](https://www.cnblogs.com/qmillet/p/13054208.html).[参考3](https://www.jianshu.com/p/619a8efcf589)

​		而使用**尾插在扩容时不会改变链表原有的顺序**，保持之前节点的引用关系。

​		但是这也不能保证线程安全，通过源码看到put/get方法都没有加**同步锁**，多线程情况最容易出现的就是：无法保证上一秒put的值，下一秒get的时候还是原值，所以线程安全还是无法保证。

1.在jdk1.7中，在多线程环境下，扩容时会造成环形链或数据丢失。

2.在jdk1.8中，在多线程环境下，会发生数据覆盖的情况。



> HashMap的扩容机制

当map中元素数量大于扩容阈值时，会进行resize()，将容量扩大到原来的2倍。阈值是指当前map容量Capacity与负载因子Loadfactor的乘积。负载因子默认尾0.75。比如原来map容量为8，当存进第7个元素时就会进行扩容。

如何扩容？

先创建一个新的Entry空数组，长度是原来的2倍；遍历原Entry数组，把所有的Entry重新Hash到新数组。



> 为什么重写equals时也要重写hash？

不同的对象的内存地址不同，hash值肯定也不相同，如果只重写equals，不重写hash，会导致equals相同的对象却返回了不一样的hash，这样在链表中很难寻找了。以保证相同的对象返回相同的hash值，不同的对象返回不同的hash值。而且在链表中比较同时比较了key的hash与equals。



> 为什么HashMap的长度是2的整数次幂，为何为16？

位预算**1<<4**速度更快。之所以选择16，是为了服务将Key映射到index的算法。

16和0.75也不是随意取的，而是经过了大量的统计。

先说答案：为了加快hash计算以及减少hash冲突

为了找到KEY的位置在哈希表的哪个槽里（table数组下标）,需要计算 **hash(KEY) % 数组长度**，但是**%操作比位运算&慢许多**。位运算直接对内存数据进行操作，不需要转成十进制。所以用 & 代替 %，为了保证 & 的计算结果等于 % 的结果需要把 length 减 1

也就是 **hash(KEY) & (length - 1)**

当length为2的整数倍时，length-1的二级制低位全为1，这时的位与运算就相当于保留值的低位的值，也就是取余操作。只要hashcode的值是均匀的，那么取余后也是均匀的。



**理由**：求余运算：a MOD b就相当与a-(a DIV b)*b 的运算。

在对10进行求余时，我们发现，余数总是整数中的个位数字，而不用管其他位是什么；在与运算时，我们经常需要使用位操作符&来取某些位上的值，例如使用0xff&0x17ae来获取低8位的值，就像这样

```java
23%16 == 7
23 (0x17)&amp; 0x0F == 0x07
```

所以，当需要对2的次幂进行求余时，可以对需要留下的低位保留，即使用1111111取余。[参考1](https://mp.weixin.qq.com/s/ktre8-C-cP_2HZxVW5fomQ)



> 链表与红黑树如何转换？

当链表中节点数量大于等于`TREEIFY_THRESHOLD=8`时，链表会转成红黑树。

当链表中节点数量小于等于`UNTREEIFY_THRESHOLD=6`时，红黑树会转成链表。

时间和空间的权衡，TreeNodes需要更多的空间。

*当hashCode离散性很好的时候，树型bin用到的概率非常小，因为数据均匀分布在每个bin中，几乎不会有bin中链表长度会达到阈值。但是在随机hashCode下，离散性可能会变差，然而JDK又不能阻止用户实现这种不好的hash算法，因此就可能导致不均匀的数据分布。不过理想情况下随机hashCode算法下所有bin中节点的分布频率会遵循泊松分布，我们可以看到，一个bin中链表长度达到8个元素的概率为0.00000006，几乎是不可能事件。这种不可能事件都发生了，说明bin中的节点数很多，查找起来效率不高。至于7，是为了作为缓冲，可以有效防止链表和树频繁转换。*

*之所以选择8，不是拍拍屁股决定的，而是根据概率统计决定的。由此可见，发展30年的Java每一项改动和优化都是非常严谨和科学的。*



> 怎么处理HashMap在线程安全上的场景？

一般使用**CurrentHashMap**。HashTable由于是在方法上直接上锁，并发度很低，被抛弃。



**Hash冲突的解决方法**

a. 链地址法：将哈希表的每个单元作为链表的头结点，所有哈希地址为 i 的元素构成一个同义词链表。即发生冲突时就把该关键字链在以该单元为头结点的链表的尾部。

b. 开放定址法：即发生冲突时，去寻找下一个空的哈希地址。只要哈希表足够大，总能找到空的哈希地址。

c. 再哈希法：即发生冲突时，由其他的函数再计算一次哈希值。

d. 建立公共溢出区：将哈希表分为基本表和溢出表，发生冲突时，将冲突的元素放入溢出表。

**HashMap采用的链地址法**



### ArrayList

> ArrayList有用过吗？它是一个什么东西？可以用来干嘛？

ArrayList就是数组列表，主要用来装载数据，当我们装载的是基本类型的数据int，long，boolean，short，byte…的时候我们只能存储他们对应的包装类，它的主要底层实现是数组Object[] elementData。

与它类似的是LinkedList，和LinkedList相比，它的查找和访问元素的速度较快，但新增，删除的速度较慢。

**小结**：ArrayList底层是用数组实现的存储。

**特点**：查询效率高，增删效率低，线程不安全。使用频率很高。



> 为啥线程 不安全还使用他呢？

因为我们正常使用的场景中，都是用来查询，不会涉及太频繁的增删，如果涉及频繁的增删，可以使用LinkedList，如果你需要线程安全就使用Vector，这就是三者的区别了，实际开发过程中还是ArrayList使用最多的。

不存在一个集合工具是查询效率又高，增删效率也高的，还线程安全的，至于为啥大家看代码就知道了，因为数据结构的特性就是优劣共存的，想找个平衡点很难，牺牲了性能，那就安全，牺牲了安全那就快速。

**Tip**：这里还是强调下大家不要为了用而用，我记得我以前最开始工作就有这个毛病。就是不管三七二十一，就是为了用而用，别人用我也用，也不管他的性能啊，是否线程安全啥的，所幸最开始公司接触的，都是线下的系统，而且没啥并发。



> 您说它的底层实现是数组，但是数组的大小是定长的，如果我们不断的往里面添加数据的话，不会有问题吗？

ArrayList可以通过构造方法在初始化的时候指定底层数组的大小。

通过无参构造方法的方式ArrayList()初始化，则赋值底层数Object[] elementData为一个默认空数组Object[] DEFAULTCAPACITY_EMPTY_ELEMENTDATA =  {}所以数组容量为0，只有真正对数据进行添加add时，才分配默认DEFAULT_CAPACITY = 10的初始容量。

实现方式比较简单，他就是通过数组扩容的方式去实现的。**扩容为原来长度的1.5倍。**



> 为啥增删慢

1. 扩容会导致数据copy。
2. 如果指定index新增，也会copy元素。



> 我问你个真实的场景，这个问题很少人知道，你可要好好回答哟！
>
> ArrayList（int initialCapacity）会不会初始化数组大小？

**不会初始化数组大小！**

而且将构造函数与initialCapacity结合使用，然后使用set（）会抛出异常，尽管该数组已创建，但是大小设置不正确。

使用sureCapacity（）也不起作用，因为它基于elementData数组而不是大小。

还有其他副作用，这是因为带有sureCapacity（）的静态DEFAULT_CAPACITY。

进行此工作的唯一方法是在使用构造函数后，根据需要使用add（）多次。

大家可能有点懵，我直接操作一下代码，大家会发现我们虽然对ArrayList设置了初始大小，但是我们打印List大小的时候还是0，我们操作下标set值的时候也会报错，数组下标越界。

再结合源码，大家仔细品读一下，这是Java Bug里面的一个经典问题了，还是很有意思的，大家平时可能也不会注意这个点。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzW9kGwS65sOQzl9X9ZBsK5II4Yyibqv9dWD9HGd8XTK6IekJ25sHfLels5aib3nuKAdtgJPxiadOPAw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



> ArrayList插入删除一定慢么？

取决于你删除的元素离数组末端有多远，ArrayList拿来作为堆栈来用还是挺合适的，push和pop操作完全不涉及数据移动操作。

删除其实跟新增是一样的，不过叫是叫删除，但是在代码里面我们发现，他还是在copy一个数组。

同理他的效率也低，因为数组如果很大的话，一样需要复制和移动的位置就大了。



> ArrayList是线程安全的么？

当然不是，线程安全版本的数组容器是Vector。

Vector的实现很简单，就是把所有的方法统统加上synchronized就完事了。

你也可以不使用Vector，用Collections.synchronizedList把一个普通ArrayList包装成一个线程安全版本的数组容器也可以，原理同Vector是一样的，就是给所有的方法套上一层synchronized。

> ArrayList用来做队列合适么？

队列一般是FIFO（先入先出）的，如果用ArrayList做队列，就需要在数组尾部追加数据，数组头部删除数组，反过来也可以。

但是无论如何总会有一个操作会涉及到数组的数据搬迁，这个是比较耗费性能的。

**结论**：ArrayList不适合做队列。



> 那数组适合用来做队列么？

数组是非常合适的。

比如ArrayBlockingQueue内部实现就是一个环形队列，它是一个定长队列，内部是用一个定长数组来实现的。



> ArrayList的遍历和LinkedList遍历性能比较如何？

论遍历ArrayList要比LinkedList快得多，ArrayList遍历最大的优势在于内存的连续性，CPU的内部缓存结构会缓存连续的内存片段，可以大幅降低读取内存的性能开销。

参考：

1. [原创 |《吊打面试官》系列-ArrayList](https://mp.weixin.qq.com/s/WoGclm7SsbURGigI3Mwr3w)                

### LinkedList



### 堆Heap

堆其实就是一种特殊的队列——优先队列。

这里要区别于操作系统里的那个“堆”，这两个虽然都叫堆，但是没有半毛钱关系，都是借用了 Heap 这个英文单词而已。

我们再来回顾一下「**堆**」在整个 Java 集合框架中的位置：

![img](https://mmbiz.qpic.cn/mmbiz_png/og5r7PHGHoiaCcicjO5FRTibxcpMQNicK6BslC7l2aGZ7nNOHt7DN0SVxOvRSFrPAILEtER49lgIsKrfq21anRt28A/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

也就是说，

- PriorityQueue 是一个类 (class)；
- PriorityQueue 继承自 Queue 这个接口 (Interface)；

那 heap 在哪呢？

heap 其实是一个**抽象的数据结构**，或者说是**逻辑上的数据结构**，并不是一个物理上真实存在的数据结构。

heap 其实有很多种实现方式，比如 binomial heap, Fibonacci heap 等等。但是面试最常考的，也是最经典的，就是 **binary heap 二叉堆**，也就是用一棵**完全二叉树**来实现的。

那完全二叉树是怎么实现的？

其实是用**数组**来实现的！

**所以 binary heap/PriorityQueue 实际上是用数组来实现的。**

这个数组的排列方式有点特别，因为它总会维护你定义的（或者默认的）**优先级最高的元素**在数组的首位，所以不是随便一个数组都叫「堆」，实际上，它在你心里，应该是一棵「完全二叉树」。

**堆的特点** 

1. 堆是一棵完全二叉树；

2. 堆序性 (heap order): 任意节点都**优于**它的**所有孩子**。

   a. 如果是任意节点都**大于**它的所有孩子，这样的堆叫**大顶堆**，Max Heap;

   b. 如果是任意节点都**小于**它的所有孩子，这样的堆叫**小顶堆**，Min Heap;

![img](https://mmbiz.qpic.cn/mmbiz_png/og5r7PHGHoiaCcicjO5FRTibxcpMQNicK6BsHFv1JX268j9icMV1eRtbIp6XyQ0SaoaI6cbQiaiajIRsiahtUK21Nmpqfw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

左图是小顶堆，可以看出对于每个节点来说，都是小于它的所有孩子的，注意是**所有孩子，包括孙子，曾孙...**

1. 既然堆是用数组来实现的，那么我们可以找到每个节点和它的父母/孩子之间的关系，从而可以直接访问到它们。

![img](https://mmbiz.qpic.cn/mmbiz_png/og5r7PHGHoiaCcicjO5FRTibxcpMQNicK6BsaVz7OusVvcCqyebEdynL6PreDicJnbAIAw53rImjTNZiaJfS2uic7Tf4g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

比如对于节点 3 来说，

- 它的 Index = 1，
- 它的 parent index = 0,
- 左孩子 left child index = 3,
- 右孩子 right child index = 4.

可以归纳出如下规律：

- 设当前节点的 index = x,
- 那么 parent index = (x-1)/2,
- 左孩子 left child index = 2*x + 1,
- 右孩子 right child index = 2*x + 2.

有些书上可能写法稍有不同，是因为它们的数组是从 1 开始的，而我这里数组的下标是从 0 开始的，都是可以的。

这样就可以从任意一个点，一步找到它的孙子、曾孙子，真的太方便了，在后文讲具体操作时大家可以更深刻的体会到。



参考：

1. [Java 集合中「堆」是啥？](https://mp.weixin.qq.com/s/eSCVJclB-IaJYkPKsWSkRA)              



## ConcurrentHashMap

> HashMap在多线程环境下存在线程安全问题，那你一般都是怎么处理这种情况的？

- 使用Collections.synchronizedMap(Map)创建线程安全的map集合；
- Hashtable
- ConcurrentHashMap

不过出于线程并发度的原因，我都会舍弃前两者使用最后的ConcurrentHashMap，他的性能和效率明显高于前两者。



> Collections.synchronizedMap是怎么实现线程安全的你有了解过么？

在SynchronizedMap内部维护了一个普通对象Map，还有排斥锁mutex，如图

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyhVLAW08sszrgEKUamuEKRYfOvAN7JoEXvgu88icnh5fso9DWDTbJZW21GvVyZpDaCw24EuaaxWZw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

```
Collections.synchronizedMap(new HashMap<>(16));
```

我们在调用这个方法的时候就需要传入一个Map，可以看到有两个构造器，如果你传入了mutex参数，则将对象排斥锁赋值为传入的对象。

如果没有，则将对象排斥锁赋值为this，即调用synchronizedMap的对象，就是上面的Map。

创建出synchronizedMap之后，再操作map的时候，就会对方法上锁，如图全是🔐

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyhVLAW08sszrgEKUamuEKRgG8CTU8Uj4k0djWqQiaiayXO7H3WTTUN0v0jegVsj8fxBcCcIl4XAmqg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



> 聊一下Hashtable么？

对数据操作的时候都会上synchronized锁，所以效率比较低下。

Hashtable 是不允许键或值为 null 的，HashMap 的键值则都可以为 null。

这是因为Hashtable使用的是**安全失败机制（fail-safe）**，这种机制会使你此次读到的数据不一定是最新的数据。

如果你使用null值，就会使得其无法判断对应的key是不存在还是为空，因为你无法再调用一次contain(key）来对key是否存在进行判断，ConcurrentHashMap同理。



> fail-fast是啥？

**快速失败（fail—fast）**是java集合中的一种机制， 在用迭代器遍历一个集合对象时，如果遍历过程中对集合对象的内容进行了修改（增加、删除、修改），则会抛出Concurrent Modification Exception。

java.util包下的集合类都是快速失败的，不能在多线程下发生并发修改（迭代过程中被修改）算是一种安全机制吧。

**Tip**：**安全失败（fail—safe）**大家也可以了解下，java.util.concurrent包下的容器都是安全失败，可以在多线程下并发使用，并发修改。



> 并发度不够，性能很低，这个时候你都怎么处理的？

ConcurrentHashMap，底层是基于 `数组 + 链表` 组成的，不过在 jdk1.7 和 1.8 中具体实现稍有不同。

**我先说一下他在1.7中的数据结构吧**：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyhVLAW08sszrgEKUamuEKR92tLGjq5XU8SCBVmGAgiaSp95mnibgngXjFjycLTSkDMpOEfKvZaFBzQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

如图所示，是由 Segment 数组、HashEntry 组成，和 HashMap 一样，仍然是**数组加链表**。

Segment 是 ConcurrentHashMap 的一个内部类，主要的组成如下：

```java
static final class Segment<K,V> extends ReentrantLock implements Serializable {

    private static final long serialVersionUID = 2249069246763182397L;

    // 和 HashMap 中的 HashEntry 作用一样，真正存放数据的桶
    transient volatile HashEntry<K,V>[] table;

    transient int count;
        // 记得快速失败（fail—fast）么？
    transient int modCount;
        // 大小
    transient int threshold;
        // 负载因子
    final float loadFactor;

}
```

HashEntry跟HashMap差不多的，但是不同点是，他使用volatile去修饰了他的数据Value还有下一个节点next。

原理上来说，ConcurrentHashMap 采用了**分段锁**技术，其中 **Segment 继承于 ReentrantLock**。

不会像 HashTable 那样不管是 put 还是 get 操作都需要做同步处理，理论上 ConcurrentHashMap 支持 CurrencyLevel (Segment 数组数量)的线程并发。

每当一个线程占用锁访问一个 Segment 时，不会影响到其他的 Segment。

就是说如果容量大小是16他的并发度就是16，可以同时允许16个线程操作16个Segment而且还是线程安全的。

**Put()操作**

- 先定位到Segment，然后再进行put操作。
- 尝试获取锁，如果获取失败肯定就有其他线程存在竞争，则利用 `scanAndLockForPut()` 自旋获取锁。重试的次数达到了 `MAX_SCAN_RETRIES` 则改为阻塞锁获取，保证能获取成功。
- 将当前 Segment 中的 table 通过 key 的 hashcode 定位到 HashEntry。
- 然后就是类似HashMap中的定位过程。

**get()操作**

get 逻辑比较简单，只需要将 Key 通过 Hash 之后定位到具体的 Segment ，再通过一次 Hash 定位到具体的元素上。

由于 HashEntry 中的 value 属性是用 volatile 关键词修饰的，保证了内存可见性，所以每次获取时都是最新值。

ConcurrentHashMap 的 get 方法是非常高效的，**因为整个过程都不需要加锁**。



**再说说在1.8中的数据结构**

查询的时候，还得遍历链表，会导致效率很低，这个跟jdk1.7的HashMap是存在的一样问题，所以他在jdk1.8完全优化了。

另外，1.8中抛弃了原有的 Segment 分段锁，而采用了 **`CAS + synchronized`** 来保证并发安全性。

跟HashMap很像，也把之前的HashEntry改成了Node，但是作用不变，把值和next采用了volatile去修饰，保证了可见性，并且也引入了红黑树，在链表大于一定值的时候会转换（默认是8）。

**Put()操作**

ConcurrentHashMap在进行put操作的还是比较复杂的，大致可以分为以下步骤：

1. 根据 key 计算出 hashcode 。
2. 判断是否需要进行初始化。
3. 即为当前 key 定位出的 Node，如果为空表示当前位置可以写入数据，利用 CAS 尝试写入，失败则自旋保证成功。
4. 如果当前位置的 `hashcode == MOVED == -1`,则需要进行扩容。
5. 如果都不满足，则利用 synchronized 锁写入数据。
6. 如果数量大于 `TREEIFY_THRESHOLD` 则要转换为红黑树。

**get()**

- 根据计算出来的 hashcode 寻址，如果就在桶上那么直接返回值。
- 如果是红黑树那就按照树的方式获取值。
- 就不满足那就按照链表的方式遍历获取值。



参考：

1. [《吊打面试官》系列-ConcurrentHashMap & Hashtable（文末送书）](https://mp.weixin.qq.com/s/AixdbEiXf3KfE724kg2YIw)                

2. [我就知道面试官接下来要问我 ConcurrentHashMap 底层原理了](https://mp.weixin.qq.com/s/My4P_BBXDnAGX1gh630ZKw)                

## 容器

### 同步容器

在Java中，同步容器主要包括2类：

- 1、Vector、Stack、HashTable
- 2、Collections类中提供的静态工厂方法创建的类



拿相对简单的Vecotr来举例，Vector这样的同步容器的所有公有方法全都是synchronized的，也就是说，我们可以在多线程场景中放心的**单独**使用这些方法，因为这些方法本身的确是线程安全的。

但是，请注意上面这句话中，有一个比较关键的词：单独

因为，虽然同步容器的所有方法都加了锁，但是对这些容器的复合操作无法保证其线程安全性。需要客户端通过主动加锁来保证。

简单举一个例子，我们定义如下删除Vector中最后一个元素方法：

```
public Object deleteLast(Vector v){
    int lastIndex  = v.size()-1;
    v.remove(lastIndex);
}
```

上面这个方法是一个复合方法，包括size(）和remove()，乍一看上去好像并没有什么问题，无论是size()方法还是remove()方法都是线程安全的，那么整个deleteLast方法应该也是线程安全的。

但是，如果多线程调用该方法的过程中，remove方法有可能抛出ArrayIndexOutOfBoundsException。

因为removeLast方法，有可能被多个线程同时执行，当线程2通过index()获得索引值为10，在尝试通过remove()删除该索引位置的元素之前，线程1把该索引位置的值删除掉了，这时线程一在执行时便会抛出异常。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/6fuT3emWI5LDJE14LEwQdOfQsD3BhaXRIBInh9PV8pfQB98NeibzsHOEuEibMiah1CTseTd5EcaaBRocAxGISbO2Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

为了避免出现类似问题，可以尝试加锁：

```
public void deleteLast() {
    synchronized (v) {
        int index = v.size() - 1;
        v.remove(index);
    }
}
```

如上，我们在deleteLast中，对v进行加锁，即可保证同一时刻，不会有其他线程删除掉v中的元素。

另外，如果以下代码会被多线程执行时，也要特别注意：

```
for (int i = 0; i < v.size(); i++) {
    v.remove(i);
}
```

由于，不同线程在同一时间操作同一个Vector，其中包括删除操作，那么就同样有可能发生线程安全问题。所以，在使用同步容器的时候，如果涉及到多个线程同时执行删除操作，就要考虑下是否需要加锁。



**同步容器的问题**

前面说过了，同步容器直接保证单个操作的线程安全性，但是无法保证复合操作的线程安全，遇到这种情况时，必须要通过主动加锁的方式来实现。

而且，除此之外，同步容易由于对其所有方法都加了锁，这就导致多个线程访问同一个容器的时候，只能进行顺序访问，即使是不同的操作，也要排队，如get和add要排队执行。这就大大的降低了容器的并发能力。



### 并发容器

针对前文提到的同步容器存在的并发度低问题，从Java5开始，java.util.concurent包下，提供了大量支持高效并发的访问的集合类，我们称之为并发容器。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/6fuT3emWI5LDJE14LEwQdOfQsD3BhaXRafShHplrGpwuepicPSibLTuFrjAchFjhyq0kicGbdYYxFNk1ibg7fBibD0g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

针对前文提到的同步容器的复合操作的问题，一般在Map中发生的比较多，所以在ConcurrentHashMap中增加了对常用复合操作的支持，比如putIfAbsent()、replace()，这2个操作都是原子操作，可以保证线程安全。

另外，并发包中的CopyOnWriteArrayList和CopyOnWriteArraySet是Copy-On-Write的两种实现。

**Copy-On-Write容器即写时复制的容器。通俗的理解是当我们往一个容器添加元素的时候，不直接往当前容器添加，而是先将当前容器进行Copy，复制出一个新的容器，然后新的容器里添加元素，添加完元素之后，再将原容器的引用指向新的容器。**

CopyOnWriteArrayList中add/remove等写方法是需要加锁的，而读方法是没有加锁的。

这样做的好处是我们可以对CopyOnWrite容器进行并发的读，当然，这里读到的数据可能不是最新的。因为写时复制的思想是通过延时更新的策略来实现数据的最终一致性的，并非强一致性。

但是，作为代替Vector的**CopyOnWriteArrayList并没有解决同步容器的复合操作的线程安全性问题**。



参考：

1. [面试官问我同步容器（如Vector）的所有操作一定是线程安全的吗？我懵了！](https://mp.weixin.qq.com/s/0cMrE87iUxLBw_qTBMYMgA)    



## 枚举Enum

参考：

1. [三歪问我为啥用枚举，枚举有哪些用法？](https://mp.weixin.qq.com/s/U5FkL9zyzr0PkAp8MJJ8BQ)                . 





# Redis

**[《我想进大厂》之 Redis 夺命连环 11 问](https://mp.weixin.qq.com/s/yLd8OpzY3V-kYz6jchwLTw)**     

**[常见面试题之缓存雪崩、缓存穿透、缓存击穿](https://mp.weixin.qq.com/s/d9An-DOYjuRdQpuVxi48DA)**                           

## 基础

#### Redis数据结构

**五种基本数据结构**

- String：字符串，是构建其他数据结构的基础 

- Hash：哈希列表 

- List：列表 

- Set：集合，在哈希列表的基础上实现 

- Sort Set：有序集合 

**复杂的数据结构**

- Pub/Sub：
- Hyperloglog：⽤于估计⼀个 set 中元素数量的概率性的数据结构。 
- Geo：geospatial,地理空间索引半径查询。 

Redis Module：

- Bitmaps：位图，在string的基础上进⾏位操作，可以实现节省空间的数据结构。 
- BloomFilter：布隆过滤器。 
- RedisSearch
- Redis-ML



> 大量的key集中过期

Redis可能出现短暂卡顿，严重会引起缓存雪崩，处理方式在过期时间上加一个随机值，让过期时间分散。

> Redis分布式锁

**setnx来争抢锁**，拿到的返回1，拿不到的返回0。这个是原子性的操作。

为了防止程序异常crash，导致锁一直得不到释放，**会设置一个过期时间**。

设置过期时间也会有个问题，就是线程A拿到key，但是操作时间过长，操作过程中key失效了，这时另外的线程B看到没锁，就自己加上锁，然后线程A执行完了任务回来反手就把锁删掉了。。。

这时候解决方法可以**给value设置一个唯一的客户端ID****，或者用**UUID**这种随机数。当解锁的时候，先获取value判断是否是当前进程加的锁，再去删除。但get()+del()操作可不是原子性的，那么删除锁的正确姿势之一，就是可以使用**lua**脚本，通过redis的**eval**/**evalsha**命令来运行。就算你在**lua**里写出花，执行也是一个命令(**eval**/**evalsha**)去执行的，一条命令没执行完，其他客户端是看不到的。

那么既然这么麻烦，有没有比较好的工具呢？就要说到**redisson**了。



Redisson是**java的redis客户端之一**，提供了一些api方便操作redis。

Redisson普通的锁实现源码主要是**RedissonLock**这个类。

源码中**加锁/释放锁**操作都是用**lua**脚本完成的，封装的非常完善，开箱即用。

加锁解锁的lua脚本考虑的非常全面，其中就包括**锁的重入性**，这点可以说是考虑非常周全。



> 假如Redis里面有1亿个key，其中有10w个key是以某个固定的已知的前缀开头的，如何将它们全部找出来？

**keys**命令：

```
keys pattern #pattern可为⼀个包含匹配模式的字符串，可以包含*,+,?,[a-z]等模式。
```

但是Redis是单线程的，这个命令会导致线程阻塞一段时间，线上服务会停顿。这时不能容忍的，这个时候可以使用**scan**指令。**scan**指令可以无阻塞的提取出指定模式的key列表，但是会有一定的重复概率，在客户端做一次去重就可以了，但是整体所花费的时间会比直接用keys指令长。



**Redis异步队列**

> 怎么用？

一般使用list结构作为队列，**rpush**生产消息，**lpop**消费消息。当lpop没有消息的时候，要适当sleep一会再重试。

> 可不可以不用sleep？

ist还有个指令叫**blpop**，在没有消息的时候，它会阻塞住直到消息到来。

> 能不能生产一次消费多次呢？

使用pub/sub主题订阅者模式，可以实现 1:N 的消息队列。

> pub/sub有什么缺点？

在消费者下线的情况下，生产的消息会丢失，得使用专业的消息队列如**RocketMQ**等。

> Redis如何实现延时队列？

使用sortedset，拿时间戳作为score，消息内容作为key调用zadd来生产消息，消费者用**zrangebyscore**指令获取N秒之前的数据轮询进行处理。



Redis命令

**Redis通用命令**

> keys	列出Redis所有的key

```shell
keys pattern #pattern可为⼀个包含匹配模式的字符串，可以包含*,+,?,[a-z]等模式。
```

> exists	用于判断一个或多个key是否存在，exists的返回值为整数，表⽰当前判断有多少个key是存在的。 

```
exists key [key ...] 
```

> del	del命令⽤于删除⼀个或多个key

```
del key [key ...] 
```

> expire，pexpire	设置key在多少秒之后过期

```
# expire命令，时间复杂度为O(1) 
expire key seconds 
# pexpire命令，时间复杂度为O(1) 
pexpire key milliseconds
```

> ttl和pttl命令⽤于获取key的过期时间，其返回值为整型，代表的意义分为⼏种情况： 
>
> 当key不存在或过期时间，返回-2。 
>
> 当key存在且永久有效时，返回-1。 
>
> 当key有设置过期时间时，返回为剩下的秒数(pttl为毫秒数) 

##### 引入及配置

> 在pom.xml中新增Redis相关依赖

```xml
<!--redis依赖配置-->
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-data-redis</artifactId>
</dependency>
```

[修改SpringBoot配置文件](http://www.macrozheng.com/#/architect/mall_arch_03?id=修改springboot配置文件)

> 在application.yml中添加Redis的配置及Redis中自定义key的配置。

[在spring节点下添加Redis的配置](http://www.macrozheng.com/#/architect/mall_arch_03?id=在spring节点下添加redis的配置)

```yml
  redis:
    host: localhost # Redis服务器地址
    database: 0 # Redis数据库索引（默认为0）
    port: 6379 # Redis服务器连接端口
    password: # Redis服务器连接密码（默认为空）
    jedis:
      pool:
        max-active: 8 # 连接池最大连接数（使用负值表示没有限制）
        max-wait: -1ms # 连接池最大阻塞等待时间（使用负值表示没有限制）
        max-idle: 8 # 连接池中的最大空闲连接
        min-idle: 0 # 连接池中的最小空闲连接
    timeout: 3000ms # 连接超时时间（毫秒）
```

[在根节点下添加Redis自定义key的配置](http://www.macrozheng.com/#/architect/mall_arch_03?id=在根节点下添加redis自定义key的配置)

```yml
# 自定义redis key
redis:
  key:
    prefix:
      authCode: "portal:authCode:"
    expire:
      authCode: 120 # 验证码超期时间
```

##### Redis使用

 结合Spring Boot 使⽤。⼀般有两种⽅式，⼀种是直接通过RedisTemplate 来使⽤，另⼀种是使⽤ Spring Cache 集成 Redis（也就是注解的⽅式）

Spring Cache三个核心注解：

- @Cachable

- @CachePut

- @CacheEvict



##### Redis问题

> Redis雪崩

大量的缓存同时失效，导致请求同时落在数据库上。

处理方式：key的失效时间加随机值

```
setRedis（key, value, time+Math.random()*10000）; 
```

> 缓存穿透和击穿

缓存穿透：指不断请求缓存和数据库中都没有的数据，如发起id=-1的数据或id为特别大不存在的数据。

解决方式：

1. 接口层增加校验
2. 可以将key-value对写为key-nul，加入缓存，可以防止用户反复用同一个id暴力攻击
3. 使用布隆过滤器（Bloom Filter）,原理是利用高效的数据结构和算法快速判断出这个key是否在数据库中，不存在直接return。

缓存击穿：一个key非常热点，在不停的扛着大量的请求，当这个key在失效的瞬间，持续的大并发直接落到数据库上。这个key就击穿了缓存。

解决方式：

1. 设置热点数据永不过期

2. 加上互斥锁

   ```java
   public static String getData(String key) throws InterruptedException { 
   	//从Redis查询数据 
   	String result = getDataFromRedis(key); 
   	//参数校验 
   	if (StringUtils.isBlank(result)) { 
   	try { 
   	//获得锁 
   	if (reenLock.tryLock()) { 
   	//去数据库查询 
   	result = getDataFromDB(key); 
   	//校验 
   	if (StringUtils.isNotBlank(result)) { 
   	//插进缓存 
   	setDataToKV(key, result); 
   	} 
   	} else { 
   	//睡⼀会再拿 
   	Thread.sleep(100L); 
   	result = getData(key); 
   } 
   } finally { 
   //释放锁 
   reenLock.unlock(); 
   } 
   }
   return result; 
   } 
   ```



> Redis淘汰策略

**随机、最近最少使用、即将过期、使用频率最少**

| 策略            | 描述                                                         |
| --------------- | ------------------------------------------------------------ |
| allkeys-lru     | 从所有KV集中优先对最近最少使用（less recently used）的数据淘汰 |
| volatile-lru    | 从已过期时间的KV集中优先对最近最少使用（less recently used）的数据淘汰 |
| allkeys-random  | 从所有KV集中随机选择数据淘汰                                 |
| volatile-random | 从已过期时间的KV随机选择数据淘汰                             |
| volatile-ttl    | 从已过期时间的KV集中优先对剩余时间短（time to live）的数据淘汰 |
| volatile-lfu    | 从已过期时间的KV集中优先对使用频率最少（less frequency used）的数据淘汰 |
| allkeys-lfu     | 从所有的KV集中优先对使用频率最少（less frequency used）的数据淘汰 |

> Redis持久化

- RDB

  快照形式是直接把内存中的数据保存到一个二进制dump.rdb文件中。当需要持久化时，Redis会fork一个子进程，子进程将数据写到磁盘上一个临时RDB文件中。当子进程完成写临时文件后，将原来的RDB替换掉，这样的好处时可以copy-on-write。

- AOF

  把所有的对Redis的服务器进行修改的命令以追加的方式存到一个文件里，是命令的集合。写入可能会比较巨大。



> Redis主从复制



##### [Redis问答](https://zhuanlan.zhihu.com/p/93515595)

**4.Reids常用5种数据类型**

- string，list，set，sorted set，hash

**6.Reids6种淘汰策略：**

- **noeviction**: 不删除策略, 达到最大内存限制时, 如果需要更多内存, 直接返回错误信息。大多数写命令都会导致占用更多的内存(有极少数会例外。
- **allkeys-lru:**所有key通用; 优先删除最近最少使用(less recently used ,LRU) 的 key。
- **volatile-lru:**只限于设置了 expire 的部分; 优先删除最近最少使用(less recently used ,LRU) 的 key。
- **allkeys-random:**所有key通用; 随机删除一部分 key。
- **volatile-random**: 只限于设置了 **expire** 的部分; 随机删除一部分 key。
- **volatile-ttl**: 只限于设置了 **expire** 的部分; 优先删除剩余时间(time to live,TTL) 短的key。

**7.Redis的并发竞争问题如何解决?**

单进程单线程模式，采用队列模式将并发访问变为串行访问。Redis本身没有锁的概念，Redis对于多个客户端连接并不存在竞争，利用setnx实现锁。

**9.Redis前端启动命令**

./redis-server

**11.Redis 持久化方案：**

Rdb 和 Aof

**14.为什么Redis是单线程的？**

Redis是基于内存的操作，CPU不是Redis的瓶颈，Redis的瓶颈最有可能是机器内存的大小或者网络带宽。既然单线程容易实现，而且CPU不会成为瓶颈，那就顺理成章地采用单线程的方案了（毕竟采用多线程会有很多麻烦！）。

**25.AOF常用配置总结**

下面是AOF常用的配置项，以及默认值；前面介绍过的这里不再详细介绍。

- appendonly no：是否开启AOF
- appendfilename "appendonly.aof"：AOF文件名
- dir ./：RDB文件和AOF文件所在目录
- appendfsync everysec：fsync持久化策略
- no-appendfsync-on-rewrite no：AOF重写期间是否禁止fsync；如果开启该选项，可以减轻文件重写时CPU和硬盘的负载（尤其是硬盘），但是可能会丢失AOF重写期间的数据；需要在负载和安全性之间进行平衡
- auto-aof-rewrite-percentage 100：文件重写触发条件之一
- auto-aof-rewrite-min-size 64mb：文件重写触发提交之一
- aof-load-truncated yes：如果AOF文件结尾损坏，Redis启动时是否仍载入AOF文件

**26.RDB和AOF的优缺点**

**RDB持久化**

优点：RDB文件紧凑，体积小，网络传输快，适合全量复制；恢复速度比AOF快很多。当然，与AOF相比，RDB最重要的优点之一是对性能的影响相对较小。

缺点：RDB文件的致命缺点在于其数据快照的持久化方式决定了必然做不到实时持久化，而在数据越来越重要的今天，数据的大量丢失很多时候是无法接受的，因此AOF持久化成为主流。此外，RDB文件需要满足特定格式，兼容性差（如老版本的Redis不兼容新版本的RDB文件）。

**AOF持久化**

与RDB持久化相对应，AOF的优点在于支持秒级持久化、兼容性好，缺点是文件大、恢复速度慢、对性能影响大。

**28.redis缓存被击穿处理机制**

使用mutex。简单地来说，就是在缓存失效的时候（判断拿出来的值为空），不是立即去load db，而是先使用缓存工具的某些带成功操作返回值的操作（比如Redis的SETNX或者Memcache的ADD）去set一个mutex  key，当操作返回成功时，再进行load db的操作并回设缓存；否则，就重试整个get缓存的方法

**29.Redis还提供的高级工具**

像慢查询分析、性能测试、Pipeline、事务、Lua自定义命令、Bitmaps、HyperLogLog、发布/订阅、Geo等个性化功能。

**30.Redis常用管理命令**

```text
# dbsize 返回当前数据库 key 的数量。
# info 返回当前 redis 服务器状态和一些统计信息。
# monitor 实时监听并返回redis服务器接收到的所有请求信息。
# shutdown 把数据同步保存到磁盘上，并关闭redis服务。
# config get parameter 获取一个 redis 配置参数信息。（个别参数可能无法获取）
# config set parameter value 设置一个 redis 配置参数信息。（个别参数可能无法获取）
# config resetstat 重置 info 命令的统计信息。（重置包括：keyspace 命中数、
# keyspace 错误数、 处理命令数，接收连接数、过期 key 数）
# debug object key 获取一个 key 的调试信息。
# debug segfault 制造一次服务器当机。
# flushdb 删除当前数据库中所有 key,此方法不会失败。小心慎用
# flushall 删除全部数据库中所有 key，此方法不会失败。小心慎用
```

**31.Reids工具命令**

```text
#redis-server：Redis 服务器的 daemon 启动程序
#redis-cli：Redis 命令行操作工具。当然，你也可以用 telnet 根据其纯文本协议来操作
#redis-benchmark：Redis 性能测试工具，测试 Redis 在你的系统及你的配置下的读写性能
$redis-benchmark -n 100000 –c 50
#模拟同时由 50 个客户端发送 100000 个 SETs/GETs 查询
#redis-check-aof：更新日志检查
#redis-check-dump：本地数据库检查
```

**35.缓存和数据库间数据一致性问题**

分布式环境下（单机就不用说了）非常容易出现缓存和数据库间的数据一致性问题，针对这一点的话，只能说，如果你的项目对缓存的要求是强一致性的，那么请不要使用缓存。我们只能采取合适的策略来降低缓存和数据库间数据不一致的概率，而无法保证两者间的强一致性。合适的策略包括 合适的缓存更新策略，更新数据库后要及时更新缓存、缓存失败时增加重试机制，例如MQ模式的消息队列。

**37.缓存雪崩问题**

存在同一时间内大量键过期（失效），接着来的一大波请求瞬间都落在了数据库中导致连接异常。

解决方案：

1、也是像解决缓存穿透一样加锁排队。

2、建立备份缓存，缓存A和缓存B，A设置超时时间，B不设值超时时间，先从A读缓存，A没有读B，并且更新A缓存和B缓存;

**38.缓存并发问题**

这里的并发指的是多个redis的client同时set  key引起的并发问题。比较有效的解决方案就是把redis.set操作放在队列中使其串行化，必须的一个一个执行，具体的代码就不上了，当然加锁也是可以的，至于为什么不用redis中的事务，留给各位看官自己思考探究。

**40.读写分离模型**

通过增加Slave DB的数量，读的性能可以线性增长。为了避免Master  DB的单点故障，集群一般都会采用两台Master  DB做双机热备，所以整个集群的读和写的可用性都非常高。读写分离架构的缺陷在于，不管是Master还是Slave，每个节点都必须保存完整的数据，如果在数据量很大的情况下，集群的扩展能力还是受限于单个节点的存储能力，而且对于Write-intensive类型的应用，读写分离架构并不适合。

**41.数据分片模型**

为了解决读写分离模型的缺陷，可以将数据分片模型应用进来。

可以将每个节点看成都是独立的master，然后通过业务实现数据分片。

结合上面两种模型，可以将每个master设计成由一个master和多个slave组成的模型。

**42. redis常见性能问题和解决方案：**

Master最好不要做任何持久化工作，如RDB内存快照和AOF日志文件

如果数据比较重要，某个Slave开启AOF备份数据，策略设置为每秒同步一次

为了主从复制的速度和连接的稳定性，Master和Slave最好在同一个局域网内

尽量避免在压力很大的主库上增加从库

**44.Redis分布式锁实现**

先拿setnx来争抢锁，抢到之后，再用expire给锁加一个过期时间防止锁忘记了释放。**如果在setnx之后执行expire之前进程意外crash或者要重启维护了，那会怎么样？**set指令有非常复杂的参数，这个应该是可以同时把setnx和expire合成一条指令来用的！

**50.手写一个 LRU 算法**

```javascript
class LRUCache<K, V> extends LinkedHashMap<K, V> {
    private final int CACHE_SIZE;

    /**
     * 传递进来最多能缓存多少数据
     *
     * @param cacheSize 缓存大小
     */
    public LRUCache(int cacheSize) {
        // true 表示让 linkedHashMap 按照访问顺序来进行排序，最近访问的放在头部，最老访问的放在尾部。
        super((int) Math.ceil(cacheSize / 0.75) + 1, 0.75f, true);
        CACHE_SIZE = cacheSize;
    }

    @Override
    protected boolean removeEldestEntry(Map.Entry<K, V> eldest) {
        // 当 map中的数据量大于指定的缓存个数的时候，就自动删除最老的数据。
        return size() > CACHE_SIZE;
    }
}
```

**51.多节点 Redis 分布式锁：Redlock 算法**

获取当前时间（start）。

依次向 N 个 `Redis`节点请求锁。请求锁的方式与从单节点 `Redis`获取锁的方式一致。为了保证在某个 `Redis`节点不可用时该算法能够继续运行，获取锁的操作都需要设置超时时间，需要保证该超时时间远小于锁的有效时间。这样才能保证客户端在向某个 `Redis`节点获取锁失败之后，可以立刻尝试下一个节点。

计算获取锁的过程总共消耗多长时间（consumeTime = end - start）。如果客户端从大多数 `Redis`节点（>= N/2 + 1) 成功获取锁，并且获取锁总时长没有超过锁的有效时间，这种情况下，客户端会认为获取锁成功，否则，获取锁失败。

如果最终获取锁成功，锁的有效时间应该重新设置为锁最初的有效时间减去 `consumeTime`。

如果最终获取锁失败，客户端应该立刻向所有 `Redis`节点发起释放锁的请求。

**52.Redis 中设置过期时间主要通过以下四种方式**

- expire key seconds：设置 key 在 n 秒后过期；
- pexpire key milliseconds：设置 key 在 n 毫秒后过期；
- expireat key timestamp：设置 key 在某个时间戳（精确到秒）之后过期；
- pexpireat key millisecondsTimestamp：设置 key 在某个时间戳（精确到毫秒）之后过期；

**53.Reids三种不同删除策略**

**定时删除**：在设置键的过期时间的同时，创建一个定时任务，当键达到过期时间时，立即执行对键的删除操作

**惰性删除**：放任键过期不管，但在每次从键空间获取键时，都检查取得的键是否过期，如果过期的话，就删除该键，如果没有过期，就返回该键

**定期删除**：每隔一点时间，程序就对数据库进行一次检查，删除里面的过期键，至于要删除多少过期键，以及要检查多少个数据库，则由算法决定。

**54.定时删除**

- **优点：**对内存友好，定时删除策略可以保证过期键会尽可能快地被删除，并释放国期间所占用的内存
- **缺点：**对cpu时间不友好，在过期键比较多时，删除任务会占用很大一部分cpu时间，在内存不紧张但cpu时间紧张的情况下，将cpu时间用在删除和当前任务无关的过期键上，影响服务器的响应时间和吞吐量

**55.定期删除**

由于定时删除会占用太多cpu时间，影响服务器的响应时间和吞吐量以及惰性删除浪费太多内存，有内存泄露的危险，所以出现一种整合和折中这两种策略的定期删除策略。

1. 定期删除策略每隔一段时间执行一次删除过期键操作，并通过限制删除操作执行的时长和频率来减少删除操作对CPU时间的影响。
2. 定时删除策略有效地减少了因为过期键带来的内存浪费。

**56.惰性删除**

- **优点：**对cpu时间友好，在每次从键空间获取键时进行过期键检查并是否删除，删除目标也仅限当前处理的键，这个策略不会在其他无关的删除任务上花费任何cpu时间。
- **缺点：**对内存不友好，过期键过期也可能不会被删除，导致所占的内存也不会释放。甚至可能会出现内存泄露的现象，当存在很多过期键，而这些过期键又没有被访问到，这会可能导致它们会一直保存在内存中，造成内存泄露。

**58.Redis常见的几种缓存策略**

- Cache-Aside
- Read-Through
- Write-Through
- Write-Behind

**60.Redis 到底是怎么实现“附近的人”**

**使用方式**

```text
GEOADD key longitude latitude member [longitude latitude member ...]
```

将给定的位置对象（纬度、经度、名字）添加到指定的key。其中，key为集合名称，member为该经纬度所对应的对象。在实际运用中，当所需存储的对象数量过多时，可通过设置多key(如一个省一个key)的方式对对象集合变相做sharding，避免单集合数量过多。

成功插入后的返回值：

```text
(integer) N
```

其中N为成功插入的个数。



##### Redis主从复制、哨兵、Cluster三种集群模式

[**Redis主从复制、哨兵、Cluster三种集群模式**](https://mp.weixin.qq.com/s/10ByEGue1_RcgiHXoq7rAA)

###### 主从复制模式



客户端可对主数据库进行读写操作，对从数据库进行读操作，主数据库写入的数据会实时自动同步给从数据库。

具体工作机制为：

1. slave启动后，向master发送SYNC命令，master接收到SYNC命令后通过bgsave保存快照（即上文所介绍的RDB持久化），并使用缓冲区记录保存快照这段时间内执行的写命令
2. master将保存的快照文件发送给slave，并继续记录执行的写命令
3. slave接收到快照文件后，加载快照文件，载入数据
4. master快照发送完后开始向slave发送缓冲区的写命令，slave接收命令并执行，完成复制初始化
5. 此后master每次执行一个写命令都会同步发送给slave，保持master与slave之间数据的一致性

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/oFA4QOeEEpOyHZgq0oDyZhTYuatLR4aic6K0JAia39N4tl991nxgVuKgoV4F0mZiaSD2dribRY7IibjhLNUmOcaIMMg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**主从复制的优缺点**

优点：

1. master能自动将数据同步到slave，可以进行读写分离，分担master的读压力
2. master、slave之间的同步是以非阻塞的方式进行的，同步期间，客户端仍然可以提交查询或更新请求

缺点：

1. 不具备自动容错与恢复功能，master或slave的宕机都可能导致客户端请求失败，需要等待机器重启或手动切换客户端IP才能恢复
2. master宕机，如果宕机前数据没有同步完，则切换IP后会存在数据不一致的问题
3. 难以支持在线扩容，Redis的容量受限于单机配置



###### Sentinel（哨兵）模式

哨兵模式基于主从复制模式，只是引入了哨兵来监控与自动处理故障。如图

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/oFA4QOeEEpOyHZgq0oDyZhTYuatLR4aicc7624M3Fm3Q6DjR0Xo7ryWeS506cKxjgia2M5PEcHmZvTdKHHoJM4UQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

哨兵顾名思义，就是来为Redis集群站哨的，一旦发现问题能做出相应的应对处理。

其功能包括

1. 监控master、slave是否正常运行
2. 当master出现故障时，能自动将一个slave转换为master（大哥挂了，选一个小弟上位）
3. 多个哨兵可以监控同一个Redis，哨兵之间也会自动监控

哨兵模式的具体工作机制：

在配置文件中通过 `sentinel monitor <master-name> <ip> <redis-port> <quorum>` 来定位master的IP、端口，一个哨兵可以监控多个master数据库，只需要提供多个该配置项即可。哨兵启动后，会与要监控的master建立两条连接：

1. 一条连接用来订阅master的`_sentinel_:hello`频道与获取其他监控该master的哨兵节点信息
2. 另一条连接定期向master发送INFO等命令获取master本身的信息

与master建立连接后，哨兵会执行三个操作：

1. 定期（一般10s一次，当master被标记为主观下线时，改为1s一次）向master和slave发送INFO命令
2. 定期向master和slave的`_sentinel_:hello`频道发送自己的信息
3. 定期（1s一次）向master、slave和其他哨兵发送PING命令

发送INFO命令可以获取当前数据库的相关信息从而实现新节点的自动发现。所以说哨兵只需要配置master数据库信息就可以自动发现其slave信息。获取到slave信息后，哨兵也会与slave建立两条连接执行监控。通过INFO命令，哨兵可以获取主从数据库的最新信息，并进行相应的操作，比如角色变更等。

接下来哨兵向主从数据库的_sentinel_:hello频道发送信息与同样监控这些数据库的哨兵共享自己的信息，发送内容为哨兵的ip端口、运行id、配置版本、master名字、master的ip端口还有master的配置版本。这些信息有以下用处：

1. 其他哨兵可以通过该信息判断发送者是否是新发现的哨兵，如果是的话会创建一个到该哨兵的连接用于发送PING命令。
2. 其他哨兵通过该信息可以判断master的版本，如果该版本高于直接记录的版本，将会更新
3. 当实现了自动发现slave和其他哨兵节点后，哨兵就可以通过定期发送PING命令定时监控这些数据库和节点有没有停止服务。

如果被PING的数据库或者节点超时（通过 `sentinel down-after-milliseconds master-name milliseconds` 配置）未回复，哨兵认为其主观下线（sdown，s就是Subjectively —— 主观地）。如果下线的是master，哨兵会向其它哨兵发送命令询问它们是否也认为该master主观下线，如果达到一定数目（即配置文件中的quorum）投票，哨兵会认为该master已经客观下线（odown，o就是Objectively —— 客观地），并选举领头的哨兵节点对主从系统发起故障恢复。若没有足够的sentinel进程同意master下线，master的客观下线状态会被移除，若master重新向sentinel进程发送的PING命令返回有效回复，master的主观下线状态就会被移除

哨兵认为master客观下线后，故障恢复的操作需要由选举的领头哨兵来执行，选举采用Raft算法：

1. 发现master下线的哨兵节点（我们称他为A）向每个哨兵发送命令，要求对方选自己为领头哨兵
2. 如果目标哨兵节点没有选过其他人，则会同意选举A为领头哨兵
3. 如果有超过一半的哨兵同意选举A为领头，则A当选
4. 如果有多个哨兵节点同时参选领头，此时有可能存在一轮投票无竞选者胜出，此时每个参选的节点等待一个随机时间后再次发起参选请求，进行下一轮投票竞选，直至选举出领头哨兵

选出领头哨兵后，领头者开始对系统进行故障恢复，从出现故障的master的从数据库中挑选一个来当选新的master,选择规则如下：

1. 所有在线的slave中选择优先级最高的，优先级可以通过slave-priority配置
2. 如果有多个最高优先级的slave，则选取复制偏移量最大（即复制越完整）的当选
3. 如果以上条件都一样，选取id最小的slave

挑选出需要继任的slave后，领头哨兵向该数据库发送命令使其升格为master，然后再向其他slave发送命令接受新的master，最后更新数据。将已经停止的旧的master更新为新的master的从数据库，使其恢复服务后以slave的身份继续运行。



###### Cluster模式

1. **基本原理**

哨兵模式解决了主从复制不能自动故障转移，达不到高可用的问题，但还是存在难以在线扩容，Redis容量受限于单机配置的问题。Cluster模式实现了Redis的分布式存储，即每台节点存储不同的内容，来解决在线扩容的问题。如图

![img](https://mmbiz.qpic.cn/sz_mmbiz_png/oFA4QOeEEpOyHZgq0oDyZhTYuatLR4aic4YUQ0SXRCYhdiclrVRVfalYVmkAr5OI9ict6IhPKEg9zk2d9ibIhlC3Ug/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Cluster采用无中心结构,它的特点如下：

1. 所有的redis节点彼此互联(PING-PONG机制),内部使用二进制协议优化传输速度和带宽
2. 节点的fail是通过集群中超过半数的节点检测失效时才生效
3. 客户端与redis节点直连,不需要中间代理层.客户端不需要连接集群所有节点,连接集群中任何一个可用节点即可

Cluster模式的具体工作机制：

1. 在Redis的每个节点上，都有一个插槽（slot），取值范围为0-16383
2. 当我们存取key的时候，Redis会根据CRC16的算法得出一个结果，然后把结果对16384求余数，这样每个key都会对应一个编号在0-16383之间的哈希槽，通过这个值，去找到对应的插槽所对应的节点，然后直接自动跳转到这个对应的节点上进行存取操作
3. 为了保证高可用，Cluster模式也引入主从复制模式，一个主节点对应一个或者多个从节点，当主节点宕机的时候，就会启用从节点
4. 当其它主节点ping一个主节点A时，如果半数以上的主节点与A通信超时，那么认为主节点A宕机了。如果主节点A和它的从节点都宕机了，那么该集群就无法再提供服务了

Cluster模式集群节点最小配置6个节点(3主3从，因为需要半数以上)，其中主节点提供读写操作，从节点作为备用节点，不提供请求，只作为故障转移使用。

**3. Cluster模式的优缺点**

优点：

1. 无中心架构，数据按照slot分布在多个节点。
2. 集群中的每个节点都是平等的关系，每个节点都保存各自的数据和整个集群的状态。每个节点都和其他所有节点连接，而且这些连接保持活跃，这样就保证了我们只需要连接集群中的任意一个节点，就可以获取到其他节点的数据。
3. 可线性扩展到1000多个节点，节点可动态添加或删除
4. 能够实现自动故障转移，节点之间通过gossip协议交换状态信息，用投票机制完成slave到master的角色转换

缺点：

1. 客户端实现复杂，驱动要求实现Smart Client，缓存slots mapping信息并及时更新，提高了开发难度。目前仅JedisCluster相对成熟，异常处理还不完善，比如常见的“max redirect exception”
2. 节点会因为某些原因发生阻塞（阻塞时间大于 cluster-node-timeout）被判断下线，这种failover是没有必要的
3. 数据通过异步复制，不保证数据的强一致性
4. slave充当“冷备”，不能缓解读压力
5. 批量操作限制，目前只支持具有相同slot值的key执行批量操作，对mset、mget、sunion等操作支持不友好
6. key事务操作支持有线，只支持多key在同一节点的事务操作，多key分布不同节点时无法使用事务功能
7. 不支持多数据库空间，单机redis可以支持16个db，集群模式下只能使用一个，即db 0

Redis Cluster模式不建议使用pipeline和multi-keys操作，减少max redirect产生的场景。



#### Redis持久化

Redis 持久化拥有以下三种⽅式： 

- **快照方式**（RDB, Redis DataBase）将某⼀个时刻的内存数据，以⼆进制的⽅式写⼊磁盘； 

- **文件追加方式**（AOF, Append Only File），记录所有的操作命令，并以⽂本的形式追加到⽂件中； 

- **混合持久化方式** ，Redis 4.0 之后新增的⽅式，混合持久化是结合了 RDB 和 AOF 的优点，在写⼊的时候，先把当前的数据以 

  RDB 的形式写⼊⽂件的开头，再将后续的操作命令以 AOF 的格式存⼊⽂件，这样既能保证 Redis 重启时的速度，⼜能简单数 

  据丢失的⻛险。 



RDB

触发方式：手动；自动。

- 手动：bgsave命令。

- 自动：配置文件
  - save m n
    - save 60 1 表明在60s内，至少有一个键发生变化，就会触发持久化。一般设置多个，如save 900 1 save 300 10

#### Redis应用场景

> 1.如何实现附近的人功能

使用zset有序队列以及geohash编码，可以实现空间搜索

> 2.接口幂等性校验

为每一次请求创建一个唯一标识token，先获取token，并将次token存入redis,请求接口时，将此token放到header或者作为请求参数请求接口，后端接口判断redis是否存在此token

> 3.抢单，redsi实现分布式锁

将SETNCX与EXPIRE融合在一起

```
SET KEY value [EX seconds] [PX milliseconds] [NX|XX]
```

> 4.如何设计秒杀系统

1. 利用浏览器缓存和CDN缓存静态数据，进行第一级流量拦截
2. 利用支持读写分离的Redis进行第二级拦截。支持60万以上的qps。
3. 利用主从版Redis缓存加速库存扣量，支持10万以上qps。
4. 使用主从版Redis实现简单的消息队列异步下单入库

> 5.如何利用Redis来统计一个网站的用户访问数

想法：field 可以先择URI+日期拼凑，key可以选择用户id，value可以设1。

- 使用Hash

  ```
  hset  index.html0101 aaaa 1来设值
  hlen index.html0101来统计次数
  ```

  缺点：内存占用多大

- 使用Bitset

  ```
  setbit 	index.html0101 1
  bitcount  index.htmo0101
  ```

  缺点：用户稀疏的话占用内存可能比hash大

- 使用概率算法HyperLogLog，一种基数评估算法,存在误差

  ```
  pfadd 	index.html0101	aaa	bbb	ccc
  pfcount 	inde.html0101
  ```

  





#### Redis设计思想

**I/O多路复用**

一种高效的I/O模型来支撑Redis的多个客户（redis-cli）。

在 I/O 多路复⽤模型中，最重要的函数调⽤就是 select，该⽅法的能够同时监控多个⽂件描述符的可读可写情况，当其中的某些 

⽂件描述符可读或者可写时，select ⽅法就会返回可读以及可写的⽂件描述符个数。 

与此同时也有其它的 I/O 多路复⽤函数 epoll/kqueue/evport，它们相⽐ select 性能更优秀，同时也能⽀撑更多的服务。





# Kafka

**[从面试角度一文学完 Kafka](https://mp.weixin.qq.com/s/QF9b9vpncLS24xMzFkanTQ)**    

## [**Kafka群集部署**](https://blog.51cto.com/14227204/2493049)

**[kafka环境搭建2-broker集群+zookeeper集群](https://www.jianshu.com/p/dc4770fc34b6)**

```shell
Step 3: 创建一个 topic
让我们创建一个名为“test”的topic
> bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test
现在我们可以运行list（列表）命令来查看这个topic：
> bin/kafka-topics.sh --list --zookeeper localhost:2181
test

Step 4: 发送一些消息
> bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

Step 5: 启动一个 consumer
> bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
```



```properties
//zookeeper配置
//server.0:代表第一台服务器的IP地址。第一个端口号（port）是从follower连接到leader机器的端口，第二个端口是用来进行leader选举时所用的端口。
//clientPort：客户端连接server的端口，即对外服务端口，一般设置为2181吧。
server.0=192.168.0.114:2287:3387  
server.1=192.168.0.114:2288:3388  
server.2=192.168.0.114:2289:3389  
clientPort=2180
clientPort=2181
clientPort=2182
//clientPort也就是kafka等连接zookeeper的端口
//kafka配置
kafka自身提供服务的端口
port=9092
port=9093
port=9094
```

分区：

## **Kakfa的设计思想**  

[Kafka如何保证百万级写入速度以及保证不丢失不重复消费](https://www.cnblogs.com/gxyandwmm/p/11432598.html)

##### 如何保证百万级写入速度：     

###### 页缓存技术 + 磁盘顺序写 +零拷贝技术

**页缓存技术 :** 

​		操作系统本身有一层缓存，叫做page cache，是在内存里的缓存，我们也可以称之为os cache，意思就是操作系统自己管理的缓存。写入磁盘文件的时候，可以直接写入这个os cache里，也就是仅仅写入内存中，接下来由操作系统自己决定什么时候把os cache里的数据真的刷入磁盘文件中。

**磁盘顺序写 :**

​		普通的机械磁盘如果你要是随机写的话，确实性能极差，也就是随便找到文件的某个位置来写数据。

但是如果你是追加文件末尾按照顺序的方式来写数据的话，那么这种磁盘顺序写的性能基本上可以跟写内存的性能本身也是差不多的。
**零拷贝技术** : 

​		数据直接从os cache中发送到网卡。就不需要把os cache里的数据拷贝到应用缓存，再从应用缓存拷贝到Socket缓存了，两次拷贝都省略了，所以叫做零拷贝。





\- **Kakfa Broker Leader的选举：**   

 

##### Kafka如何做到不丢失不重复消费



###### **kafka的消息传递机制**

message delivery semantic 也就是消息传递语义。这是一个通用的概念，也就是消息传递过程中消息传递的保证性。

分为三种：

**最多一次（at most once）**: 消息可能丢失也可能被处理，但最多只会被处理一次。

可能丢失 不会重复

**至少一次（at least once）**: 消息不会丢失，但可能被处理多次。

可能重复 不会丢失

**精确传递一次（exactly once）**: 消息被处理且只会被处理一次。

不丢失 不重复 就一次

而kafka其实有两次消息传递，一次生产者发送消息给kafka，一次消费者去kafka消费消息。

两次传递都会影响最终结果，

两次都是精确一次，最终结果才是精确一次。

两次中有一次会丢失消息，或者有一次会重复，那么最终的结果就是可能丢失或者重复的。



**一、Produce端消息传递**

```
properties.put("acks", "all");
```

其中指定了一个参数acks 可以有三个值选择：

 0： producer完全不管broker的处理结果 回调也就没有用了 并不能保证消息成功发送 但是这种吞吐量最高

-1或者all等同： leader broker会等消息写入 并且ISR都写入后 才会响应，这种只要ISR有副本存活就肯定不会丢失，但吞吐量最低。

 1： 默认的值 leader broker自己写入后就响应，不会等待ISR其他的副本写入，只要leader broker存活就不会丢失，即保证了不丢失，也保证了吞吐量。

所以设置为0时，实现了at most once，而且从这边看只要保证集群稳定的情况下，不设置为0，消息不会丢失。

但是还有一种情况就是消息成功写入，而这个时候由于网络问题producer没有收到写入成功的响应，producer就会开启重试的操作，直到网络恢复，消息就发送了多次。这就是at least once了。

kafka producer 的参数acks 的默认值为1，所以默认的producer级别是at least once。并不能exactly once。



出现丢失或者重复的原因：

**丢失的原因：**

broker没收到；broker收到没同步，broker挂掉。

**重复的原因：**消息写入成功后，网络问题producer没有收到响应，producer重试后网络恢复，导致消息发送多次。



0: 完全不管broker的处理结果，会丢消息，不会重复

-1：让消息写入leader和所有的副本，ISR列表中的所有replica都返回确认消息。不会丢消息。会重复

1：默认的值。leader broker自己写入后就响应，不会等待ISR其他的副本写入，只要leader broker存活就不会丢失。leaderbroke挂掉丢消息。会重复。所以默认的producer级别是at least once。并不能exactly once。

2：partition leader和其他一个follower成功的时候就返回，不管其他的。不会丢消息。会重复。



**二、Consumer端消息传递**

消费端不存在消息丢失的问题，只有消息重复。

导致重复的原因：

​		就是消息已经消费了，但是提交偏移量时出错。

```
 props.put("enable.auto.commit", "true");
```

若设置为true consumer在消费之前提交位移 就实现了at most once

若设置为false,是消费后提交, 就实现了 at least once 默认的配置就是这个。

默认值为true ，所以默认的consumer级别是at least once。也并不能exactly once。



三、**精确一次**

通过了解producer端与consumer端的设置，我们发现kafka在两端的默认配置都是at least once，可能重复，通过配置也不能做到exactly once，好像kafka的消息一定会丢失或者重复的，

是不是没有办法做到exactly once了呢？

确实在kafka 0.11.0.0版本之前producer端确实是不可能的，

**但是在kafka 0.11.0.0版本之后，kafka正式推出了idempotent producer。**

**也就是幂等的producer还有对事务的支持。**



##### 幂等的producer

kafka 0.11.0.0版本引入了idempotent producer机制，在这个机制中同一消息可能被producer发送多次，但是在broker端只会写入一次，他为每一条消息编号去重，而且对kafka开销影响不大。

如何设置开启呢？ 需要设置producer端的新参数 

> enable.idempotent = true

而多分区的情况，我们需要保证原子性的写入多个分区，即写入到多个分区的消息要么全部成功，要么全部回滚。

这时候就需要使用事务

> 在producer端设置 transcational.id为一个指定字符串。

**这样幂等producer只能保证单分区上无重复消息；事务可以保证多分区写入消息的完整性。**

这样producer端实现了exactly once，那么consumer端呢？

consumer端由于可能无法消费事务中所有消息，并且消息可能被删除，所以事务并不能解决consumer端exactly  once的问题，我们可能还是需要自己处理这方面的逻辑。比如自己管理offset的提交，不要自动提交，也是可以实现exactly once的。

**还有一个选择就是使用kafka自己的流处理引擎，也就是Kafka Streams，**

> 设置processing.guarantee=exactly_once，就可以轻松实现exactly once了。





# 多线程

## 锁

**锁类型**

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aNvORaIktWZgicKekEn5YS5ULbJsgdUvfSHibrSEj3EnVMzHf53ykYnjA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 锁原理

#### volatile

**防止指令重排序保证有序性**

**保证可见性，不保证原子性**

- 可见性：当某个线程修改volatile变量时，JMM会强制将这个修改更新到主内存中，并且让其他线程工作内存中存储的副本失效。

- volatile变量并不能保证其操作的原子性，具体来说像i++这种操作并不是原子操作，使用volatile修饰变量后仍然不能保证这一点。

为什么不能保证原子性？

**我的不解之处在于：**

既然i是被volatile修饰的变量，那么对于i的操作应该是线程之间是可见的啊，就算A.,B两个线程都同时读到i的值是5，但是如果A线程执行完i的操作以后应该会把B线程读到的i的值置为无效并强制B重新读入i的新值也就是6然后才会进行自增操作才对啊。

后来参照其他博客终于想通了：

```
i++操作可以被拆分为三步：

      1，线程读取i的值

      2、i进行自增计算

      3、刷新回i的值
```

即

```
1、线程读取i

2、temp = i + 1

3、i = temp
```

> **当 i=5 的时候A,B两个线程同时读入了 i 的值， 然后A线程执行了 temp = i + 1的操作， 要注意，此时的 i 的值还没有变化，然后B线程也执行了 temp = i + 1的操作，注意，此时A，B两个线程保存的 i 的值都是5，temp 的值都是6， 然后A线程执行了 i = temp （6）的操作，此时i的值会立即刷新到主存并通知其他线程保存的 i 值失效， 此时B线程需要重新读取 i 的值那么此时B线程保存的 i 就是6，同时B线程保存的 temp 还仍然是6， 然后B线程执行 i=temp （6），所以导致了计算结果比预期少了1。**

是这样吗？看起来好像是，但是为什么B线程重新读取A刷进主存的值后，不执行加一运算而是直接就赋值了？重新查资料

> 简单的说，修改volatile变量分为四步：
> 1）读取volatile变量到local
> 2）修改变量值
> 3）local值写回
> 4）插入内存屏障，即lock指令，让其他线程可见

------

> 从最终汇编语言从面来看，volatile使得每次将i进行了修改之后，增加了一个内存屏障lock addl $0x0,(%rsp)保证修改的值必须刷新到主内存才能进行内存屏障后续的指令操作。但是内存屏障之前的指令并不是原子的。
>
> 内存屏障是线程安全的,但是内存屏障之前的指令并不是.在某一时刻线程1将i的值load取出来，放置到cpu缓存中，然后再将此值放置到寄存器A中，然后A中的值自增1（寄存器A中保存的是中间值，没有直接修改i，因此其他线程并不会获取到这个自增1的值）。如果在此时线程2也执行同样的操作，获取值i==10,自增1变为11，然后马上刷入主内存。此时由于线程2修改了i的值，实时的线程1中的i==10的值缓存失效，重新从主内存中读取，变为11。接下来线程1恢复。将自增过后的A寄存器值11赋值给cpu缓存i。这样就出现了线程安全问题。

但是这里解释仍旧存在上述问题，为什么重新load值之后不走寄存器而是直接就赋值了？

------

> 这里的解释是，当线程B刷进主内存后，如果此时A线程原来已经将i读完，在temp = i 操作时，这时线程A因为总线嗅探机制，会把线程A中工作内存中的i值设为无效，然后重新load主内存。但是此时1）步操作已完成，**不会再去重新执行，而是直接进行后面temp = temp +1 d的操作，这个操作是在寄存器中进行，不会再涉及到i值的读取，也就是说，B的可见性来的太晚了**。



**总结就是：线程在工作内存对值的修改需要写入主存，写入后主内存改变会立即生效，即是线程因为总线嗅探机制，会把工作内存中的值设为无效，然后重新load主内存。因为i++操作需要2步，先load后放入寄存器中计算（使用了临时变量），所以load完后对i的值的改变不会影响后面的操作。**



先来跟着丙丙来看一段demo的代码：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzhiaXUhn9W2XjuqeziaG1ibdvgtlXcS2aHf8I7LeM23TPexQztAQZnQ6rrZOUTNoqIgvladRt5X74Xw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

你会发现，永远都不会输出**有点东西**这一段代码，按道理线程改了flag变量，主线程也能访问到的呀？



##### JMM（JavaMemoryModel）

`Java内存模型(JavaMemoryModel)`描述了Java程序中各种变量(线程共享变量)的访问规则，以及在JVM中将变量，存储到内存和从内存中读取变量这样的底层细节。

**JMM有以下规定：**

所有的共享变量都存储于主内存，这里所说的变量指的是实例变量和类变量，不包含局部变量，因为局部变量是线程私有的，因此不存在竞争问题。

每一个线程还存在自己的工作内存，线程的工作内存，保留了被线程使用的变量的工作副本。

`线程对变量的所有的操作(读，取)都必须在工作内存中完成，而不能直接读写主内存中的变量`。

不同线程之间也不能直接访问对方工作内存中的变量，线程间变量的值的传递需要通过主内存中转来完成。



**本地内存和主内存的关系：**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzhiaXUhn9W2XjuqeziaG1ibdvOgPyiaPib3U7oR6ZS77CqlAVp7BkTxS30UhDN1X6YJRfCGQadBP6xd9Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

正是因为这样的机制，才导致了可见性问题的存在，那我们就讨论下可见性的解决方案。



##### 可见性的解决方案

###### 加锁

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzhiaXUhn9W2XjuqeziaG1ibdvEpR6SEg6ibWX4WOZXoCYUpcfc4Bkx00McJ3uVo6PAyM7fXDQ48X22kg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**为啥加锁可以解决可见性问题呢？**

因为某一个线程进入synchronized代码块前后，线程会获得锁，清空工作内存，从主内存拷贝共享变量最新的值到工作内存成为副本，执行代码，将修改后的副本的值刷新回主内存中，线程释放锁。

而获取不到锁的线程会阻塞等待，所以变量的值肯定一直都是最新的。



###### Volatile修饰共享变量

之前我们说过当多个处理器的运算任务都涉及同一块主内存区域时，将可能导致各自的缓存数据不一致，举例说明变量在多个CPU之间的共享。

如果真的发生这种情况，那同步回到主内存时以谁的缓存数据为准呢？

为了解决一致性的问题，需要各个处理器访问缓存时都遵循一些协议，在读写时要根据协议来进行操作，这类协议有MSI、`MESI（IllinoisProtocol）`、MOSI、Synapse、Firefly及DragonProtocol等。

聊一下Intel的MESI吧

**MESI（缓存一致性协议）**

当CPU写数据时，如果发现操作的变量是共享变量，即在其他CPU中也存在该变量的副本，会发出信号通知其他CPU将该变量的缓存行置为无效状态，因此当其他CPU需要读取这个变量时，发现自己缓存中缓存该变量的缓存行是无效的，那么它就会从内存重新读取。

> 至于是怎么发现数据是否失效呢？

**嗅探**

每个处理器通过嗅探在总线上传播的数据来检查自己缓存的值是不是过期了，当处理器发现自己缓存行对应的内存地址被修改，就会将当前处理器的缓存行设置成无效状态，当处理器对这个数据进行修改操作的时候，会重新从系统内存中把数据读到处理器缓存里。

**总线风暴**

由于Volatile的MESI缓存一致性协议，需要不断的从主内存嗅探和cas不断循环，无效交互会导致总线带宽达到峰值。

所以不要大量使用Volatile，至于什么时候去使用Volatile什么时候使用锁，根据场景区分。

我们再来聊一下`指令重排序`的问题

**as-if-serial**

不管怎么重排序，单线程下的执行结果不能被改变。

编译器、runtime和处理器都必须遵守as-if-serial语义。

> 那Volatile是怎么保证不会被执行重排序的呢？

**内存屏障**

java编译器会在生成指令系列时在适当的位置会插入`内存屏障`指令来禁止特定类型的处理器重排序。

为了实现volatile的内存语义，JMM会限制特定类型的编译器和处理器重排序，JMM会针对编译器制定volatile重排序规则表：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzhiaXUhn9W2XjuqeziaG1ibdvh07EXHvYzpX7DTvOPwqjeRIIrUr3WoPtXHCBSicEL92uk4xZSiaanwuA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

需要注意的是：volatile写是在前面和后面**分别插入内存屏障**，而volatile读操作是在**后面插入两个内存屏障**。

**happens-before**

如果一个操作执行的结果需要对另一个操作可见，那么这两个操作之间必须存在happens-before关系。

```
volatile域规则：对一个volatile域的写操作，happens-before于任意线程后续对这个volatile域的读。
```

如果现在我的变了flag变成了false，那么后面的那个操作，一定要知道我变了。

聊了这么多，我们要知道Volatile是没办法保证原子性的，一定要保证原子性，可以使用其他方法。

**要解决也简单，要么用原子类，比如AtomicInteger，要么加锁(`记得关注Atomic的底层`)。**



###### 应用

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpzhiaXUhn9W2XjuqeziaG1ibdvs2S8eLDBnWul1cmiapWuTPcibd7Xakzm8yMSVt05TquIKtgxItIOX7Mw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

单例有8种写法，我说一下里面比较特殊的一种，涉及Volatile的。

**大家可能好奇为啥要双重检查？如果不用Volatile会怎么样？**

我先讲一下`禁止指令重排序`的好处。

对象实际上创建对象要进过如下几个步骤：

- 分配内存空间。
- 调用构造器，初始化实例。
- 返回地址给引用

上面我不是说了嘛，是可能发生指令重排序的，那有可能构造函数在对象初始化完成前就赋值完成了，在内存里面开辟了一片存储区域后直接返回内存的引用，这个时候还没真正的初始化完对象。

但是别的线程去判断instance！=null，直接拿去用了，其实这个对象是个半成品，那就有空指针异常了。

**可见性怎么保证的？**

因为可见性，线程A在自己的内存初始化了对象，还没来得及写回主内存，B线程也这么做了，那就创建了多个对象，不是真正意义上的单例了。

上面提到了volatile与synchronized，那我聊一下他们的区别。



**volatile与synchronized的区别**

volatile只能修饰实例变量和类变量，而synchronized可以修饰方法，以及代码块。

volatile保证数据的可见性，但是不保证原子性(多线程进行写操作，不保证线程安全);而synchronized是一种排他(互斥)的机制。

volatile用于禁止指令重排序：可以解决单例双重检查对象初始化代码执行乱序问题。

volatile可以看做是轻量版的synchronized，volatile不保证原子性，但是如果是对一个共享变量进行多个线程的赋值，而没有其他的操作，那么就可以用volatile来代替synchronized，因为赋值本身是有原子性的，而volatile又保证了可见性，所以就可以保证线程安全了。



参考：

1. [面试官想到，一个Volatile，敖丙都能吹半小时](https://mp.weixin.qq.com/s/Oa3tcfAFO9IgsbE22C5TEg)           



#### **AQS**

**`要点`**：

- 抽象队列式同步器，定义了很多锁相关的方法

`AQS`中 维护了一个`volatile int state`（代表共享资源）和一个`FIFO`线程等待队列（多线程争用资源被阻塞时会进入此队列）。当`state=1`则代表当前对象锁已经被占有，其他线程来加锁时则会失败，加锁失败的线程会被放入一个`FIFO`的等待队列中，等待锁释放。



​		AbstractQueuedSynchronized 抽象队列式的同步器，AQS定义了一套多线程访问共享资源的同步器框架，许多同步类实现都依赖于它，如常用的ReentrantLock/Semaphore/CountDownLatch…

​		AbstractQueuedSynchronizer是CountDownLatch/FutureTask/ReentrantLock/RenntrantReadWriteLock/Semaphore的基础，因此AbstractQueuedSynchronizer是Lock/Executor实现的前提。公平锁、不公平锁、Condition、CountDownLatch、Semaphore等放到后面的篇幅中说明。

AQS：也就是队列同步器，这是实现 ReentrantLock 的基础。

AQS 有一个 state 标记位，值为1  时表示有线程占用，其他线程需要进入到同步队列等待，同步队列是一个双向链表。

当获得锁的线程需要等待某个条件时，会进入 condition 的等待队列，等待队列可以有多个。

当 condition 条件满足时，线程会从等待队列重新进入同步队列进行获取锁的竞争。

​		基本的思想是表现为一个同步器，支持下面两个操作：

**获取锁**：首先判断当前状态是否允许获取锁，如果是就获取锁，否则就阻塞操作或者获取失败，也就是说如果是独占锁就可能阻塞，如果是共享锁就可能失败。另外如果是阻塞线程，那么线程就需要进入阻塞队列。当状态位允许获取锁时就修改状态，并且如果进了队列就从队列中移除。

> while(synchronization state does not allow acquire){
>
> enqueue current thread if not already queued;
>
> possibly block current thread;
>
> }
>
> dequeue current thread if it was queued;

**释放锁**:这个过程就是修改状态位，如果有线程因为状态位阻塞的话就唤醒队列中的一个或者更多线程。

> update synchronization state;
>
> if(state may permit a blocked thread to acquire)
>
> unlock one or more queued threads;

要支持上面两个操作就必须有下面的条件：

- 原子性操作同步器的状态位  
- 阻塞和唤醒线程  
- 一个有序的队列 

　　![img](https://images2015.cnblogs.com/blog/721070/201705/721070-20170504110246211-10684485.png)

　　**AQS维护了一个volatile int state(代表共享资源)和一个FIFO线程等待队列（多线程争用资源被阻塞时会进入此队列）。**

　　state的访问方式有三种：

```
1 getState()
2 setState()
3 compareAndSetState()
```

​		AQS定义两种资源共享方式：Exclusive（独占，只有一个线程能执行，如ReentrantLock）和Share（共享，多个线程可同时执行，如Semaphore/CountDownLatch）。

不同的自定义同步器争用共享资源的方式也不同。自定义同步器在实现时只需要实现共享资源state的获取与释放方式即可，至于具体线程等待队列的维护（如获取资源失败入队/唤醒出队等），AQS已经在顶层实现好了。自定义同步器实现时主要实现以下几种方法：

```
1 isHeldExclusively():该线程是否正在独占资源。只有用到condition才需要去实现它。
2 tryAquire(int):独占方式。尝试获取资源，成功则返回true，失败则返回false。
3 tryRelease(int):独占方式。尝试释放资源，成功则返回true，失败则返回false。
4 tryAcquireShared(int):共享方式。尝试获取资源。负数表示失败；0表示成功，但没有剩余可用资源；正数表示成功，且有剩余资源。
5 tryReleaseShared(int):共享方式。尝试释放资源，如果释放后允许唤醒后续等待结点返回true，否则返回false。
```

　　以ReentrantLock为例，state初始化为0，表示未锁定状态。A线程lock()时，会调用tryAcquire()独占该锁并将state+1。此后，其他线程再tryAcquire()时就会失败，直到A线程unlock()到state=0（即释放锁）为止，其他线程才有机会获取该锁。当然，释放锁之前，A线程自己是可以重复获取此锁的（state会累加），这就是可重入的概念。但要注意，获取多少次就要释放多少次，这样才能保证state是能回到零态的。

　　再以CountDownLatch为例，任务分为N个子线程去执行，state为初始化为N（注意N要与线程个数一致）。这N个子线程是并行执行的，每个子线程执行完后countDown()一次，state会CAS减1。等到所有子线程都执行完后（即state=0），会unpark()主调用线程，然后主调用线程就会await()函数返回，继续后余动作。

　　一般来说，自定义同步器要么是独占方法，要么是共享方式，他们也只需实现tryAcquire-tryRelease、tryAcquireShared-tryReleaseShared中的一种即可。但AQS也支持自定义同步器同时实现独占和共享两种方式，如ReentrantReadWriteLock。



参考：

1. [我画了35张图就是为了让你深入 AQS](https://mp.weixin.qq.com/s/trsjgUFRrz40Simq2VKxTA)                



#### **CAS**

​		CAS（Compare and Swap 比较并交换）是乐观锁技术，当多个线程尝试使用CAS同时更新同一个变量时，只有其中一个线程能更新变量的值，而其他线程都失败，失败的线程并不会被挂起，而是被告知这次竞争中失败，并可以再次尝试。 

​		**CAS操作中包含三个操作数——需要读写的内存位置（V）、进行比较的预期原值（A）和拟写入的新值（B）**。如果内存位置V的值与预期原值A相匹配，那么处理器会自动将该位置值更新为新值B，否则处理器不做任何操作。无论哪种情况，它都会在CAS指令之前返回该位置的值（在CAS的一些特殊情况下将仅返回CAS是否成功，而不提取当前值）。CAS有效地说明了“我认为位置V应该包含值A；如果包含该值，则将B放到这个位置；否则，不要更改该位置，只告诉我这个位置现在的值即可”。这其实和乐观锁的冲突检查+数据更新的原理是一样的。

CAS是借助C来调用CPU底层指令实现的。



```java
public static void increment() {
    do{
        int k = i;
        int j = k + 1;
    }while (compareAndSet(i, k, j))
}
```

```java
private volatile int value;
//Unsafe.getAndAddInt
public final int getAndAddInt(Object var1, long var2, int var4) {
	int var5;
	do{
        //拿到主存拷贝到工作内存中的值
		var5 = this.getIntVolatile(var1, var2);
        //当前主存值与期望值一样，修改
	} while(!this.compareAndSwapInt(var1,var2,var5,var5+var4));
	return var5;
}
```

假设线程A和线程B同时执行getAndInt操作（分别跑在不同的CPU上）

- tomicInteger里面的value原始值为3，即主内存中AtomicInteger的 value 为3，根据JMM模型，线程A和线程B各自持有一份价值为3的副本，分别存储在各自的工作内存
- 线程A通过getIntVolatile(var1 , var2) 拿到value值3，这是线程A被挂起（该线程失去CPU执行权）
- 线程B也通过getIntVolatile(var1, var2)方法获取到value值也是3，此时刚好线程B没有被挂起，并执行了compareAndSwapInt方法，比较内存的值也是3，成功修改内存值为4，线程B打完收工，一切OK
- 这是线程A恢复，执行CAS方法，比较发现自己手里的数字3和主内存中的数字4不一致，说明该值已经被其它线程抢先一步修改过了，那么A线程本次修改失败，只能够重新读取后在来一遍了，也就是在执行do while
- 线程A重新获取value值，因为变量value被volatile修饰，所以其它线程对它的修改，线程A总能够看到，线程A继续执行compareAndSwapInt进行比较替换，直到成功。

**总结就是：**

​		**线程在修改值前拿本地内存与主存进行比较，此时不允许其他线程占用CPU，如果本地值与主存值相同，则修改；否则重新读取主内存值，循环操作，直至成功。这里的核心在于比较过程是独占CPU。**



**ABA问题：谁偷偷更改了我的值**

​	虽然这种 CAS 的机制能够保证increment() 方法，但依然有一些问题，例如，当线程A即将要执行第三步的时候，线程 B 把 i  的值加1，之后又马上把 i 的值减 1，然后，线程 A 执行第三步，这个时候线程 A 是认为并没有人修改过 i 的值，因为 i  的值并没有发生改变。而这，就是我们平常说的**ABA问题**。

​	对于基本类型的值来说，这种把**数字改变了在改回原来的值**是没有太大影响的，但如果是对于引用类型的话，就会产生很大的影响了。

**来个版本控制吧**

​		为了解决这个 ABA  的问题，我们可以引入版本控制，例如，每次有线程修改了引用的值，就会进行版本的更新，虽然两个线程持有相同的引用，但他们的版本不同，这样，我们就可以预防 ABA 问题了。

​		JDK从1.5开始提供了**AtomicStampedReference**类来解决ABA问题，具体操作封装在compareAndSet()中。compareAndSet()首先检查当前引用和当前标志与预期引用和预期标志是否相等，如果都相等，则以原子方式将引用值和标志的值设置为给定的更新值。

​		**只能保证一个共享变量的原子操作**。对一个共享变量执行操作时，CAS能够保证原子操作，但是对多个共享变量操作时，CAS是无法保证操作的原子性的。

​		Java从1.5开始JDK提供了**AtomicReference**类来保证引用对象之间的原子性，可以把多个变量放在一个对象里来进行CAS操作。

**Java8 对 CAS 的优化。**

> 由于采用这种 CAS 机制是没有对方法进行加锁的，所以，所有的线程都可以进入 increment() 这个方法，假如进入这个方法的线程太多，就会出现一个问题：每次有线程要执行第三个步骤的时候，i 的值老是被修改了，所以线程又到回到第一步继续重头再来。
>
> 而这就会导致一个问题：由于线程太密集了，太多人想要修改 i 的值了，进而大部分人都会修改不成功，白白着在那里循环消耗资源。
>
> 为了解决这个问题，Java8 引入了一个 cell[] 数组，它的工作机制是这样的：假如有 5 个线程要对 i  进行自增操作，由于 5 个线程的话，不是很多，起冲突的几率较小，那就让他们按照以往正常的那样，采用 CAS 来自增吧。
>
> 但是，如果有 100 个线程要对 i 进行自增操作的话，这个时候，冲突就会大大增加，系统就会把这些线程分配到不同的 cell  数组元素去，假如 cell[10] 有 10 个元素吧，且元素的初始化值为 0，那么系统就会把 100 个线程分成 10 组，每一组对 cell 数组其中的一个元素做自增操作，这样到最后，cell 数组 10 个元素的值都为 10，系统在把这 10 个元素的值进行汇总，进而得到  100，二这，就等价于 100 个线程对 i 进行了 100 次自增操作。
>
> 当然，我这里只是举个例子来说明 Java8 对 CAS 优化的大致原理，具体的大家有兴趣可以去看源码，或者去搜索对应的文章哦



#### synchronized

synchronized之前一直都是重量级的锁，但是后来java官方是对他进行过升级的，他现在采用的是锁升级的方式去做的。

针对 synchronized 获取锁的方式，JVM 使用了锁升级的优化方式，就是先使用**偏向锁**优先同一线程然后再次获取锁，如果失败，就升级为 **CAS 轻量级锁**，如果失败就会短暂**自旋**，防止线程被系统挂起。最后如果以上都失败就升级为**重量级锁**。

所以是一步步升级上去的，最初也是通过很多轻量级的方式锁定的。



Synchronized一般都是用在下面这几种场景：

- 修饰实例方法，对当前实例对象this加锁；

- 修饰静态方法，对当前类的Class对象加锁；

- 修饰代码块，指定一个加锁的对象，给对象加锁；

**其实就是锁方法、锁代码块和锁对象，那他们是怎么实现加锁的呢？**

在这之前，我就先跟大家聊一下我们Java对象的构成



##### 对象内存分布

在 JVM 中，对象在内存中分为三块区域：

- 对象头

- - **Mark Word（标记字段）**：默认存储对象的HashCode，分代年龄和锁标志位信息。它会根据对象的状态复用自己的存储空间，也就是说在运行期间Mark Word里存储的数据会随着锁标志位的变化而变化。
  - **Klass Point（类型指针）**：对象指向它的类元数据的指针，虚拟机通过这个指针来确定这个对象是哪个类的实例。

- 实例数据

- - 这部分主要是存放类的数据信息，父类的信息。

- 对其填充

- - 由于虚拟机要求对象起始地址必须是8字节的整数倍，填充数据不是必须存在的，仅仅是为了字节对齐。

    Tip：不知道大家有没有被问过一个空对象占多少个字节？就是8个字节，是因为对齐填充的关系哈，不到8个字节对其填充会帮我们自动补齐。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOvbqJ6aDgsiaAKZWI1GdoInfBevrHfVXic06kLnUy3xKcJJkqDv7UKK5Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



​		最开始提到过对象头，他会关联到一个monitor对象，当我们进入一个人方法的时候，执行**monitorenter**，就会获取当前对象的一个所有权，这个时候monitor进入数为1，当前的这个线程就是这个monitor的owner；如果你已经是这个monitor的owner了，你再次进入，就会把进入数+1；当他执行完**monitorexit**，对应的进入数就-1，直到为0，才可以被其他线程持有。所谓的互斥，其实在这里，就是看你能否获得monitor的所有权，一旦你成为owner就是获得者。

​		大家说熟悉的锁升级过程，其实就是在ObjectMonitor源码里面，调用了不同的实现去获取获取锁，失败就调用更高级的实现，最后升级完成。



**我们经常说到的，有序性、可见性、原子性，synchronized又是怎么做到的呢?**

- **有序性**

我在Volatile章节已经说过了CPU会为了优化我们的代码，会对我们程序进行重排序。

**as-if-serial**

不管编译器和CPU如何重排序，必须保证在单线程情况下程序的结果是正确的，还有就是有数据依赖的也是不能重排序的。

- **可见性**

同样在Volatile章节我介绍到了现代计算机的内存结构，以及JMM（Java内存模型），这里我需要说明一下就是JMM并不是实际存在的，而是一套规范，这个规范描述了很多java程序中各种变量（线程共享变量）的访问规则，以及在JVM中将变量存储到内存和从内存中读取变量这样的底层细节，Java内存模型是对共享数据的可见性、有序性、和原子性的规则和保障。

大家感兴趣，也记得去了解计算机的组成部分，cpu、内存、多级缓存等，会帮助更好的理解java这么做的原因。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOialcoD9IRXH5jUskMiaHfPd8AKmWZYGAerLH3bpulF72IYhrK2kuia9Pg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

- **原子性**

其实他保证原子性很简单，确保同一时间只有一个线程能拿到锁，能够进入代码块这就够了。

这几个是我们使用锁经常用到的特性，那synchronized他自己本身又具有哪些特性呢？

- **可重入性**

synchronized锁对象的时候有个计数器，他会记录下线程获取锁的次数，在执行完对应的代码块之后，计数器就会-1，直到计数器清零，就释放锁了。

那可重入有什么好处呢？

可以避免一些死锁的情况，也可以让我们更好封装我们的代码。

- **不可中断性**

不可中断就是指，一个线程获取锁之后，另外一个线程处于阻塞或者等待状态，前一个不释放，后一个也一直会阻塞或者等待，不可以被中断。

值得一提的是，Lock的tryLock方法是可以被中断的。



##### 锁升级

synchronized在1.6前是重量级锁，后面官方进行了升级，获取锁过程是一个锁升级的过程。

升级方向：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOiaEtKGL0EickicibDjwEqKRK8rMUz7kxlSmiapXejO8fmmcyBGBSSju8TYQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Tip：切记这个升级过程是不可逆的，最后我会说明他的影响，涉及使用场景。

看完他的升级，我们就来好好聊聊每一步怎么做的吧。



###### 偏向锁

之前我提到过了，对象头是由Mark Word和Klass pointer 组成，锁争夺也就是对象头指向的Monitor对象的争夺，一旦有线程持有了这个对象，标志位修改为1，就进入偏向模式，同时会把这个线程的ID记录在对象的Mark Word中。

这个过程是采用了CAS乐观锁操作的，每次同一线程进入，虚拟机就不进行任何同步的操作了，对标志位+1就好了，不同线程过来，CAS会失败，也就意味着获取锁失败。

**线程ID记录在对象的MarkWord中，锁标志位修改为1，进入偏向模式。**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOVdzHLLufkld1RKmmR5pPMvAv6BhShLnNQLiaNYwpeiah3JLqkRnibqfLw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



###### 轻量级锁

还是跟Mark Work 相关，如果这个对象是无锁的，jvm就会在当前线程的栈帧中建立一个叫锁记录（Lock Record）的空间，用来存储锁对象的Mark Word 拷贝，然后把Lock Record中的owner指向当前对象。

JVM接下来会利用CAS尝试把对象原本的Mark Word 更新会Lock Record的指针，成功就说明加锁成功，改变锁标志位，执行相关同步操作。

如果失败了，就会判断当前对象的Mark Word是否指向了当前线程的栈帧，是则表示当前的线程已经持有了这个对象的锁，否则说明被其他线程持有了，继续锁升级，修改锁的状态，之后等待的线程也阻塞。

**当前线程在栈帧中新开辟锁记录（Lock Record）的空间，拷贝对象的Mark Word，然后把Lock Record中的owner指向当前对象，接着JVM会利用CAS尝试把对象原本的Mark Word 更新为Lock Record的指针，成功就说明加锁成功，改变锁标志位，执行相关同步操作。**意思就是将MarkWord拷贝到线程私有的栈帧中，而原对象只存储指针了。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOpWZtXMM1bW69vLYavfIPohHK8ysAuT2ZTptNiaiazzu3sO87HyOIWo8g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



###### 自旋锁

我不是在上面提到了Linux系统的用户态和内核态的切换很耗资源，其实就是线程的等待唤起过程，那怎么才能减少这种消耗呢？

自旋，过来的现在就不断自旋，防止线程被挂起，一旦可以获取资源，就直接尝试成功，直到超出阈值，自旋锁的默认大小是10次，-XX：PreBlockSpin可以修改。

自旋都失败了，那就升级为重量级的锁，像1.5的一样，等待唤起咯。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyB6WkMTL2IUapfTtGH6FFOYCtibWcIFcWA6Tdat8QSaQTmN28NXSwvibX7P0ibWez8fY8sibdCkOvjQQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



> 用synchronized还是Lock呢？

我们先看看他们的区别：

- synchronized是关键字，是JVM层面的底层啥都帮我们做了，而Lock是一个接口，是JDK层面的有丰富的API。
- synchronized会自动释放锁，而Lock必须手动释放锁。
- synchronized是不可中断的，Lock可以中断也可以不中断。
- 通过Lock可以知道线程有没有拿到锁，而synchronized不能。
- synchronized能锁住方法和代码块，而Lock只能锁住代码块。
- Lock可以使用读锁提高多线程读效率。
- synchronized是非公平锁，ReentrantLock可以控制是否是公平锁。

两者一个是JDK层面的一个是JVM层面的，我觉得最大的区别其实在，我们是否需要丰富的api，还有一个我们的场景。

**比如我现在是滴滴，我早上有打车高峰，我代码使用了大量的synchronized，有什么问题？锁升级过程是不可逆的，过了高峰我们还是重量级的锁，那效率是不是大打折扣了？这个时候你用Lock是不是很好？**

场景是一定要考虑的，我现在告诉你哪个好都是扯淡，因为脱离了业务，一切技术讨论都没有了价值。



参考：

1. [死磕Synchronized底层实现](https://mp.weixin.qq.com/s/2ka1cDTRyjsAGk_-ii4ngw)                



#### Lock



#### ThreadLocal

threadlocal使用方法很简单

```java
static final ThreadLocal<T> sThreadLocal = new ThreadLocal<T>();
sThreadLocal.set()
sThreadLocal.get()
```

​		threadlocal而是一个线程内部的存储类，可以在指定线程内存储数据，数据存储以后，只有指定线程可以得到存储数据。

​		大致意思就是ThreadLocal提供了线程内存储变量的能力，这些变量不同之处在于每一个线程读取的变量是对t应的互相独立的。通过get和set方法就可以得到当前线程对应的值。

​		做个不恰当的比喻，从表面上看ThreadLocal相当于维护了一个map，key就是当前的线程，value就是需要存储的对象。

​		**这里的这个比喻是不恰当的，实际上是ThreadLocal的静态内部类ThreadLocalMap为每个Thread都维护了一个数组table，ThreadLocal确定了一个数组下标，而这个下标就是value存储的对应位置。**。

作为一个存储数据的类，关键点就在get和set方法。



ThreadLocal的作用主要是做数据隔离，填充的数据只属于当前线程，变量的数据对别的线程而言是相对隔离的，在多线程环境下，如何防止自己的变量被其它线程篡改。

> 你能跟我说说它隔离有什么用，会用在什么场景么？

事务隔离级别

Spring采用Threadlocal的方式，来保证单个线程中的数据库操作使用的是同一个数据库连接，同时，采用这种方式可以使业务层使用事务时不需要感知并管理connection对象，通过传播级别，巧妙地管理多个事务配置之间的切换，挂起和恢复。

Spring框架里面就是用的ThreadLocal来实现这种隔离，主要是在`TransactionSynchronizationManager`这个类里面。

Spring的事务主要是ThreadLocal和AOP去做实现的，我这里提一下，大家知道每个线程自己的链接是靠ThreadLocal保存的就好了。

> 除了源码里面使用到ThreadLocal的场景，你自己有使用他的场景么？一般你会怎么用呢？

之前我们上线后发现部分用户的日期居然不对了，排查下来是`SimpleDataFormat`的锅，当时我们使用SimpleDataFormat的parse()方法，内部有一个Calendar对象，调用SimpleDataFormat的parse()方法会先调用Calendar.clear（），然后调用Calendar.add()，如果一个线程先调用了add()然后另一个线程又调用了clear()，这时候parse()方法解析的时间就不对了。

其实要解决这个问题很简单，让每个线程都new 一个自己的 `SimpleDataFormat`就好了，但是1000个线程难道new1000个`SimpleDataFormat`？

所以当时我们使用了线程池加上ThreadLocal包装`SimpleDataFormat`，再调用initialValue让每个线程有一个`SimpleDataFormat`的副本，从而解决了线程安全的问题，也提高了性能。

参考：

1. [Java面试必问：ThreadLocal终极篇     淦！](https://mp.weixin.qq.com/s/LzkZXPtLW2dqPoz3kh3pBQ)



### 锁类型

来源：[美团技术团队](https://mp.weixin.qq.com/s/E2fOUHOabm10k_EVugX08g)

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aNvORaIktWZgicKekEn5YS5ULbJsgdUvfSHibrSEj3EnVMzHf53ykYnjA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



[乐观锁、悲观锁](#乐观锁、悲观锁-头)<a name = "乐观锁、悲观锁-尾"></a>

- [乐观锁](#乐观锁-头)<a name = "乐观锁-尾"></a> 

- [悲观锁](#悲观锁-头)<a name = "悲观锁-尾"></a>

  使用数据时认为一定有别的线程来修改数据。synchronized关键字和Lock的实现类。

[自旋锁、适应性自旋锁](#自旋锁、适应性自旋锁-头)<a name = "自旋锁、适应性自旋锁-尾"></a>

- [自旋锁](#自旋锁-头)<a name = "自旋锁-尾"></a>
- [适应性自旋锁](#适应性自旋锁-头)<a name = "适应性自旋锁-尾"></a>

[无锁、偏向锁、轻量级锁、重量级锁](#无锁、偏向锁、轻量级锁、重量级锁-头)<a name = "无锁、偏向锁、轻量级锁、重量级锁-尾"></a>

- [无锁](#无锁-头)<a name = "无锁-尾"></a>
- [偏向锁](#偏向锁-头)<a name ="偏向锁-尾"></a>

- [轻量级锁](#轻量级锁)<a name = "轻量级锁-尾"></a>

- [重量级锁](#重量级锁-头)<a name = "重量级锁-尾"></a>

[公平锁、非公平锁](#公平锁、非公平锁-头)<a name = "公平锁、非公平锁-尾"></a>

- [公平锁](#公平锁-头)<a name = "公平锁-尾"></a>
- [非公平锁](#非公平锁-头)<a name = "非公平锁-尾"></a>

[可重入锁、非可重入锁](#可重入锁、非可重入锁-头)<a name = "可重入锁、非可重入锁-尾"></a>

- [可重入锁](#可重入锁-头)<a name = "可重入锁-尾"></a>
- [非可重入锁](#非可重入锁-尾)<a name ="非可重入锁-尾"></a>

[独享锁、共享锁](#独享锁、共享锁-头)<a name = "独享锁、共享锁-尾"></a>

- [独享锁](#独享锁-头)<a name = "独享锁-尾"></a>
- [共享锁](#共享锁-头)<a name = "共享锁-尾"></a>





##### 乐观锁、悲观锁<a name = "乐观锁、悲观锁-头"></a>

乐观锁与悲观锁是一种广义上的概念，体现了看待线程同步的不同角度。

> 先说概念。对于同一个数据的并发操作，悲观锁认为自己在使用数据的时候一定有别的线程来修改数据，因此在获取数据的时候会先加锁，确保数据不会被别的线程修改。Java中，synchronized关键字和Lock的实现类都是悲观锁。
>
> 而乐观锁认为自己在使用数据时不会有别的线程修改数据，所以不会添加锁，只是在更新数据的时候去判断之前有没有别的线程更新了这个数据。如果这个数据没有被更新，当前线程将自己修改的数据成功写入。如果数据已经被其他线程更新，则根据不同的实现方式执行不同的操作（例如报错或者自动重试）。

- 乐观锁<a name ="乐观锁-头"></a>

  使用数据是认为不会有别的线程修改数据。CAS。

- 悲观锁<a name ="悲观锁-头"></a>

  使用数据时认为一定有别的线程来修改数据。synchronized关键字和Lock的实现类。



##### **自旋锁、适应性自旋锁**<a name = "自旋锁、适应性自旋锁-头"></a>

**自旋锁 VS 适应性自旋锁**，让当前线程进行自旋，如果在自旋完成后前面锁定同步资源的线程已经释放了锁，那么当前线程就可以不必阻塞而是直接获取同步资源，从而避免切换线程的开销。

> ​		阻塞或唤醒一个Java线程需要操作系统切换CPU状态来完成，这种状态转换需要耗费处理器时间。如果同步代码块中的内容过于简单，状态转换消耗的时间有可能比用户代码执行的时间还要长。
>
> ​		在许多场景中，同步资源的锁定时间很短，为了这一小段时间去切换线程，线程挂起和恢复现场的花费可能会让系统得不偿失。如果物理机器有多个处理器，能够让两个或以上的线程同时并行执行，我们就可以让后面那个请求锁的线程不放弃CPU的执行时间，看看持有锁的线程是否很快就会释放锁。
>
> ​		而为了让当前线程“稍等一下”，我们需让当前线程进行自旋，如果在自旋完成后前面锁定同步资源的线程已经释放了锁，那么当前线程就可以不必阻塞而是直接获取同步资源，从而避免切换线程的开销。这就是自旋锁。

- [**自旋锁**](#自旋锁-尾)<a name= "自旋锁-头"></a>

**当竞争存在时**，如果线程可以很快获得锁(大部分情况都是)，那么可以不在OS层挂起线程，让线程做几个空操纵（自旋，默认是10次，可以使用-XX:PreBlockSpin来更改）。如果同步块很短，自旋成功，节省线程挂起切换时间。

JVM层面的锁。JDK1.6中-XX:+UseSpinning开启。1.7以后去掉此参数，改为内置自适应的自旋锁（适应性自旋锁）。

- 适应性自旋锁<a name = "适应性自旋锁-头"></a>

自适应意味着自旋的时间（次数）不再固定，而是由前一次在同一个锁上的自旋时间及锁的拥有者的状态来决定。如果在同一个锁对象上，自旋等待刚刚成功获得过锁，并且持有锁的线程正在运行中，那么虚拟机就会认为这次自旋也是很有可能再次成功，进而它将允许自旋等待持续相对更长的时间。如果对于某个锁，自旋很少成功获得过，那在以后尝试获取这个锁时将可能省略掉自旋过程，直接阻塞线程，避免浪费处理器资源。

> 偏向锁、轻量级锁、自选锁总结

JVM层面的锁，不是Java语言曾main的锁优化方法。偏向锁可用时会先尝试获取偏向锁，进行偏向模式；否则轻量级锁可用会先尝试轻量级锁；如果失败，尝试自旋锁；再失败，尝试普通锁，使用OS互拆量在操作系统层挂起。



##### 无锁、偏向锁、轻量级锁、重量级锁<a name ="无锁、偏向锁、轻量级锁、重量级锁"></a>

> 这四种锁是指锁的状态，专门针对synchronized的。在介绍这四种锁状态之前还需要介绍一些额外的知识。
>
> 首先为什么Synchronized能实现线程同步？
>
> 在回答这个问题之前我们需要了解两个重要的概念：“Java对象头”、“Monitor”。

**Java对象头**

synchronized是悲观锁，在操作同步资源之前需要给同步资源先加锁，这把锁就是存在Java对象头里的，而Java对象头又是什么呢？

我们以Hotspot虚拟机为例，Hotspot的对象头主要包括两部分数据：Mark Word（标记字段，32位）、Klass Pointer（类型指针）。

**Mark Word**：默认存储对象的HashCode，垃圾回收标记，分代年龄和锁标志位信息。这些信息都是与对象自身定义无关的数据，所以Mark Word被设计成一个非固定的数据结构以便在极小的空间内存存储尽量多的数据。它会根据对象的状态复用自己的存储空间，也就是说在运行期间Mark Word里存储的数据会随着锁标志位的变化而变化。

——指向锁记录的指针
——指向monitor的指针
——GC标记
——偏向锁线程ID

**Klass Point**：对象指向它的类元数据的指针，虚拟机通过这个指针来确定这个对象是哪个类的实例。

**Monitor**：Monitor可以理解为一个同步工具或一种同步机制，通常被描述为一个对象。每一个Java对象就有一把看不见的锁，称为内部锁或者Monitor锁。

Monitor是线程私有的数据结构，每一个线程都有一个可用monitor record列表，同时还有一个全局的可用列表。每一个被锁住的对象都会和一个monitor关联，同时monitor中有一个Owner字段存放拥有该锁的线程的唯一标识，表示该锁被这个线程占用。

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aPyc0L5Dn6L5mupGBVuofgnFThXAmmBvZwhk2FRpj0dc7BRpfe6GWlA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



- [**无锁**](#无锁-尾)<a name = "无锁-头"></a>

无锁没有对资源进行锁定，所有的线程都能访问并修改同一个资源，但同时只有一个线程能修改成功。

无锁的特点就是修改操作在循环内进行，线程会不断的尝试修改共享资源。如果没有冲突就修改成功并退出，否则就会继续循环尝试。如果有多个线程修改同一个值，必定会有一个线程能修改成功，而其他修改失败的线程会不断重试直到修改成功。上面我们介绍的CAS原理及应用即是无锁的实现。无锁无法全面代替有锁，但无锁在某些场合下的性能是非常高的。



- **[偏向锁](#偏向锁-尾)**<a name ="偏向锁-头"></a>

线程之间大部分情况是**没有竞争**的，意思就是锁总是由同一线程多次获得，不存在多线程竞争，所以通过偏向来提高性能。所谓偏向，就是偏心，即锁会偏向于当前已经占有锁的线程。将对象头Mark的标记设置为偏向，并将线程ID写入对象头Mark。**只要没有竞争**，获得偏向锁的线程，在将来进入同步块，不需要做同步。当其他线程请求相同的锁时，此时存在竞争，偏向模式结束。（在竞争激烈的场合，偏向锁会增加系统负担）

> 当一个线程访问同步代码块并获取锁时，会在Mark Word里存储锁偏向的线程ID。在线程进入和退出同步块时不再通过CAS操作来加锁和解锁，而是检测Mark Word里是否存储着指向当前线程的偏向锁。引入偏向锁是为了在无多线程竞争的情况下尽量减少不必要的轻量级锁执行路径，因为轻量级锁的获取及释放依赖多次CAS原子指令，而偏向锁只需要在置换ThreadID的时候依赖一次CAS原子指令即可。
>
> 偏向锁只有遇到其他线程尝试竞争偏向锁时，持有偏向锁的线程才会释放锁，线程不会主动释放偏向锁。偏向锁的撤销，需要等待全局安全点（在这个时间点上没有字节码正在执行），它会首先暂停拥有偏向锁的线程，判断锁对象是否处于被锁定状态。撤销偏向锁后恢复到无锁（标志位为“01”）或轻量级锁（标志位为“00”）的状态。
>
> 偏向锁在JDK 6及以后的JVM里是默认启用的。可以通过JVM参数关闭偏向锁：-XX:-UseBiasedLocking=false，关闭之后程序默认会进入轻量级锁状态。
>
> JVM层面的锁。-XX:+UseBiasedLocking 默认启用。

- [**轻量级锁**](#轻量级锁-尾)<a name = "轻量级锁"></a>

是指当锁是偏向锁是，被另外的线程访问，偏向锁就会升级为轻量级锁，其他线程会通过自旋的形式尝试获取锁，不会阻塞，从而提高性能。

如果对象没有被锁定，将**对象头的Mark指针**保存到锁对象BasicObjectLock（嵌入在线程栈中的对象）中，将对象头设置为指向锁的指针。

如果轻量级锁失败，表示存在竞争，升级为重量级锁（常规锁）。在没有锁竞争的前提下，减少传统锁使用OS互斥量产生的性能损耗。

> 在代码进入同步块的时候，如果同步对象锁状态为无锁状态（锁标志位为“01”状态，是否为偏向锁为“0”），虚拟机首先将在当前线程的栈帧中建立一个名为锁记录（Lock Record）的空间，用于存储锁对象目前的Mark Word的拷贝，然后拷贝对象头中的Mark Word复制到锁记录中。
>
> 拷贝成功后，虚拟机将使用CAS操作尝试将对象的Mark Word更新为指向Lock Record的指针，并将Lock Record里的owner指针指向对象的Mark Word。
>
> 如果这个更新动作成功了，那么这个线程就拥有了该对象的锁，并且对象Mark Word的锁标志位设置为“00”，表示此对象处于轻量级锁定状态。
>
> 如果轻量级锁的更新操作失败了，虚拟机首先会检查对象的Mark Word是否指向当前线程的栈帧，如果是就说明当前线程已经拥有了这个对象的锁，那就可以直接进入同步块继续执行，否则说明多个线程竞争锁。
>
> 若当前只有一个等待线程，则该线程通过自旋进行等待。但是当自旋超过一定的次数，或者一个线程在持有锁，一个在自旋，又有第三个来访时，轻量级锁升级为重量级锁。

JVM层面的锁。内置实现。

- **[重量级锁](#重量级锁-尾)**<a name = "重量级锁-头"></a>

升级为重量级锁时，锁标志的状态值变为“10”，此时Mark Word中存储的是指向重量级锁的指针，此时等待锁的线程都会进入阻塞状态。

整体的锁状态升级流程如下：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/hEx03cFgUsUWxF3IJSFicIicbpueYm7MoKm1LZdLiccu4M4FTLJibfGDCAxcP6C8MlD2g6reTaNKdndbGqfu4tqiafw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

综上，偏向锁通过对比Mark Word解决加锁问题，避免执行CAS操作。而轻量级锁是通过用CAS操作和自旋来解决加锁问题，避免线程阻塞和唤醒而影响性能。重量级锁是将除了拥有锁的线程以外的线程都阻塞。



#####  公平锁、非公平锁<a name ="公平锁、非公平锁-头"></a>

- 公平锁<a name = "公平锁-头"></a>

公平锁是指**多个线程按照申请锁的顺序来获取锁**，线程直接进入队列中排队，队列中的第一个线程才能获得锁。公平锁的优点是等待锁的线程不会饿死。缺点是整体吞吐效率相对非公平锁要低，等待队列中除第一个线程以外的所有线程都会阻塞，CPU唤醒阻塞线程的开销比非公平锁大。

- 非公平锁<a name = "非公平锁-头"></a>

非公平锁是**多个线程加锁时直接尝试获取锁，获取不到才会到等待队列的队尾等待**。但如果此时锁刚好可用，那么这个线程可以无需阻塞直接获取到锁，所以非公平锁有可能出现后申请锁的线程先获取锁的场景。非公平锁的优点是可以减少唤起线程的开销，整体的吞吐效率高，因为线程有几率不阻塞直接获得锁，CPU不必唤醒所有线程。缺点是处于等待队列中的线程可能会饿死，或者等很久才会获得锁。



##### 可重入锁、非可重入锁<a name = "可重入锁、非可重入锁-头"></a>

- [可重入锁](#可重入锁-尾)<a name = "可重入锁-头"></a>

可重入锁又名递归锁，是指在同一个线程在外层方法获取锁的时候，再进入该线程的内层方法会自动获取锁（前提锁对象得是同一个对象或者class），不会因为之前已经获取过还没释放而阻塞。Java中ReentrantLock和synchronized都是可重入锁，可重入锁的一个优点是可一定程度避免死锁。

- [非可重入锁](#非可重入锁-头)<a name ="非可重入锁-头"></a>

如果是一个不可重入锁，那么当前线程在调用doOthers()之前需要将执行doSomething()时获取当前对象的锁释放掉，实际上该对象锁已被当前线程所持有，且无法释放。所以此时会出现死锁。



之前我们说过ReentrantLock和synchronized都是重入锁，那么我们通过重入锁ReentrantLock以及非可重入锁NonReentrantLock的源码来对比分析一下为什么非可重入锁在重复调用同步资源时会出现死锁。

首先ReentrantLock和NonReentrantLock都继承父类AQS，其父类AQS中维护了一个同步状态status来计数重入次数，status初始值为0。

当线程尝试获取锁时，可重入锁先尝试获取并更新status值，如果status == 0表示没有其他线程在执行同步代码，则把status置为1，当前线程开始执行。如果status != 0，则判断当前线程是否是获取到这个锁的线程，如果是的话执行status+1，且当前线程可以再次获取锁。而非可重入锁是直接去获取并尝试更新当前status的值，如果status != 0的话会导致其获取锁失败，当前线程阻塞。

释放锁时，可重入锁同样先获取当前status的值，在当前线程是持有锁的线程的前提下。如果status-1 == 0，则表示当前线程所有重复获取锁的操作都已经执行完毕，然后该线程才会真正释放锁。而非可重入锁则是在确定当前线程是持有锁的线程之后，直接将status置为0，将锁释放。

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aay4Ds7sfFExRdsFAgnIB8CvsE49YfoeytS3hp8JJmuibaDedx85xV0Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

##### [独享锁、共享锁](#独享锁、共享锁-尾)<a name = "独享锁、共享锁-头"></a>

独享锁和共享锁同样是一种概念。

- [独享锁](#独享锁-尾)<a name = "独享锁-头"></a>

独享锁也叫排他锁，是指该锁一次只能被一个线程所持有。如果线程T对数据A加上排它锁后，则其他线程不能再对A加任何类型的锁。获得排它锁的线程即能读数据又能修改数据。JDK中的synchronized和JUC中Lock的实现类就是互斥锁。

- [共享锁](#共享锁-尾)<a name = "共享锁-头"></a>

共享锁是指该锁可被多个线程所持有。如果线程T对数据A加上共享锁后，则其他线程只能对A再加共享锁，不能加排它锁。获得共享锁的线程只能读数据，不能修改数据。



独享锁与共享锁也是通过AQS来实现的，通过实现不同的方法，来实现独享或者共享。

下图为ReentrantReadWriteLock的部分源码：

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aWazYOsalicGsSCfe4Qa6MdWrAr6LRRZERa772UAuFXKiclnt7vXYNSUg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



我们看到ReentrantReadWriteLock有两把锁：ReadLock和WriteLock，由词知意，一个读锁一个写锁，合称“读写锁”。再进一步观察可以发现ReadLock和WriteLock是靠内部类Sync实现的锁。Sync是AQS的一个子类，这种结构在CountDownLatch、ReentrantLock、Semaphore里面也都存在。

在ReentrantReadWriteLock里面，读锁和写锁的锁主体都是Sync，但读锁和写锁的加锁方式不一样。读锁是共享锁，写锁是独享锁。读锁的共享锁可保证并发读非常高效，而读写、写读、写写的过程互斥，因为读锁和写锁是分离的。所以ReentrantReadWriteLock的并发性相比一般的互斥锁有了很大提升。

那读锁和写锁的具体加锁方式有什么区别呢？在了解源码之前我们需要回顾一下其他知识。

在最开始提及AQS的时候我们也提到了state字段（int类型，32位），该字段用来描述有多少线程获持有锁。

在独享锁中这个值通常是0或者1（如果是重入锁的话state值就是重入的次数），在共享锁中state就是持有锁的数量。但是在ReentrantReadWriteLock中有读、写两把锁，所以需要在一个整型变量state上分别描述读锁和写锁的数量（或者也可以叫状态）。于是将state变量“按位切割”切分成了两个部分，高16位表示读锁状态（读锁个数），低16位表示写锁状态（写锁个数）。如下图所示：

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7aUpVCDzUWQMLx2zVYI9ZvibVmRv4r1TYiaHIhAiaJ2fTu3drCEkjUP3KDA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

了解了概念之后我们再来看代码，先看写锁的加锁源码：

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsUWxF3IJSFicIicbpueYm7MoK6c6s9TAnUbp3GVsACzylPEsY9icicf2ibzIkSUnsI4bzNNo45OZzicIVuA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

- 这段代码首先取到当前锁的个数c，然后再通过c来获取写锁的个数w。因为写锁是低16位，所以取低16位的最大值与当前的c做与运算（ int w = exclusiveCount(c); ），高16位和0与运算后是0，剩下的就是低位运算的值，同时也是持有写锁的线程数目。
- 在取到写锁线程的数目后，首先判断是否已经有线程持有了锁。如果已经有线程持有了锁（c!=0），则查看当前写锁线程的数目，如果写线程数为0（即此时存在读锁）或者持有锁的线程不是当前线程就返回失败（涉及到公平锁和非公平锁的实现）。
- 如果写入锁的数量大于最大数（65535，2的16次方-1）就抛出一个Error。
- 如果当且写线程数为0（那么读线程也应该为0，因为上面已经处理c!=0的情况），并且当前线程需要阻塞那么就返回失败；如果通过CAS增加写线程数失败也返回失败。
- 如果c=0，w=0或者c>0，w>0（重入），则设置当前线程或锁的拥有者，返回成功！

tryAcquire()除了重入条件（当前线程为获取了写锁的线程）之外，增加了一个读锁是否存在的判断。如果存在读锁，则写锁不能被获取，原因在于：必须确保写锁的操作对读锁可见，如果允许读锁在已被获取的情况下对写锁的获取，那么正在运行的其他读线程就无法感知到当前写线程的操作。

因此，只有等待其他读线程都释放了读锁，写锁才能被当前线程获取，而写锁一旦被获取，则其他读写线程的后续访问均被阻塞。写锁的释放与ReentrantLock的释放过程基本类似，每次释放均减少写状态，当写状态为0时表示写锁已被释放，然后等待的读写线程才能够继续访问读写锁，同时前次写线程的修改对后续的读写线程可见。

接着是读锁的代码：

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsUWxF3IJSFicIicbpueYm7MoK2gLzj1JdQdicVCqgWFXID0DPnsbgmemdsSJ8OIZVqaYHlYbic0OtTXxg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

可以看到在tryAcquireShared(int unused)方法中，如果其他线程已经获取了写锁，则当前线程获取读锁失败，进入等待状态。如果当前线程获取了写锁或者写锁未被获取，则当前线程（线程安全，依靠CAS保证）增加读状态，成功获取读锁。读锁的每次释放（线程安全的，可能有多个读线程同时释放读锁）均减少读状态，减少的值是“1<<16”。所以读写锁才能实现读读的过程共享，而读写、写读、写写的过程互斥。

此时，我们再回头看一下互斥锁ReentrantLock中公平锁和非公平锁的加锁源码：

![img](https://mmbiz.qpic.cn/mmbiz_png/hEx03cFgUsXibicYtRt824nicRjKGTibicl7akVcxczUO1NOBlSBGYlibr9XZDNRSSaEgdiaj0JLnA7mh71WdLsjalW8w/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



我们发现在ReentrantLock虽然有公平锁和非公平锁两种，但是它们添加的都是独享锁。根据源码所示，当某一个线程调用lock方法获取锁时，如果同步资源没有被其他线程锁住，那么当前线程在使用CAS更新state成功后就会成功抢占该资源。而如果公共资源被占用且不是被当前线程占用，那么就会加锁失败。所以可以确定ReentrantLock无论读操作还是写操作，添加的锁都是都是独享锁。



##### 互斥锁、自旋锁

**`要点`**：

- 互斥锁是一种「独占锁」，线程A加锁成功后不释放，线程B加锁就会失败，线程B释放CPU然后阻塞。
- 自旋锁是通过CPU提供的CAS函数来修改值，失败后不断重试，直至成功。不会主动产生线程上下文切换，所以开销要小一点。



- **互斥锁**加锁失败后，线程会**释放 CPU** ，给其他线程；
- **自旋锁**加锁失败后，线程会**忙等待**，直到它拿到锁；

互斥锁是一种「独占锁」，比如当线程 A 加锁成功后，此时互斥锁已经被线程 A 独占了，只要线程 A 没有释放手中的锁，线程 B 加锁就会失败，于是就会释放 CPU 让给其他线程，**既然线程 B 释放掉了 CPU，自然线程 B 加锁的代码就会被阻塞**。

**对于互斥锁加锁失败而阻塞的现象，是由操作系统内核实现的**。当加锁失败时，内核会将线程置为「睡眠」状态，等到锁被释放后，内核会在合适的时机唤醒线程，当这个线程成功获取到锁后，于是就可以继续执行。



**自旋锁**是通过 CPU 提供的 `CAS` 函数（*Compare And Swap*），在「用户态」完成加锁和解锁操作，不会主动产生线程上下文切换，所以相比互斥锁来说，会快一些，开销也小一些。

一般加锁的过程，包含两个步骤：

- 第一步，查看锁的状态，如果锁是空闲的，则执行第二步；
- 第二步，将锁设置为当前线程持有；

CAS 函数就把这两个步骤合并成一条硬件级指令，形成**原子指令**，这样就保证了这两个步骤是不可分割的，要么一次性执行完两个步骤，要么两个步骤都不执行。

使用自旋锁的时候，当发生多线程竞争锁的情况，加锁失败的线程会「忙等待」，直到它拿到锁。这里的「忙等待」可以用 `while` 循环等待实现，不过最好是使用 CPU 提供的 `PAUSE` 指令来实现「忙等待」，因为可以减少循环等待时的耗电量。

自旋锁是最比较简单的一种锁，一直自旋，利用 CPU 周期，直到锁可用。**需要注意，在单核 CPU 上，需要抢占式的调度器（即不断通过时钟中断一个线程，运行其他线程）。否则，自旋锁在单 CPU 上无法使用，因为一个自旋的线程永远不会放弃 CPU。**

自旋锁开销少，在多核系统下一般不会主动产生线程切换，适合异步、协程等在用户态切换请求的编程方式，但如果被锁住的代码执行时间过长，自旋的线程会长时间占用 CPU 资源，所以自旋的时间和被锁住的代码执行的时间是成「正比」的关系，我们需要清楚的知道这一点。

自旋锁与互斥锁使用层面比较相似，但实现层面上完全不同：**当加锁失败时，互斥锁用「线程切换」来应对，自旋锁则用「忙等待」来应对**。

它俩是锁的最基本处理方式，更高级的锁都会选择其中一个来实现，比如读写锁既可以选择互斥锁实现，也可以基于自旋锁实现。



##### 读写锁

**`要点`**：

当「写锁」没有被线程持有时，多个线程能够并发地持有读锁，一旦「写锁」被线程持有后，读线程的获取读锁的操作会被阻塞，而且其他写线程的获取写锁的操作也会被阻塞。



读写锁从字面意思我们也可以知道，它由「读锁」和「写锁」两部分构成，如果只读取共享资源用「读锁」加锁，如果要修改共享资源则用「写锁」加锁。

所以，**读写锁适用于能明确区分读操作和写操作的场景**。

读写锁的工作原理是：

- 当「写锁」没有被线程持有时，多个线程能够并发地持有读锁，这大大提高了共享资源的访问效率，因为「读锁」是用于读取共享资源的场景，所以多个线程同时持有读锁也不会破坏共享资源的数据。
- 但是，一旦「写锁」被线程持有后，读线程的获取读锁的操作会被阻塞，而且其他写线程的获取写锁的操作也会被阻塞。

所以说，写锁是独占锁，因为任何时刻只能有一个线程持有写锁，类似互斥锁和自旋锁，而读锁是共享锁，因为读锁可以被多个线程同时持有。

知道了读写锁的工作原理后，我们可以发现，**读写锁在读多写少的场景，能发挥出优势**。

另外，根据实现的不同，读写锁可以分为「读优先锁」和「写优先锁」。

读优先锁期望的是，读锁能被更多的线程持有，以便提高读线程的并发性，它的工作方式是：当读线程 A 先持有了读锁，写线程 B 在获取写锁的时候，会被阻塞，并且在阻塞过程中，后续来的读线程 C 仍然可以成功获取读锁，最后直到读线程 A 和 C 释放读锁后，写线程 B 才可以成功获取读锁。如下图：

![img](https://mmbiz.qpic.cn/mmbiz_png/J0g14CUwaZflJahXjfiaG4OvTA9DA2UibzGiaX1mvYx5jzfQaYsG9hYbicIzos7M9SkKz0wWMoxBk9RwyguyWwtricA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

而写优先锁是优先服务写线程，其工作方式是：当读线程 A 先持有了读锁，写线程 B 在获取写锁的时候，会被阻塞，并且在阻塞过程中，后续来的读线程 C 获取读锁时会失败，于是读线程 C  将被阻塞在获取读锁的操作，这样只要读线程 A 释放读锁后，写线程 B 就可以成功获取读锁。如下图：

![img](https://mmbiz.qpic.cn/mmbiz_png/J0g14CUwaZflJahXjfiaG4OvTA9DA2UibzskMiariaXsTzJYibmXK6vGf9fWOlJI6oSaB0ibBIp40Gia5V0VsWclRvttw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

读优先锁对于读线程并发性更好，但也不是没有问题。我们试想一下，如果一直有读线程获取读锁，那么写线程将永远获取不到写锁，这就造成了写线程「饥饿」的现象。

写优先锁可以保证写线程不会饿死，但是如果一直有写线程获取写锁，读线程也会被「饿死」。

既然不管优先读锁还是写锁，对方可能会出现饿死问题，那么我们就不偏袒任何一方，搞个「公平读写锁」。



**死锁**

​		如果一个线程永远不释放另外一个线程需要的资源那么就会导致死锁。这有两种情况：

- 一种情况是线程A永远不释放锁，结果B一直拿不到锁，所以线程B就“死掉”了；
- 第二种情况下，线程A拥有线程B需要的锁Y，同时线程B拥有线程A需要的锁X，那么这时候线程A/B互相依赖对方释放锁，于是二者都“死掉”了。
- 还有一种情况为发生死锁，如果一个线程总是不能被调度，那么等待此线程结果的线程可能就死锁了。这种情况叫做**线程饥饿死锁**。比如说在前面介绍的非公平锁中，如果某些线程非常活跃，在高并发情况下这类线程可能总是拿到锁，那么那些活跃度低的线程可能就一直拿不到锁，这样就发生了“饥饿死”。



**避免死锁的解决方案**

- **尽可能的按照锁的使用规范请求锁，**

- **另外锁的请求粒度要小（不要在不需要锁的地方占用锁，锁不用了尽快释放）；**
- **在高级锁里面总是使用tryLock或者定时机制（这个以后会讲，就是指定获取锁超时的时间，如果时间到了还没有获取到锁那么就放弃）。**高级锁（Lock）里面的这两种方式可以有效的避免死锁。



### **锁优化**

- 减少锁持有时间：减少同步块

- 减小锁粒度: concurrentHashMap

- 锁分离：ReadWriteLock、LinkedBlockingQueue

- 锁粗化：

- 锁消除：

- 无锁：CAS（Compare And Swap）;非阻塞的同步；CAS(V,E,N)



## java.util.concurrent

### 包基本内容

**类图结构：**

![J.U.C](https://img-blog.csdn.net/20170301212847989?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvd2J3ang=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

脑图地址： http://www.xmind.net/m/tJy5，感谢[深入浅出 Java Concurrency ](http://www.blogjava.net/xylz/archive/2010/06/30/324915.html)，此脑图在这篇基础上修改而来。

java.util.concurrent包含了很多内容， 本文将会挑选其中常用的一些类来进行大概的说明：

**locks部分**：显式锁(互斥锁和速写锁)相关；
**atomic部分**：原子变量类相关，是构建非阻塞算法的基础；
**executor部分**：线程池相关；
**collections部分**：并发容器相关；
**tools部分**：同步工具相关，如信号量、闭锁、栅栏等功能；

**包括原子操作、锁机制、并发容器、线程池等内容。**



### **atomic**







### **locks**

-[*Lock*](#Lock-tail)接口<a name = "Lock-head"></a>

├ ——**[ReentrantLock](#ReentrantLock-tail)**<a name = "ReentrantLock-head"></a>

├ ——├ ——ReentrantReadWriteLock.ReadLock

├ ——├ ——ReentrantReadWriteLock.WriteLock

-**[Condition](#Condition-tail)**<a name = "Condition-head"></a>

-[*ReadWriteLock*](#ReadWriteLock-tail)接口<a name = "ReadWriteLock-head"></a>

├ ——[**ReentrantReadWriteLock**](#ReentrantReadWriteLock-tail)<a name = "ReentrantReadWriteLock-head"></a>



- [*Lock*](#Lock-head)接口<a name = "Lock-tail"></a>

```java
void lock();
void lockInterruptibly() throws InterruptedException;
Condition newCondition();
boolean tryLock();
boolean tryLock(long time, TimeUnit unit) throws InterruptedException;
void unlock();
```

Lock的性能比synchronized的要好得多。如果可以的话总是使用Lock替代synchronized是一个明智的选择。



- **[ReentrantLock](#ReentrantLock-head)**<a name = "ReentrantLock-tail"></a>

简单用法

相比于synchronized，ReentrantLock在功能上更加丰富，它具有可重入、可中断、可限时、公平锁等特点。必须在finally中进行解锁操作，如果不在 finally解锁，有可能代码出现异常锁没被释放，而synchronized是由JVM来释放锁。


```java
public class Test implements Runnable
{
	public static ReentrantLock lock = new ReentrantLock();
	public static int i = 0;
	@Override
    public void run()
    {
        for (int j = 0; j < 10000000; j++)
        {
            lock.lock();
            try
            {
                i++;
            }
            finally
            {
                lock.unlock();
            }
        }
}

public static void main(String[] args) throws InterruptedException
{
	Test test = new Test();
	Thread t1 = new Thread(test);
	Thread t2 = new Thread(test);
	t1.start();
	t2.start();
	t1.join();
	t2.join();
	System.out.println(i);
}
}   
```

- **[Condition](#Condition-head)**<a name = "Condition-tail"></a>

Condition一般是配合ReentrantLock使用，类似synchronized与Object.wait()/signal()

​		条件（也称为*条件队列* 或*条件变量*）为线程提供了一个含义，以便在某个状态条件现在可能为 true 的另一个线程通知它之前，一直挂起该线程（即让其“等待”）。因为访问此共享状态信息发生在不同的线程中，所以它必须受保护，因此要将某种形式的锁与该条件相关联。等待提供一个条件的主要属性是：*以原子方式* 释放相关的锁，并挂起当前线程，就像 `Object.wait` 做的那样。

​		上述API说明表明条件变量需要与锁绑定，而且多个Condition需要绑定到同一锁上。前面的**Lock**中提到，获取一个条件变量的方法是**Lock.newCondition()**。

​		每一个**Lock**可以有任意数据的**Condition**对象，**Condition**是与**Lock**绑定的，所以就有**Lock**的公平性特性：如果是公平锁，线程为按照FIFO的顺序从*Condition.await*中释放，如果是非公平锁，那么后续的锁竞争就不保证FIFO顺序了。

**使用方式：**

- **多个Condition需要绑定到同一锁上 Condition condition = lock.newCondition();** 

- **在此之前必须先拿到锁lock.lock()**

- **如果线程拿到锁后没达到自己任务条件如何处理？是等待（自旋挂起，因为下次被唤醒还可能抢到锁，但是仍然不是自己的条件，要继续等待）？在哪个condition上await()阻塞，或者直接lock.unlock()释放锁（一般是与线程自己的任务有关）;**

- **正常情况需要干什么，事情做完之后要唤醒signal()哪种Condition（也就是之后的任务）**

- **任务执行完释放锁，这样在Condition上await的线程才能拿到锁。**

  

```java
private Condition condition = lock.newCondition(); 
try{
    lock.lock();
    condition.await();//释放lock锁并在这里阻塞
}
finally lock.unlock();
-------------------------
lock.lock();
condition.signal();
lock.unlock();
//condition.await()/signal只能在得到锁以后使用。
```

```java
public void run() {
    for (int i = 0; i < 10; ) {
        try {
            lock.lock();
            while (state % 3 != num) {
                self.await();
            }
            System.out.print(letter);
            next.signal();
            state++;
            i++;
        } catch (InterruptedException e) {
            e.printStackTrace();
        } finally {
            lock.unlock();
        }
    }
```



- [*ReadWriteLock*](#ReadWriteLock-head)<a name = "ReadWriteLock-tail"></a>

ReentrantLock  实现了标准的互斥操作，也就是一次只能有一个线程持有锁，也即所谓独占锁的概念。前面的章节中一直在强调这个特点。显然这个特点在一定程度上面减低了吞吐量，实际上独占锁是一种保守的锁策略，在这种情况下任何“读/读”，“写/读”，“写/写”操作都不能同时发生。但是同样需要强调的一个概念是，锁是有一定的开销的，当并发比较大的时候，锁的开销就比较客观了。所以如果可能的话就尽量少用锁，非要用锁的话就尝试看能否改造为读写锁。

*ReadWriteLock 接口*

> public interface ReadWriteLock {
> Lock readLock();
> Lock writeLock();
> }

ReadWriteLock描述的是：**一个资源能够被多个读线程访问，或者被一个写线程访问，但是不能同时存在读写线程。**也就是说读写锁使用的场合是一个共享资源被大量读取操作，而只有少量的写操作（修改数据）。

ReadWriteLock是区分功能的锁。读和写是两种不同的功能，读-读不互斥，读-写互斥，写-写互斥。

在ReadWriteLock中每次读取共享数据就需要读取锁，当需要修改共享数据时就需要写入锁。看起来好像是两个锁，但其实不尽然，在下一节中的分析中会解释这点奥秘。

使用方式：

```java
private static ReentrantReadWriteLock readWriteLock=new ReentrantReadWriteLock(); 
private static Lock readLock = readWriteLock.readLock(); 
private static Lock writeLock = readWriteLock.writeLock();
```

ReadWriteLock需要严格区分读写操作，如果读操作使用了写入锁，那么降低读操作的吞吐量，如果写操作使用了读取锁，那么就可能发生数据错误。

```java
	final ReadWriteLock lock = new ReentrantReadWriteLock();
    final Lock r = lock.readLock();
    final Lock w = lock.writeLock(); 

	public V put(K key, V value) {
     w.lock();
     try {
       return map.put(key, value);
     } finally {
       w.unlock();
     }
   }

    public V get(Object key) {
        r.lock();
        try {
            return map.get(key);
        } finally {
            r.unlock();
        }
    } 
```



- [**ReentrantReadWriteLock**](#ReentrantReadWriteLock-head)<a name = "ReentrantReadWriteLock-tail"></a>

​		上一节中提到，ReadWriteLock看起来有两个锁：readLock/writeLock。如果真的是两个锁的话，它们之间又是如何相互影响的呢？

​		事实上在ReentrantReadWriteLock里锁的实现是靠java.util.concurrent.locks.ReentrantReadWriteLock.Sync完成的。这个类看起来比较眼熟，实际上它是AQS的一个子类，这中类似的结构在CountDownLatch、ReentrantLock、Semaphore里面都存在。同样它也有两种实现：公平锁和非公平锁，也就是java.util.concurrent.locks.ReentrantReadWriteLock.FairSync和java.util.concurrent.locks.ReentrantReadWriteLock.NonfairSync。

​		在ReentrantReadWriteLock里面的锁主体就是一个Sync，也就是上面提到的FairSync或者NonfairSync，所以说**实际上只有一个锁，只是在获取读取锁和写入锁的方式上不一样**，所以前面才有读写锁是独占锁的两个不同视图一说。

​		ReentrantReadWriteLock里面有两个类：ReadLock/WriteLock，这两个类都是Lock的实现。

- 线程进入读锁的前提条件：
  - 没有其他线程的写锁，
  - 没有写请求或者有写请求，但调用线程和持有锁的线程是同一个。

- 线程进入写锁的前提条件：
  - 没有其他线程的读锁
  - 没有其他线程的写锁

ReadWriteLock需要严格区分读写操作，如果读操作使用了写入锁，那么降低读操作的吞吐量，如果写操作使用了读取锁，那么就可能发生数据错误。

另外ReentrantReadWriteLock还有以下几个特性：

- 公平性
  - 非公平锁（默认） 这个和独占锁的非公平性一样，由于读线程之间没有锁竞争，所以读操作没有公平性和非公平性，写操作时，由于写操作可能立即获取到锁，所以会推迟一个或多个读操作或者写操作。因此非公平锁的吞吐量要高于公平锁。  
  - 公平锁  利用AQS的CLH队列，释放当前保持的锁（读锁或者写锁）时，优先为等待时间最长的那个写线程分配写入锁，当前前提是写线程的等待时间要比所有读线程的等待时间要长。同样一个线程持有写入锁或者有一个写线程已经在等待了，那么试图获取公平锁的（非重入）所有线程（包括读写线程）都将被阻塞，直到最先的写线程释放锁。如果读线程的等待时间比写线程的等待时间还有长，那么一旦上一个写线程释放锁，这一组读线程将获取锁。
- 重入性
  - 读写锁允许读线程和写线程按照请求锁的顺序重新获取读取锁或者写入锁。当然了只有写线程释放了锁，读线程才能获取重入锁。  
  - 写线程获取写入锁后可以再次获取读取锁，但是读线程获取读取锁后却不能获取写入锁。  
  - 另外读写锁最多支持65535个递归写入锁和65535个递归读取锁。
- 锁降级
  - 写线程获取写入锁后可以获取读取锁，然后释放写入锁，这样就从写入锁变成了读取锁，从而实现锁降级的特性。
- 锁升级    
  - 读取锁是不能直接升级为写入锁的。因为获取一个写入锁需要释放所有读取锁，所以如果有两个读取锁视图获取写入锁而都不释放读取锁时就会发生死锁。
- 锁获取中断
  - 读取锁和写入锁都支持获取锁期间被中断。这个和独占锁一致。
- 条件变量
  - 写入锁提供了条件变量(Condition)的支持，这个和独占锁一致，但是读取锁却不允许获取条件变量，将得到一个`UnsupportedOperationException`异常。
- 重入数
  - 读取锁和写入锁的数量最大分别只能是65535（包括重入数）。这在下节中有介绍。

**基本使用**

使用很简单，那就是在写方法和读方法分开使用两把锁。

```java
public class ReadAndWriteLockTest {
    ReadWriteLock readAndWriteLock = new ReentrantReadWriteLock(true);
    private final static Lock readLock = readAndWriteLock.readLock();
    private final static Lock writeLock = readAndWriteLock.writeLock();
    private final static List<String> data = new ArrayList<>();
    
    public static void main(String[] args) {
        new Thread(()->write()).start();
         new Thread(()->read()).start();
    }
    
    public static void write() {
        try{
            writeLock.lock();
        	data.add("写数据");
        } finally {
            writeLock.unlock();
        } 
    }
    
    public static void read() {
        try{
            readLock.lock();
        	System.out.print(Arrays.asList(data));
        } finally {
            readLock.unlock();
        }
    } 
}
```















excutors

[*-Executor*](#Executor-tail)<a name = "Executor-head"></a>接口的接口 对象的集合（单列集合） 
├ ——[*-ExecutorService*](#ExecutorService-tail)<a name = "ExecutorService-head"></a>接口：元素按进入先后有序保存，可重复 
├ ——├ —— [**ScheduledExecutorService**](#ScheduledExecutorService)  线程不安全 
├ ——├ —— [**ScheduledThreadPoolExecutor**](#ScheduledExecutorService)
├ ——├ ——├ —— AbstractExecutorService
├ ——├ ——├ —— **[ThreadPoolExecutor](#ThreadPoolExecutor-tail)**<a name ="ThreadPoolExecutor-head"></a>

├ ——├ ——├ —— ForkJoinPool

-[*Future*](#Future)

├ ——*RunnableFure*
├ ——├ ——RunnableScheduledFuture
├ ——├ ——FutureTask 

├ ——ScheduledFuture

├ ——ForkJoinTash



[*Executor*](#Executor-head)<a name = "Executor-tail"></a>

Executor的execute方法只是执行一个Runnable的任务，当然了从某种角度上将最后的实现类也是在线程中启动此任务的。根据线程池的执行策略最后这个任务可能在新的线程中执行，或者线程池中的某个线程，甚至是调用者线程中执行（相当于直接运行Runnable的run方法）。

[*ExecutorService*](#ExecutorService-head)<a name = "ExecutorService-tail"></a>

ExecutorService在Executor的基础上增加了一些方法，其中有两个核心的方法：

- Future<?> submit(Runnable task)  
- <T> Future<T> submit(Callable<T> task) 

​		它们的区别在于Runnable在执行完毕后没有结果，Callable执行完毕后有一个结果。这在多个线程中传递状态和结果是非常有用的。另外他们的相同点在于都返回一个Future对象。Future对象可以阻塞线程直到运行完毕（获取结果，如果有的话），也可以取消任务执行，当然也能够检测任务是否被取消或者是否执行完毕。

​		在没有Future之前我们检测一个线程是否执行完毕通常使用Thread.join()或者用一个死循环加状态位来描述线程执行完毕。现在有了更好的方法能够阻塞线程，检测任务执行完毕甚至取消执行中或者未开始执行的任务。





##### **[ThreadPoolExecutor](#ThreadPoolExecutor-head)**<a name ="ThreadPoolExecutor-tail"></a>

使用最多的构造方法

```java
public ThreadPoolExecutor(int corePoolSize, // 1
                              int maximumPoolSize,  // 2
                              long keepAliveTime,  // 3
                              TimeUnit unit,  // 4
                              BlockingQueue<Runnable> workQueue, // 5
                              ThreadFactory threadFactory,  // 6
                              RejectedExecutionHandler handler )
```

| 序号 | 名称            | 类型                     | 含义                                                         |
| ---- | --------------- | ------------------------ | ------------------------------------------------------------ |
| 1    | corePoolSize    | int                      | 线程池核心数量。*它的数量决定了添加的任务是开辟新的线程去执行，还是放到workQueue任务队列中去；* |
| 2    | maximumPoolSize | int                      | 线程池中线程最大数量。*这个参数会根据你使用的workQueue任务队列的类型，决定线程池会开辟的最大线程数量；* |
| 3    | keepAliveTime   | long                     | 线程最大空闲时间。*当线程池中**空闲线程**数量超过corePoolSize时，多余的线程会在多长时间内被销毁；* |
| 4    | unit            | TimeUnit                 | 时间单位                                                     |
| 5    | workQueue       | BlockingQueue<Runnable>  | 线程等待队列。*任务队列，被添加到线程池中，但尚未被执行的任务；* |
| 6    | threadFactory   | ThreadFactory            | 线程创建工厂。*用于创建线程，一般用默认即可；*               |
| 7    | handler         | RejectedExecutionHandler | 拒绝策略。*当任务太多来不及处理时，如何拒绝任务；*           |

###### **workQueue任务队列**

它一般分为直接提交队列、有界任务队列、无界任务队列、优先任务队列；

- **SynchronousQueue直接提交队列** 

​		SynchronousQueue是一个特殊的BlockingQueue，它没有容量，没执行一个插入操作就会阻塞，需要再执行一个删除操作才会被唤醒，反之每一个删除操作也都要等待对应的插入操作。

​		当任务队列为SynchronousQueue，创建的线程数大于maximumPoolSize时，直接执行了拒绝策略抛出异常。

​		使用SynchronousQueue队列，提交的任务不会被保存，总是会马上提交执行。如果用于执行任务的线程数量小于maximumPoolSize，则尝试创建新的进程，如果达到maximumPoolSize设置的最大值，则根据你设置的handler执行拒绝策略。因此这种方式你提交的任务不会被缓存起来，而是会被马上执行，在这种情况下，你需要对你程序的并发量有个准确的评估，才能设置合适的maximumPoolSize数量，否则很容易就会执行拒绝策略；

- **ArrayBlockingQueue有界的任务队列**

```java
pool = new ThreadPoolExecutor(1, 2, 1000, TimeUnit.MILLISECONDS, new ArrayBlockingQueue<Runnable>(10),Executors.defaultThreadFactory(),new ThreadPoolExecutor.AbortPolicy());
```

​		使用ArrayBlockingQueue有界任务队列，若有新的任务需要执行时，线程池会创建新的线程，直到创建的线程数量达到corePoolSize时，则会将新的任务加入到等待队列中。若等待队列已满，即超过ArrayBlockingQueue初始化的容量，则继续创建线程，直到线程数量达到maximumPoolSize设置的最大线程数量，若大于maximumPoolSize，则执行拒绝策略。在这种情况下，线程数量的上限与有界任务队列的状态有直接关系，如果有界队列初始容量较大或者没有达到超负荷的状态，线程数将一直维持在corePoolSize以下，反之当任务队列已满时，则会以maximumPoolSize为最大线程数上限。

- **LinkedBlockingQueue无界的任务队列**

```java
pool = new ThreadPoolExecutor(1, 2, 1000, TimeUnit.MILLISECONDS, new LinkedBlockingQueue<Runnable>(),Executors.defaultThreadFactory(),new ThreadPoolExecutor.AbortPolicy());
```

​		使用无界任务队列，线程池的任务队列可以无限制的添加新的任务，而线程池创建的最大线程数量就是你corePoolSize设置的数量，也就是说在这种情况下maximumPoolSize这个参数是无效的，哪怕你的任务队列中缓存了很多未执行的任务，当线程池的线程数达到corePoolSize后，就不会再增加了；若后续有新的任务加入，则直接进入队列等待，当使用这种任务队列模式时，一定要注意你任务提交与处理之间的协调与控制，不然会出现队列中的任务由于无法及时处理导致一直增长，直到最后资源耗尽的问题。

- **PriorityBlockingQueue优先任务队列**

​		PriorityBlockingQueue它其实是一个特殊的无界队列，它其中无论添加了多少个任务，线程池创建的线程数也不会超过corePoolSize的数量，只不过其他队列一般是按照先进先出的规则处理任务，而PriorityBlockingQueue队列可以自定义规则根据任务的优先级顺序先后执行。

```
pool = new ThreadPoolExecutor(1, 2, 1000, TimeUnit.MILLISECONDS, new PriorityBlockingQueue<Runnable>(),Executors.defaultThreadFactory(),new ThreadPoolExecutor.AbortPolicy());
for(int i=0;i<20;i++) {
            pool.execute(new ThreadTask(i));
        } 
---------------------------------------------------        
public class ThreadTask implements Runnable,Comparable<ThreadTask>{
        public ThreadTask(int priority) {
                this.priority = priority;
            }
        //当前对象和其他对象做比较，当前优先级大就返回-1，优先级小就返回1,值越小优先级越高
        public int compareTo(ThreadTask o) {
             return  this.priority>o.priority?-1:1;
        }    
}
```



###### RejectedExecutionHandler拒绝策略

​		一般我们创建线程池时，为防止资源被耗尽，任务队列都会选择创建有界任务队列，但种模式下如果出现任务队列已满且线程池创建的线程数达到你设置的最大线程数时，这时就需要你指定ThreadPoolExecutor的RejectedExecutionHandler参数即合理的拒绝策略，来处理线程池"超载"的情况。ThreadPoolExecutor自带的拒绝策略如下：

- **AbortPolicy**策略：该策略会直接抛出异常，阻止系统正常工作；

- **CallerRunsPolicy**策略：如果线程池的线程数量达到上限，该策略会把任务队列中的任务放在调用者线程当中运行；
- **DiscardOledestPolicy**策略：该策略会丢弃任务队列中最老的一个任务，也就是当前任务队列中最先被添加进去的，马上要被执行的那个任务，并尝试再次提交；
- **DiscardPolicy**策略：该策略会默默丢弃无法处理的任务，不予任何处理。当然使用此策略，业务场景中需允许任务的丢失；

以上内置的策略均实现了*RejectedExecutionHandler*接口，当然你也可以自己扩展RejectedExecutionHandler接口，定义自己的拒绝策略。



###### 预定义线程池

知道了各个参数的作用后，我们开始构造符合我们期待的线程池。首先看JDK给我们预定义的几种线程池：

**FixedThreadPool**

```java
public static ExecutorService newFixedThreadPool(int nThreads) {
        return new ThreadPoolExecutor(nThreads, nThreads,
                                      0L, TimeUnit.MILLISECONDS,
                                      new LinkedBlockingQueue<Runnable>());
    }
```

> - corePoolSize与maximumPoolSize相等，即其线程全为核心线程，是一个固定大小的线程池，是其优势；
> - keepAliveTime = 0 该参数默认对核心线程无效，而FixedThreadPool全部为核心线程；
> - workQueue 为LinkedBlockingQueue（无界阻塞队列），队列最大值为Integer.MAX_VALUE。如果任务提交速度持续大余任务处理速度，会造成队列大量阻塞。因为队列很大，很有可能在拒绝策略前，内存溢出。是其劣势；
> - FixedThreadPool的任务执行是无序的；

适用场景：可用于Web服务瞬时削峰，但需注意长时间持续高峰情况造成的队列阻塞。



**CachedThreadPool**

```java
    public static ExecutorService newCachedThreadPool() {
        return new ThreadPoolExecutor(0, Integer.MAX_VALUE,
                                      60L, TimeUnit.SECONDS,
                                      new SynchronousQueue<Runnable>());
    }
```

> - corePoolSize = 0，maximumPoolSize = Integer.MAX_VALUE，即线程数量几乎无限制；
> - keepAliveTime = 60s，线程空闲60s后自动结束。
> - workQueue 为 SynchronousQueue 同步队列，这个队列类似于一个接力棒，入队出队必须同时传递，因为CachedThreadPool线程创建无限制，不会有队列等待，所以使用SynchronousQueue；

适用场景：快速处理大量耗时较短的任务，如Netty的NIO接受请求时，可使用CachedThreadPool。

**SingleThreadExecutor**

```java
public static ExecutorService newSingleThreadExecutor() {
        return new FinalizableDelegatedExecutorService
            (new ThreadPoolExecutor(1, 1,
                                    0L, TimeUnit.MILLISECONDS,
                                    new LinkedBlockingQueue<Runnable>()));
    }
```

**ScheduledThreadPool**

```java
 public static ScheduledExecutorService newScheduledThreadPool(int corePoolSize) {
        return new ScheduledThreadPoolExecutor(corePoolSize);
    }
```

newScheduledThreadPool调用的是ScheduledThreadPoolExecutor的构造方法，而ScheduledThreadPoolExecutor继承了ThreadPoolExecutor，构造是还是调用了其父类的构造方法。

```java
    public ScheduledThreadPoolExecutor(int corePoolSize) {
        super(corePoolSize, Integer.MAX_VALUE, 0, NANOSECONDS,
              new DelayedWorkQueue());
    }
```





### **collections**

*-Queue*

├ ——ConcurrentLinkedQueue

├ ——*[BlockingQueue](#BlockingQueue)* 接口。有限的 阻塞队列。为空或者满都会阻塞。
├ ——├ ——ArrayBlockingQueue 有界数组阻塞队列。内部实现是将对象放入到一个数组里。一旦初始化，大小无法修改。

├ ——├ ——LinkedBlockingQueue 有界链阻塞队列。

├ ——├ ——PriorityBlockingQueue 无界的并发队列。

├ ——├ ——SynchronousQueue一个特殊队列。他的内部同时只能够容乃单个元素，否则阻塞。

├ ——├ ——DelayQueue 延迟队列

├ ——├ ——TransferQueue

├ ——├ ——├ ——LinkedTransferQueue

├ ——Deque

├ ——├ ——ArrayDeque

├ ——├ ——LinkedList

├ ——├ ——BlockingDeque
├ ——├ ——├ ——LinkedBlockingDeque

**-CopyOnWriteArrayList**

**-CopyOnWriteArraySet**

-ConcurrentSkipListSet 

-[*ConcurrentMap*](#ConcurrentMap-tail)<a name = "ConcurrentMap-head"></a> 一个能够对别人的访问进行并发处理的java.util.Map接口。

├ ——**[ConcurrentHashMap](#ConcurrentHashMap-tail)**<a name = "ConcurrentHashMap-head"></a>是HashMap的线程安全版本

├ ——ConcurrentNavigableMap

├ ——├ ——ConcurrentSkipListMap 是TreeMap的线程安全版本





- *BlockingQueue*<a name = "BlockingQueue"></a>

- [*ConcurrentMap*](#ConcurrentMap-tail)<a name = "ConcurrentMap-head"></a>

除了实现Map接口里面对象的方法外，ConcurrentHashMap还实现了ConcurrentMap里面的四个方法。

```java
V putIfAbsent(K key,V value)
boolean remove(Object key,Object value)
boolean replace(K key,V oldValue,V newValue)
V replace(K key,V value)
```



- **[ConcurrentHashMap](#ConcurrentHashMap-head)**<a name = "ConcurrentHashMap-tail"></a>

​		在[读写锁章节部分](http://www.blogjava.net/xylz/archive/2010/07/14/326080.html)介绍过一种是用读写锁实现Map的方法。此种方法看起来可以实现Map响应的功能，而且吞吐量也应该不错。但是通过前面对[读写锁原理](http://www.blogjava.net/xylz/archive/2010/07/15/326152.html)的分析后知道，读写锁的适合场景是读操作>>写操作，也就是读操作应该占据大部分操作，另外读写锁存在一个很严重的问题是读写操作不能同时发生。要想解决读写同时进行问题（至少不同元素的读写分离），那么就只能将锁拆分，不同的元素拥有不同的锁，这种技术就是“锁分离”技术。

​		默认情况下**ConcurrentHashMap是用了16个类似HashMap  的结构，其中每一个HashMap拥有一个独占锁。**也就是说最终的效果**就是通过某种Hash算法，将任何一个元素均匀的映射到某个HashMap的Map.Entry上面，而对某个一个元素的操作就集中在其分布的HashMap上，与其它HashMap无关。这样就支持最多16个并发的写操作。**

![image](http://www.blogjava.net/images/blogjava_net/xylz/WindowsLiveWriter/JavaConcurrency18part3ConcurrentMap3_693/image_thumb_3.png)

​		在ConcurrentHashMap中是通过hash(key.hashCode())和segmentFor(hash)来得到Segment的。这里和HashMap还是有点不同的，这里采用的算法叫Wang/Jenkins hash。**总之它的目的就是使元素能够均匀的分布在不同的Segment上，这样才能够支持最多segmentMask+1个并发，这里segmentMask+1是segments的大小**。

​		显然在不能够对Segment扩容的情况下，segments的大小就应该是固定的。所以在ConcurrentHashMap中segments/segmentMask/segmentShift都是常量，一旦初始化后就不能被再次修改，其中segmentShift是查找Segment的一个常量偏移量。

​		有了Segment以后再定位HashEntry就和HashMap中定位HashEntry一样了，先将hash值与Segment中HashEntry的大小减1进行与操作定位到HashEntry链表，然后遍历链表就可以完成相应的操作了。

​		能够定位元素以后ConcurrentHashMap就已经具有了HashMap的功能了，现在要解决的就是如何并发的问题。要解决并发问题，加锁是必不可免的。再回头看Segment的类图，可以看到Segment除了有一个volatile类型的元素大小count外，Segment还是集成自ReentrantLock的。另外在前面的原子操作和锁机制中介绍过，要想最大限度的支持并发，那么能够利用的思路就是尽量读操作不加锁，写操作不加锁。如果是读操作不加锁，写操作加锁，对于竞争资源来说就需要定义为[volatile](http://www.blogjava.net/xylz/archive/2010/07/03/325168.html)类型的。[volatile](http://www.blogjava.net/xylz/archive/2010/07/03/325168.html)类型能够保证[happens-before法则](http://www.blogjava.net/xylz/archive/2010/07/03/325168.html)，所以volatile能够近似保证正确性的情况下最大程度的降低加锁带来的影响，同时还与写操作的锁不产生冲突。

​		同时为了防止在遍历HashEntry的时候被破坏，那么对于HashEntry的数据结构来说，除了value之外其他属性就应该是常量，否则不可避免的会得到ConcurrentModificationException。这就是为什么HashEntry数据结构中key,hash,next是常量的原因(final类型）。

​		有了上面的分析和条件后再来看Segment的get/put/remove就容易多了。



**CopyOnWriteArrayList/CopyOnWriteArraySet**

Copy-On-Write容器即写时复制的容器。通俗的理解是当我们往一个容器添加元素的时候，不直接往当前容器添加，而是先将当前容器进行Copy，复制出一个新的容器，然后新的容器里添加元素，添加完元素之后，再将原容器的引用指向新的容器。





### **tools**

[-**CountDownLatch**](#CountDownLatch-tail)<a name = "CountDownLatch-head"></a> 
[-**CyclicBarrier**](#CyclicBarrier-tail)<a name = "CyclicBarrier-head"></a>
[-**Semaphore**](#Semaphore-tail)<a name ="Semaphore-head"></a>
-[**Executors**](#Executors-tail)<a name = "Executors-head"></a>
-[Exchanger](#Exchanger-tail)<a name = "Exchanger-head"></a>





#### [**CountDownLatch**](#CountDownLatch-head)<a name = "CountDownLatch-tail"></a>

​		闭锁的一个实现，允许一个或者多个线程等待某个事件的发生。其实很简单，就是一个倒计时器。是一个非常实用的多线程控制工具类。

​		CountDownLatch有一个正数计数器，**countDown方法对计数器做减操作，await方法等待计数器达到0。所有await的线程都会阻塞直到计数器为0或者等待线程中断或者超时。**

**使用方式：**

​		**一般使用就是维护2个CountDownLatch。Task任务wait主线程main latch的countdown到0，后被唤醒并执行，执行完后countdown Task的latch。主线程wait等待Task的latch到0后才被唤醒继续执行。**

​		注意使用时要业务上主动拆分任务。

​		所谓共享锁是说所有共享锁的线程共享同一个资源，一旦任意一个线程拿到共享资源，那么所有线程就都拥有的同一份资源。也就是通常情况下共享锁只是一个标志，所有线程都等待这个标识是否满足，一旦满足所有线程都被激活（相当于所有线程都拿到锁一样）。这里的闭锁**CountDownLatch**就是基于共享锁的实现。

**CountDownLatch**的API如下。

```java
public void await() throws InterruptedException  
public boolean await(long timeout, TimeUnit unit) throws InterruptedException  
public void countDown()  
public long getCount()
```

常用的就下面几个方法：

```java
//实例化一个倒计数器，count指定计数个数
CountDownLatch(int count) 
//计数器传入task中，countDownLatch.await()方法，等主信号发布（即count值为0）
countDownLatch.await()
//任务完成，计数减一
countDown() 
//主线程等待，当计数减到0时，所有线程并行执行
await() 
// 调用await()方法的线程会被挂起，它会等待直到count值为0才继续执行
```

调用await()的线程会被挂起，如果初始为3，那么会等countDown3次才会唤醒。

```java
public class TestCountDownLatch {

    private static final int N = 10;

    public static void main(String[] args) throws InterruptedException {
        CountDownLatch doneSignal = new CountDownLatch(N);
        CountDownLatch startSignal = new CountDownLatch(1);//开始执行信号

        for (int i = 1; i <= N; i++) {
            new Thread(new Worker(i, doneSignal, startSignal)).start();//线程启动了
        }
        System.out.println("begin------------");
        startSignal.countDown();//开始执行啦
        doneSignal.await();//等待所有的线程执行完毕
        System.out.println("Ok");

    }

    static class Worker implements Runnable {

        private final CountDownLatch doneSignal;
        private final CountDownLatch startSignal;
        private int beginIndex;


        public Worker(int beginIndex, CountDownLatch doneSignal, CountDownLatch startSignal) {
            this.doneSignal = doneSignal;
            this.startSignal = startSignal;
            this.beginIndex = beginIndex;
        }

        @Override
        public void run() {
            try {
                startSignal.await();//等待开始执行信号的发布
                beginIndex = (beginIndex - 1) * 10 + 1;
                for (int i = beginIndex; i <= beginIndex + 10; i++) {
                    System.out.println(i);
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            } finally {
                doneSignal.countDown();
            }
        }
    }
}
```



#### [**CyclicBarrier**](#CyclicBarrier-head)<a name = "CyclicBarrier-tail"></a>

如果说[CountDownLatch](http://www.blogjava.net/xylz/archive/2010/07/09/325612.html)是一次性的，那么**CyclicBarrier**循环栅栏正好可以循环使用。它允许一组线程互相等待，直到到达某个公共屏障点 (common barrier point)。所谓屏障点就是一组任务执行完毕的时刻。

什么叫循环利用？看下面

**构造方法**

```java
public CyclicBarrier(int parties)
public CyclicBarrier(int parties, Runnable barrierAction)
```

- parties 是参与线程的个数
- 第二个构造方法有一个 Runnable 参数，这个参数的意思是最后一个到达线程要做的任务

**重要方法**

```java
public int await() throws InterruptedException, BrokenBarrierException
public int await(long timeout, TimeUnit unit) throws InterruptedException, BrokenBarrierException, TimeoutException
```

- 线程调用 await() 表示自己已经到达栅栏，等待其他线程到达
- BrokenBarrierException 表示栅栏已经被破坏，破坏的原因可能是其中一个线程 await() 时被中断或者超时

```java
public class CyclicBarrierDemo {

    static class TaskThread extends Thread {
        CyclicBarrier barrier;
        public TaskThread(CyclicBarrier barrier) {
            this.barrier = barrier;
        }
        
        @Override
        public void run() {
            try {
                Thread.sleep(1000);
                System.out.println(getName() + " 到达栅栏 A");
                barrier.await();
                System.out.println(getName() + " 冲破栅栏 A"); 
                Thread.sleep(2000);
                System.out.println(getName() + " 到达栅栏 B");
                barrier.await();
                System.out.println(getName() + " 冲破栅栏 B");
            } catch (Exception e) {
                e.printStackTrace();
            }
        }
    }
    
    public static void main(String[] args) {
        int threadNum = 5;
        CyclicBarrier barrier = new CyclicBarrier(threadNum, new Runnable() {
            @Override
            public void run() {
                System.out.println(Thread.currentThread().getName() + " 完成最后任务");
            }
        });
        for(int i = 0; i < threadNum; i++) {
            new TaskThread(barrier).start();
        }
    }
    
}
```

打印结果：

```java
Thread-1 到达栅栏 A
Thread-3 到达栅栏 A
Thread-0 到达栅栏 A
Thread-4 到达栅栏 A
Thread-2 到达栅栏 A
Thread-2 完成最后任务
Thread-2 冲破栅栏 A
Thread-1 冲破栅栏 A
Thread-3 冲破栅栏 A
Thread-4 冲破栅栏 A
Thread-0 冲破栅栏 A
Thread-4 到达栅栏 B
Thread-0 到达栅栏 B
Thread-3 到达栅栏 B
Thread-2 到达栅栏 B
Thread-1 到达栅栏 B
Thread-1 完成最后任务
Thread-1 冲破栅栏 B
Thread-0 冲破栅栏 B
Thread-4 冲破栅栏 B
Thread-2 冲破栅栏 B
Thread-3 冲破栅栏 B
```

**也就是说，所有先到栅栏barrier.wait()的线程都会等待，直到最一个到达后才会继续执行，继续到达下一个栅栏（如果有），而且最后到达的线程会执行栅栏中的Runnable的任务**



#### [Semaphore](#Semaphore-head)<a name = "Semaphore-tail"></a>

Semaphore 是一个计数信号量。必须由获取它的线程释放。常用于限制可以访问某些资源的线程数量，例如通过 Semaphore 限流。

说白了，Semaphore是一个计数器，在计数器不为0的时候对线程就放行，一旦达到0，那么所有请求资源的新线程都会被阻塞，包括增加请求到许可的线程，也就是说Semaphore不是可重入的。每一次请求一个许可都会导致计数器减少1，同样每次释放一个许可都会导致计数器增加1，一旦达到了0，新的许可请求线程将被挂起。

缓存池正好使用此思想来实现的，比如链接池、对象池等。

Semaphore 只有3个操作：

1. 初始化Semaphore semaphore = new Semaphore(3);
2. void acquire()`:从此信号量获取一个许可，在提供一个许可前一直将线程阻塞，否则线程被中断。`
3. void release():释放一个许可，将其返回给信号量。

```java
public class StudySemaphore {

    public static void main(String[] args) {
        ExecutorService executorService = Executors.newCachedThreadPool();
        
        //信号量，只允许 3个线程同时访问
        Semaphore semaphore = new Semaphore(3);

        for (int i=0;i<10;i++){
            final long num = i;
            executorService.submit(new Runnable() {
                @Override
                public void run() {
                    try {
                        //获取许可
                        semaphore.acquire();
                        //执行
                        System.out.println("Accessing: " + num);
                        Thread.sleep(new Random().nextInt(5000)); // 模拟随机执行时长
                        //释放
                        semaphore.release();
                        System.out.println("Release..." + num);
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            });
        }

        executorService.shutdown();
    }

}
```

输出：

```
Accessing: 0
Accessing: 1
Accessing: 2
Release...1
Accessing: 3
Release...2
Accessing: 4
Release...0
Accessing: 5
Release...3
Accessing: 6
Accessing: 7
Release...4
Accessing: 8
Release...6
Release...5
Accessing: 9
Release...8
Release...7
Release...9
```



**总结**

1. CountDownLatch 是一个线程等待其他线程， CyclicBarrier 是多个线程互相等待。
2. CountDownLatch 的计数是减 1 直到 0，CyclicBarrier 是加 1，直到指定值。
3. CountDownLatch 是一次性的， CyclicBarrier  可以循环利用。
4. CyclicBarrier 可以在最后一个线程达到屏障之前，选择先执行一个操作。
5. Semaphore ，需要拿到许可才能执行，并可以选择公平和非公平模式。



参考：

1. [终于有人把 CountDownLatch，CyclicBarrier，Semaphore 说明白了!](https://mp.weixin.qq.com/s/TDw7GnzDw5FK3RWwkIzzZA)



### 多线程使用示例

#### **[实现ABC交叉打印](https://blog.csdn.net/xiaokang123456kao/article/details/77331878)**

##### Synchronized同步法

可以看到程序一共定义了a,b,c三个对象锁，分别对应A、B、C三个线程。A线程最先运行，A线程按顺序申请c,a对象锁，打印操作后按顺序释放a,c对象锁，并且通过notify操作唤醒线程B。线程B首先等待获取A锁，再申请B锁，后打印B，再释放B，A锁，唤醒C。线程C等待B锁，再申请C锁，后打印C，再释放C,B锁，唤醒A。看起来似乎没什么问题，但如果你仔细想一下，就会发现有问题，就是初始条件，三个线程必须按照A,B,C的顺序来启动，但是这种假设依赖于JVM中线程调度、执行的顺序。

**wait(),notify(),Thread.sleep()**

```java
public class ThreadTask implements Runnable {
        public String name;
        public Object pre;
        public Object self;

        public ThreadTask(String name, Object pre, Object self) {
            this.name = name;
            this.pre = pre;
            this.self = self;
        }

        public static int count = 10;

        @Override
        public void run() {
            while (count > 0) {
                synchronized (pre) {
                    synchronized (self) {
                        System.out.print(name);
                        count --;
                        self.notify();
                    }
                    // 确保后面第一个线程拿到此锁，避免pre.wait()之后后面第二个线程拿到此锁导致顺序错误
//                    try {
//                        Thread.sleep(
//                                1000
//                        );
//                    } catch (InterruptedException e) {
//                        e.printStackTrace();
//                    }
                    try {
                        if (count == 0) {// 如果count==0,表示这是最后一次打印操作，通过notifyAll操作释放对象锁。并让线程唤醒避免一直处于休眠
                            pre.notifyAll();
                        } else {
                            pre.wait(); // 立即释放 prev锁，当前线程休眠，等待唤醒
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }
}
```

```java
public static void main(String[] args) {
    Object A = new Object();
    Object B = new Object();
    Object C = new Object();
    ThreadCommunity community = new ThreadCommunity();
    ThreadTask threadA = new ThreadTask("A", C, A);
    ThreadTask threadB = new ThreadTask("B", A, B);
    ThreadTask threadC = new ThreadTask("C", B, C);

    try {
        new Thread(threadA).start();
        Thread.sleep(1000);
        new Thread(threadB).start();
        Thread.sleep(1000);
        new Thread(threadC).start();
    } catch (InterruptedException e) {
        e.printStackTrace();
    }
}
```

##### Lock锁方法

通过ReentrantLock我们可以很方便的进行显式的锁操作，即获取锁和释放锁，对于同一个对象锁而言，统一时刻只可能有一个线程拿到了这个锁，此时其他线程通过lock.lock()来获取对象锁时都会被阻塞，直到这个线程通过lock.unlock()操作释放这个锁后，其他线程才能拿到这个锁。

```java
public class ABC_Lock {
    private static Lock lock = new ReentrantLock();// 通过JDK5中的Lock锁来保证线程的访问的互斥
    private static int state = 0;//通过state的值来确定是否打印

    static class ThreadA extends Thread {
        @Override
        public void run() {
            for (int i = 0; i < 10;) {
                try {
                    lock.lock();
                    while (state % 3 == 0) {// 多线程并发，不能用if，必须用循环测试等待条件，避免虚假唤醒
                        System.out.print("A");
                        state++;
                        i++;
                    }
                } finally {
                    lock.unlock();// unlock()操作必须放在finally块中
                }
            }
        }
    }

    static class ThreadB extends Thread {
        @Override
        public void run() {
            for (int i = 0; i < 10;) {
                try {
                    lock.lock();
                    while (state % 3 == 1) {// 多线程并发，不能用if，必须用循环测试等待条件，避免虚假唤醒
                        System.out.print("B");
                        state++;
                        i++;
                    }
                } finally {
                    lock.unlock();// unlock()操作必须放在finally块中
                }
            }
        }
    }

    static class ThreadC extends Thread {
        @Override
        public void run() {
            for (int i = 0; i < 10;) {
                try {
                    lock.lock();
                    while (state % 3 == 2) {// 多线程并发，不能用if，必须用循环测试等待条件，避免虚假唤醒
                        System.out.print("C");
                        state++;
                        i++;
                    }
                } finally {
                    lock.unlock();// unlock()操作必须放在finally块中
                }
            }
        }
    }

    public static void main(String[] args) {
        new ThreadA().start();
        new ThreadB().start();
        new ThreadC().start();
    }
}
```

##### ReentrantLock结合Condition

Condition.await()会立即释放锁，并在原地阻塞。Condition.signal将会从上次阻塞的地方唤醒继续执行。

```java
public class ABC_Condition {
    private static Lock lock = new ReentrantLock();
    private static Condition A = lock.newCondition();
    private static Condition B = lock.newCondition();
    private static Condition C = lock.newCondition();

    private static int count = 0;

    static class ThreadA extends Thread {
        @Override
        public void run() {
            try {
                lock.lock();
                for (int i = 0; i < 10; i++) {
                    while (count % 3 != 0){//注意这里是不等于0，也就是说在count % 3为0之前，当前线程一直阻塞状态
                        A.await(); // A释放lock锁
                        System.out.println("将在这里继续执行");
                    }
                    System.out.print("A");
                    count++;
                    B.signal(); // A执行完唤醒B线程
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            } finally {
                lock.unlock();
            }
        }
    }

    static class ThreadB extends Thread {
        @Override
        public void run() {
            try {
                lock.lock();
                for (int i = 0; i < 10; i++) {
                    while (count % 3 != 1)
                        B.await();// B释放lock锁，当前面A线程执行后会通过B.signal()唤醒该线程
                    System.out.print("B");
                    count++;
                    C.signal();// B执行完唤醒C线程
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            } finally {
                lock.unlock();
            }
        }
    }

    static class ThreadC extends Thread {
        @Override
        public void run() {
            try {
                lock.lock();
                for (int i = 0; i < 10; i++) {
                    while (count % 3 != 2)
                        C.await();// C释放lock锁
                    System.out.print("C");
                    count++;
                    A.signal();// C执行完唤醒A线程
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            } finally {
                lock.unlock();
            }
        }
    }

    public static void main(String[] args) throws InterruptedException {
        new ThreadA().start();
        new ThreadB().start();
        new ThreadC().start();
    }
}
```

##### Semaphore信号量方式

Semaphore又称信号量，是操作系统中的一个概念，在Java并发编程中，信号量控制的是线程并发的数量。

```
public Semaphore(int permits)
```

其中参数permits就是允许同时运行的线程数目; 
  Semaphore是用来保护一个或者多个共享资源的访问，Semaphore内部维护了一个计数器，其值为可以访问的共享资源的个数。一个线程要访问共享资源，先获得信号量，如果信号量的计数器值大于1，意味着有共享资源可以访问，则使其计数器值减去1，再访问共享资源。如果计数器值为0,线程进入休眠。当某个线程使用完共享资源后，释放信号量，并将信号量内部的计数器加1，之前进入休眠的线程将被唤醒并再次试图获得信号量。

Semaphore使用时需要先构建一个参数来指定共享资源的数量，Semaphore构造完成后即是获取Semaphore、共享资源使用完毕后释放Semaphore。

```java
Semaphore semaphore = new Semaphore(10,true);  
semaphore.acquire();  
//do something here  
semaphore.release();  
```

```java
public class ABC_Semaphore {
    // 以A开始的信号量,初始信号量数量为1
    private static Semaphore A = new Semaphore(1);
    // B、C信号量,A完成后开始,初始信号数量为0
    private static Semaphore B = new Semaphore(0);
    private static Semaphore C = new Semaphore(0);

    static class ThreadA extends Thread {
        @Override
        public void run() {
            try {
                for (int i = 0; i < 10; i++) {
                    A.acquire();// A获取信号执行,A信号量减1,当A为0时将无法继续获得该信号量
                    System.out.print("A");
                    B.release();// B释放信号，B信号量加1（初始为0），此时可以获取B信号量
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    static class ThreadB extends Thread {
        @Override
        public void run() {
            try {
                for (int i = 0; i < 10; i++) {
                    B.acquire();
                    System.out.print("B");
                    C.release();
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    static class ThreadC extends Thread {
        @Override
        public void run() {
            try {
                for (int i = 0; i < 10; i++) {
                    C.acquire();
                    System.out.println("C");
                    A.release();
                }
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public static void main(String[] args) throws InterruptedException {
        new ThreadA().start();
        new ThreadB().start();
        new ThreadC().start();
    }
}
```





# **Linux**

### Java开发环境

#### **JDK**

​	如果是仅仅安装JDK8，那么在命令窗口中输入命令：

sudo apt installoracle-java8-set-default，自动就会下载安装并配置好环境变量。

​	如果是安装现在最新的JDK版本JDK10，那么需要在Oracle官网http://www.oracle.com/technetwork/java/javase/downloads/index.html在如下页面中下载JDK（.tar.gz）

​	将其解压缩（-C后面是想解压到的路径）：

```
sudo tar -zxvf ~/Downloads/jdk-8u45-linux-i586.tar.gz -C /usr/lib
```

**配置JDK环境变量：**

根据官网介绍：

Starting with version 8u40, the JDK installation is integrated with the alternatives framework and after installation, the alternatives framework is updated to reflect the binaries from the recently installed JDK. Java commands such as java, javac, javadoc, and javap can be invoked from the command line.

所以根本无需像大多数网站介绍的那样需要修改/etc/profile文件，仅需要在shell中运行下面两条命令：

```
sudo update-alternatives --install /usr/bin/java java **/usr/share/jdk-10.0.1**/binjava 1000
```

```
sudo update-alternatives --install /usr/bin/javac javac **/usr/share/jdk-10.0.1**/binjavac 1000
```

其中加粗是自己安装的JDK主目录的绝对路径

因为系统中还安装了OpenJDK，所以还要执行以下命令来将安装的版本设置为默认的JDK，首先在shell中用下面的命令查看JAVA的版本和优先级：

```
update-alternatives --display java
```

随后执行命令选择JAVA版本：

```
update-alternatives–config java
```

执行完之后会列出系统中所有的JDK，让你选择一个作为默认
最后还是执行一下java -version来确认JDK安装成功与否：

#### **Tomcat**

1. 下载并解压缩到部署位置(8.0.30)

2. 配置环境变量

   ```
   `startup.sh----->catalina.sh----->setclassspath.shJAVA_HOME=/usr/lib/jdk1.8.0_66JRE_HOME=$JAVA_HOME/jre`
   ```

备注：这里的配置可以不写（如果jdk是8u40及以后版本）

1. 启动tomcat： 

```
sudo ./bin/startup.sh
```

1. 关闭tomcat： 

```
sudo ./bin/shutdown.sh
```

#### Mysql

```
sudo apt-get install mysql-server
sudo apt-get install mysql-client
sudo apt-get install libmysqlclient-dev
```



1. 查看默认配置文件

```undefined
sudo cat /etc/mysql/debian.cn
```

​	2. 以默认配置登陆mysql

```cpp
mysql -u debian-sys-maint -p        // 用户名以自己的配置文件为准
```

 输入上面密码

​	3. 更改密码

```csharp
use mysql;
// 下一行，密码改为了yourpassword，可以设置成其他的
update mysql.user set authentication_string=password('yourpassword') where user='root' and Host ='localhost';
update user set plugin="mysql_native_password"; 
flush privileges;
quit;
```

4. 重启mysql

```csharp
sudo service mysql restart
mysql -u root -p
```

​	5.设置允许远程访问

```
sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
```

注释掉bind-address = 127.0.0.1： 

保存退出，然后进入mysql服务，执行授权命令：

```
grant all on *.* to root@'%' identified by '你的密码' with grant option;
flush privileges;
```

然后执行quit命令退出mysql服务，执行如下命令重启mysql

```
sudo service mysql restart
```



#### apt更换源

进入etc/apt/目录中，备份sources.list文件

 修改文件内容：

```
`sudo vim /etc/apt/sources.list`
```

```
#删除内容，并添加以下内容：## Generated by deepin-installer      
deb [by-hash=force]   https://mirrors.tuna.tsinghua.edu.cn/deepin  panda main contrib non-free
```

仓库

```
cp /etc/apt/sources.list /etc/apt/sources.list.bak        此命令是备份该官方源文件
```



### 常用命令

#### 文件管理

| **命令 ** | **功能**           |
| --------- | ------------------ |
| pwd       | 显示当前目录       |
| cd        | 改变所在目录       |
| grep      | 在文件中查找某字符 |
| touch     | 创建文件           |
| rm        | 删除文件           |
| ls        | 查看目录下的内容   |
| cat       | 显示文件的内容     |
| cp        | 复制文件           |
| mv        | 移动文件           |
| rmdir     | 删除目录           |

> 查找当前⽬录下所有⽂件⾥，含有某个字符串的⾏

ack foo 就可以在当前⽬录所有⽂件⾥查找 foo

**2、文档编辑**      

**3、文件传输**      

**4、磁盘管理**      

**5、磁盘维护**

**6、网络通讯**

**7、系统管理**      

**8、系统设置**      

**9、备份压缩**      

#### 服务篇

##### ip 

deepin: 	http://192.168.0.114

##### mysql

启动服务 

```
sudo service mysql restart
```

##### tomcat

启动 `

```
sudo ./bin/startup.sh`
```

#### 工具

##### vim

### 运维问题

[**怎么排查CPU飙升**](https://mp.weixin.qq.com/s/_CTgVIAcnO5T4oVv4Nnyvg)                

[Linux终端查看最消耗CPU内存的进程](https://www.linuxprobe.com/linux-sort-max-mc.html)

**1.CPU占用最多的前10个进程**

```
ps auxw|head -1;ps auxw|sort -rn -k3|head -10
```

**2.内存消耗最多的前10个进程**

```
ps auxw|head -1;ps auxw|sort -rn -k4|head -10
```

或者：

```
ps auxw --sort=rss
ps auxw --sort=%cpu
```



### Mysql调优

> cpu⽅⾯： 

vmstat、sar top、htop、nmon、mpstat 

> 内存： 

free 、ps -aux 、 

> IO设备（磁盘、⽹络）： 

iostat 、 ss 、 netstat 、 iptraf、iftop、lsof、 

**vmstat 命令说明：** 

Procs：r显⽰有多少进程正在等待CPU时间。b显⽰处于不可中断的休眠的进程数量。在等待I/OMemory：swpd显⽰被交换到磁盘 

的数据块的数量。未被使⽤的数据块，⽤⼾缓冲数据块，⽤于操作系统的数据块的数量Swap：操作系统每秒从磁盘上交换到内存 

和从内存交换到磁盘的数据块的数量。s1和s0最好是0Io：每秒从设备中读⼊b1的写⼊到设备b0的数据块的数量。反映了磁盘 

I/OSystem：显⽰了每秒发⽣中断的数量(in)和上下⽂交换(cs)的数量Cpu：显⽰⽤于运⾏⽤⼾代码，系统代码，空闲，等待I/O的 

CPU时间 

**iostat命令说明** 

实例命令：iostat -dk 1 5 

iostat -d -k -x 5 （查看设备使⽤率（%util）和响应时间（await）） 

1) tps：该设备每秒的传输次数。“⼀次传输”意思是“⼀次I/O请求”。多个逻辑请求可能会被合并为“⼀次I/O请求”。 

2) iops ：硬件出⼚的时候，⼚家定义的⼀个每秒最⼤的IO次数,"⼀次传输"请求的⼤⼩是未知的。 

3) kBread/s：每秒从设备（drive expressed）读取的数据量； 

4) KBwrtn/s：每秒向设备（drive expressed）写⼊的数据量； 

5) kBread：读取的总数据量；7、kBwrtn：写⼊的总数量数据量；这些单位都为Kilobytes。 



**系统层面entire的解决办法**

问题⼀：cpu负载⾼，IO负载低 

1、内存不够 2、磁盘性能差 3、SQL问题 ------>去数据库层，进⼀步排查sql问题 4、IO出问题了（磁盘到临界了、raid设计不好、 

raid降级、锁、在单位时间内tps过⾼） 5、tps过⾼: ⼤量的⼩数据IO、⼤量的全表扫描 

问题⼆：IO负载⾼，cpu负载低 

1、⼤量⼩的IO 写操作：2、autocommit ，产⽣⼤量⼩IO 3、IO/PS,磁盘的⼀个定值，硬件出⼚的时候，⼚家定义的⼀个每秒最⼤ 

的IO次数。4、⼤量⼤的IO 写操作 5、SQL问题的⼏率⽐较⼤ 

问题三：IO和cpu负载都很⾼ 

硬件不够了或sql存在问题 



**基础优化**

**1. 优化思路**

定位问题点: 

硬件 --> 系统 --> 应⽤ --> 数据库 --> 架构（⾼可⽤、读写分离、分库分表） 

处理⽅向： 

明确优化⽬标、性能和安全的折中、防患未然 





# Spring

**1.Spring两大核心**

**控制反转（IOC）**或者依赖注入（DI）：对象的创建（包括对象中依赖关系）交给容器管理，需要的时候直接向容器索取

**面向切面编程（AOP）**

**Spring AOP就是基于动态代理的**，如果要代理的对象，实现了某个接口，那么Spring AOP会使用**JDK Proxy**，去创建代理对象，而对于没有实现接口的对象，就无法使用 JDK Proxy 去进行代理了，这时候Spring AOP会使用**Cglib** ，这时候Spring AOP会使用 **Cglib** 生成一个被代理对象的子类来作为代理

## IOC容器

Spring 提供了以下两种不同类型的容器。

| 序号 | 容器 & 描述                                                  |
| ---- | ------------------------------------------------------------ |
| 1    | [Spring BeanFactory 容器](https://www.w3cschool.cn/wkspring/j3181mm3.html)它是最简单的容器，给 DI 提供了基本的支持，它用 org.springframework.beans.factory.BeanFactory  接口来定义。 |
| 2    | [Spring ApplicationContext 容器](https://www.w3cschool.cn/wkspring/yqdx1mm5.html) ApplicationContext 容器包括 BeanFactory 容器的所有功能，所以通常不建议使用BeanFactory。该容器是由  org.springframework.context.ApplicationContext 接口定义。 |

```java
ApplicationContext ac = new ClassPathXmlApplicationContext("cn/itcast/a_hello/applicationContext.xml");
```



**ApplicationContext三个实现**

- **FileSystemXmlApplicationContext ：**此容器从一个XML文件中加载beans的定义，XML Bean 配置文件的全路径名必须提供给它的构造函数。
- **ClassPathXmlApplicationContext：**此容器也从一个XML文件中加载beans的定义，这里，你需要正确设置classpath因为这个容器将在classpath里找bean配置。
- **WebXmlApplicationContext：**此容器加载一个XML文件，此文件定义了一个WEB应用的所有bean。



**容器是如何初始化的？**

容器的初始化是通过refresh()方法来完成的，总共包括三个步骤：

- 定位:通过Resource定位BeanDefinition，BeanDefinition抽象了对bean的定义，比如bean的信息，依赖关系等。这个过程可以想象成寻找bean的过程。

- 载入:BeanDefinition的信息已经定位到了，第二步就是把定义的BeanDefinition在Ioc容器中转化成一个Spring内部标示的数据结构的过程。

- 注册:将抽象好的BeanDefinition统一注册到IoC容器中，IoC容器是通过hashMap来维护BeanDefinition信息的，key为beanName，value为BeanDefinition。



> IOC容器创建对象的方式：

无参构造器；带参构造器；创建工厂类，并调用其方法创建。

然后再通过配置的property属性setter到对象。

> 容器给对象属性赋值

- Set方法（常用）

- 内部bean

- p名称空间

- 自动装配

  - autowire="byName" or autowire="byType"

- 注解

  - 使用注解步骤

    - 先引入context名称空间

      xmlns:context="http://www.springframework.org/schema/context"

    - 开启注解扫描

      <context:component-scan base-package="cn.itcast.e_anno2"></context:component-scan>

    - 使用注解

      - @Component 指定把一个对象加入IOC容器
      - @Repository  作用同@Component； 在持久层使用
      - @Service   作用同@Component； 在业务逻辑层使用
      - @Controller  作用同@Component； 在控制层使用 
      - @Resource   属性注入

> Bean作用域

scope配置项有5个属性，用于描述不同的作用域。

① singleton

使用该属性定义Bean时，IOC容器仅创建一个Bean实例，IOC容器每次返回的是同一个Bean实例。

② prototype

使用该属性定义Bean时，IOC容器可以创建多个Bean实例，每次返回的都是一个新的实例。

③ request

该属性仅对HTTP请求产生作用，使用该属性定义Bean时，每次HTTP请求都会创建一个新的Bean，适用于WebApplicationContext环境。

④ session

该属性仅用于HTTP Session，同一个Session共享一个Bean实例。不同Session使用不同的实例。

⑤ global-session

该属性仅用于HTTP Session，同session作用域不同的是，所有的Session共享一个Bean实例。



> Bean的生命周期

Spring管理Bean的生命周期就复杂多了，正确理解Bean 的生命周期非常重要，因为Spring对Bean的管理可扩展性非常强，下面展示了一个Bean的构造过程

![深究Spring中Bean的生命周期](https://www.javazhiyin.com/wp-content/uploads/2019/05/java0-1558500658.jpg)

**Bean 的生命周期**

如上图所示，Bean 的生命周期还是比较复杂的，下面来对上图每一个步骤做文字描述:

1. Spring启动，查找并加载需要被Spring管理的bean，进行Bean的实例化
2. Bean实例化后对将Bean的引入和值注入到Bean的属性中
3. 如果Bean实现了BeanNameAware接口的话，Spring将Bean的Id传递给setBeanName()方法
4. 如果Bean实现了BeanFactoryAware接口的话，Spring将调用setBeanFactory()方法，将BeanFactory容器实例传入
5. 如果Bean实现了ApplicationContextAware接口的话，Spring将调用Bean的setApplicationContext()方法，将bean所在应用上下文引用传入进来。
6. 如果Bean实现了BeanPostProcessor接口，Spring就将调用他们的postProcessBeforeInitialization()方法。
7. 如果Bean 实现了InitializingBean接口，Spring将调用他们的afterPropertiesSet()方法。类似的，如果bean使用init-method声明了初始化方法，该方法也会被调用
8. 如果Bean 实现了BeanPostProcessor接口，Spring就将调用他们的postProcessAfterInitialization()方法。
9. 此时，Bean已经准备就绪，可以被应用程序使用了。他们将一直驻留在应用上下文中，直到应用上下文被销毁。
10. 如果bean实现了DisposableBean接口，Spring将调用它的destory()接口方法，同样，如果bean使用了destory-method 声明销毁方法，该方法也会被调用。

> **上面是Spring 中Bean的核心接口和生命周期，面试回答上述过程已经足够了。但是翻阅JavaDoc文档发现除了以上接口外，还有另外的初始化过程涉及的接口：**
>
> **摘自org.springframework.beans.factory.BeanFactory， 全部相关接口如下，上述已有的就不用着重标注，把额外的相关接口着重标注下**

![深究Spring中Bean的生命周期](https://www.javazhiyin.com/wp-content/uploads/2019/05/java10-1558500659.jpg)

**Bean 完整的生命周期**

文字解释如下：

————————————初始化————————————

- BeanNameAware.setBeanName() 在创建此bean的bean工厂中设置bean的名称，在普通属性设置之后调用，在InitializinngBean.afterPropertiesSet()方法之前调用
- `BeanClassLoaderAware.setBeanClassLoader()`: 在普通属性设置之后，InitializingBean.afterPropertiesSet()之前调用
- BeanFactoryAware.setBeanFactory() : 回调提供了自己的bean实例工厂，在普通属性设置之后，在InitializingBean.afterPropertiesSet()或者自定义初始化方法之前调用
- `EnvironmentAware.setEnvironment()`: 设置environment在组件使用时调用
- `EmbeddedValueResolverAware.setEmbeddedValueResolver()`: 设置StringValueResolver 用来解决嵌入式的值域问题
- `ResourceLoaderAware.setResourceLoader()`: 在普通bean对象之后调用，在afterPropertiesSet 或者自定义的init-method 之前调用，在 ApplicationContextAware 之前调用。
- `ApplicationEventPublisherAware.setApplicationEventPublisher()`: 在普通bean属性之后调用，在初始化调用afterPropertiesSet 或者自定义初始化方法之前调用。在 ApplicationContextAware 之前调用。
- `MessageSourceAware.setMessageSource()`: 在普通bean属性之后调用，在初始化调用afterPropertiesSet 或者自定义初始化方法之前调用，在 ApplicationContextAware 之前调用。
- ApplicationContextAware.setApplicationContext():  在普通Bean对象生成之后调用，在InitializingBean.afterPropertiesSet之前调用或者用户自定义初始化方法之前。在ResourceLoaderAware.setResourceLoader，ApplicationEventPublisherAware.setApplicationEventPublisher，MessageSourceAware之后调用。
- `ServletContextAware.setServletContext()`: 运行时设置ServletContext，在普通bean初始化后调用，在InitializingBean.afterPropertiesSet之前调用，在 ApplicationContextAware 之后调用**注：是在WebApplicationContext 运行时**
- BeanPostProcessor.postProcessBeforeInitialization() :  将此BeanPostProcessor 应用于给定的新bean实例  在任何bean初始化回调方法(像是InitializingBean.afterPropertiesSet或者自定义的初始化方法）之前调用。这个bean将要准备填充属性的值。返回的bean示例可能被普通对象包装，默认实现返回是一个bean。
- BeanPostProcessor.postProcessAfterInitialization() :  将此BeanPostProcessor 应用于给定的新bean实例  在任何bean初始化回调方法(像是InitializingBean.afterPropertiesSet或者自定义的初始化方法)之后调用。这个bean将要准备填充属性的值。返回的bean示例可能被普通对象包装
- InitializingBean.afterPropertiesSet(): 被BeanFactory在设置所有bean属性之后调用(并且满足BeanFactory 和 ApplicationContextAware)。

————————————销毁————————————

在BeanFactory 关闭的时候，Bean的生命周期会调用如下方法:

- `DestructionAwareBeanPostProcessor.postProcessBeforeDestruction()`: 在销毁之前将此BeanPostProcessor 应用于给定的bean实例。能够调用自定义回调，像是DisposableBean 的销毁和自定义销毁方法，这个回调仅仅适用于工厂中的单例bean(包括内部bean)
- 实现了自定义的destory()方法

## **AOP**

AOP 术语

在我们开始使用 AOP 工作之前，让我们熟悉一下 AOP 概念和术语。这些术语并不特定于 Spring，而是与 AOP 有关的。

| 项            | 描述                                                         |
| ------------- | ------------------------------------------------------------ |
| Aspect        | 一个模块具有一组提供横切需求的 APIs。例如，一个日志模块为了记录日志将被 AOP 方面调用。应用程序可以拥有任意数量的方面，这取决于需求。 |
| Join point    | 在你的应用程序中它代表一个点，你可以在插件 AOP 方面。你也能说，它是在实际的应用程序中，其中一个操作将使用 Spring AOP 框架。 |
| Advice        | 这是实际行动之前或之后执行的方法。这是在程序执行期间通过 Spring AOP 框架实际被调用的代码。 |
| Pointcut      | 这是一组一个或多个连接点，通知应该被执行。你可以使用表达式或模式指定切入点正如我们将在 AOP 的例子中看到的。 |
| Introduction  | 引用允许你添加新方法或属性到现有的类中。                     |
| Target object | 被一个或者多个方面所通知的对象，这个对象永远是一个被代理对象。也称为被通知对象。 |
| Weaving       | Weaving 把方面连接到其它的应用程序类型或者对象上，并创建一个被通知的对象。这些可以在编译时，类加载时和运行时完成。 |



**JoinPoint：连接点，说白了，就是可以被增强的方法；**

**PointCut：切入点，对哪些JoinPoint进行拦截；**

**Advice：通知，就是拦截后的动作；**

**Aspect：切面，把增强应用到具体方法的过程；**

**Spring的AOP需要借助aspectj来实现，可以通过XML，也可以通过注解来完成。**

比如，采用XML方式的话，需要指明用A类的哪个方法对B类的哪些方法上进行增强，这里就涉及到execution表达式了；

比如，采用注解方式的话，就更加简单了，先在XML中开启AOP（<aop:aspectj-autoproxy />），然后在增强方法上直接使用类似@Before(value="execution(具体的表达式)")即可；



spring 支持 **@AspectJ annotation style** 的方法和**基于模式**的方法来实现自定义方面。

| 方法                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [XML Schema based](https://www.w3cschool.cn/wkspring/omps1mm6.html) | 方面是使用常规类以及基于配置的 XML 来实现的。                |
| [@AspectJ based](https://www.w3cschool.cn/wkspring/k4q21mm8.html) | @AspectJ 引用一种声明方面的风格作为带有 Java 5 注释的常规 Java 类注释。 |



# SpringMVC

**[Spring MVC 的请求流程](https://www.jianshu.com/p/91a2d0a1e45a)**

下图为 Spring MVC 的请求流程：

![img](https://upload-images.jianshu.io/upload_images/7896890-65ef874ad7da59a2.png?imageMogr2/auto-orient/strip|imageView2/2/w/784)

**第一站：DispatcherServlet**

从请求离开浏览器以后，第一站到达的就是 DispatcherServlet，看名字这是一个 Servlet，通过 J2EE 的学习，我们知道 Servlet 可以拦截并处理 HTTP 请求，DispatcherServlet 会拦截所有的请求，并且将这些请求发送给 Spring MVC 控制器。

```xml
<servlet>
    <servlet-name>dispatcher</servlet-name>
    <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
    <load-on-startup>1</load-on-startup>
</servlet>
<servlet-mapping>
    <servlet-name>dispatcher</servlet-name>
    <!-- 拦截所有的请求 -->
    <url-pattern>/</url-pattern>
</servlet-mapping>
```

**DispatcherServlet 的任务就是拦截请求发送给 Spring MVC 控制器。**

**第二站：处理器映射（HandlerMapping）**

- **问题：** 典型的应用程序中可能会有多个控制器，这些请求到底应该发给哪一个控制器呢？

所以 DispatcherServlet 会查询一个或多个处理器映射来确定请求的下一站在哪里，处理器映射会**根据请求所携带的 URL 信息来进行决策**，例如上面的例子中，我们通过配置 simpleUrlHandlerMapping 来将 /hello 地址交给 helloController 处理：

```xml
<bean id="simpleUrlHandlerMapping"
      class="org.springframework.web.servlet.handler.SimpleUrlHandlerMapping">
    <property name="mappings">
        <props>
            <!-- /hello 路径的请求交给 id 为 helloController 的控制器处理-->
            <prop key="/hello">helloController</prop>
        </props>
    </property>
</bean>
<bean id="helloController" class="controller.HelloController"></bean>
```

**第三站：控制器(Controller)**

一旦选择了合适的控制器， DispatcherServlet 会将请求发送给选中的控制器，到了控制器，请求会卸下其负载（用户提交的请求）等待控制器处理完这些信息。

**第四站：返回 DispatcherServlet**

当控制器在完成逻辑处理后，通常会产生一些信息，这些信息就是需要返回给用户并在浏览器上显示的信息，它们被称为**模型（Model）**。仅仅返回原始的信息时不够的——这些信息需要以用户友好的方式进行格式化，一般会是 HTML，所以，信息需要发送给一个**视图（view）**，通常会是 JSP。

控制器所做的最后一件事就是将模型数据打包，并且表示出用于渲染输出的视图名**（逻辑视图名）。它接下来会将请求连同模型和视图名发送回 DispatcherServlet。**

**第五站：视图解析器**

这样以来，控制器就不会和特定的视图相耦合，传递给 DispatcherServlet 的视图名并不直接表示某个特定的 JSP。（实际上，它甚至不能确定视图就是 JSP）相反，**它传递的仅仅是一个逻辑名称，这个名称将会用来查找产生结果的真正视图。**

DispatcherServlet 将会使用视图解析器（view resolver）来将逻辑视图名匹配为一个特定的视图实现，它可能是也可能不是 JSP。

**第六站：视图**

既然 DispatcherServlet 已经知道由哪个视图渲染结果了，那请求的任务基本上也就完成了。

它的最后一站是视图的实现，在这里它交付模型数据，请求的任务也就完成了。视图使用模型数据渲染出结果，这个输出结果会通过响应对象传递给客户端。



**SpringMVC详细运行流程图**

![图片描述](https://img1.sycdn.imooc.com/55d2d17f0001065208580652.png)

**十九、SpringMVC运行原理**

1. 客户端请求提交到DispatcherServlet；
2. 由DispatcherServlet控制器查询一个或多个HandlerMapping，找到处理请求的Controller；
3. DispatcherServlet将请求提交到Controller；
4. Controller调用业务逻辑处理后，返回ModelAndView；
5. DispatcherServlet查询一个或多个ViewResoler视图解析器，找到ModelAndView指定的视图；
6. 视图负责将结果显示到客户端。



[**深入了解SpringMVC执行流程**](https://zhuanlan.zhihu.com/p/42602265)



# SpringBoot

**Spring Boot 的核心配置文件有哪几个？它们的区别是什么？**

> Spring Boot 的核心配置文件是 application 和 bootstrap 配置文件。
>  application 配置文件这个容易理解，主要用于 Spring Boot 项目的自动化配置。
>  bootstrap 配置文件有以下几个应用场景。
>  使用 Spring Cloud Config 配置中心时，这时需要在 bootstrap 配置文件中添加连接到配置中心的配置属性来加载外部配置中心的配置信息； 一些固定的不能被覆盖的属性；一些加密/解密的场景

**Spring Boot 的核心注解是哪个？它主要由哪几个注解组成的？**

> 启动类上面的注解是@SpringBootApplication，它也是 Spring Boot 的核心注解 主要组合包含了以下 3 个注解：
>  1.@SpringBootConfiguration：组合了 @Configuration 注解，实现配置文件的功能。
>  2.@EnableAutoConfiguration：打开自动配置的功能，也可以关闭某个自动配置的选项，如关闭数据源自动配置功能： @SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })。
>  3.@ComponentScan：Spring组件扫描。



作者：若丨寒
链接：https://www.jianshu.com/p/14ef39ed8ad3
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。



**Spring Boot自动配置原理**



### 整合其他框架

#### ElasticSearch 

> 地址：[mall-learning项目](http://www.macrozheng.com/#/architect/mall_arch_07?id=%E5%9C%A8pomxml%E4%B8%AD%E6%B7%BB%E5%8A%A0%E7%9B%B8%E5%85%B3%E4%BE%9D%E8%B5%96)

Spring Data Elasticsearch是Spring提供的一种以Spring Data风格来操作数据存储的方式，它可以避免编写大量的样板代码。

[在pom.xml中添加相关依赖](http://www.macrozheng.com/#/architect/mall_arch_07?id=在pomxml中添加相关依赖)

```xml
<!--Elasticsearch相关依赖-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-elasticsearch<artifactId>
</dependency>
```

[修改SpringBoot配置文件](http://www.macrozheng.com/#/architect/mall_arch_07?id=修改springboot配置文件)

> 修改application.yml文件，在spring节点下添加Elasticsearch相关配置。

```yml
data:
  elasticsearch:
    repositories:
      enabled: true
    cluster-nodes: 127.0.0.1:9300 # es的连接地址及端口号
    cluster-name: elasticsearch # es集群的名称
```

### Spring Data JPA

**JPA的出现主要是为了简化持久层开发以及整合ORM技术**

**[SpringBoot学习笔记九：Spring Data Jpa的使用](https://www.jianshu.com/p/c23c82a8fcfc)**

Spring Data JPA的主要类及结构图

　　七个Repository接口：

　　　　1.Repository

　　　　2.CrudRepository

　　　　3.PagingAndSortingRepository

　　　　4.QueryByExampleExecutor

　　　　5.JpaRepository

　　　　6.JpaSpeccificationExecutor

　　　　7.QueryDslPredicateExecutor

　　两个实现类：

　　　　1.SimpleJpaRepository

　　　　2.QueryDslJpaRepository

![img](https://img2018.cnblogs.com/blog/1217603/201906/1217603-20190627095909253-1585940270.png)

**配置**：

**pom.xml**

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

**application.yml**

```yml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/test?useUnicode=true&characterEncoding=UTF-8&zeroDateTimeBehavior=convertToNull&allowMultiQueries=true&useSSL=false
    username: root
    password: mysql123
  jpa:
    database: MySQL
    database-platform: org.hibernate.dialect.MySQL5InnoDBDialect
    show-sql: true
    hibernate:
      ddl-auto: update
```

#### Repository 接口

```
Repository 接口是 Spring Data JPA 中为我我们提供的所有接口中的顶层接口 Repository 提供了两种查询方式的支持
    1)基于方法名称命名规则查询
    2)基于@Query 注解查询
```

**1）方法名称命名规则查询**

```
规则:
    findBy(关键字)+属性名称(属性名称的首字母大写)+查询条件(首字母大写)
```

| 关键字             | 方法命名                       | sql where 字句             |
| ------------------ | ------------------------------ | :------------------------- |
| And                | findByNameAndPwd               | where name= ? and pwd =?   |
| Or                 | findByNameOrSex                | where name= ? or sex=?     |
| Is,Equal           | findById,                      | findByIdEquals             |
| Between            | findByIdBetween                | where id between ? and ?   |
| LessThan           | findByIdLessThan               | where id < ?               |
| LessThanEqual      | findByIdLessThanEquals         | where id <= ?              |
| GreaterThan        | findByIdGreaterThan            | where id > ?               |
| GreaterThanEqual   | findByIdGreaterThanEquals      | where id > = ?             |
| After              | findByIdAfter                  | where id > ?               |
| Before             | findByIdBefore                 | where id < ?               |
| IsNull             | findByNameIsNull               | where name is null         |
| isNotNull,Not Null | findByNameNotNull              | where name is not          |
| Like               | findByNameLike                 | where name like ?          |
| NotLike            | findByNameNotLike              | where name not like ?      |
| StartingWith       | findByNameStartingWith         | where name like '?%'       |
| EndingWith         | findByNameEndingWith           | where name like '%?'       |
| Containing         | findByNameContaining           | where name like '%?%'      |
| OrderBy            | findByIdOrderByXDesc           | where id=? order by x desc |
| Not                | findByNameNot                  | where name <> ?            |
| In                 | findByIdIn(Collection<?> c)    | where id in (?)            |
| NotIn              | findByIdNotIn(Collection<?> c) | where id not   in (?)      |
| True               | findByAaaTue                   | where aaa = true           |
| False              | findByAaaFalse                 | where aaa = false          |
| IgnoreCase         | findByNameIgnoreCase           | where UPPER(name)=UPPER(?) |

**2）基于@Query 注解的查询**

​	*2.1）通过 JPQL 语句查询*

```
JPQL:	
    通过 Hibernate 的 HQL 演变过来的。他和 HQL 语法及其相似
```

```java
public interface UsersDao extends Repository<Users, Integer> {	
	//使用@Query注解查询
	@Query(value="from Users where username = ?")
	List<Users> queryUserByNameUseJPQL(String name);
	
	@Query("from Users where username like ?")
	List<Users> queryUserByLikeNameUseJPQL(String name);
	
	@Query("from Users where username = ? and userage >= ?")
	List<Users> queryUserByNameAndAge(String name,Integer age);	
}
```

​	*2.2）通过 SQL 语句查询*

```java
public interface UsersDao extends Repository<Users, Integer> {
	//使用@Query注解查询SQL
	//nativeQuery:默认的是false.表示不开启sql查询。是否对value中的语句做转义。
	@Query(value="select * from t_users where username = ?",nativeQuery=true)
	List<Users> queryUserByNameUseSQL(String name);

	@Query(value="select * from t_users where username like ?",nativeQuery=true)
	List<Users> queryUserByLikeNameUseSQL(String name);
	
	@Query(value="select * from t_users where username = ? and userage >= ?",nativeQuery=true)
	List<Users> queryUserByNameAndAgeUseSQL(String name,Integer age);
	
}
```

**3 ) 通过@Query 注解完成数据更新**

```java
public interface UsersDao extends Repository<Users, Integer> {
@Query("update Users set userage = ? where userid = ?")
	@Modifying //@Modifying当前语句是一个更新语句
	void updateUserAgeById(Integer age,Integer id);
}
```



# MyBatis

Mybatis是一个orm类型的半自动框架，执行了对JDBC的封装，是一个持久层框架。

**通常一个Xml映射文件，都会写一个Dao接口与之对应，请问，这个Dao接口的工作原理是什么？Dao接口里的方法，参数不同时，方法能重载吗？**

> 答：Dao接口即MApper接口，接口的全限名，就是映射文件的namespace的值，接口的方法名，就是映射文件中Mapper的Statement的id值，接口方法内的参数，就是传递个sql的参数！因为mapper接口是没有实现类的，所以在调用方法时，需要拿全限定路径名称加上方法名作为key值！
>
> 不能重载

**Mybatis全局配置文件中有哪些标签?分别代表什么意思?**

> 答：
> configuration 配置
>  properties 属性:可以加载properties配置文件的信息
>  settings 设置：可以设置mybatis的全局属性
>  typeAliases 类型命名
>  typeHandlers 类型处理器
>  objectFactory 对象工厂
>  plugins 插件
>  environments 环境
>  environment 环境变量
>  transactionManager 事务管理器
>  dataSource 数据源
>  mappers 映射器

**Mybatis 中一级缓存与二级缓存的区别？**

缓存：合理使用缓存是优化中最常见的方法之一，将从数据库中查询出来的数据放入缓存中，下次使用时不必从数据库查询，而是直接从缓存中读取，避免频繁操作数据库，减轻数据库的压力，同时提高系统性能。

- 一级缓存是SqlSession级别的缓存：
   Mybatis对缓存提供支持，但是在没有配置的默认情况下，它只开启一级缓存。一级缓存在操作数据库时需要构造sqlSession对象，在对象中有一个数据结构用于存储缓存数据。不同的sqlSession之间的缓存数据区域是互相不影响的。也就是他只能作用在同一个sqlSession中，不同的sqlSession中的缓存是互相不能读取的。

- 二级缓存是mapper级别的缓存：
   MyBatis的二级缓存是mapper级别的缓存，它可以提高对数据库查询的效率，以提高应用的性能。多个SqlSession去操作同一个Mapper的sql语句，多个SqlSession可以共用二级缓存，二级缓存是跨SqlSession的。

**简述一下Mybatis 的编程步骤**

> A.创建 SqlSessionFactory
> B.通过 SqlSessionFactory 创建 SqlSession
> C.通过 sqlsession 执行数据库操作
> D.调用 session.commit()提交事务
> E.调用 session.close()关闭会话





# MySql

**[理解完这些基本上能解决面试中MySql的事务问题](https://mp.weixin.qq.com/s/ENXsM73sD61vQJnKKYJmug)**    

**[浅谈MySQL并发控制：隔离级别、锁与MVCC](https://mp.weixin.qq.com/s/glcsuhr2cc7S7G2z-TAmyA)**    

**[国庆肝了8天整整2W字的数据库知识点](https://mp.weixin.qq.com/s/J3kCOJwyv2nzvI0_X0tlnA)**

**[MySQL调优](https://mp.weixin.qq.com/s/e0CqJG2-PCDgKLjQfh02tw)**

**[国庆肝了8天整整2W字的数据库知识点](https://mp.weixin.qq.com/s/J3kCOJwyv2nzvI0_X0tlnA)**

**[MySQL索引凭什么让查询效率提高这么多？](https://mp.weixin.qq.com/s/qESZSzHoxUKQRJhb1EQA_Q)**

**[MySQL的索引是怎么加速查询的？](https://mp.weixin.qq.com/s/7TPVOT7sloDUKmhldf9uvg)**

**[数据库索引](https://mp.weixin.qq.com/s/_9rDde9wRYoZeh07EASNQQ)**

**[MySql主从复制，从原理到实践！](https://mp.weixin.qq.com/s/eEWMSTAUF1H-gFBx26jujw)**

**[MySQL 的 InnoDB 存储引擎是怎么设计的？](https://mp.weixin.qq.com/s/wr2gJGQSA8QH_lmPh1XOkw)**

**[数据库基础知识](https://mp.weixin.qq.com/s/NDL1Q6nqdPq5oMBWSpq4ug)**

**[原来MySQL面试还会问这些(``undo log``)](https://mp.weixin.qq.com/s/Lx4TNPLQzYaknR7D3gmOmQ)**

**[数据库连接池到底应该设多大？这篇文章可能会颠覆你的认知](https://mp.weixin.qq.com/s/dQFSrXEmgBMh1PW835rlwQ)**

**[漫话：如何给女朋友解释什么是撞库、脱库和洗库？](https://mp.weixin.qq.com/s/L0XUMHInnwN9gSYGH2nzdg)**

**[用对了这些场景下的索引，技术总监夸我棒](https://mp.weixin.qq.com/s/-gmAPfiKMNJgHhIZqR2C4A)**

**[MVCC和事务隔离级别的关系](https://mp.weixin.qq.com/s/0-YEqTMd0OaIhW99WqavgQ)**

**[MySQL事务与MVCC如何实现的隔离级别](https://mp.weixin.qq.com/s/CZHuGT4sKs_QHD_bv3BfAQ)**

**[我说 SELECT COUNT(*) 会造成全表扫描，面试官让我回去等通知](https://mp.weixin.qq.com/s/SNRvdmyS57oWS_CyYKVvSA)**



![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTIzp5SWFrcGlcD3SSKo1OWl3zgCFDlPtPcoqUTfaM9NaEQ67m21I5YQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**Mysql架构**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdsIkRX56rPzJ9S1lj1svQZHcwxH43DYuJRJk0uD8vmS7pibTqqa62Zuw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



## 存储引擎

### InnoDB

InnoDB 是 MySQL 默认的事务型存储引擎，只要在需要它不支持的特性时，才考虑使用其他存储引擎。

InnoDB 采用 MVCC 来支持高并发，并且实现了四个标准隔离级别(未提交读、提交读、可重复读、可串行化)。其默认级别时可重复读（`REPEATABLE READ`），在可重复读级别下，通过 MVCC + Next-Key Locking 防止幻读。

主索引时聚簇索引，在索引中保存了数据，从而避免直接读取磁盘，因此对主键查询有很高的性能。

InnoDB 内部做了很多优化，包括从磁盘读取数据时采用的可预测性读，能够自动在内存中创建 hash 索引以加速读操作的自适应哈希索引，以及能够加速插入操作的插入缓冲区等。

InnoDB 支持真正的在线热备份，MySQL 其他的存储引擎不支持在线热备份，要获取一致性视图需要停止对所有表的写入，而在读写混合的场景中，停止写入可能也意味着停止读取。

**一张是 MySQL 架构图，另一张则是 InnoDB 架构图：**

![img](https://mmbiz.qpic.cn/mmbiz_png/lA1CtgibZZmyiaicGXrxl6QZicE8Ms4ny8M280ib6znLOcVlTk8C9e11eJUWHEnP5ViafRkyPcAicR6dTQqbcI2QBjk1g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_png/lA1CtgibZZmyiaicGXrxl6QZicE8Ms4ny8M2PRyKZKibWGlfBDde8MVjy4FyMb7QQY9MZOtTu405hwsMiaPC9SpWy3Mg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### [InnoDB 内存架构](https://mp.weixin.qq.com/s/wr2gJGQSA8QH_lmPh1XOkw)

从上面第二张图可以看到，InnoDB 主要分为两大块：

- **InnoDB In-Memory Structures**
- **InnoDB On-Disk Structures**

内存和磁盘，让我们先从内存开始。

**1、Buffer Pool**

> The buffer pool is an area in main memory where InnoDB caches table and index data as it is accessed.

正如之前提到的，MySQL 不会直接去修改磁盘的数据，因为这样做太慢了，MySQL 会先改内存，然后记录 redo log，等有空了再刷磁盘，如果内存里没有数据，就去磁盘 load。

而这些数据存放的地方，就是 Buffer Pool。

我们平时开发时，会用 redis 来做缓存，缓解数据库压力，其实 MySQL 自己也做了一层类似缓存的东西。

MySQL 是以「页」（page）为单位从磁盘读取数据的，Buffer Pool 里的数据也是如此，实际上，Buffer Pool 是`a linked list of pages`，一个以页为元素的链表。

为什么是链表？因为和缓存一样，它也需要一套淘汰算法来管理数据。

Buffer Pool 采用基于 LRU（least recently used） 的算法来管理内存：

![img](https://mmbiz.qpic.cn/mmbiz_png/lA1CtgibZZmyiaicGXrxl6QZicE8Ms4ny8M2hYhdUAiaBnGljDySByIwrqCEJa7cEuHJtsQTx0B18mvcv16yF37H2yQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

> 关于 Buffer Pool 的更多知识，诸如如何配置大小、如何监控等等：Buffer Pool

**2、Change Buffer**

上面提到过，如果内存里没有对应「页」的数据，MySQL 就会去把数据从磁盘里 load 出来，如果每次需要的「页」都不同，或者不是相邻的「页」，那么每次 MySQL 都要去 load，这样就很慢了。

于是如果 MySQL 发现你要修改的页，不在内存里，就把你要对页的修改，先记到一个叫 Change Buffer 的地方，同时记录 redo  log，然后再慢慢把数据 load 到内存，load 过来后，再把 Change Buffer 里记录的修改，应用到内存（Buffer  Pool）中，这个动作叫做 **merge**；而把内存数据刷到磁盘的动作，叫 **purge**：

- **merge：Change Buffer -> Buffer Pool**
- **purge：Buffer Pool -> Disk**

![img](https://mmbiz.qpic.cn/mmbiz_png/lA1CtgibZZmyiaicGXrxl6QZicE8Ms4ny8M2Mlelug7BicNibmORekXWGdsJjSp49dYJbiania6ZUzNmoricSZhKwfI7BVA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

> The change buffer is a special data structure that caches changes to **secondary index** pages when those pages are not in the **buffer pool**. The buffered changes, which may result from INSERT, UPDATE, or DELETE operations (DML), are **merged** later when the pages are loaded into the buffer pool by other read operations.

上面是 MySQL 官网对 Change Buffer 的定义，仔细看的话，你会发现里面提到：Change Buffer  只在操作「二级索引」（secondary index）时才使用，原因是「聚簇索引」（clustered  indexes）必须是「唯一」的，也就意味着每次插入、更新，都需要检查是否已经有相同的字段存在，也就没有必要使用 Change Buffer  了；另外，「聚簇索引」操作的随机性比较小，通常在相邻的「页」进行操作，比如使用了自增主键的「聚簇索引」，那么 insert  时就是递增、有序的，不像「二级索引」，访问非常随机。

> 如果想深入理解 Change Buffer 的原理，除了 MySQL 官网的介绍：Change Buffer，还可以阅读下《MySQL技术内幕》的「2.6.1 - 插入缓冲」章节，里面会从 Change Buffer 的前身 —— Insert Buffer 开始讲起，很透彻。

**3、Adaptive Hash Index**

MySQL 索引，不管是在磁盘里，还是被 load 到内存后，都是 B+ 树，B+ 树的查找次数取决于树的深度。你看，数据都已经放到内存了，还不能“一下子”就找到它，还要“几下子”，这空间牺牲的是不是不太值得？

尤其是那些频繁被访问的数据，每次过来都要走 B+ 树来查询，这时就会想到，我用一个指针把数据的位置记录下来不就好了？

这就是「自适应哈希索引」（Adaptive Hash Index）。自适应，顾名思义，MySQL 会自动评估使用自适应索引是否值得，如果观察到建立哈希索引可以提升速度，则建立。

**4、Log Buffer**

> The log buffer is the memory area that holds data to be written to the log files on disk.

从上面架构图可以看到，Log Buffer 里的 redo log，会被刷到磁盘里：

![img](https://mmbiz.qpic.cn/mmbiz_png/lA1CtgibZZmyiaicGXrxl6QZicE8Ms4ny8M2uH048BxxvGmG3dzpU6Cibwhg2auN7sy8vrmFSqcheed7ZZ7trqcZbzA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**Operating System Cache**

在内存和磁盘之间，你看到 MySQL 画了一层叫做 Operating System Cache 的东西，其实这个不属于 InnoDB  的能力，而是操作系统为了提升性能，在磁盘前面加的一层高速缓存，这里不展开细讲，感兴趣的同学可以参考下维基百科：Page Cache

#### InnoDB 磁盘架构

磁盘里有什么呢？除了表结构定义和索引，还有一些为了高性能和高可靠而设计的角色，比如 redo log、``undo log``、Change Buffer，以及 Doublewrite Buffer 等等.

> 有同学会问，那表的数据呢？其实只要理解了 InnoDB 里的所有表数据，都以索引（聚簇索引+二级索引）的形式存储起来，就知道索引已经包含了表数据。

**1、表空间（Tablespaces）**

从架构图可以看到，Tablespaces 分为五种：

- The System Tablespace
- File-Per-Table Tablespaces
- General Tablespace
- Undo Tablespaces
- Temporary Tablespaces

其中，我们平时创建的表的数据，可以存放到 The System Tablespace 、File-Per-Table Tablespaces、General Tablespace 三者中的任意一个地方，具体取决于你的配置和创建表时的 sql 语句。

> 这里同样不展开，如何选择不同的表空间存储数据？不同表空间各自的优势劣势等等，传送门：Tablespaces

**2、Doublewrite Buffer**

**如果说 Change Buffer 是提升性能，那么 Doublewrite Buffer 就是保证数据页的可靠性。**

怎么理解呢？

前面提到过，MySQL 以「页」为读取和写入单位，一个「页」里面有多行数据，写入数据时，MySQL 会先写内存中的页，然后再刷新到磁盘中的页。

这时问题来了，假设在某一次从内存刷新到磁盘的过程中，一个「页」刷了一半，突然操作系统或者 MySQL 进程奔溃了，这时候，内存里的页数据被清除了，而磁盘里的页数据，刷了一半，处于一个中间状态，不尴不尬，可以说是一个「不完整」，甚至是「坏掉的」的页。

有同学说，不是有 Redo Log 么？其实这个时候 Redo Log 也已经无力回天，Redo Log  是要在磁盘中的页数据是正常的、没有损坏的情况下，才能把磁盘里页数据 load 到内存，然后应用 Redo  Log。而如果磁盘中的页数据已经损坏，是无法应用 Redo Log 的。

所以，MySQL 在刷数据到磁盘之前，要先把数据写到另外一个地方，也就是 Doublewrite Buffer，写完后，再开始写磁盘。Doublewrite  Buffer 可以理解为是一个备份（recovery），万一真的发生 crash，就可以利用 Doublewrite Buffer  来修复磁盘里的数据。

> 留个问题，有了 Doublewrite Buffer 后，不就意味着 MySQL 要写两次磁盘？性能岂不是很差？



### MyISAM

设计简单，数据以紧密格式存储。对于只读数据，或者表比较小、可以容忍修复操作，则依然可以使用它。

提供了大量的特性，包括压缩表、空间数据索引等。

不支持事务。

不支持行级锁，只能对整张表加锁，读取时会对需要读到的所有表加共享锁，写入时则对表加排它锁。但在表有读取操作的同时，也可以往表中插入新的记录，这被称为并发插入（CONCURRENT INSERT）。

可以手工或者自动执行检查和修复操作，但是和事务恢复以及崩溃恢复不同，可能导致一些数据丢失，而且修复操作是非常慢的。

如果指定了 DELAY_KEY_WRITE  选项，在每次修改执行完成时，不会立即将修改的索引数据写入磁盘，而是会写到内存中的键缓冲区，只有在清理键缓冲区或者关闭表的时候才会将对应的索引块写入磁盘。这种方式可以极大的提升写入性能，但是在数据库或者主机崩溃时会造成索引损坏，需要执行修复操作。

### InnoDB 和 MyISAM 的比较

- 事务：InnoDB 是事务型的，可以使用 Commit 和 Rollback 语句。
- 并发：MyISAM 只支持表级锁，而 InnoDB 还支持行级锁。
- 外键：InnoDB 支持外键。
- 备份：InnoDB 支持在线热备份。
- 崩溃恢复：MyISAM 崩溃后发生损坏的概率比 InnoDB 高很多，而且恢复的速度也更慢。
- 其它特性：MyISAM 支持压缩表和空间数据索引。



## 日志系统

**mysql的日志系统可以用来保证原子性等。**

MySQL的日志有很多种，如二进制日志（binlog）、错误日志、查询日志、慢查询日志等，此外InnoDB存储引擎还提供了两种日志：redo log（重做日志）和``undo log``（回滚日志）。这里将重点针对InnoDB引擎，对重做日志、回滚日志和二进制日志这三种进行分析。



### **重做日志（redo log）**

**什么是redo log？**

假设我们有一条sql语句：

```
update user_table set name='java3y' where id = '3'
```

MySQL执行这条SQL语句，肯定是先把`id=3`的这条记录查出来，然后将`name`字段给改掉。这没问题吧？

实际上Mysql的基本存储结构是**页**(记录都存在页里边)，所以MySQL是先把这条记录所在的**页**找到，然后把该页加载到内存中，将对应记录进行修改。

现在就可能存在一个问题：**如果在内存中把数据改了，还没来得及落磁盘，而此时的数据库挂了怎么办**？显然这次更改就丢了。

如果每个请求都需要将数据**立马**落磁盘之后，那速度会很慢，MySQL可能也顶不住。所以MySQL是怎么做的呢？

MySQL引入了`redo log`，内存写完了，然后会写一份`redo log`，这份`redo log`记载着这次**在某个页上做了什么修改**。

重做日志（`redo log`）是InnoDB引擎层的日志，用来记录事务操作引起数据的变化，记录的是**数据页的物理修改**。

其实写`redo log`的时候，也会有`buffer`，是先写`buffer`，再真正落到磁盘中的。至于从`buffer`什么时候落磁盘，会有配置供我们配置。

![img](https://mmbiz.qpic.cn/sz_mmbiz_jpg/2BGWl1qPxib3SEnwZ7m4kDYIic90VDw9UjVQ9icBCTlEVdUzOf0T4mBKawOneZ5AQKloHH128wA99bz3BcBic9GiaXA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

写`redo log`也是需要写磁盘的，但它的好处就是`顺序IO`（我们都知道顺序IO比随机IO快非常多）。

所以，`redo log`的存在为了：当我们修改的时候，写完内存了，但数据还没真正写到磁盘的时候。此时我们的数据库挂了，我们可以根据`redo log`来对数据进行恢复。因为`redo log`是顺序IO，所以**写入的速度很快**，并且`redo log`记载的是物理变化（xxxx页做了xxx修改），文件的体积很小，**恢复速度很快**。

`redo log`的作用是为**持久化**而生的。写完内存，如果数据库挂了，那我们可以通过`redo log`来恢复内存还没来得及刷到磁盘的数据，将`redo log`加载到内存里边，那内存就能恢复到挂掉之前的数据了。

`binlog`的作用是**复制和恢复**而生的。

- 主从服务器需要保持数据的一致性，通过`binlog`来同步数据。
- 如果整个数据库的数据都被删除了，`binlog`存储着所有的数据变更情况，那么可以通过`binlog`来对数据进行恢复。

又看到这里，你会想：”如果整个数据库的数据都被删除了，那我可以用`redo log`的记录来恢复吗？“**不能**

因为功能的不同，`redo log` 存储的是物理数据的变更，如果我们内存的数据已经刷到了磁盘了，那`redo log`的数据就无效了。所以`redo log`不会存储着**历史**所有数据的变更，**文件的内容会被覆盖的**。

`redo log`是MySQL的InnoDB引擎所产生的。

`binlog`无论MySQL用什么引擎，都会有的。



**`redo log`的写入细节**

InnoDB引擎对数据的更新，是先将更新记录写入`redo log`日志，然后会在系统空闲的时候或者是按照设定的更新策略再将日志中的内容更新到磁盘之中。这就是所谓的预写式技术（Write Ahead logging）。这种技术可以大大减少IO操作的频率，提升数据刷新的效率。

#### **脏数据刷盘**

值得注意的是，`redo log`日志的大小是固定的，为了能够持续不断的对更新记录进行写入，在redo log日志中设置了两个标志位置，checkpoint和write_pos，分别表示记录擦除的位置和记录写入的位置。redo log日志的数据写入示意图可见下图。![img](https://mmbiz.qpic.cn/mmbiz_png/TdGLaSU675hcsS4wOSWWZhZ2WayIL6wVQoJ8UL0cuFGmur9ksdpzUvafNiaOmF1xEjea3cNPUX2sMVD8bpz5ic9Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

当write_pos标志到了日志结尾时，会从结尾跳至日志头部进行重新循环写入。所以`redo log`的逻辑结构并不是线性的，而是可看作一个圆周运动。write_pos与checkpoint中间的空间可用于写入新数据，写入和擦除都是往后推移，循环往复的。

当write_pos追上checkpoint时，表示`redo log`日志已经写满。这时不能继续执行新的数据库更新语句，需要停下来先删除一些记录，执行checkpoint规则腾出可写空间。

> checkpoint规则：checkpoint触发后，将buffer中脏数据页和脏日志页都刷到磁盘。

> 脏数据：指内存中未刷到磁盘的数据。

`redo log`中最重要的概念就是**缓冲池buffer pool**，这是在**内存中**分配的一个区域，包含了磁盘中部分数据页的映射，作为访问数据库的缓冲。

> 当请求读取数据时，会先判断是否在缓冲池命中，如果未命中才会在磁盘上进行检索后放入缓冲池；

> 当请求写入数据时，会先写入缓冲池，缓冲池中修改的数据会定期刷新到磁盘中。这一过程也被称之为刷脏 。

因此，**当数据修改时，除了修改buffer pool中的数据，还会在`redo log`中记录这次操作；当事务提交时，会根据`redo log`的记录对数据进行刷盘。**如果MySQL宕机，重启时可以读取`redo log`中的数据，对数据库进行恢复，从而保证了事务的持久性，使得数据库获得crash-safe能力。



#### **脏日志刷盘**

除了上面提到的对于脏数据的刷盘，实际上`redo log`日志在记录时，为了保证日志文件的持久化，也需要经历将日志记录从内存写入到磁盘的过程。`redo log`日志可分为两个部分，一是存在易失性内存中的缓存日志`redo log buff`，二是保存在磁盘上的`redo log`日志文件`redo log file`。

为了确保每次记录都能够写入到磁盘中的日志中，每次将`redo log buffer`中的日志写入`redo log file`的过程中都会调用一次操作系统的`fsync`操作。

> fsync函数：包含在UNIX系统头文件#include <unistd.h>中，用于同步内存中所有已修改的文件数据到储存设备。

在写入的过程中，还需要经过操作系统内核空间的os buffer。`redo log`日志的写入过程可见下图。![img](https://mmbiz.qpic.cn/mmbiz_png/TdGLaSU675hcsS4wOSWWZhZ2WayIL6wVMR1BLAHcRCUibTeI23AxvDryp7RxEKvWWkAM0uGjD8IUrIVowF2SxdA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

从`redo log buffer`写日志到磁盘的`redo log file`中，过程如下： 

![img](https://images2018.cnblogs.com/blog/733013/201805/733013-20180508101949424-938931340.png)

MySQL支持用户自定义在commit时如何将`log buffer`中的日志刷`log file`中。这种控制通过变量 `innodb_flush_log_at_trx_commit` 的值来决定。该变量有3种值：0、1、2，默认为1。但注意，这个变量只是控制commit动作是否刷新`log buffer`到磁盘。

- 当设置为1的时候，事务每次提交都会将`log buffer`中的日志写入os buffer并调用fsync()刷到log file on disk中。这种方式即使系统崩溃也不会丢失任何数据，但是因为每次提交都写入磁盘，IO的性能较差。
- 当设置为0的时候，事务提交时不会将`log buffer`中日志写入到os buffer，而是每秒写入os  buffer并调用fsync()写入到log file on  disk中。也就是说设置为0时是(大约)每秒刷新写入到磁盘中的，当系统崩溃，会丢失1秒钟的数据。
- 当设置为2的时候，每次提交都仅写入到os buffer，然后是每秒调用fsync()将os buffer中的日志写入到log file on disk。

![img](https://images2018.cnblogs.com/blog/733013/201805/733013-20180508104623183-690986409.png)

​		注意，有一个变量 `innodb_flush_log_at_timeout` 的值为1秒，该变量表示的是刷日志的频率，很多人误以为是控制 `innodb_flush_log_at_trx_commit` 值为0和2时的1秒频率，实际上并非如此。测试时将频率设置为5和设置为1，当 `innodb_flush_log_at_trx_commit` 设置为0和2的时候性能基本都是不变的。关于这个频率是控制什么的，在后面的"刷日志到磁盘的规则"中会说。

​		在主从复制结构中，要保证事务的持久性和一致性，需要对日志相关变量设置为如下：

- **如果启用了二进制日志，则设置`sync_binlog`=1，即每提交一次事务同步写到磁盘中。**
- **总是设置`innodb_flush_log_at_trx_commit`=1，即每提交一次事务都写到磁盘中。**

上述两项变量的设置保证了：每次提交事务都写入二进制日志和事务日志，并在提交时将它们刷新到磁盘中。

​		选择刷日志的时间会严重影响数据修改时的性能，特别是刷到磁盘的过程。下例就测试了 `innodb_flush_log_at_trx_commit` 分别为0、1、2时的差距。

​		最后可以发现，其实值为2和0的时候，它们的差距并不太大，但2却比0要安全的多。它们都是每秒从os  buffer刷到磁盘，它们之间的时间差体现在log buffer刷到os buffer上。因为将log buffer中的日志刷新到os  buffer只是内存数据的转移，并没有太大的开销，所以每次提交和每秒刷入差距并不大。可以测试插入更多的数据来比较，以下是插入100W行数据的情况。从结果可见，值为2和0的时候差距并不大，但值为1的性能却差太多。

​		尽管设置为0和2可以大幅度提升插入性能，但是在故障的时候可能会丢失1秒钟数据，这1秒钟很可能有大量的数据，从上面的测试结果看，100W条记录也只消耗了20多秒，1秒钟大约有4W-5W条数据，尽管上述插入的数据简单，但却说明了数据丢失的大量性。**更好的插入数据的做法是将值设置为1，然后修改存储过程，将每次循环都提交修改为只提交一次**，这样既能保证数据的一致性，也能提升性能。



#### [日志刷盘的规则](https://www.cnblogs.com/f-ck-need-u/archive/2018/05/08/9010872.html)

`log buffer`中未刷到磁盘的日志称为脏日志(`dirty log`)。

在上面的说过，默认情况下事务每次提交的时候都会刷事务日志到磁盘中，这是因为变量 `innodb_flush_log_at_trx_commit` 的值为1。但是innodb不仅仅只会在有commit动作后才会刷日志到磁盘，这只是innodb存储引擎刷日志的规则之一。

刷日志到磁盘有以下几种规则：

**1.发出commit动作时。已经说明过，commit发出后是否刷日志由变量 `innodb_flush_log_at_trx_commit` 控制。**

**2.每秒刷一次。这个刷日志的频率由变量 `innodb_flush_log_at_timeout` 值决定，默认是1秒。要注意，这个刷日志频率和commit动作无关。**

**3.当log buffer中已经使用的内存超过一半时。**

**4.当有checkpoint时，checkpoint在一定程度上代表了刷到磁盘时日志所处的LSN位置。**



#### 数据页刷盘的规则及checkpoint

内存中(buffer pool)未刷到磁盘的数据称为脏数据(dirty data)。由于数据和日志都以页的形式存在，所以脏页表示脏数据和脏日志。

上一节介绍了日志是何时刷到磁盘的，不仅仅是日志需要刷盘，脏数据页也一样需要刷盘。

**在innodb中，数据刷盘的规则只有一个：checkpoint。**但是触发checkpoint的情况却有几种。**不管怎样，checkpoint触发后，会将buffer中脏数据页和脏日志页都刷到磁盘。**

innodb存储引擎中checkpoint分为两种：

- sharp checkpoint：在重用redo log文件(例如切换日志文件)的时候，将所有已记录到redo log中对应的脏数据刷到磁盘。
- fuzzy checkpoint：一次只刷一小部分的日志到磁盘，而非将所有脏日志刷盘。有以下几种情况会触发该检查点：
  - master thread checkpoint：由master线程控制，**每秒或每10秒**刷入一定比例的脏页到磁盘。
  - flush_lru_list checkpoint：从MySQL5.6开始可通过 innodb_page_cleaners 变量指定专门负责脏页刷盘的page cleaner线程的个数，该线程的目的是为了保证lru列表有可用的空闲页。
  - async/sync flush checkpoint：同步刷盘还是异步刷盘。例如还有非常多的脏页没刷到磁盘(非常多是多少，有比例控制)，这时候会选择同步刷到磁盘，但这很少出现；如果脏页不是很多，可以选择异步刷到磁盘，如果脏页很少，可以暂时不刷脏页到磁盘
  - dirty page too much checkpoint：脏页太多时强制触发检查点，目的是为了保证缓存有足够的空闲空间。too much的比例由变量 innodb_max_dirty_pages_pct 控制，MySQL 5.6默认的值为75，即当脏页占缓冲池的百分之75后，就强制刷一部分脏页到磁盘。

由于刷脏页需要一定的时间来完成，所以记录检查点的位置是在每次刷盘结束之后才在redo log中标记的。

> MySQL停止时是否将脏数据和脏日志刷入磁盘，由变量innodb_fast_shutdown={ 0|1|2  }控制，默认值为1，即停止时只做一部分purge，忽略大多数flush操作(但至少会刷日志)，在下次启动的时候再flush剩余的内容，实现fast shutdown。



### **二进制日志（`binlog`）**

**什么是`binlog`？**

`binlog`记录了数据库表结构和表数据变更，比如`update/delete/insert/truncate/create`。它不会记录`select`（因为这没有对表没有进行变更）

`binlog`我们可以简单理解为：存储着每条变更的`SQL`语句（当然从下面的图看来看，不止SQL，还有XID「事务Id」等等）

![img](https://mmbiz.qpic.cn/sz_mmbiz_jpg/2BGWl1qPxib3SEnwZ7m4kDYIic90VDw9UjlU0UN3CiaXoZRF6tsIuHlLFDicwgk6BaX5ySeUnGichSWibxN3Z4du8FPA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**`binlog`一般用来做什么？**

主要有两个作用：**复制和恢复数据**

- MySQL在公司使用的时候往往都是**一主多从**结构的，从服务器需要与主服务器的数据保持一致，这就是通过`binlog`来实现的
- 数据库的数据被干掉了，我们可以通过`binlog`来对数据进行恢复。

因为`binlog`记录了数据库表的变更，所以我们可以用`binlog`进行复制（主从复制)和恢复数据。



二进制日志`binlog`是服务层的日志，还被称为归档日志。`binlog`主要记录数据库的变化情况，内容包括数据库所有的更新操作。所有涉及数据变动的操作，都要记录进二进制日志中。因此有了`binlog`可以很方便的对数据进行复制和备份，因而也常用作主从库的同步。

这里binlog所存储的内容看起来似乎与`redo log`很相似，但是其实不然。`redo log`是一种物理日志，记录的是实际上对某个数据进行了怎么样的修改；而`binlog`是逻辑日志，记录的是SQL语句的原始逻辑，比如”给ID=2这一行的a字段加1 "。`binlog`日志中的内容是二进制的，根据日记格式参数的不同，可能基于SQL语句、基于数据本身或者二者的混合。一般常用记录的都是SQL语句。

这里的物理和逻辑的概念，我的个人理解是：

> 物理的日志可看作是实际数据库中数据页上的变化信息，只看重结果，而不在乎是通过“何种途径”导致了这种结果；
>
> 逻辑的日志可看作是通过了某一种方法或者操作手段导致数据发生了变化，存储的是逻辑性的操作。

同时，`redo log`是基于crash recovery，保证MySQL宕机后的数据恢复；而`binlog`是基于point-in-time recovery，保证服务器可以基于时间点对数据进行恢复，或者对数据进行备份。

事实上最开始MySQL是没有`redo log`日志的。因为起先MySQL是没有InnoDB引擎的，自带的引擎是MyISAM。`binlog`是服务层的日志，因此所有引擎都能够使用。但是光靠`binlog`日志只能提供归档的作用，无法提供crash-safe能力，所以InnoDB引擎就采用了学自于Oracle的技术，也就是`redo log`，这才拥有了crash-safe能力。这里对`redo log`日志和`binlog`日志的特点分别进行了对比：![img](https://mmbiz.qpic.cn/mmbiz_jpg/TdGLaSU675iaCHFO63Imian2ibWop8NxviaumzcdHzgIAdthM4YofuA7fE35JbCaOnnAlNkj2HcVlCHUmeGzrakJmg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

在MySQL执行更新语句时，都会涉及到`redo log`日志和`binlog`日志的读写。一条更新语句的执行过程如下：

![img](https://mmbiz.qpic.cn/mmbiz_png/TdGLaSU675hcsS4wOSWWZhZ2WayIL6wVQoV44BicNcjAPlb0gtibRVAOfuZj1Wy49yV8Q89V4FBaeibGnqiczwZCRA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

从上图可以看出，MySQL在执行更新语句的时候，在服务层进行语句的解析和执行，在引擎层进行数据的提取和存储；同时在服务层对`binlog`进行写入，在InnoDB内进行`redo log`的写入。

不仅如此，在对`redo log`写入时有两个阶段的提交，一是`binlog`写入之前prepare状态的写入，二是`binlog`写入之后commit状态的写入。

之所以要安排这么一个两阶段提交，自然是有它的道理的。现在我们可以假设不采用两阶段提交的方式，而是采用“单阶段”进行提交，即要么先写入`redo log`，后写入`binlog`；要么先写入`binlog`，后写入`redo log`。这两种方式的提交都会导致原先数据库的状态和被恢复后的数据库的状态不一致。

**先写入`redo log`，后写入`binlog`：**

在写完`redo log`之后，数据此时具有crash-safe能力，因此系统崩溃，数据会恢复成事务开始之前的状态。但是，若在`redo log`写完时候，`binlog`写入之前，系统发生了宕机。此时`binlog`没有对上面的更新语句进行保存，导致当使用binlog进行数据库的备份或者恢复时，就少了上述的更新语句。从而使得id=2这一行的数据没有被更新。

由此可见，两阶段的提交就是为了避免上述的问题，使得`binlog`和`redo log`中保存的信息是一致的。

![img](https://mmbiz.qpic.cn/mmbiz_png/TdGLaSU675hcsS4wOSWWZhZ2WayIL6wV4czM4JJo5HibPI7vicHv5yNWzO11NpRTAdRH3JGO5ho2Tib9D6INMzSlw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



### **回滚日志（```undo log```）**

回滚日志同样也是InnoDB引擎提供的日志，顾名思义，回滚日志的作用就是对数据进行回滚。当事务对数据库进行修改，InnoDB引擎不仅会记录`redo log`，还会生成对应的```undo log```日志；如果事务执行失败或调用了rollback，导致事务需要回滚，就可以利用``undo log``中的信息将数据回滚到修改之前的样子。

但是```undo log```与`redo log`不一样，它属于逻辑日志。它对SQL语句执行相关的信息进行记录。当发生回滚时，InnoDB引擎会根据```undo log```日志中的记录做与之前相反的工作。比如对于每个数据插入操作（insert），回滚时会执行数据删除操作（delete）；对于每个数据删除操作（delete），回滚时会执行数据插入操作（insert）；对于每个数据更新操作（update），回滚时会执行一个相反的数据更新操作（update），把数据改回去。``undo log``由两个作用，一是提供回滚，二是实现MVCC。







## 索引

**索引有哪些数据结构**

Hash、B+

**Hash过程**

![img](https://mmbiz.qpic.cn/mmbiz_gif/uChmeeX1FpwUFWcYd1A97ia8Fde0dgBM8UVcIFNOOU5NB81Sv7CY3iaTcsdUibjYmHuSAwOLRnYKpwGIkyaPd9gXg/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

哈希表的特点就是**可以快速的精确查询，但是不支持范围查询**。

> 问个题外话，那Hash表在哪些场景比较适合？

等值查询的场景，就只有KV（Key，Value）的情况，例如Redis、Memcached等这些NoSQL的中间件。

> 你说的是无序的Hash表，那有没有有序的数据结构？

**有序数组**，它就比较优秀了呀，它在等值查询的和范围查询的时候都很Nice。

> 那它完全没有缺点么？

不是的，有序的适合静态数据，因为如果我们新增、删除、修改数据的时候就会改变他的结构。

比如你新增一个，那在你新增的位置后面所有的节点都会后移，成本很高。

> 那照你这么说他根本就不优秀啊，特点也没地方放。

此言差矣，可以用来做静态存储引擎啊，用来保存静态数据，例如你2019年的支付宝账单，2019年的淘宝购物记录等等都是很合适的，都是不会变动的历史数据。



### 背景

#### 磁盘IO和预读

先说一下磁盘IO，磁盘读取数据靠的是机械运动，每一次读取数据需要**寻道、寻点、拷贝到内存**三步操作。

**寻道**时间是磁臂移动到指定磁道所需要的时间，一般在5ms以下；

**寻点**是从磁道中找到数据存在的那个点，平均时间是半圈时间，如果是一个7200转/min的磁盘，寻点时间平均是600000/7200/2=4.17ms；

**拷贝到内存**的时间很快，和前面两个时间比起来可以忽略不计，所以一**次IO的时间平均是在9ms左右**。听起来很快，但数据库百万级别的数据过一遍就达到了9000s，显然就是灾难级别的了。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyeHJZwK0jOlicB72AqSldRrJVzpEllfzbiar6XicwOboVOSmyQqMnFNkDy9rPz5rO9Q6XkU1Qakria1g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyeHJZwK0jOlicB72AqSldRrHwZ2mIvJOAqBuwEypaKiborEBsnrpe5ZHC4sJcLn9zFm7PFFZSKujOQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

考虑到磁盘IO是非常高昂的操作，计算机操作系统做了预读的优化，当一次IO时，不光把当前磁盘地址的数据，而是把**相邻的数据**也都读取到内存缓冲区内，因为当计算机访问一个地址的数据的时候，与其相邻的数据也会很快被访问到。

每一次IO读取的数据我们称之为一页(page)，具体一页有多大数据跟操作系统有关，一般为4k或8k，也就是我们读取一页内的数据时候，实际上才发生了一次IO。

那我们想要优化数据库查询，就要**尽量减少磁盘的IO操作**，所以就出现了索引。

#### 索引是什么？

`MySQL`官方对索引的定义为：索引(Index)是帮助`MySQL`高效获取数据的数据结构。

`MySQL`中常用的索引在物理上分两类，B-树索引和哈希索引。

### [BTree索引](https://mp.weixin.qq.com/s/qESZSzHoxUKQRJhb1EQA_Q)

`BTree`又叫多路平衡查找树，一颗m叉的BTree特性如下：

- 树中每个节点最多包含m个孩子。
- 除根节点与叶子节点外，每个节点至少有[ceil(m/2)]个孩子（ceil()为向上取整）。
- 若根节点不是叶子节点，则至少有两个孩子。
- 所有的叶子节点都在同一层。
- 每个非叶子节点由n个key与n+1个指针组成，其中[ceil(m/2)-1] <= n <= m-1 。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyeHJZwK0jOlicB72AqSldRraDfPEGjZ7SRDRzx9A8SwPxhEGJ19vNZV6f8m8uEnC21K2YgUfm9T3g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

这是一个3叉（只是举例，真实会有很多叉）的BTree结构图，每一个方框块我们称之为一个磁盘块或者叫做一个block块，这是操作系统一次IO往内存中读的内容，一个块对应四个扇区，紫色代表的是磁盘块中的数据key，黄色代表的是数据data，蓝色代表的是指针p，指向下一个磁盘块的位置。

来模拟下查找key为29的data的过程：

1、根据根结点指针读取文件目录的根磁盘块1。【磁盘IO操作**1次**】

2、磁盘块1存储17，35和三个指针数据。我们发现17<29<35，因此我们找到指针p2。

3、根据p2指针，我们定位并读取磁盘块3。【磁盘IO操作**2次**】

4、磁盘块3存储26，30和三个指针数据。我们发现26<29<30，因此我们找到指针p2。

5、根据p2指针，我们定位并读取磁盘块8。【磁盘IO操作**3次**】

6、磁盘块8中存储28，29。我们找到29，获取29所对应的数据data。

> 由此可见，BTree索引使每次磁盘I/O取到内存的数据都发挥了作用，从而提高了查询效率。

**但是有没有什么可优化的地方呢？**

我们从图上可以看到，每个节点中不仅包含数据的key值，还有data值。而每一个页的存储空间是有限的，如果data数据较大时将会导致每个节点（即一个页）能存储的key的数量很小，当存储的数据量很大时同样会导致B-Tree的深度较大，增大查询时的磁盘I/O次数，进而影响查询效率。





### B+Tree索引

`B+Tree`是在`B-Tree`基础上的一种优化，使其更适合实现外存储索引结构。在B+Tree中，所有数据记录节点都是按照键值大小顺序存放在同一层的叶子节点上，而非叶子节点上只存储key值信息，这样可以大大加大每个节点存储的key值数量，降低B+Tree的高度。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpyeHJZwK0jOlicB72AqSldRrhtQWiaBRz65Q1jWgNQGnd3KHOFRqibz7asHxaa96bUGdrRu159pDuu3A/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**B+Tree相对于B-Tree有几点不同：**

非叶子节点只存储键值信息， 数据记录都存放在叶子节点中， 将上一节中的B-Tree优化，由于B+Tree的非叶子节点只存储键值信息，所以B+Tree的高度可以被压缩到特别的低。

具体的数据如下：

> InnoDB存储引擎中页的大小为16KB，一般表的主键类型为INT（占用4个字节）或BIGINT（占用8个字节），指针类型也一般为4或8个字节，也就是说一个页（B+Tree中的一个节点）中大概存储16KB/(8B+8B)=1K个键值（因为是估值，为方便计算，这里的K取值为〖10〗^3）。
>
> 也就是说一个深度为3的B+Tree索引可以维护10^3 * 10^3 * 10^3 = 10亿 条记录。（这种计算方式存在误差，而且没有计算叶子节点，如果计算叶子节点其实是深度为4了）

我们只需要进行三次的IO操作就可以从10亿条数据中找到我们想要的数据，比起最开始的百万数据9000秒不知道好了多少个华莱士了。

而且在B+Tree上通常有两个头指针，一个指向根节点，另一个指向关键字最小的叶子节点，而且所有叶子节点（即数据节点）之间是一种链式环结构。所以我们除了可以对B+Tree进行主键的范围查找和分页查找，还可以从根节点开始，进行随机查找。

数据库中的B+Tree索引可以分为聚集索引（clustered index）和辅助索引（secondary index）。

上面的B+Tree示例图在数据库中的实现即为聚集索引，聚集索引的B+Tree中的叶子节点存放的是整张表的行记录数据，辅助索引与聚集索引的区别在于辅助索引的叶子节点并不包含行记录的全部数据，而是存储相应行数据的聚集索引键，即主键。

当通过辅助索引来查询数据时，InnoDB存储引擎会遍历辅助索引找到主键，然后再通过主键在聚集索引中找到完整的行记录数据。

![img](https://mmbiz.qpic.cn/mmbiz_gif/uChmeeX1FpyeHJZwK0jOlicB72AqSldRrJR88Ko3YEJib3rVE5X2MLTXKjAqeM1dOcxNHag0YVNhbib1NLGAicH1Dw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

不过，虽然索引可以加快查询速度，提高 MySQL 的处理性能，但是过多地使用索引也会造成以下**弊端**：

- 创建索引和维护索引要耗费时间，这种时间随着数据量的增加而增加。
- 除了数据表占数据空间之外，每一个索引还要占一定的物理空间。如果要建立聚簇索引，那么需要的空间就会更大。
- 当对表中的数据进行增加、删除和修改的时候，索引也要动态地维护，这样就降低了数据的维护速度。

> 注意：索引可以在一些情况下加速查询，但是在某些情况下，会降低效率。

索引只是提高效率的一个因素，因此在建立索引的时候应该遵循以下原则：

- 在经常需要搜索的列上建立索引，可以加快搜索的速度。
- 在作为主键的列上创建索引，强制该列的唯一性，并组织表中数据的排列结构。
- 在经常使用表连接的列上创建索引，这些列主要是一些外键，可以加快表连接的速度。
- 在经常需要根据范围进行搜索的列上创建索引，因为索引已经排序，所以其指定的范围是连续的。
- 在经常需要排序的列上创建索引，因为索引已经排序，所以查询时可以利用索引的排序，加快排序查询。
- 在经常使用 WHERE 子句的列上创建索引，加快条件的判断速度。

现在大家知道索引为啥能这么快了吧，其实就是一句话，通过索引的结构最大化的减少数据库的IO次数，毕竟，一次IO的时间真的是太久了。。。

### B+ Tree 原理

B+树是B树的升级版，只是把非叶子节点冗余一下，这么做的好处是**为了提高范围查找的效率**。

提高了的原因也无非是会有指针指向下一个节点的叶子节点。

#### 数据结构

B Tree 指的是 Balance Tree，也就是平衡树，平衡树是一颗查找树，并且所有叶子节点位于同一层。

**B+ Tree 是 B 树的一种变形，它是基于 B Tree 和叶子节点顺序访问指针进行实现，通常用于数据库和操作系统的文件系统中。**

B+ 树有两种类型的节点：内部节点（也称索引节点）和叶子节点，内部节点就是非叶子节点，内部节点不存储数据，只存储索引，数据都存在叶子节点。

内部节点中的 key 都按照从小到大的顺序排列，对于内部节点中的一个 key，左子树中的所有 key 都小于它，右子树中的 key 都大于等于它，叶子节点的记录也是按照从小到大排列的。

每个叶子节点都存有相邻叶子节点的指针。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NT3GcgC6qgN63zsZk932mZdib9nuGQYHHxgd3icfOG32nZh973IgrmBwNA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 操作

**查找**

查找以典型的方式进行，类似于二叉查找树。起始于根节点，自顶向下遍历树，选择其分离值在要查找值的任意一边的子指针。在节点内部典型的使用是二分查找来确定这个位置。

**插入**

- Perform a search to determine what bucket the new record should go into.

- If the bucket is not full(a most b - 1 entries after the insertion，b 是节点中的元素个数，一般是页的整数倍),add tht record.

- Otherwise,before inserting the new record

- - original node has 「(L+1)/2」items
  - new node has 「(L+1)/2」items
  - split the bucket.
  - Move  「(L+1)/2」-th key to the parent,and insert the new node to the parent.
  - Repeat until a parent is found that need not split.

- If the root splits,treat it as if it has an empty parent ans split as outline above.

B-trees grow as the root and not at the leaves.

**删除**

和插入类似，只不过是自下而上的合并操作。

#### 树的常见特性

**AVL 树**

平衡二叉树，一般是用平衡因子差值决定并通过旋转来实现，左右子树树高差不超过1，那么和红黑树比较它是严格的平衡二叉树，平衡条件非常严格（树高差只有1），只要插入或删除不满足上面的条件就要通过旋转来保持平衡。由于旋转是非常耗费时间的。所以 AVL 树适用于插入/删除次数比较少，但查找多的场景。

**红黑树**

通过对从根节点到叶子节点路径上各个节点的颜色进行约束，确保没有一条路径会比其他路径长2倍，因而是近似平衡的。所以相对于严格要求平衡的AVL树来说，它的旋转保持平衡次数较少。适合，查找少，插入/删除次数多的场景。（现在部分场景使用跳表来替换红黑树，可搜索“为啥 redis 使用跳表(skiplist)而不是使用 red-black？”）

**B/B+ 树**

多路查找树，出度高，磁盘IO低，一般用于数据库系统中。

#### B + 树与红黑树的比较

红黑树等平衡树也可以用来实现索引，但是文件系统及数据库系统普遍采用 B+ Tree 作为索引结构，主要有以下两个原因：

（一）磁盘 IO 次数

B+ 树一个节点可以存储多个元素，相对于红黑树的树高更低，磁盘 IO 次数更少。

（二）磁盘预读特性

为了减少磁盘 I/O 操作，磁盘往往不是严格按需读取，而是每次都会预读。预读过程中，磁盘进行顺序读取，顺序读取不需要进行磁盘寻道。每次会读取页的整数倍。

操作系统一般将内存和磁盘分割成固定大小的块，每一块称为一页，内存与磁盘以页为单位交换数据。数据库系统将索引的一个节点的大小设置为页的大小，使得一次 I/O 就能完全载入一个节点。

#### B + 树与 B 树的比较

**B+ 树的磁盘 IO 更低**

B+ 树的内部节点并没有指向关键字具体信息的指针。因此其内部节点相对 B 树更小。如果把所有同一内部结点的关键字存放在同一盘块中，那么盘块所能容纳的关键字数量也越多。一次性读入内存中的需要查找的关键字也就越多。相对来说IO读写次数也就降低了。

**B+ 树的查询效率更加稳定**

由于非叶子结点并不是最终指向文件内容的结点，而只是叶子结点中关键字的索引。所以任何关键字的查找必须走一条从根结点到叶子结点的路。所有关键字查询的路径长度相同，导致每一个数据的查询效率相当。

**B+ 树元素遍历效率高**

B 树在提高了磁盘IO性能的同时并没有解决元素遍历的效率低下的问题。正是为了解决这个问题，B+树应运而生。B+树只要遍历叶子节点就可以实现整棵树的遍历。而且在数据库中基于范围的查询是非常频繁的，而 B 树不支持这样的操作（或者说效率太低）。

### MySQL 索引

索引是在存储引擎层实现的，而不是在服务器层实现的，所以不同存储引擎具有不同的索引类型和实现。

#### B+ Tree 索引

是大多数 MySQL 存储引擎的默认索引类型。

- 因为不再需要进行全表扫描，只需要对树进行搜索即可，所以查找速度快很多。
- 因为 B+ Tree 的有序性，所以除了用于查找，还可以用于排序和分组。
- 可以指定多个列作为索引列，多个索引列共同组成键。
- 适用于全键值、键值范围和键前缀查找，其中键前缀查找只适用于最左前缀查找。如果不是按照索引列的顺序进行查找，则无法使用索引。

InnoDB 的 B+Tree 索引分为主索引和辅助索引。主索引的叶子节点 data 域记录着完整的数据记录，这种索引方式被称为聚簇索引。因为无法把数据行存放在两个不同的地方，所以一个表只能有一个聚簇索引。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NT4u7Q1jkb9dRLSkQN6KnUyIAGGPg8fCgYsFs06yZSpr1pe9hE4IDtGA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

辅助索引的叶子节点的 data 域记录着主键的值，因此在使用辅助索引进行查找时，需要先查找到主键值，然后再到主索引中进行查找，这个过程也被称作回表。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTVwSEmEEtZFEiahLGibwt2SPzhA2Sym5NSiaeEdcGciasVuIIia6jDl8REqQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 哈希索引

哈希索引能以 O(1) 时间进行查找，但是失去了有序性：

- 无法用于排序与分组；
- 只支持精确查找，无法用于部分查找和范围查找。

InnoDB 存储引擎有一个特殊的功能叫“自适应哈希索引”，当某个索引值被使用的非常频繁时，会在 B+Tree 索引之上再创建一个哈希索引，这样就让 B+Tree 索引具有哈希索引的一些优点，比如快速的哈希查找。

#### 全文索引

MyISAM 存储引擎支持全文索引，用于查找文本中的关键词，而不是直接比较是否相等。

查找条件使用 MATCH AGAINST，而不是普通的 WHERE。

全文索引使用倒排索引实现，它记录着关键词到其所在文档的映射。

InnoDB 存储引擎在 MySQL 5.6.4 版本中也开始支持全文索引。

#### 空间数据索引

MyISAM 存储引擎支持空间数据索引（R-Tree），可以用于地理数据存储。空间数据索引会从所有维度来索引数据，可以有效地使用任意维度来进行组合查询。

必须使用 GIS 相关的函数来维护数据。



### 索引的优点

- 大大减少了服务器需要扫描的数据行数。
- 帮助服务器避免进行排序和分组，以及避免创建临时表（B+Tree 索引是有序的，可以用于 ORDER BY 和 GROUP BY 操作。临时表主要是在排序和分组过程中创建，不需要排序和分组，也就不需要创建临时表）。
- 将随机 I/O 变为顺序 I/O（B+Tree 索引是有序的，会将相邻的数据都存储在一起）。



### 索引的使用条件

- 对于非常小的表、大部分情况下简单的全表扫描比建立索引更高效；
- 对于中到大型的表，索引就非常有效；
- 但是对于特大型的表，建立和维护索引的代价将会随之增长。这种情况下，需要用到一种技术可以直接区分出需要查询的一组数据，而不是一条记录一条记录地匹配，例如可以使用分区技术。

> **为什么对于非常小的表，大部分情况下简单的全表扫描比建立索引更高效？**
>
> 如果一个表比较小，那么显然直接遍历表比走索引要快（因为需要回表）。
>
> 注：首先，要注意这个答案隐含的条件是查询的数据不是索引的构成部分，否也不需要回表操作。其次，查询条件也不是主键，否则可以直接从聚簇索引中拿到数据。



### [如何合理创建索引](https://mp.weixin.qq.com/s/-gmAPfiKMNJgHhIZqR2C4A)

上面谈的其实就是索引**最基本**的东西，N叉树，跳表、LSM我都没讲，同时要创建出好的索引要顾及到很多的方面：

- **最左前缀匹配原则**。这是非常重要、非常重要、非常重要（重要的事情说三遍）的原则，MySQL会一直向右匹配直到遇到范围查询 （>,<,BETWEEN,LIKE）就停止匹配。
- 尽量选择**区分度高的列作为索引**，区分度的公式是 COUNT(DISTINCT col)/COUNT(*)。表示字段不重复的比率，比率越大我们扫描的记录数就越少。
- **索引列不能参与计算，尽量保持列“干净”**。比如， FROM_UNIXTIME(create_time)='2016-06-06' 就不能使用索引，原因很简单，**B+树中存储的都是数据表中的字段值**，但是进行检索时，需要把所有元素都应用函数才能比较，显然这样的代价太大。所以语句要写成 ：create_time=UNIX_TIMESTAMP('2016-06-06')。
- 尽可能的**扩展索引**，不要新建立索引。比如表中已经有了a的索引，现在要加（a,b）的索引，那么只需要修改原来的索引即可。
- 单个多列组合索引和多个单列索引的检索查询效果不同，因为在执行SQL时，***MySQL只能使用一个索引**，会从多个单列索引中选择一个限制最为严格的索引*(经指正，在MySQL5.0以后的版本中，有“合并索引”的策略，翻看了《高性能MySQL 第三版》，书作者认为：**还是应该建立起比较好的索引，而不应该依赖于“合并索引”这么一个策略**)。
- “合并索引”策略简单来讲，就是使用多个单列索引，然后将这些结果用“union或者and”来合并起来



#### 索引不生效的原因

1、索引列是表示式的一部分，或是函数的一部分

如下 SQL：

```
SELECT book_id FROM BOOK WHERE book_id + 1 = 5;
```

或者

```
SELECT book_id FROM BOOK WHERE TO_DAYS(CURRENT_DATE) - TO_DAYS(gmt_create) <= 10
```

上述两个 SQL 虽然在列 book_id 和 gmt_create 设置了索引 ，但由于它们是表达式或函数的一部分，导致索引无法生效，最终导致全表扫描。

2、隐式类型转换

以上两种情况相信不少人都知道索引不能生效，但下面这种隐式类型转换估计会让不少人栽跟头，来看下下面这个例子:

假设有以下表:

```
CREATE TABLE `tradelog` (
  `id` int(11) NOT NULL,
  `tradeid` varchar(32) DEFAULT NULL,
  `operator` int(11) DEFAULT NULL,
  `t_modified` datetime DEFAULT NULL,
   PRIMARY KEY (`id`),
   KEY `tradeid` (`tradeid`),
   KEY `t_modified` (`t_modified`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

执行 SQL 语句

```
SELECT * FROM tradelog WHERE tradeid=110717;
```

交易编号 tradeid 上有索引，但用 EXPLAIN 执行却发现使用了全表扫描，为啥呢，tradeId 的类型是 varchar(32), 而此 SQL 用 tradeid 一个数字类型进行比较，发生了隐形转换，会隐式地将字符串转成整型，如下:

```
mysql> SELECT * FROM tradelog WHERE CAST(tradid AS signed int) = 110717;
```

这样也就触发了上文中第一条的规则 ，即：索引列不能是函数的一部分。

3、隐式编码转换

这种情况非常隐蔽，来看下这个例子

```
CREATE TABLE `trade_detail` ( 
 `id` int(11) NOT NULL, 
 `tradeid` varchar(32) DEFAULT NULL, 
 `trade_step` int(11) DEFAULT NULL, /*操作步骤*/ 
 `step_info` varchar(32) DEFAULT NULL, /*步骤信息*/ 
   PRIMARY KEY (`id`), KEY `tradeid` (`tradeid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

trade_defail 是交易详情， tradelog 是操作此交易详情的记录，现在要查询 id=2 的交易的所有操作步骤信息，则我们会采用如下方式

```
SELECT d.* FROM tradelog l, trade_detail d WHERE d.tradeid=l.tradeid AND l.id=2;
```

由于 tradelog 与 trade_detail 这两个表的字符集不同，且 tradelog 的字符集是 utf8mb4，而  trade_detail 字符集是 utf8, utf8mb4 是 utf8 的超集，所以会自动将 utf8 转成  utf8mb4。即上述语句会发生如下转换:

```
SELECT d.* FROM tradelog l, trade_detail d WHERE (CONVERT(d.traideid USING utf8mb4)))=l.tradeid AND l.id=2;
```

自然也就触发了 「索引列不能是函数的一部分」这条规则。怎么解决呢，第一种方案当然是把两个表的字符集改成一样，如果业务量比较大，生产上不方便改的话，还有一种方案是把 utf8mb4 转成 utf8，如下

```
mysql> SELECT d.* FROM tradelog l , trade_detail d WHERE d.tradeid=CONVERT(l.tradeid USING utf8) AND l.id=2; 
```

这样索引列就生效了。

4、使用 order by 造成的全表扫描

```
SELECT * FROM user ORDER BY age DESC
```

上述语句在 age 上加了索引，但依然造成了全表扫描，这是因为我们使用了 SELECT *,导致回表查询，MySQL 认为回表的代价比全表扫描更大，所以不选择使用索引，如果想使用到 age 的索引，我们可以用覆盖索引来代替:

```
SELECT age FROM user ORDER BY age DESC
```

或者加上 limit 的条件（数据比较小）

```
SELECT * FROM user ORDER BY age DESC limit 10
```

这样就能利用到索引。

#### 无法避免对索引列使用函数，怎么使用索引

有时候我们无法避免对索引列使用函数，但这样做会导致全表索引，是否有更好的方式呢。

比如我现在就是想记录 2016 ~ 2018 所有年份 7月份的交易记录总数

```
mysql> SELECT count(*) FROM tradelog WHERE month(t_modified)=7;
```

由于索引列是函数的参数，所以显然无法用到索引，我们可以将它改造成基本字段区间的查找如下

```
SELECT count(*) FROM tradelog WHERE
    -> (t_modified >= '2016-7-1' AND t_modified<'2016-8-1') or
    -> (t_modified >= '2017-7-1' AND t_modified<'2017-8-1') or 
    -> (t_modified >= '2018-7-1' AND t_modified<'2018-8-1');
```

##### 前缀索引与索引选择性

之前我们说过，如于长字符串的字段（如 url），我们可以用伪哈希索引的形式来创建索引，以避免索引变得既大又慢，除此之外其实还可以用前缀索引（字符串的部分字符）的形式来达到我们的目的，那么这个前缀索引应该如何选取呢，这叫涉及到一个叫索引选择性的概念

> 索引选择性：不重复的索引值（也称为基数，cardinality）和数据表的记录总数的比值，比值越高，代表索引的选择性越好，唯一索引的选择性是最好的，比值是 1。

画外音：我们可以通过 **SHOW INDEXES FROM table** 来查看每个索引 cardinality 的值以评估索引设计的合理性

怎么选择这个比例呢，我们可以分别取前 3，4，5，6，7 的前缀索引，然后再比较下选择这几个前缀索引的选择性，执行以下语句

```
SELECT 
 COUNT(DISTINCT LEFT(city,3))/COUNT(*) as sel3,
 COUNT(DISTINCT LEFT(city,4))/COUNT(*) as sel4,
 COUNT(DISTINCT LEFT(city,5))/COUNT(*) as sel5,
 COUNT(DISTINCT LEFT(city,6))/COUNT(*) as sel6,
 COUNT(DISTINCT LEFT(city,7))/COUNT(*) as sel7
FROM city_demo
```

得结果如下

| sel3   | sel4   | sel5   | sel6   | sel7   |
| :----- | :----- | :----- | :----- | :----- |
| 0.0239 | 0.0293 | 0.0305 | 0.0309 | 0.0310 |

可以看到当前缀长度为 7 时，索引选择性提升的比例已经很小了，也就是说应该选择 city 的前六个字符作为前缀索引，如下

```
ALTER TABLE city_demo ADD KEY(city(6))
```

我们当前是以平均选择性为指标的，有时候这样是不够的，还得考虑最坏情况下的选择性，以这个 demo 为例，可能一些人看到选择 4，5 的前缀索引与选择 6，7 的选择性相差不大，那就得看下选择 4，5 的前缀索引分布是否均匀了

```
SELECT 
    COUNT(*) AS  cnt, 
    LEFT(city, 4) AS pref
  FROM city_demo GROUP BY pref ORDER BY cnt DESC LIMIT 5
```

可能会出现以下结果

| cnt  | pref |
| :--- | :--- |
| 305  | Sant |
| 200  | Toul |
| 90   | Chic |
| 20   | Chan |

可以看到分布极不均匀，以 Sant，Toul 为前缀索引的数量极多，这两者的选择性都不是很理想，所以要选择前缀索引时也要考虑最差的选择性的情况。

前缀索引虽然能实现索引占用空间小且快的效果，但它也有明显的弱点，MySQL 无法使用前缀索引做 ORDER BY 和 GROUP BY ，而且也无法使用前缀索引做覆盖扫描，前缀索引也有可能增加扫描行数。

假设有以下表数据及要执行的 SQL

| id   | email              |
| :--- | :----------------- |
| 1    | zhangssxyz@163.com |
| 2    | zhangs1@163.com    |
| 3    | zhangs1@163.com    |
| 4    | zhangs1@163.com    |

```
SELECT id,email FROM user WHERE email='zhangssxyz@xxx.com';
```

如果我们针对 email 设置的是整个字段的索引，则上表中根据 「zhangssxyz@163.com」查询到相关记记录后,再查询此记录的下一条记录，发现没有，停止扫描，此时可知**只扫描一行记录**，如果我们以前六个字符（即 email(6)）作为前缀索引，则显然要扫描四行记录，并且获得行记录后不得不回到主键索引再判断 email 字段的值，所以使用前缀索引要评估它带来的这些开销。

另外有一种情况我们可能需要考虑一下，如果前缀基本都是相同的该怎么办，比如现在我们为某市的市民建立一个人口信息表，则这个市人口的身份证虽然不同，但身份证前面的几位数都是相同的，这种情况该怎么建立前缀索引呢。

一种方式就是我们上文说的，针对身份证建立哈希索引，另一种方式比较巧妙，将身份证倒序存储，查的时候可以按如下方式查询:

```
SELECT field_list FROM t WHERE id_card = reverse('input_id_card_string');
```

这样就可以用身份证的后六位作前缀索引了，是不是很巧妙 ^_^

实际上上文所述的索引选择性同样适用于联合索引的设计，如果没有特殊情况，我们一般建议在建立联合索引时，把选择性最高的列放在最前面，比如，对于以下语句：

```
SELECT * FROM payment WHERE staff_id = xxx AND customer_id = xxx;
```

单就这个语句而言， (staff_id，customer_id) 和  (customer_id, staff_id) 这两个联合索引我们应该建哪一个呢，可以统计下这两者的选择性。

```
SELECT 
 COUNT(DISTINCT staff_id)/COUNT(*) as staff_id_selectivity,
 COUNT(DISTINCT customer_id)/COUNT(*) as customer_id_selectivity,
 COUNT(*)
FROM payment
```

结果为: ;

```
staff_id_selectivity: 0.0001
customer_id_selectivity: 0.0373
COUNT(*): 16049
```

从中可以看出 customer_id 的选择性更高，所以应该选择 customer_id 作为第一列。



#### 索引设计准则：三星索引

上文我们得出了一个索引列顺序的经验 法则：将选择性最高的列放在索引的最前列，这种建立在某些场景可能有用，但通常不如避免随机 IO 和 排序那么重要，这里引入索引设计中非常著名的一个准则：三星索引。

如果一个查询满足三星索引中三颗星的所有索引条件，**理论上**可以认为我们设计的索引是最好的索引。什么是三星索引

1. 第一颗星：WHERE 后面参与查询的列可以组成了单列索引或联合索引
2. 第二颗星：避免排序，即如果 SQL 语句中出现 order by colulmn，那么取出的结果集就已经是按照 column 排序好的，不需要再生成临时表
3. 第三颗星：SELECT 对应的列应该尽量是索引列，即尽量避免回表查询。

所以对于如下语句:

```
SELECT age, name, city where age = xxx and name = xxx order by age
```

设计的索引应该是 (age, name,city) 或者 (name, age,city)

当然 了三星索引是一个比较理想化的标准，实际操作往往只能满足期望中的一颗或两颗星，考虑如下语句:

```
SELECT age, name, city where age >= 10 AND age <= 20 and city = xxx order by name desc
```

假设我们分别为这三列建了联合索引，则显然它符合第三颗星（使用了覆盖索引），如果索引是（city, age, name)，则虽然满足了第一颗星，但排序无法用到索引，不满足第二颗星，如果索引是 (city, name,  age)，则第二颗星满足了，但此时 age 在 WHERE 中的搜索条件又无法满足第一星，

另外第三颗星（尽量使用覆盖索引）也无法完全满足，试想我要 SELECT 多列，要把这多列都设置为联合索引吗，这对索引的维护是个问题，因为每一次表的 CURD 都伴随着索引的更新，很可能频繁伴随着页分裂与页合并。

综上所述，三星索引只是给我们构建索引提供了一个参考，索引设计应该尽量靠近三星索引的标准，但实际场景我们一般无法同时满足三星索引，一般我们会优先选择满足第三颗星（因为回表代价较大）至于第一，二颗星就要依赖于实际的成本及实际的业务场景考虑。

## Mysql调优



### **Explain**

expain出来的信息有10列，分别是id、select_type、table、type、possible_keys、key、key_len、ref、rows、Extra。

**概要描述：**
id:选择标识符
select_type:表示查询的类型。
table:输出结果集的表
partitions:匹配的分区
type:表示表的连接类型
possible_keys:表示查询时，可能使用的索引
key:表示实际使用的索引
key_len:索引字段的长度
ref:列与索引的比较
rows:扫描出的行数(估算的行数)
filtered:按表条件过滤的行百分比
Extra:执行情况的描述和说明

**下面对这些字段出现的可能进行解释：**

一、 **id**

SELECT识别符。这是SELECT的查询序列号

 **我的理解是SQL执行的顺序的标识，SQL从大到小的执行**

1. id相同时，执行顺序由上至下

2. 如果是子查询，id的序号会递增，id值越大优先级越高，越先被执行

3. id如果相同，可以认为是一组，从上往下顺序执行；在所有组中，id值越大，优先级越高，越先执行

```
-- 查看在研发部并且名字以Jef开头的员工，经典查询
explain select e.no, e.name from emp e left join dept d on e.dept_no = d.no where e.name like 'Jef%' and d.name = '研发部';
```

![img](https://images2018.cnblogs.com/blog/512541/201808/512541-20180803143413064-173136748.png)

 

**二、select_type**

   ***\*示查询中每个select子句的类型\****

(1) SIMPLE(简单SELECT，不使用UNION或子查询等)

(2) PRIMARY(子查询中最外层查询，查询中若包含任何复杂的子部分，最外层的select被标记为PRIMARY)

(3) UNION(UNION中的第二个或后面的SELECT语句)

(4) DEPENDENT UNION(UNION中的第二个或后面的SELECT语句，取决于外面的查询)

(5) UNION RESULT(UNION的结果，union语句中第二个select开始后面所有select)

(6) SUBQUERY(子查询中的第一个SELECT，结果不依赖于外部查询)

(7) DEPENDENT SUBQUERY(子查询中的第一个SELECT，依赖于外部查询)

(8) DERIVED(派生表的SELECT, FROM子句的子查询)

(9) UNCACHEABLE SUBQUERY(一个子查询的结果不能被缓存，必须重新评估外链接的第一行)

**三、table**

显示这一步所访问数据库中表名称（显示这一行的数据是关于哪张表的），有时不是真实的表名字，可能是简称，例如上面的e，d，也可能是第几步执行的结果的简称

 

**四、type**

对表访问方式，表示MySQL在表中找到所需行的方式，又称“访问类型”。

常用的类型有： **ALL、index、range、 ref、eq_ref、const、system、****NULL（从左到右，性能从差到好）**

ALL：Full Table Scan， MySQL将遍历全表以找到匹配的行

index: Full Index Scan，index与ALL区别为index类型只遍历索引树

range:只检索给定范围的行，使用一个索引来选择行

ref: 表示上述表的连接匹配条件，即哪些列或常量被用于查找索引列上的值

eq_ref: 类似ref，区别就在使用的索引是唯一索引，对于每个索引键值，表中只有一条记录匹配，简单来说，就是多表连接中使用primary key或者 unique key作为关联条件

const、system: 当MySQL对查询某部分进行优化，并转换为一个常量时，使用这些类型访问。如将主键置于where列表中，MySQL就能将该查询转换为一个常量，system是const类型的特例，当查询的表只有一行的情况下，使用system

NULL: MySQL在优化过程中分解语句，执行时甚至不用访问表或索引，例如从一个索引列里选取最小值可以通过单独索引查找完成。

 

**五、possible_keys**

**指出MySQL能使用哪个索引在表中找到记录，查询涉及到的字段上若存在索引，则该索引将被列出，但不一定被查询使用（该查询可以利用的索引，如果没有任何索引显示 null）**

该列完全独立于EXPLAIN输出所示的表的次序。这意味着在possible_keys中的某些键实际上不能按生成的表次序使用。
如果该列是NULL，则没有相关的索引。在这种情况下，可以通过检查WHERE子句看是否它引用某些列或适合索引的列来提高你的查询性能。如果是这样，创造一个适当的索引并且再次用EXPLAIN检查查询

 

**六、Key**

**key列显示MySQL实际决定使用的键（索引），必然包含在possible_keys中**

如果没有选择索引，键是NULL。要想强制MySQL使用或忽视possible_keys列中的索引，在查询中使用FORCE INDEX、USE INDEX或者IGNORE INDEX。

 

**七、key_len**

**表示索引中使用的字节数，可通过该列计算查询中使用的索引的长度（key_len显示的值为索引字段的最大可能长度，并非实际使用长度，即key_len是根据表定义计算而得，不是通过表内检索出的）**

不损失精确性的情况下，长度越短越好 

 

**八、ref**

**列与索引的比较，表示上述表的连接匹配条件，即哪些列或常量被用于查找索引列上的值**

 

**九、rows**

 **估算出结果集行数，表示MySQL根据表统计信息及索引选用情况，估算的找到所需的记录所需要读取的行数**

 

**十、Extra**

**该列包含MySQL解决查询的详细信息,有以下几种情况：**

Using where:不用读取表中所有信息，仅通过索引就可以获取所需数据，这发生在对表的全部的请求列都是同一个索引的部分的时候，表示mysql服务器将在存储引擎检索行后再进行过滤

Using temporary：表示MySQL需要使用临时表来存储结果集，常见于排序和分组查询，常见 group by ; order by

Using filesort：当Query中包含 order by 操作，而且无法利用索引完成的排序操作称为“文件排序”

```
-- 测试Extra的filesort
explain select * from emp order by name;
```

Using join buffer：改值强调了在获取连接条件时没有使用索引，并且需要连接缓冲区来存储中间结果。如果出现了这个值，那应该注意，根据查询的具体情况可能需要添加索引来改进能。

Impossible where：这个值强调了where语句会导致没有符合条件的行（通过收集统计信息不可能存在结果）。

Select tables optimized away：这个值意味着仅通过使用索引，优化器可能仅从聚合函数结果中返回一行

No tables used：Query语句中使用from dual 或不含任何from子句

```
-- explain select now() from dual;
```

**总结：**
• EXPLAIN不会告诉你关于触发器、存储过程的信息或用户自定义函数对查询的影响情况
• EXPLAIN不考虑各种Cache
• EXPLAIN不能显示MySQL在执行查询时所作的优化工作
• 部分统计信息是估算的，并非精确值
• EXPALIN只能解释SELECT操作，其他操作要重写为SELECT后查看执行计划。



**数据库的组成**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdsIkRX56rPzJ9S1lj1svQZHcwxH43DYuJRJk0uD8vmS7pibTqqa62Zuw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

我们所谓的调优也就是在，执行器执行之前的分析器，优化器阶段完成的，那我们开发工作中怎么去调优的呢？

帅丙一般在开发涉及SQL的业务都会去本地环境跑一遍SQL，用explain去看一下执行计划，看看分析的结果是否符合自己的预期，用没用到相关的索引，然后再去线上环境跑一下看看执行时间（这里只有查询语句，修改语句也无法在线上执行）。

遇SQL不决explain，但是这里就要说到第一个坑了。

##### **排除缓存干扰**

有可能是走了数据库缓存，在执行SQL的时候，记得加上SQL NoCache去跑SQL，这样跑出来的时间就是真实的查询时间了。

大家如果是8.0以上的版本就不用担心这个问题，如果是8.0之下的版本，记得排除缓存的干扰。

##### **Explain**

**explain你记得哪些字段，分别有什么含义？**

**那我再问大家一下，你们认为统计这个统计的行数就是完全对的么？索引一定会走到最优索引么？**

行数只是一个接近的数字，不是完全正确的，索引也不一定就是走最优的，是可能走错的。

一般走错都是因为优化器在选择的时候发现，走A索引没有额外的代价，比如走B索引并不能直接拿到我们的值，还需要回到主键索引才可以拿到，多了一次回表的过程，这个也是会被优化器考虑进去的。

他发现走A索引不需要回表，没有额外的开销，所有他选错了。

如果是上面的统计信息错了，那简单，我们用analyze table tablename 就可以重新统计索引信息了，所以在实践中，如果你发现explain的结果预估的rows值跟实际情况差距比较大，可以采用这个方法来处理。

还有一个方法就是force index强制走正确的索引，或者优化SQL，最后实在不行，可以新建索引，或者删掉错误的索引。

##### **覆盖索引**

索引包含所有需要查询的字段的值。

具有以下优点：

- 索引通常远小于数据行的大小，只读取索引能大大减少数据访问量。
- 一些存储引擎（例如 MyISAM）在内存中只缓存索引，而数据依赖于操作系统来缓存。因此，只访问索引可以不使用系统调用（通常比较费时）。
- 对于 InnoDB 引擎，若辅助索引能够覆盖查询，则无需访问主索引。

上面我提到了，可能需要回表这样的操作，那我们怎么能做到不回表呢？在自己的索引上就查到自己想要的，不要去主键索引查了。

覆盖索引

如果在我们建立的索引上就已经有我们需要的字段，就不需要回表了，在电商里面也是很常见的，我们需要去商品表通过各种信息查询到商品id，id一般都是主键，可能sql类似这样：

```
select itemId from itemCenter where size between 1 and 6
```

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdbogaIRdPMI9UGHfV0gmaBibs2aibkqjicRaU3FMPWG6N9zmL8ialIgoplg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

因为商品id itemId一般都是主键，在size索引上肯定会有我们这个值，这个时候就不需要回主键表去查询id信息了。

由于覆盖索引可以减少树的搜索次数，显著提升查询性能，所以使用覆盖索引是一个常用的性能优化手段。

##### 联合索引

还是商品表举例，我们需要根据他的名称，去查他的库存，假设这是一个很高频的查询请求，你会怎么建立索引呢？

大家可以思考上面的回表的消耗对SQL进行优化。

是的建立一个，名称和库存的联合索引，这样名称查出来就可以看到库存了，不需要查出id之后去回表再查询库存了，联合索引在我们开发过程中也是常见的，但是并不是可以一直建立的，大家要思考索引占据的空间。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdVD2avC7eId86BoSCr0YmWIwZ5vKotylv1RoCyoeXVppVXOu7mN2JRg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

刚才我举的例子其实有点生硬，正常通过商品名称去查询库存的请求是不多的，但是也不代表没有哈，真来了，难道我们去全表扫描？

##### 最左匹配原则

大家在写sql的时候，最好能利用到现有的SQL最大化利用，像上面的场景，如果利用一个模糊查询 itemname like ’敖丙%‘，这样还是能利用到这个索引的，而且如果有这样的联合索引，大家也没必要去新建一个商品名称单独的索引了。

很多时候我们索引可能没建对，那你调整一下顺序，可能就可以优化到整个SQL了。

##### 索引下推

MySQL 5.6 引入的索引下推优化（index condition pushdown)， 可以在索引遍历过程中，对索引中包含的字段先做判断，直接过滤掉不满足条件的记录，减少回表次数。

##### 唯一索引普通索引选择难题

这个在我的面试视频里面其实问了好几次了，核心是需要回答到change buffer，那change buffer又是个什么东西呢？

当需要更新一个数据页时，如果数据页在内存中就直接更新，而如果这个数据页还没有在内存中的话，在不影响数据一致性的前提下，InooDB会将这些更新操作缓存在change buffer中，这样就不需要从磁盘中读入这个数据页了。

在下次查询需要访问这个数据页的时候，将数据页读入内存，然后执行change buffer中与这个页有关的操作，通过这种方式就能保证这个数据逻辑的正确性。

需要说明的是，虽然名字叫作change buffer，实际上它是可以持久化的数据。也就是说，change buffer在内存中有拷贝，也会被写入到磁盘上。

将change buffer中的操作应用到原数据页，得到最新结果的过程称为merge。

除了访问这个数据页会触发merge外，系统有后台线程会定期merge。在数据库正常关闭（shutdown）的过程中，也会执行merge操作。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdJDYUT3ic7xe6r3o64DgNojLb6S26DOibWfksos9sCRdIYTN9AdGkc1Eg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

显然，如果能够将更新操作先记录在change buffer，减少读磁盘，语句的执行速度会得到明显的提升。而且，数据读入内存是需要占用buffer pool的，所以这种方式还能够避免占用内存，提高内存利用率

那么，**什么条件下可以使用change buffer呢？**

对于唯一索引来说，所有的更新操作都要先判断这个操作是否违反唯一性约束。

要判断表中是否存在这个数据，而这必须要将数据页读入内存才能判断，如果都已经读入到内存了，那直接更新内存会更快，就没必要使用change buffer了。

因此，唯一索引的更新就不能使用change buffer，实际上也只有普通索引可以使用。

change buffer用的是buffer pool里的内存，因此不能无限增大，change  buffer的大小，可以通过参数innodb_change_buffer_max_size来动态设置，这个参数设置为50的时候，表示change buffer的大小最多只能占用buffer pool的50%。

将数据从磁盘读入内存涉及随机IO的访问，是数据库里面成本最高的操作之一，change buffer因为减少了随机磁盘访问，所以对更新性能的提升是会很明显的。

**change buffer的使用场景**

因为merge的时候是真正进行数据更新的时刻，而change buffer的主要目的就是将记录的变更动作缓存下来，所以在一个数据页做merge之前，change buffer记录的变更越多（也就是这个页面上要更新的次数越多），收益就越大。

因此，对于写多读少的业务来说，页面在写完以后马上被访问到的概率比较小，此时change buffer的使用效果最好，这种业务模型常见的就是账单类、日志类的系统。

反过来，假设一个业务的更新模式是写入之后马上会做查询，那么即使满足了条件，将更新先记录在change buffer，但之后由于马上要访问这个数据页，会立即触发merge过程。这样随机访问IO的次数不会减少，反而增加了change  buffer的维护代价，所以，对于这种业务模式来说，change buffer反而起到了副作用。

##### 前缀索引

**对于 BLOB、TEXT 和 VARCHAR 类型的列，必须使用前缀索引，只索引开始的部分字符。**

**前缀长度的选取需要根据索引选择性来确定。**

我们存在邮箱作为用户名的情况，每个人的邮箱都是不一样的，那我们是不是可以在邮箱上建立索引，但是邮箱这么长，我们怎么去建立索引呢？

MySQL是支持前缀索引的，也就是说，你可以定义字符串的一部分作为索引。默认地，如果你创建索引的语句不指定前缀长度，那么索引就会包含整个字符串。

**我们是否可以建立一个区分度很高的前缀索引，达到优化和节约空间的目的呢？**

使用前缀索引，定义好长度，就可以做到既节省空间，又不用额外增加太多的查询成本。

上面说过覆盖索引了，覆盖索引是不需要回表的，但是前缀索引，即使你的联合索引已经包涵了相关信息，他还是会回表，因为他不确定你到底是不是一个完整的信息，就算你是www.aobing@mogu.com一个完整的邮箱去查询，他还是不知道你是否是完整的，所以他需要回表去判断一下。

**下面这个也是我在阿里面试面试官问过我的，很长的字段，想做索引我们怎么去优化他呢？**

因为存在一个磁盘占用的问题，索引选取的越长，占用的磁盘空间就越大，相同的数据页能放下的索引值就越少，搜索的效率也就会越低。

我当时就回答了一个hash，把字段hash为另外一个字段存起来，每次校验hash就好了，hash的索引也不大。

我们都知道只要区分度过高，都可以，那我们可以采用倒序，或者删减字符串这样的情况去建立我们自己的区分度，不过大家需要注意的是，调用函数也是一次开销哟，这点当时没注意。

就比如本来是www.aobing@qq,com 其实前面的`www.`基本上是没任何区分度的，所有人的邮箱都是这么开头的，你一搜一大堆出来，放在索引还浪费内存，你可以substring()函数截取掉前面的，然后建立索引。

我们所有人的身份证都是区域开头的，同区域的人很多，那怎么做良好的区分呢？REVERSE（）函数翻转一下，区分度可能就高了。

这些操作都用到了函数，我就说一下函数的坑。

##### 条件字段函数操作

日常开发过程中，大家经常对很多字段进行函数操作，如果对日期字段操作，浮点字符操作等等，大家需要注意的是，如果对字段做了函数计算，就用不上索引了，这是MySQL的规定。

对索引字段做函数操作，可能会破坏索引值的有序性，因此优化器就决定放弃走树搜索功能。

需要注意的是，优化器并不是要放弃使用这个索引。

这个时候大家可以用一些取巧的方法，比如 select * from tradelog where id + 1 = 10000 就走不上索引，select * from tradelog where id = 9999就可以。

##### 隐式类型转换

select * from t where id = 1

如果id是字符类型的，1是数字类型的，你用explain会发现走了全表扫描，根本用不上索引，为啥呢？

因为MySQL底层会对你的比较进行转换，相当于加了 CAST( id AS signed int) 这样的一个函数，上面说过函数会导致走不上索引。

##### 隐式字符编码转换

还是一样的问题，如果两个表的字符集不一样，一个是utf8mb4，一个是utf8，因为utf8mb4是utf8的超集，所以一旦两个字符比较，就会转换为utf8mb4再比较。

转换的过程相当于加了CONVERT(id USING utf8mb4)函数，那又回到上面的问题了，用到函数就用不上索引了。

还有大家一会可能会遇到mysql突然卡顿的情况，那可能是MySQLflush了。

**flush**

redo log大家都知道，也就是我们对数据库操作的日志，他是在内存中的，每次操作一旦写了redo log就会立马返回结果，但是这个redo log总会找个时间去更新到磁盘，这个操作就是flush。

在更新之前，当内存数据页跟磁盘数据页内容不一致的时候，我们称这个内存页为“脏页”。

内存数据写入到磁盘后，内存和磁盘上的数据页的内容就一致了，称为“干净页“。

**那什么时候会flush呢？**

1. InnoDB的redo log写满了，这时候系统会停止所有更新操作，把checkpoint往前推进，redo log留出空间可以继续写。
2. 系统内存不足，当需要新的内存页，而内存不够用的时候，就要淘汰一些数据页，空出内存给别的数据页使用。如果淘汰的是“脏页”，就要先将脏页写到磁盘。

> 你一定会说，这时候难道不能直接把内存淘汰掉，下次需要请求的时候，从磁盘读入数据页，然后拿redo log出来应用不就行了？

这里其实是从性能考虑的，如果刷脏页一定会写盘，就保证了每个数据页有两种状态：

- 一种是内存里存在，内存里就肯定是正确的结果，直接返回；
- 另一种是内存里没有数据，就可以肯定数据文件上是正确的结果，读入内存后返回。这样的效率最高。

1. MySQL认为系统“空闲”的时候，只要有机会就刷一点“脏页”。
2. MySQL正常关闭，这时候，MySQL会把内存的脏页都flush到磁盘上，这样下次MySQL启动的时候，就可以直接从磁盘上读数据，启动速度会很快。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdIDDZn9DklW7ib3T6HgTQLEJDbJutVebGaic4kibqx9Uv90IxL7GbHrkgA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**那我们怎么做才能把握flush的时机呢？**

Innodb刷脏页控制策略，我们每个电脑主机的io能力是不一样的，你要正确地告诉InnoDB所在主机的IO能力，这样InnoDB才能知道需要全力刷脏页的时候，可以刷多快。

这就要用到innodb_io_capacity这个参数了，它会告诉InnoDB你的磁盘能力，这个值建议设置成磁盘的IOPS，磁盘的IOPS可以通过fio这个工具来测试。

正确地设置innodb_io_capacity参数，可以有效的解决这个问题。

这中间有个有意思的点，刷脏页的时候，旁边如果也是脏页，会一起刷掉的，并且如果周围还有脏页，这个连带责任制会一直蔓延，这种情况其实在机械硬盘时代比较好，一次IO就解决了所有问题，

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdT0X0HobbjgfiakiaHDY6gMSNuEsGZBLUFvHpJDQnYWAV9mYl4hrqllwQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

但是现在都是固态硬盘了，innodb_flush_neighbors=0这个参数可以不产生连带制，在MySQL 8.0中，innodb_flush_neighbors参数的默认值已经是0了。

##### 总结

在本文中我提到了以下知识点：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1Fpz8Sib2PsicNMxibibNic5p0JicUdqrUWrN4WVIhpAHDCnRFzvxSzN94FXe8vAib6qrvMzfjgGCvSxMmLEKg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

应该还不算全，行锁、表锁、间隙锁、同步场景等等都没怎么提到，因为他们的场景比较复杂，每种都可以单独开一篇了，丁奇的MySQL里面算是很全了，还有就是高性能MySQL大家可以展开看看，要是懒也可以等我总结。

每个点我也没多仔细的讲解，主要是篇幅原因，其实每个点在MySQL相关书籍都是很多篇幅才介绍完的，我就做个总结，对具体的概念不了解可以用搜索引擎查询相关概念，不过我想我说得还算通俗易懂。

-------------------------------------------------------------------------------------------------------------------------------

- 减少回表操作

  查询条件（limit等）放到子查询中，子查询只查主键ID，然后使用子查询中确定的逐渐关联查询其他属性字段

- 应尽量避免全表扫描，首先应考虑在 where 及 order by 涉及的列上建立索引。

- 应尽量避免在 where 子句中使用!=或<>操作符，否则将引擎放弃使用索引而进行全表扫描。

- 应尽量避免在 where 子句中对字段进行 null 值判断，否则将导致引擎放弃使用索引而进行全表扫描，如：select id from t where num is null，可以在num上设置默认值0，确保表中num列没有null值，然后这样查询：select id from t where num=0

- 应尽量避免在 where 子句中使用 or 来连接条件，否则将导致引擎放弃使用索引而进行全表扫描，如：select id from t where num=10 or num=20可以这样查询：select id from t where num=10 union all select id from t where num=20

- 下面的查询也将导致全表扫描：select id from t where name like '%abc%'若要提高效率，可以考虑全文检索。

- in 和 not in 也要慎用，否则会导致全表扫描，如：select id from t where num in(1,2,3)对于连续的数值，能用 between 就不要用 in 了：select id from t where num between 1 and 3

- 如果在 where  子句中使用参数，也会导致全表扫描。因为SQL只有在运行时才会解析局部变量，但优化程序不能将访问计划的选择推迟到运行时；它必须在编译时进行选择。然而，如果在编译时建立访问计划，变量的值还是未知的，因而无法作为索引选择的输入项。如下面语句将进行全表扫描：select id from t where num=@num可以改为强制查询使用索引：select id from t with(index(索引名)) where num=@num

- 应尽量避免在 where 子句中对字段进行表达式操作，这将导致引擎放弃使用索引而进行全表扫描。如：select id from t where num/2=100应改为:select id from t where num=100*2

- 应尽量避免在where子句中对字段进行函数操作，这将导致引擎放弃使用索引而进行全表扫描。如：select id from t where substring(name,1,3)='abc'--name以abc开头的id select id from t where datediff(day,createdate,'2005-11-30')=0--'2005-11-30'生成的id应改为:select id from t where name like 'abc%' select id from t where createdate>='2005-11-30' and createdate<'2005-12-1'

- 不要在 where 子句中的“=”左边进行函数、算术运算或其他表达式运算，否则系统将可能无法正确使用索引。

- 在使用索引字段作为条件时，如果该索引是复合索引，那么必须使用到该索引中的第一个字段作为条件时才能保证系统使用该索引，否则该索引将不会被使用，并且应尽可能的让字段顺序与索引顺序相一致。

- 不要写一些没有意义的查询，如需要生成一个空表结构：select col1,col2 into #t from t where 1=0这类代码不会返回任何结果集，但是会消耗系统资源的，应改成这样：create table #t(...)

- 很多时候用 exists 代替 in 是一个好的选择：select num from a where num in(select num from b)用下面的语句替换：select num from a where exists(select 1 from b where num=a.num)

- 并不是所有索引对查询都有效，SQL是根据表中数据来进行查询优化的，当索引列有大量数据重复时，SQL查询可能不会去利用索引，如一表中有字段sex，male、female几乎各一半，那么即使在sex上建了索引也对查询效率起不了作用。

- 索引并不是越多越好，索引固然可以提高相应的 select 的效率，但同时也降低了 insert 及 update 的效率，因为  insert 或 update  时有可能会重建索引，所以怎样建索引需要慎重考虑，视具体情况而定。一个表的索引数最好不要超过6个，若太多则应考虑一些不常使用到的列上建的索引是否有必要。

- 应尽可能的避免更新 clustered 索引数据列，因为 clustered  索引数据列的顺序就是表记录的物理存储顺序，一旦该列值改变将导致整个表记录的顺序的调整，会耗费相当大的资源。若应用系统需要频繁更新  clustered 索引数据列，那么需要考虑是否应将该索引建为 clustered 索引。

- 尽量使用数字型字段，若只含数值信息的字段尽量不要设计为字符型，这会降低查询和连接的性能，并会增加存储开销。这是因为引擎在处理查询和连接时会逐个比较字符串中每一个字符，而对于数字型而言只需要比较一次就够了。

- 尽可能的使用 varchar/nvarchar 代替 char/nchar ，因为首先变长字段存储空间小，可以节省存储空间，其次对于查询来说，在一个相对较小的字段内搜索效率显然要高些。

- 任何地方都不要使用 select * from t ，用具体的字段列表代替“*”，不要返回用不到的任何字段。

- 尽量使用表变量来代替临时表。如果表变量包含大量数据，请注意索引非常有限（只有主键索引）。

- 避免频繁创建和删除临时表，以减少系统表资源的消耗。

- 临时表并不是不可使用，适当地使用它们可以使某些例程更有效，例如，当需要重复引用大型表或常用表中的某个数据集时。但是，对于一次性事件，最好使用导出表。

- 在新建临时表时，如果一次性插入数据量很大，那么可以使用 select into 代替 create table，避免造成大量 log ，以提高速度；如果数据量不大，为了缓和系统表的资源，应先create table，然后insert。

- 如果使用到了临时表，在存储过程的最后务必将所有的临时表显式删除，先 truncate table ，然后 drop table ，这样可以避免系统表的较长时间锁定。

- 尽量避免使用游标，因为游标的效率较差，如果游标操作的数据超过1万行，那么就应该考虑改写。

- 使用基于游标的方法或临时表方法之前，应先寻找基于集的解决方案来解决问题，基于集的方法通常更有效。

- 与临时表一样，游标并不是不可使用。对小型数据集使用 FAST_FORWARD  游标通常要优于其他逐行处理方法，尤其是在必须引用几个表才能获得所需的数据时。在结果集中包括“合计”的例程通常要比使用游标执行的速度快。如果开发时间允许，基于游标的方法和基于集的方法都可以尝试一下，看哪一种方法的效果更好。

- 在所有的存储过程和触发器的开始处设置 SET NOCOUNT ON ，在结束时设置 SET NOCOUNT OFF 。无需在执行存储过程和触发器的每个语句后向客户端发送 DONE_IN_PROC 消息。

- 尽量避免向客户端返回大数据量，若数据量过大，应该考虑相应需求是否合理。

- 尽量避免大事务操作，提高系统并发能力。



总结起来就是：

- 减少where中使用!=或<>，is null，or, like, in, not in, 表达式操作，函数操作等
- 减少不必要的字段，索引，临时表



### 查询性能优化

#### 合理创建索引

##### 独立的列

在进行查询时，索引列不能是表达式的一部分，也不能是函数的参数，否则无法使用索引。

例如下面的查询不能使用 actor_id 列的索引：

```
SELECT actor_id FROM sakila.actor WHERE actor_id + 1 = 5;
```

##### 多列索引

在需要使用多个列作为条件进行查询时，使用多列索引比使用多个单列索引性能更好。例如下面的语句中，最好把 actor_id 和 film_id 设置为多列索引。

```
SELECT film_id, actor_ id FROM sakila.film_actor
WHERE actor_id = 1 AND film_id = 1;
```

##### 索引列的顺序

让选择性最强的索引列放在前面。

索引的选择性是指：不重复的索引值和记录总数的比值。最大值为 1，此时每个记录都有唯一的索引与其对应。选择性越高，每个记录的区分度越高，查询效率也越高。

例如下面显示的结果中 customer_id 的选择性比 staff_id 更高，因此最好把 customer_id 列放在多列索引的前面。

```
SELECT COUNT(DISTINCT staff_id)/COUNT(*) AS staff_id_selectivity,
COUNT(DISTINCT customer_id)/COUNT(*) AS customer_id_selectivity,
COUNT(*)
FROM payment;
   staff_id_selectivity: 0.0001
customer_id_selectivity: 0.0373
               COUNT(*): 16049
```





#### 使用 explain 分析 select 查询语句

> explain 用来分析 SELECT 查询语句，开发人员可以通过分析 Explain 结果来优化查询语句。

**select_type**

常用的有 SIMPLE 简单查询，UNION 联合查询，SUBQUERY 子查询等。

**table**

要查询的表

**possible_keys**

> The possible indexes to choose

可选择的索引

**key**

> The index actually chosen

实际使用的索引

**rows**

> Estimate of rows to be examined

扫描的行数

**type**

索引查询类型，经常用到的索引查询类型：

**const：使用主键或者唯一索引进行查询的时候只有一行匹配 ref：使用非唯一索引 range：使用主键、单个字段的辅助索引、多个字段的辅助索引的最后一个字段进行范围查询 index：和all的区别是扫描的是索引树 all：扫描全表：**

**system**

**触发条件：表只有一行，这是一个 const type 的特殊情况**

**const**

**触发条件：在使用主键或者唯一索引进行查询的时候只有一行匹配。**

```
SELECT * FROM tbl_name WHERE primary_key=1;

SELECT * FROM tbl_name
  WHERE primary_key_part1=1 AND primary_key_part2=2;
```

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTNNW7F0ajXcjfFs6kHcoWIAyY920TVVgFTJTc1giaXzPePsW301ShEKQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**eq_ref**

**触发条件：在进行联接查询的，使用主键或者唯一索引并且只匹配到一行记录的时候**

```
SELECT * FROM ref_table,other_table
  WHERE ref_table.key_column=other_table.column;

SELECT * FROM ref_table,other_table
  WHERE ref_table.key_column_part1=other_table.column
  AND ref_table.key_column_part2=1;
```

**ref**

触发条件：使用非唯一索引

```
SELECT * FROM ref_table WHERE key_column=expr;

SELECT * FROM ref_table,other_table
  WHERE ref_table.key_column=other_table.column;

SELECT * FROM ref_table,other_table
  WHERE ref_table.key_column_part1=other_table.column
  AND ref_table.key_column_part2=1;
```

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTeLYbiaFptWSq4nW3SSP6oV6qib6DypmF8ZgtFbMkfml5ziblKpSvJC2Mg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**range**

**触发条件：只有在使用主键、单个字段的辅助索引、多个字段的辅助索引的最后一个字段进行范围查询才是 range**

```
SELECT * FROM tbl_name
  WHERE key_column = 10;

SELECT * FROM tbl_name
  WHERE key_column BETWEEN 10 and 20;

SELECT * FROM tbl_name
  WHERE key_column IN (10,20,30);

SELECT * FROM tbl_name
  WHERE key_part1 = 10 AND key_part2 IN (10,20,30);
```

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTqibvfjbkMahpAqdS4qa7n2By8x99cRJs3AxYUd7Aib1VeNQHdwsEScFQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**index**

> The index join type is the same as ALL, except that the index tree is scanned. This occurs two ways:

触发条件：

只扫描索引树

1）查询的字段是索引的一部分，覆盖索引。2）使用主键进行排序

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTDlcHRquopsKaAL5VCq7GmZBwrGicyCmNuN7eVANnKk071e4v4bkHsPg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**all**

触发条件：全表扫描，不走索引

#### 优化数据访问

##### 减少请求的数据量

- 只返回必要的列：最好不要使用 SELECT * 语句。
- 只返回必要的行：使用 LIMIT 语句来限制返回的数据。
- 缓存重复查询的数据：使用缓存可以避免在数据库中进行查询，特别在要查询的数据经常被重复查询时，缓存带来的查询性能提升将会是非常明显的。

##### 减少服务器端扫描的行数

最有效的方式是使用索引来覆盖查询。

#### 重构查询方式

##### 切分大查询

一个大查询如果一次性执行的话，可能一次锁住很多数据、占满整个事务日志、耗尽系统资源、阻塞很多小的但重要的查询。

```
DELETE FROM messages WHERE create < DATE_SUB(NOW(), INTERVAL 3 MONTH);
rows_affected = 0
do {
    rows_affected = do_query(
    "DELETE FROM messages WHERE create  < DATE_SUB(NOW(), INTERVAL 3 MONTH) LIMIT 10000")
} while rows_affected > 0
```

##### 分解大连接查询

将一个大连接查询分解成对每一个表进行一次单表查询，然后在应用程序中进行关联，这样做的好处有：

- 让缓存更高效。对于连接查询，如果其中一个表发生变化，那么整个查询缓存就无法使用。而分解后的多个查询，即使其中一个表发生变化，对其它表的查询缓存依然可以使用。
- 分解成多个单表查询，这些单表查询的缓存结果更可能被其它查询使用到，从而减少冗余记录的查询。
- 减少锁竞争；
- 在应用层进行连接，可以更容易对数据库进行拆分，从而更容易做到高性能和可伸缩。
- 查询本身效率也可能会有所提升。例如下面的例子中，使用 IN() 代替连接查询，可以让 MySQL 按照 ID 顺序进行查询，这可能比随机的连接要更高效。

```
SELECT * FROM tag
JOIN tag_post ON tag_post.tag_id=tag.id
JOIN post ON tag_post.post_id=post.id
WHERE tag.tag='mysql';
SELECT * FROM tag WHERE tag='mysql';
SELECT * FROM tag_post WHERE tag_id=1234;
SELECT * FROM post WHERE post.id IN (123,456,567,9098,8904);
```

## 事务

事务是指满足 ACID 特性的一组操作，可以通过 Commit 提交一个事务，也可以使用 Rollback 进行回滚。

### ACID

事务最基本的莫过于 ACID 四个特性了，这四个特性分别是：

- Atomicity：原子性
- Consistency：一致性
- Isolation：隔离性
- Durability：持久性

**原子性**

事务被视为不可分割的最小单元，事务的所有操作要么全部成功，要么全部失败回滚。

**一致性**

数据库在事务执行前后都保持一致性状态，在一致性状态下，所有事务对一个数据的读取结果都是相同的。

**隔离性**

一个事务所做的修改在最终提交以前，对其他事务是不可见的。

**持久性**

一旦事务提交，则其所做的修改将会永远保存到数据库中。即使系统发生崩溃，事务执行的结果也不能丢。

### ACID 之间的关系

事务的 ACID 特性概念很简单，但不好理解，主要是因为这几个特性不是一种平级关系：

- 只有满足一致性，事务的结果才是正确的。
- 在无并发的情况下，事务串行执行，隔离性一定能够满足。此时只要能满足原子性，就一定能满足一致性。在并发的情况下，多个事务并行执行，事务不仅要满足原子性，还需要满足隔离性，才能满足一致性。
- 事务满足持久化是为了能应对数据库崩溃的情况。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTGYL30g0TKLx51l4f5Hs9DUzWicjAgDLrJWse8Aia81kxtuJic5OXIrwBQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 隔离问题

以下概念是事务隔离级别要实际解决的问题。

**脏读**

脏读指的是读到了其他事务未提交的数据，未提交意味着这些数据可能会回滚，也就是可能最终不会存到数据库中，也就是不存在的数据。读到了并一定最终存在的数据，这就是脏读。

**不可重复读**

对比可重复读，不可重复读指的是在同一事务内，不同的时刻读到的同一批数据可能是不一样的，可能会受到其他事务的影响，比如其他事务改了这批数据并提交了。通常针对数据**更新（UPDATE）**操作。

**可重复读**

可重复读指的是在一个事务内，最开始读到的数据和事务结束前的任意时刻读到的同一批数据都是一致的。通常针对数据**更新（UPDATE）**操作。

**幻读**

幻读是针对数据**插入（INSERT）**操作来说的。假设事务A对某些行的内容作了更改，但是还未提交，此时事务B插入了与事务A更改前的记录相同的记录行，并且在事务A提交之前先提交了，而这时，在事务A中查询，会发现好像刚刚的更改对于某些数据未起作用，但其实是事务B刚插入进来的，让用户感觉很魔幻，感觉出现了幻觉，这就叫幻读。



当然,   从总的结果来看,   不可重复读和幻读似乎两者都表现为两次读取的结果不一致.

但如果你从控制的角度来看,   两者的区别就比较大
对于前者,   只需要锁住满足条件的记录
对于后者,   要锁住满足条件及其相近的记录
避免不可重复读需要锁行就行
避免幻影读则需要锁表

### 隔离级别

**未提交读（`READ UNCOMMITTED`）**

事务中的修改，即使没有提交，对其他事务也是可见的。

**提交读（`READ COMMITTED`）**

一个事务只能读取已经提交的事务所做的修改。换句话说，一个事务所做的修改在提交之前对其他事务是不可见的。

**可重复读（`REPEATABLE READ`）**

保证在同一个事务中多次读取同样数据的结果是一样的。

**可串行化（`SERIALIZABLE`）**

强制事务串行执行。

需要加锁实现，而其它隔离级别通常不需要。

| 隔离级别 | 脏读 | 不可重复读 | 幻影读 |
| :------: | :--: | :--------: | :----: |
| 未提交读 |  √   |     √      |   √    |
|  提交读  |  ×   |     √      |   √    |
| 可重复读 |  ×   |     ×      |   √    |
| 可串行化 |  ×   |     ×      |   ×    |



### Mysql事务的实现

[MySQL事务与MVCC如何实现的隔离级别](https://mp.weixin.qq.com/s/CZHuGT4sKs_QHD_bv3BfAQ)

**原子性(`Atomicity`)**

**当事务对数据库进行修改时，InnoDB会生成对应的```undo log```；如果事务执行失败或调用了`rollback`，导致事务需要回滚，便可以利用```undo log```中的信息将数据回滚到修改之前的样子。**



**隔离性(`Isolation`)**

通过MVCC与

MySQL默认的隔离级别是 `REPEATABLE-READ`，也就是可重复读。

MVCC+锁实现。

**持久性(`Durability`)**

`redo log`实现

**一致性(`Consistency`)**



**MySQL 中是如何实现事务隔离的**



#### **多版本并发控制（MVCC）**

**不同事务同时操作同一条数据产生的问题**

示例：

| **发生时间** | **SessionA**                       | **SessionB**                      |
| ------------ | ---------------------------------- | --------------------------------- |
| 1            | begin;                             |                                   |
| 2            |                                    | begin;                            |
| 3            |                                    | 查询余额 = 1000元                 |
| 4            | 查询余额 = 1000元                  |                                   |
| 5            |                                    | 存入金额 100元，修改余额为 1100元 |
| 6            | 取出现金100元，此时修改余额为900元 |                                   |
| 8            |                                    | 提交事务（余额=1100）             |
| 9            | 提交事务（余额=900）               |                                   |

| **发生时间** | **SessionA**                       | **SessionB**                      |
| ------------ | ---------------------------------- | --------------------------------- |
| 1            | begin;                             |                                   |
| 2            |                                    | begin;                            |
| 3            |                                    | 查询余额 = 1000元                 |
| 4            | 查询余额 = 1000元                  |                                   |
| 5            |                                    | 存入金额 100元，修改余额为 1100元 |
| 6            | 取出现金100元，此时修改余额为900元 |                                   |
| 8            |                                    | 提交事务（余额=1100）             |
| 9            | 撤销事务（余额恢复为1000元）       |                                   |

上面的两种情况就是对于一条数据，多个事务同时操作可能会产生的问题，会出现某个事务的操作被覆盖而导致数据丢失。

**LBCC 解决数据丢失**

**LBCC，基于锁的并发控制，`Lock Based Concurrency Control`。**

使用锁的机制，在当前事务需要对数据修改时，将当前事务加上锁，同一个时间只允许一条事务修改当前数据，其他事务必须等待锁释放之后才可以操作。

**MVCC 解决数据丢失**

**MVCC，多版本的并发控制，`Multi-Version Concurrency Control`。**

使用版本来控制并发情况下的数据问题，在B事务开始修改账户且事务未提交时，当A事务需要读取账户余额时，此时会读取到B事务修改操作之前的账户余额的副本数据，但是如果A事务需要修改账户余额数据就必须要等待B事务提交事务。

**MVCC使得数据库读不会对数据加锁，普通的SELECT请求不会加锁，提高了数据库的并发处理能力**。 借助MVCC，数据库可以实现``READ COMMITTED``，``REPEATABLE READ``等隔离级别，用户可以查看当前数据的前一个或者前几个历史版本，保证了ACID中的I特性（隔离性)。



#### InnoDB的MVCC实现逻辑

##### **InnoDB存储引擎保存的MVCC的数据**

InnoDB的MVCC是通过在每行记录后面保存两个隐藏的列来实现的。**一个保存了行的事务ID（`DB_TRX_ID`），一个保存了行的回滚指针（`DB_ROLL_PT`）**。每开始一个新的事务，都会自动递增产 生一个新的事务id。事务开始时刻的会把事务id放到当前事务影响的行事务id中，当查询时需要用当前事务id和每行记录的事务id进行比较。

下面看一下在``REPEATABLE READ``隔离级别下，MVCC具体是如何操作的。

**MVCC 在mysql 中的实现依赖的是 ```undo log``` 与 ``read view`` 。**



###### **`undo log`**

`undo log`根据行为的不同，`undo log`分为两种：**`insert undo log`** 和 **`update undo log`**

- **`insert undo log`：**

insert 操作中产生的`undo log`，因为insert操作记录只对当前事务本身课件，对于其他事务此记录不可见，所以 `insert undo log` 可以在事务提交后直接删除而不需要进行purge操作。

> purge的主要任务是将数据库中已经 mark del 的数据删除，另外也会批量回收undo pages

数据库 Insert时的数据初始状态：

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwJKFFbFRxaw5IqeicribHhXUF3xzFfFBQeL8SNsvqnUw71LgTuOagzP9U9191r9RLzt12uIAIZMPgQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

- **`update undo log`：**

  update 或 delete 操作中产生的 `undo log`。因为会对已经存在的记录产生影响，为了提供 MVCC机制，因此`update undo log` 不能在事务提交时就进行删除，而是将事务提交时放到入 history list 上，等待 purge 线程进行最后的删除操作。

  **数据第一次被修改时：**

  ![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwJKFFbFRxaw5IqeicribHhXUCV7aqgyYufAg75OCdW0NvX7tOMN9m0LEOQtY9BKrxJbOZ5ngTGDiavA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

**当另一个事务第二次修改当前数据：**

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwJKFFbFRxaw5IqeicribHhXU5X2wmfQ1UPMKlreE4GNjcA40jwhV5ic9rmJnZNf1HuVssHd2Qbo4Ujw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

为了保证事务并发操作时，在写各自的`undo log`时不产生冲突，InnoDB采用回滚段的方式来维护`undo log`的并发写入和持久化。回滚段实际上是一种 Undo 文件组织方式。



###### `ReadView`

**``ReadView`` （或者可以称之为Snapshot）**``ReadView``是某一个时间点，事务执行状态的一个快照，可以用来判断事务的可见性。``ReadView``的基本结构如下：

```java
`ReadView` {
    creator_trx_id
    low_limit_id
    up_limit_id
    ids
	... 
}
```

**`creator_trx_id`** 创建这个``ReadView``的事务ID

**`low_limit_id`** 所有事务ID大于或等于`low_limit_id`对当前事务都不可见

**`up_limit_id`** 所有事务ID严格小于`up_limit_id`的事务对当前事务可见

**`ids`** 未提交的事务ID列表

**可见性的判断**

事务通过用当前事务（或语句，取决于隔离级别）的``ReadView``来判断一个事务id的操作是否对当前事务可见。判断可见性的伪代码如下：

```
IsVisible(trx_id)
    if (trx_id == creator_trx_id)     // 当前事务
    	return true;
    else if (trx_id < up_limit_id)    // `ReadView`创建时, 事务已提交
   		return true;
    else if (trx_id >= low_limit_id)  // `ReadView`创建时，事务还未被创建
    	return false;
    else if (trx_id is in `m_ids`)  // `ReadView`创建时，事务正在执行，但未提交        		return false    
    else                          // `ReadView`创建时, 事务已提交       
    	return true;
```



对于 **RU(``READ UNCOMMITTED``)** 隔离级别下，所有事务直接读取数据库的最新值即可，和 **``SERIALIZABLE``** 隔离级别，所有请求都会加锁，同步执行。所以这对这两种情况下是不需要使用到 **`read view`** 的版本控制。

对于 **RC(``READ COMMITTED``)** 和 **RR(``REPEATABLE READ``)** 隔离级别的实现就是通过上面的版本控制来完成。两种隔离界别下的核心处理逻辑就是判断所有版本中哪个版本是当前事务可见的处理。针对这个问题InnoDB在设计上增加了**``ReadView``**的设计，**``ReadView``**中主要包含当前系统中还有哪些活跃的读写事务，把它们的事务id放到一个列表中，我们把这个列表命名为为**``m_ids``**。

对于查询时的版本链数据是否看见的判断逻辑：

- 如果被访问版本的 `trx_id` 属性值小于 ``m_ids`` 列表中最小的事务id，表明生成该版本的事务在生成 ``ReadView`` 前已经提交，所以该版本可以被当前事务访问。
- 如果被访问版本的 `trx_id` 属性值大于 ``m_ids`` 列表中最大的事务id，表明生成该版本的事务在生成 ``ReadView`` 后才生成，所以该版本不可以被当前事务访问。
- 如果被访问版本的 `trx_id` 属性值在 ``m_ids`` 列表中最大的事务id和最小事务id之间，那就需要判断一下 `trx_id` 属性值是不是在 ``m_ids``  列表中，如果在，说明创建 ``ReadView`` 时生成该版本的事务还是活跃的，该版本不可以被访问；如果不在，说明创建 ``ReadView``  时生成该版本的事务已经被提交，该版本可以被访问。

**区别**

- **使用``READ COMMITTED``隔离级别的事务在每次查询开始时都会生成一个独立的 `ReadView`。**
- **使用``REPEATABLE READ``隔离级别的事务在事务开始后第一次读取数据时生成一个``ReadView``（``m_ids``列表），之后读取数据不会重新生成。**

**举个例子：**



##### `READ COMMITTED` 隔离级别下的``ReadView``

**每次读取数据前都生成一个`ReadView` (`m_ids`列表)**

| **时间** | **Transaction 777**                          | **Transaction 888**                           | **Trasaction 999**               |
| -------- | -------------------------------------------- | --------------------------------------------- | -------------------------------- |
| T1       | begin;                                       |                                               |                                  |
| T2       |                                              | begin;                                        | begin；                          |
| T3       | UPDATE user SET name = ‘CR7’ WHERE id = 1;   |                                               |                                  |
| T4       |                                              | …                                             |                                  |
| T5       | UPDATE user SET name = ‘Messi’ WHERE id = 1; |                                               | SELECT * FROM user where id = 1; |
| T6       | commit;                                      |                                               |                                  |
| T7       |                                              | UPDATE user SET name = ‘Neymar’ WHERE id = 1; |                                  |
| T8       |                                              |                                               | SELECT * FROM user where id = 1; |
| T9       |                                              | UPDATE user SET name = ‘Dybala’ WHERE id = 1; |                                  |
| T10      |                                              | commit;                                       |                                  |
| T11      |                                              |                                               | SELECT * FROM user where id = 1; |

这里分析下上面的情况下的`ReadView`

时间点 T5 情况下的 SELECT 语句：

当前时间点的版本链：

![img](https://img-blog.csdnimg.cn/img_convert/b58f07de1e070884335f5e068e7feb8f.png)

> 此时 SELECT 语句执行，当前数据的版本链如上，因为当前的事务777，和事务888 都未提交，所以此时的活跃事务的`ReadView`的列表情况 **`m_ids`：[777, 888]** ，因此查询语句会根据当前版本链中小于 **`m_ids`** 中的最大的版本数据，即查询到的是 Mbappe。

时间点 T8 情况下的 SELECT 语句：

当前时间的版本链情况：

![img](https://img-blog.csdnimg.cn/img_convert/8c392ee3d87c0817418f5218e843c0dd.png)

> 此时 SELECT 语句执行，当前数据的版本链如上，因为当前的事务777已经提交，和事务888 未提交，所以此时的活跃事务的`ReadView`的列表情况 **`m_ids`：[888]** ，因此查询语句会根据当前版本链中小于 **`m_ids`** 中的最大的版本数据，即查询到的是 Messi。

时间点 T11 情况下的 SELECT 语句：

当前时间点的版本链信息：

![img](https://img-blog.csdnimg.cn/img_convert/3d98a4a76a2b072de16fecb266612f08.png)

> 此时 SELECT 语句执行，当前数据的版本链如上，因为当前的事务777和事务888 都已经提交，所以此时的活跃事务的`ReadView`的列表为空 ，因此查询语句会直接查询当前数据库最新数据，即查询到的是 Dybala。

**总结：** **使用`READ COMMITTED`隔离级别的事务在每次查询开始时都会生成一个独立的 `ReadView`。**

##### `REPEATABLE READ` 隔离级别下的`ReadView`

**在事务开始后第一次读取数据时生成一个`ReadView`（`m_ids`列表）**

| **时间** | **Transaction 777**                          | **Transaction 888**                           | **Trasaction 999**               |
| -------- | -------------------------------------------- | --------------------------------------------- | -------------------------------- |
| T1       | begin;                                       |                                               |                                  |
| T2       |                                              | begin;                                        | begin；                          |
| T3       | UPDATE user SET name = ‘CR7’ WHERE id = 1;   |                                               |                                  |
| T4       |                                              | …                                             |                                  |
| T5       | UPDATE user SET name = ‘Messi’ WHERE id = 1; |                                               | SELECT * FROM user where id = 1; |
| T6       | commit;                                      |                                               |                                  |
| T7       |                                              | UPDATE user SET name = ‘Neymar’ WHERE id = 1; |                                  |
| T8       |                                              |                                               | SELECT * FROM user where id = 1; |
| T9       |                                              | UPDATE user SET name = ‘Dybala’ WHERE id = 1; |                                  |
| T10      |                                              | commit;                                       |                                  |
| T11      |                                              |                                               | SELECT * FROM user where id = 1; |

时间点 T5 情况下的 SELECT 语句：

当前版本链：

![img](https://img-blog.csdnimg.cn/img_convert/aa8736eecbe0458fa32513ed7b0db131.png)

> 再当前执行select语句时生成一个`ReadView`，此时 **`m_ids`** 内容是：[777,888]，所以但前根据`ReadView`可见版本查询到的数据为 Mbappe。

时间点 T8 情况下的 SELECT 语句：

当前的版本链：

![img](https://img-blog.csdnimg.cn/img_convert/97491a234ccba0c4ec01746d1cedbcf3.png)

> 此时在当前的 Transaction 999 的事务里。由于T5的时间点已经生成了`ReadView`，所以再当前的事务中只会生成一次`ReadView`，所以此时依然沿用T5时的**`m_ids`：[777,999]**，所以此时查询数据依然是 Mbappe。

时间点 T11 情况下的 SELECT 语句：

当前的版本链：

![img](https://img-blog.csdnimg.cn/img_convert/03483323ad1e171da2aca16644e3f699.png)

> 此时情况跟T8完全一样。由于T5的时间点已经生成了`ReadView`，所以再当前的事务中只会生成一次`ReadView`，所以此时依然沿用T5时的**`m_ids`：[777,999]**，所以此时查询数据依然是 Mbappe。



##### MVCC总结

所谓的MVCC（Multi-Version Concurrency Control ，多版本并发控制）指的就是在使用 **READ COMMITTD** 、**`REPEATABLE READ`** 这两种隔离级别的事务在执行普通的 SEELCT 操作时访问记录的版本链的过程，这样子可以使不同事务的 `读-写` 、 `写-读` 操作并发执行，从而提升系统性能。

在 MySQL 中， `READ COMMITTED` 和 `REPEATABLE READ` 隔离级别的的一个非常大的区别就是它们生成  `ReadView` 的时机不同。在 `READ COMMITTED` 中每次查询都会生成一个实时的  `ReadView`，做到保证每次提交后的数据是处于当前的可见状态。而 `REPEATABLE READ` 中，在当前事务第一次查询时生成当前的  `ReadView`，并且当前的 `ReadView` 会一直沿用到当前事务提交，以此来保证可重复读（`REPEATABLE READ`）。



**区别**

- **使用`READ COMMITTED`隔离级别的事务在每次查询开始时都会生成一个独立的 `ReadView`。**
- **使用`REPEATABLE READ`隔离级别的事务在事务开始后第一次读取数据时生成一个`ReadView`（`m_ids`列表），之后读取数据不会重新生成。**





## 锁

锁是数据库系统区别于文件系统的一个关键特性。锁机制用于管理对共享资源的并发访问。

### 锁类型

**共享锁（读锁、S Lock）**

允许事务读一行数据。其他事务可以读，但不能写。

**排他锁（写锁、X Lock）**

允许事务删除或者更新一行数据。其他事务不能读取，也不能写。

**意向共享锁（IS Lock）**

事务想要获得一张表中某几行的共享锁

**意向排他锁**

事务想要获得一张表中某几行的排他锁

### **粒度锁**

MySQL 不同的存储引擎支持不同的锁机制，所有的存储引擎都以自己的方式显现了锁机制，服务器层完全不了解存储引擎中的锁实现： 

- MyISAM 和 MEMORY 存储引擎采用的是表级锁（table-level locking）
- BDB 存储引擎采用的是页面锁（page-level locking），但也支持表级锁
- InnoDB 存储引擎既支持行级锁（row-level locking），也支持表级锁，但默认情况下是采用行级锁。

默认情况下，表锁和行锁都是自动获得的， 不需要额外的命令。 

但是在有的情况下， 用户需要明确地进行锁表或者进行事务的控制， 以便确保整个事务的完整性，这样就需要使用事务控制和锁定语句来完成。



**不同粒度锁的比较：**

- 表级锁：开销小，加锁快；不会出现死锁；锁定粒度大，发生锁冲突的概率最高，并发度最低。 

- - 这些存储引擎通过总是一次性同时获取所有需要的锁以及总是按相同的顺序获取表锁来避免死锁。
  - 表级锁更适合于以查询为主，并发用户少，只有少量按索引条件更新数据的应用，如Web 应用

- 行级锁：开销大，加锁慢；会出现死锁；锁定粒度最小，发生锁冲突的概率最低，并发度也最高。

- - 最大程度的支持并发，同时也带来了最大的锁开销。
  - 在 InnoDB 中，除单个 SQL 组成的事务外，
    锁是逐步获得的，这就决定了在 InnoDB 中发生死锁是可能的。
  - 行级锁只在存储引擎层实现，而Mysql服务器层没有实现。 行级锁更适合于有大量按索引条件并发更新少量不同数据，同时又有并发查询的应用，如一些在线事务处理（OLTP）系统

- 页面锁：开销和加锁时间界于表锁和行锁之间；会出现死锁；锁定粒度界于表锁和行锁之间，并发度一般。



### [**InnoDB行级锁和表级锁**](https://zhuanlan.zhihu.com/p/29150809)

#### **InnoDB锁模式** 

InnoDB 实现了以下两种类型的**行锁**： 

- 共享锁（S）：允许一个事务去读一行，阻止其他事务获得相同数据集的排他锁。 
- 排他锁（X）：允许获得排他锁的事务更新数据，阻止其他事务取得相同数据集的共享读锁和排他写锁。

为了允许行锁和表锁共存，实现多粒度锁机制，InnoDB 还有两种内部使用的意向锁（Intention Locks），这两种意向锁都是**表锁**：

- 意向共享锁（IS）：事务打算给数据行加行共享锁，事务在给一个数据行加共享锁前必须先取得该表的 IS 锁。 
- 意向排他锁（IX）：事务打算给数据行加行排他锁，事务在给一个数据行加排他锁前必须先取得该表的 IX 锁。

**锁模式的兼容情况：**

![img](https://pic4.zhimg.com/80/v2-37761612ead11ddc3762a4c20ddab3f3_720w.jpg)

（如果一个事务请求的锁模式与当前的锁兼容， InnoDB 就将请求的锁授予该事务； 反之， 如果两者不兼容，该事务就要等待锁释放。）



#### **InnoDB加锁方法**

- 意向锁是 InnoDB 自动加的， 不需用户干预。 

- 对于 UPDATE、 DELETE 和 INSERT 语句， InnoDB
  会自动给涉及数据集加排他锁（X)；

- 对于普通 SELECT 语句，InnoDB 不会加任何锁；
  事务可以通过以下语句显式给记录集加共享锁或排他锁：

- - 共享锁（S）：SELECT * FROM table_name WHERE ... LOCK IN SHARE MODE。 其他 session  仍然可以查询记录，并也可以对该记录加 share mode 的共享锁。但是如果当前事务需要对该记录进行更新操作，则很有可能造成死锁。
  - 排他锁（X)：SELECT * FROM table_name WHERE ... FOR UPDATE。其他 session 可以查询该记录，但是不能对该记录加共享锁或排他锁，而是等待获得锁



- **隐式锁定：** 

InnoDB在事务执行过程中，使用两阶段锁协议：

随时都可以执行锁定，InnoDB会根据隔离级别在需要的时候自动加锁；

锁只有在执行commit或者rollback的时候才会释放，并且所有的锁都是在**同一时刻**被释放。 

- **显式锁定 ：** 

```text
select ... lock in share mode //共享锁 
select ... for update //排他锁 
```

**select for update：**

在执行这个 select 查询语句的时候，会将对应的索引访问条目进行上排他锁（X 锁），也就是说这个语句对应的锁就相当于update带来的效果。

select *** for update 的使用场景：为了让自己查到的数据确保是最新数据，并且查到后的数据只允许自己来修改的时候，需要用到 for update 子句。

**select lock in share mode ：**in share mode 子句的作用就是将查找到的数据加上一个 share 锁，这个就是表示其他的事务只能对这些数据进行简单的select  操作，并不能够进行 DML 操作。select *** lock in share mode  使用场景：为了确保自己查到的数据没有被其他的事务正在修改，也就是说确保查到的数据是最新的数据，并且不允许其他人来修改数据。但是自己不一定能够修改数据，因为有可能其他的事务也对这些数据 使用了 in share mode 的方式上了 S 锁。

**性能影响：**
select for update 语句，相当于一个 update 语句。在业务繁忙的情况下，如果事务没有及时的commit或者rollback 可能会造成其他事务长时间的等待，从而影响数据库的并发使用效率。
select lock in share mode 语句是一个给查找的数据上一个共享锁（S 锁）的功能，它允许其他的事务也对该数据上S锁，但是不能够允许对该数据进行修改。如果不及时的commit 或者rollback 也可能会造成大量的事务等待。

**for update 和 lock in share mode 的区别：**

前一个上的是排他锁（X 锁），一旦一个事务获取了这个锁，其他的事务是没法在这些数据上执行 for update ；后一个是共享锁，多个事务可以同时的对相同数据执行 lock in share mode。

#### InnoDB 行锁实现方式

- InnoDB 行锁是通过给索引上的索引项加锁来实现的，这一点 MySQL 与 Oracle 不同，后者是通过在数据块中对相应数据行加锁来实现的。InnoDB 这种行锁实现特点意味着：只有通过索引条件检索数据，InnoDB 才使用行级锁，否则，InnoDB 将使用表锁！
- 不论是使用主键索引、唯一索引或普通索引，InnoDB 都会使用行锁来对数据加锁。
- 只有执行计划真正使用了索引，才能使用行锁：即便在条件中使用了索引字段，但是否使用索引来检索数据是由 MySQL 通过判断不同执行计划的代价来决定的，如果 MySQL 认为全表扫描效率更高，比如对一些很小的表，它就不会使用索引，这种情况下  InnoDB 将使用表锁，而不是行锁。因此，在分析锁冲突时，
  别忘了检查 SQL 的执行计划（可以通过 explain 检查 SQL 的执行计划），以确认是否真正使用了索引。（更多阅读：[MySQL索引总结](https://link.zhihu.com/?target=http%3A//mp.weixin.qq.com/s/h4B84UmzAUJ81iBY_FXNOg)）
- 由于 MySQL 的行锁是针对索引加的锁，不是针对记录加的锁，所以虽然多个session是访问不同行的记录， 但是如果是使用相同的索引键，  是会出现锁冲突的（后使用这些索引的session需要等待先使用索引的session释放锁后，才能获取锁）。 应用设计的时候要注意这一点。

#### **InnoDB的间隙锁**

当我们用范围条件而不是相等条件检索数据，并请求共享或排他锁时，InnoDB会给符合条件的已有数据记录的索引项加锁；对于键值在条件范围内但并不存在的记录，叫做“间隙（GAP)”，InnoDB也会对这个“间隙”加锁，这种锁机制就是所谓的间隙锁（Next-Key锁）。

很显然，在使用范围条件检索并锁定记录时，InnoDB这种加锁机制会阻塞符合条件范围内键值的并发插入，这往往会造成严重的锁等待。因此，在实际应用开发中，尤其是并发插入比较多的应用，我们要尽量优化业务逻辑，尽量使用相等条件来访问更新数据，避免使用范围条件。 

**InnoDB使用间隙锁的目的：**

1. 防止幻读，以满足相关隔离级别的要求；
2. 满足恢复和复制的需要：

MySQL 通过 BINLOG 录入执行成功的 INSERT、UPDATE、DELETE 等更新数据的 SQL 语句，并由此实现 MySQL  数据库的恢复和主从复制。MySQL 的恢复机制（复制其实就是在 Slave Mysql 不断做基于 BINLOG 的恢复）有以下特点：

一是 MySQL 的恢复是 SQL 语句级的，也就是重新执行 BINLOG 中的 SQL 语句。

二是 MySQL 的 Binlog 是按照事务提交的先后顺序记录的， 恢复也是按这个顺序进行的。

由此可见，MySQL 的恢复机制要求：在一个事务未提交前，其他并发事务不能插入满足其锁定条件的任何记录，也就是不允许出现幻读。

#### **InnoDB 在不同隔离级别下的一致性读及锁的差异：**

锁和多版本数据（MVCC）是 InnoDB 实现一致性读和 ISO/ANSI SQL92 隔离级别的手段。

因此，在不同的隔离级别下，InnoDB 处理 SQL 时采用的一致性读策略和需要的锁是不同的：

![img](https://pic2.zhimg.com/80/v2-c83c6459f8dc93a5f157fe1e3080088d_720w.jpg)



![img](https://pic1.zhimg.com/80/v2-568951f4cdfeb9416042627a7b94c4ac_720w.jpg)



对于许多 SQL，隔离级别越高，InnoDB 给记录集加的锁就越严格（尤其是使用范围条件的时候），产生锁冲突的可能性也就越高，从而对并发性事务处理性能的 影响也就越大。 

因此， 我们在应用中， 应该尽量使用较低的隔离级别， 以减少锁争用的机率。实际上，通过优化事务逻辑，大部分应用使用 Read Commited  隔离级别就足够了。对于一些确实需要更高隔离级别的事务， 可以通过在程序中执行 SET SESSION TRANSACTION ISOLATION 

LEVEL REPEATABLE READ 或 SET SESSION TRANSACTION ISOLATION LEVEL SERIALIZABLE 动态改变隔离级别的方式满足需求。

#### 获取 InnoDB 行锁争用情况：

可以通过检查 InnoDB_row_lock 状态变量来分析系统上的行锁的争夺情况：

```text
mysql> show status like 'innodb_row_lock%'; 
+-------------------------------+-------+ 
| Variable_name | Value | 
+-------------------------------+-------+ 
| InnoDB_row_lock_current_waits | 0 | 
| InnoDB_row_lock_time | 0 | 
| InnoDB_row_lock_time_avg | 0 | 
| InnoDB_row_lock_time_max | 0 | 
| InnoDB_row_lock_waits | 0 | 
+-------------------------------+-------+ 
5 rows in set (0.01 sec)
```

#### **LOCK TABLES 和 UNLOCK TABLES**

Mysql也支持lock tables和unlock tables，这都是在服务器层（MySQL Server层）实现的，和存储引擎无关，它们有自己的用途，并不能替代事务处理。 （除了禁用了autocommint后可以使用，其他情况不建议使用）： 

- LOCK TABLES 可以锁定用于当前线程的表。如果表被其他线程锁定，则当前线程会等待，直到可以获取所有锁定为止。 
- UNLOCK TABLES 可以释放当前线程获得的任何锁定。当前线程执行另一个 LOCK TABLES 时，
  或当与服务器的连接被关闭时，所有由当前线程锁定的表被隐含地解锁

#### **LOCK TABLES语法**

- 在用 LOCK TABLES 对 InnoDB 表加锁时要注意，要将 AUTOCOMMIT 设为 0，否则MySQL 不会给表加锁；
- 事务结束前，不要用 UNLOCK TABLES 释放表锁，因为 UNLOCK TABLES会隐含地提交事务；
- COMMIT 或 ROLLBACK 并不能释放用 LOCK TABLES 加的表级锁，必须用UNLOCK TABLES 释放表锁。

正确的方式见如下语句：
例如，如果需要写表 t1 并从表 t 读，可以按如下做：

```text
SET AUTOCOMMIT=0; 
LOCK TABLES t1 WRITE, t2 READ, ...; 
[do something with tables t1 and t2 here]; 
COMMIT; 
UNLOCK TABLES;
```

#### 使用LOCK TABLES的场景

给表显示加表级锁（InnoDB表和MyISAM都可以），一般是为了在一定程度模拟事务操作，实现对某一时间点多个表的一致性读取。（与MyISAM默认的表锁行为类似）

在用 LOCK TABLES 给表显式加表锁时，必须同时取得所有涉及到表的锁，并且 MySQL 不支持锁升级。也就是说，在执行 LOCK  TABLES 后，只能访问显式加锁的这些表，不能访问未加锁的表；同时，如果加的是读锁，那么只能执行查询操作，而不能执行更新操作。

其实，在MyISAM自动加锁（表锁）的情况下也大致如此，MyISAM 总是一次获得 SQL 语句所需要的全部锁，这也正是 MyISAM 表不会出现死锁（Deadlock Free）的原因。

例如，有一个订单表 orders，其中记录有各订单的总金额 total，同时还有一个 订单明细表 order_detail，其中记录有各订单每一产品的金额小计  subtotal，假设我们需要检 查这两个表的金额合计是否相符，可能就需要执行如下两条 SQL：  

```text
Select sum(total) from orders; 
Select sum(subtotal) from order_detail; 
```

这时，如果不先给两个表加锁，就可能产生错误的结果，因为第一条语句执行过程中，
order_detail 表可能已经发生了改变。因此，正确的方法应该是： 

```text
Lock tables orders read local, order_detail read local; 
Select sum(total) from orders; 
Select sum(subtotal) from order_detail; 
Unlock tables;
```

（在 LOCK TABLES 时加了“local”选项，其作用就是允许当你持有表的读锁时，其他用户可以在满足 MyISAM 表并发插入条件的情况下，在表尾并发插入记录（MyISAM 存储引擎支持“并发插入”））

### MVCC

多版本并发控制（Multi-Version Concurrency Control, MVCC）是 MySQL 的 InnoDB  存储引擎实现隔离级别的一种具体方式，用于实现提交读和可重复读这两种隔离级别。而未提交读隔离级别总是读取最新的数据行，无需使用  MVCC。可串行化隔离级别需要对所有读取的行都加锁，单纯使用 MVCC 无法实现。

#### 基础概念

**版本号**

- 系统版本号：是一个递增的数字，每开始一个新的事务，系统版本号就会自动递增。
- 事务版本号：事务开始时的系统版本号。

**隐藏的列**

MVCC 在每行记录后面都保存着两个隐藏的列，用来存储两个版本号：

- 创建版本号：指示创建一个数据行的快照时的系统版本号；
- 删除版本号：如果该快照的删除版本号大于当前事务版本号表示该快照有效，否则表示该快照已经被删除了。

**Undo 日志**

MVCC 使用到的快照存储在 Undo 日志中，该日志通过回滚指针把一个数据行（Record）的所有快照连接起来。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTicpeQdfCyQT59DuCHeT2QEoPfpjz0zvjYlAmX4vD3IN1kAE9aNibBibdg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 实现过程

以下实现过程针对可重复读隔离级别。

当开始一个事务时，该事务的版本号肯定大于当前所有数据行快照的创建版本号，理解这一点很关键。数据行快照的创建版本号是创建数据行快照时的系统版本号，系统版本号随着创建事务而递增，因此新创建一个事务时，这个事务的系统版本号比之前的系统版本号都大，也就是比所有数据行快照的创建版本号都大。

**SELECT**

多个事务必须读取到同一个数据行的快照，并且这个快照是距离现在最近的一个有效快照。但是也有例外，如果有一个事务正在修改该数据行，那么它可以读取事务本身所做的修改，而不用和其它事务的读取结果一致。

把没有对一个数据行做修改的事务称为 T，T 所要读取的数据行快照的创建版本号必须小于等于 T 的版本号，因为如果大于 T  的版本号，那么表示该数据行快照是其它事务的最新修改，因此不能去读取它。除此之外，T 所要读取的数据行快照的删除版本号必须是未定义或者大于 T  的版本号，因为如果小于等于 T 的版本号，那么表示该数据行快照是已经被删除的，不应该去读取它。

**INSERT**

将当前系统版本号作为数据行快照的创建版本号。

**DELETE**

将当前系统版本号作为数据行快照的删除版本号。

**UPDATE**

将当前系统版本号作为更新前的数据行快照的删除版本号，并将当前系统版本号作为更新后的数据行快照的创建版本号。可以理解为先执行 DELETE 后执行 INSERT。

#### 快照读与当前读

在可重复读级别中，通过MVCC机制，虽然让数据变得可重复读，但我们读到的数据可能是历史数据，是不及时的数据，不是数据库当前的数据！这在一些对于数据的时效特别敏感的业务中，就很可能出问题。

对于这种读取历史数据的方式，我们叫它快照读 (snapshot read)，而读取数据库当前版本数据的方式，叫当前读 (current read)。很显然，在MVCC中：

**快照读**

MVCC 的 SELECT 操作是快照中的数据，不需要进行加锁操作。

```
select * from table ….;
```

**当前读**

MVCC 其它会对数据库进行修改的操作（INSERT、UPDATE、DELETE）需要进行加锁操作，从而读取最新的数据。可以看到 MVCC 并不是完全不用加锁，而只是避免了 SELECT 的加锁操作。

```
INSERT;
UPDATE;
DELETE;
```

在进行 SELECT 操作时，可以强制指定进行加锁操作。以下第一个语句需要加 S 锁，第二个需要加 X 锁。

```
- select * from table where ? lock in share mode;
- select * from table where ? for update;
```

事务的隔离级别实际上都是定义的当前读的级别，MySQL为了减少锁处理（包括等待其它锁）的时间，提升并发能力，引入了快照读的概念，使得select不用加锁。而update、insert这些“当前读”的隔离性，就需要通过加锁来实现了。

### 锁算法

#### Record Lock

锁定一个记录上的索引，而不是记录本身。

如果表没有设置索引，InnoDB 会自动在主键上创建隐藏的聚簇索引，因此 Record Locks 依然可以使用。

#### Gap Lock

锁定索引之间的间隙，但是不包含索引本身。例如当一个事务执行以下语句，其它事务就不能在 t.c 中插入 15。

```
SELECT c FROM t WHERE c BETWEEN 10 and 20 FOR UPDATE;
```

#### Next-Key Lock

它是 Record Locks 和 Gap Locks 的结合，不仅锁定一个记录上的索引，也锁定索引之间的间隙。例如一个索引包含以下值：10, 11, 13, and 20，那么就需要锁定以下区间：

```
(-∞, 10]
(10, 11]
(11, 13]
(13, 20]
(20, +∞)
```

> **在 InnoDB 存储引擎中，SELECT 操作的不可重复读问题通过 MVCC 得到了解决，而 UPDATE、DELETE 的不可重复读问题通过  Record Lock 解决，INSERT 的不可重复读问题是通过 Next-Key Lock（Record Lock + Gap  Lock）解决的。**



## 分库分表数据切分

### 水平切分

水平切分又称为 Sharding，它是将同一个表中的记录拆分到多个结构相同的表中。

当一个表的数据不断增多时，Sharding 是必然的选择，它可以将数据分布到集群的不同节点上，从而缓存单个数据库的压力。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTDY4S3c0lral4cRic5FGqO5U5RicuhKx7VqPgk75CC6Ra9Vhc7PCdM12w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 垂直切分

垂直切分是将一张表按列分成多个表，通常是按照列的关系密集程度进行切分，也可以利用垂直气氛将经常被使用的列喝不经常被使用的列切分到不同的表中。

在数据库的层面使用垂直切分将按数据库中表的密集程度部署到不通的库中，例如将原来电商数据部署库垂直切分称商品数据库、用户数据库等。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTjeVApdic37kA3icLTWwFHHj33WLFiaFBTlqxqPvBpZ8icUWv0f3FWJh27w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### Sharding 策略

- 哈希取模：hash(key)%N
- 范围：可以是 ID 范围也可以是时间范围
- 映射表：使用单独的一个数据库来存储映射关系

### Sharding 存在的问题

**事务问题**

使用分布式事务来解决，比如 XA 接口

**连接**

可以将原来的连接分解成多个单表查询，然后在用户程序中进行连接。

**唯一性**

- 使用全局唯一 ID （GUID）
- 为每个分片指定一个 ID 范围
- 分布式 ID 生成器（如 Twitter 的 Snowflake 算法）

## 复制

### 主从复制

**什么是主从复制？** 

主从复制是指将主数据库的DDL和DML操作通过二进制日志传到从数据库上，然后在从数据库上对这些日志进行重新执行，从而使从数据库和主数据库的数据保持一致。



**主从复制的原理** 

- MySql主库在事务提交时会把数据变更作为事件记录在二进制日志Binlog中；
- 主库推送二进制日志文件Binlog中的事件到从库的中继日志Relay Log中，之后从库根据中继日志重做数据变更操作，通过逻辑复制来达到主库和从库的数据一致性；
- MySql通过三个线程来完成主从库间的数据复制，其中Binlog Dump线程跑在主库上，I/O线程和SQL线程跑着从库上；
- 当在从库上启动复制时，首先创建I/O线程连接主库，主库随后创建Binlog Dump线程读取数据库事件并发送给I/O线程，I/O线程获取到事件数据后更新到从库的中继日志Relay  Log中去，之后从库上的SQL线程读取中继日志Relay Log中更新的数据库事件并应用，如下图所示。

![img](https://mmbiz.qpic.cn/mmbiz_png/CKvMdchsUwlc9vLQe9Ugu4Q3ZUQu9ezDKRmmK2hsjoicDbdDF7PTgTxAqZy9CD3mow4wOhlMK4JTVRBVFygSnWg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



主要涉及三个线程：binlog 线程、I/O 线程和 SQL 线程。

- binlog 线程 ：负责将主服务器上的数据更改写入二进制日志（Binary log）中。
- I/O 线程 ：负责从主服务器上读取- 二进制日志，并写入从服务器的中继日志（Relay log）。
- SQL 线程 ：负责读取中继日志，解析出主服务器已经执行的数据更改并在从服务器中重放（Replay）。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTsbic5vbEYibPGEG0zpDoWWQZGWWicRfsazEBAZicXHg15KkeDeqy273licQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



**主从复制**

主从数据库数据同步，保持一致性。

主从复制的原理实际上就是通过`bin log`日志实现的。`bin log`日志中保存了数据库中所有SQL语句，通过对`bin log`日志中SQL的复制，然后再进行语句的执行即可实现从数据库与主数据库的同步。



主从复制的过程可见下图。主从复制的过程主要是靠三个线程进行的，一个运行在主服务器中的发送线程，用于发送`binlog`日志到从服务器。两外两个运行在从服务器上的I/O线程和SQL线程。I/O线程用于读取主服务器发送过来的`binlog`日志内容，并拷贝到本地的中继日志中。SQL线程用于读取中继日志中关于数据更新的SQL语句并执行，从而实现主从库的数据一致。

![img](https://mmbiz.qpic.cn/mmbiz_png/TdGLaSU675hcsS4wOSWWZhZ2WayIL6wVXaTZGkKruLLLkqfWF87ZsnaUuru7u3evCjNVxKOcAhGxicj3m0ibwiasQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

之所以需要实现主从复制，实际上是由实际应用场景所决定的。主从复制能够带来的好处有：

> 1. 通过复制实现数据的异地备份，当主数据库故障时，可切换从数据库，避免数据丢失。
>
> 2. 可实现架构的扩展，当业务量越来越大，I/O访问频率过高时，采用多库的存储，可以降低磁盘I/O访问的频率，提高单个机器的I/O性能。
>
> 3. 可实现读写分离，使数据库能支持更大的并发。
>
> 4. 实现服务器的负载均衡，通过在主服务器和从服务器之间切分处理客户查询的负荷。



**mysql主从是异步复制过程**

master开启`bin-log`功能，日志文件用于记录数据库的读写增删
 需要开启3个线程，master IO线程，slave开启 IO线程 SQL线程，
 Slave 通过IO线程连接master，并且请求某个`bin-log`，position之后的内容。
 MASTER服务器收到slave IO线程发来的日志请求信息，io线程去将bin-log内容，position返回给slave IO线程。
 slave服务器收到bin-log日志内容，将bin-log日志内容写入relay-log中继日志，创建一个master.info的文件，该文件记录了master ip 用户名 密码 master bin-log名称，bin-log position。
 slave端开启SQL线程，实时监控relay-log日志内容是否有更新，解析文件中的SQL语句，在slave数据库中去执行。



**如果数据库误操作, 如何执行数据恢复?**

DB宕机后重启，InnoDB 会首先去查看数据页中的LSN的数值。这个值代表数据页被刷新回磁盘的 LSN 的大小。然后再去查看 redo log 的 LSN 的大小。

如果数据页中的 LSN 值大说明数据页领先于 redo log 刷新回磁盘，不需要进行恢复。反之需要从redo log中恢复数据。

> 注：LSN 是 日志序列号， 为 log sequence number 的缩写，主要用于发生 crash 时对数据进行 recovery。LSN是一个一直递增的整型数字，表示事务写入到日志的字节总量。
>
> LSN 不仅只存在于重做日志中，在每个数据页头部也会有对应的 LSN 号，该 LSN 记录当前页最后一次修改的 LSN 号，用于在 recovery 时对比重做日志 LSN 号决定是否对该页进行恢复数据。
>
> 前面说的check point也是由 LSN 号记录的，LSN 号串联起一个事务开始到恢复的过程。

如果将 innodb_flush_log_at_trx_commit 和 sync_binlog 参数设置成 1，前者表示每次事务的  redo log 都直接持久化到磁盘，后者表示每次事务的 binlog 都直接持久化到磁盘，可以双重保证 MySQL  异常重启之后的数据不会丢失。



**mycat进行主从切换，当一台mysql服务器宕机之后，mycat会切换至另一台进行连接，两台mysql互为主从。**



### 读写分离

主服务器处理写操作以及实时性要求比较高的读操作，而从服务器处理读操作。

读写分离能提高性能的原因在于：

- 主从服务器负责各自的读和写，极大程度缓解了锁的争用；
- 从服务器可以使用 MyISAM，提升查询性能以及节约系统开销；
- 增加冗余，提高可用性。

读写分离常用代理方式来实现，代理服务器接收应用层传来的读写请求，然后决定转发到哪个服务器。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTdSFSNCGjGtjJX0m6iaKL1t7TliaOVnBggj0PJ8cNOPwN2lXJhqDQN8ng/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

## 关系数据库设计理论

### 函数依赖

记 A->B 表示 A 函数决定 B，也可以说 B 函数依赖于 A。

如果 {A1，A2，... ，An} 是关系的一个或多个属性的集合，该集合函数决定了关系的其它所有属性并且是最小的，那么该集合就称为键码。

对于 A->B，如果能找到 A 的真子集 A'，使得 A'-> B，那么 A->B 就是部分函数依赖，否则就是完全函数依赖。

对于 A->B，B->C，则 A->C 是一个传递函数依赖

### 异常

以下的学生课程关系的函数依赖为 {Sno, Cname} -> {Sname, Sdept, Mname, Grade}，键码为 {Sno, Cname}。也就是说，确定学生和课程之后，就能确定其它信息。

| Sno  | Sname  | Sdept  | Mname  | Cname  | Grade |
| :--: | :----: | :----: | :----: | :----: | :---: |
|  1   | 学生-1 | 学院-1 | 院长-1 | 课程-1 |  90   |
|  2   | 学生-2 | 学院-2 | 院长-2 | 课程-2 |  80   |
|  2   | 学生-2 | 学院-2 | 院长-2 | 课程-1 |  100  |
|  3   | 学生-3 | 学院-2 | 院长-2 | 课程-2 |  95   |

不符合范式的关系，会产生很多异常，主要有以下四种异常：

- 冗余数据：例如 `学生-2` 出现了两次。
- 修改异常：修改了一个记录中的信息，但是另一个记录中相同的信息却没有被修改。
- 删除异常：删除一个信息，那么也会丢失其它信息。例如删除了 `课程-1` 需要删除第一行和第三行，那么 `学生-1` 的信息就会丢失。
- 插入异常：例如想要插入一个学生的信息，如果这个学生还没选课，那么就无法插入。

### 范式

范式理论是为了解决以上提到四种异常。

高级别范式的依赖于低级别的范式，1NF 是最低级别的范式。

#### 第一范式 (1NF)

属性不可分。

#### 第二范式 (2NF)

每个非主属性完全函数依赖于键码。

可以通过分解来满足。

**分解前**

| Sno  | Sname  | Sdept  | Mname  | Cname  | Grade |
| :--: | :----: | :----: | :----: | :----: | :---: |
|  1   | 学生-1 | 学院-1 | 院长-1 | 课程-1 |  90   |
|  2   | 学生-2 | 学院-2 | 院长-2 | 课程-2 |  80   |
|  2   | 学生-2 | 学院-2 | 院长-2 | 课程-1 |  100  |
|  3   | 学生-3 | 学院-2 | 院长-2 | 课程-2 |  95   |

以上学生课程关系中，{Sno, Cname} 为键码，有如下函数依赖：

- Sno -> Sname, Sdept
- Sdept -> Mname
- Sno, Cname-> Grade

Grade 完全函数依赖于键码，它没有任何冗余数据，每个学生的每门课都有特定的成绩。

Sname, Sdept 和 Mname 都部分依赖于键码，当一个学生选修了多门课时，这些数据就会出现多次，造成大量冗余数据。

**分解后**

关系-1

| Sno  | Sname  | Sdept  | Mname  |
| :--: | :----: | :----: | :----: |
|  1   | 学生-1 | 学院-1 | 院长-1 |
|  2   | 学生-2 | 学院-2 | 院长-2 |
|  3   | 学生-3 | 学院-2 | 院长-2 |

有以下函数依赖：

- Sno -> Sname, Sdept
- Sdept -> Mname

关系-2

| Sno  | Cname  | Grade |
| :--: | :----: | :---: |
|  1   | 课程-1 |  90   |
|  2   | 课程-2 |  80   |
|  2   | 课程-1 |  100  |
|  3   | 课程-2 |  95   |

有以下函数依赖：

- Sno, Cname ->  Grade

#### 第三范式 (3NF)

非主属性不传递函数依赖于键码。

上面的 关系-1 中存在以下传递函数依赖：

- Sno -> Sdept -> Mname

可以进行以下分解：

关系-11

| Sno  | Sname  | Sdept  |
| :--: | :----: | :----: |
|  1   | 学生-1 | 学院-1 |
|  2   | 学生-2 | 学院-2 |
|  3   | 学生-3 | 学院-2 |

关系-12

| Sdept  | Mname  |
| :----: | :----: |
| 学院-1 | 院长-1 |
| 学院-2 | 院长-2 |

### ER 图

Entity-Relationship，有三个组成部分：实体、属性、联系。

用来进行关系型数据库系统的概念设计。

### 实体的三种联系

包含一对一，一对多，多对多三种。

- 如果 A 到 B 是一对多关系，那么画个带箭头的线段指向 B；
- 如果是一对一，画两个带箭头的线段；
- 如果是多对多，画两个不带箭头的线段。

下图的 Course 和 Student 是一对多的关系。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTct681BjhuyiaVIPbxERpzmmCfPGumDcicxg5mkCSkKVaoyIoJDMH1KpA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 表示出现多次的关系

一个实体在联系出现几次，就要用几条线连接。

下图表示一个课程的先修关系，先修关系出现两个 Course 实体，第一个是先修课程，后一个是后修课程，因此需要用两条线来表示这种关系。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NThdZ4y9CyaAaHDVqKnKIC4nSVHPpGZYUymzesgno3nnYCLxq9ZTjKqg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 联系的多向性

虽然老师可以开设多门课，并且可以教授多名学生，但是对于特定的学生和课程，只有一个老师教授，这就构成了一个三元联系。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTa1a3acMMust1JOSpZfmJHu7pXwJUlhTlvxvVUTG10NmCLuEBgfiafow/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 表示子类

用一个三角形和两条线来连接类和子类，与子类有关的属性和联系都连到子类上，而与父类和子类都有关的连到父类上。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/uChmeeX1FpwqHyYbEIPyeesNicgZ2s5NTqbrdVw5g3szXRVzMj1rVpItVB3TZcia3CAB2D5iceMZEftGuesoKWLwQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





- 



## 其他使用相关

### JSON

> 在实际业务中经常会使用到 JSON 数据类型，在查询过程中主要有两种使用需求：
>
> 1. 在 where 条件中有通过 json 中的某个字段去过滤返回结果的需求
> 2. 查询 json 字段中的部分字段作为返回结果（减少内存占用）

#### JSON_CONTAINS

**JSON_CONTAINS(target, candidate[, path])**

**如果在 json 字段 target 指定的位置 path，找到了目标值 condidate，返回 1，否则返回 0**

**如果只是检查在指定的路径是否存在数据，使用JSON_CONTAINS_PATH()**

```
mysql> SET @j = '{"a": 1, "b": 2, "c": {"d": 4}}';
mysql> SET @j2 = '1';
mysql> SELECT JSON_CONTAINS(@j, @j2, '$.a');
+-------------------------------+
| JSON_CONTAINS(@j, @j2, '$.a') |
+-------------------------------+
|                             1 |
+-------------------------------+
mysql> SELECT JSON_CONTAINS(@j, @j2, '$.b');
+-------------------------------+
| JSON_CONTAINS(@j, @j2, '$.b') |
+-------------------------------+
|                             0 |
+-------------------------------+

mysql> SET @j2 = '{"d": 4}';
mysql> SELECT JSON_CONTAINS(@j, @j2, '$.a');
+-------------------------------+
| JSON_CONTAINS(@j, @j2, '$.a') |
+-------------------------------+
|                             0 |
+-------------------------------+
mysql> SELECT JSON_CONTAINS(@j, @j2, '$.c');
+-------------------------------+
| JSON_CONTAINS(@j, @j2, '$.c') |
+-------------------------------+
|                             1 |
+-------------------------------+
```

#### JSON_CONTAINS_PATH

**JSON_CONTAINS_PATH(json_doc, one_or_all, path[, path] ...)**

**如果在指定的路径存在数据返回 1，否则返回 0**

```
mysql> SET @j = '{"a": 1, "b": 2, "c": {"d": 4}}';
mysql> SELECT JSON_CONTAINS_PATH(@j, 'one', '$.a', '$.e');
+---------------------------------------------+
| JSON_CONTAINS_PATH(@j, 'one', '$.a', '$.e') |
+---------------------------------------------+
|                                           1 |
+---------------------------------------------+
mysql> SELECT JSON_CONTAINS_PATH(@j, 'all', '$.a', '$.e');
+---------------------------------------------+
| JSON_CONTAINS_PATH(@j, 'all', '$.a', '$.e') |
+---------------------------------------------+
|                                           0 |
+---------------------------------------------+
mysql> SELECT JSON_CONTAINS_PATH(@j, 'one', '$.c.d');
+----------------------------------------+
| JSON_CONTAINS_PATH(@j, 'one', '$.c.d') |
+----------------------------------------+
|                                      1 |
+----------------------------------------+
mysql> SELECT JSON_CONTAINS_PATH(@j, 'one', '$.a.d');
+----------------------------------------+
| JSON_CONTAINS_PATH(@j, 'one', '$.a.d') |
+----------------------------------------+
|                                      0 |
+----------------------------------------+
```

实际使用：

```
        $conds = new Criteria();
        $conds->andWhere('dept_code', 'in', $deptCodes);
        if (!empty($aoiAreaId)) {
            $aoiAreaIdCond = new Criteria();
            $aoiAreaIdCond->orWhere("JSON_CONTAINS_PATH(new_aoi_area_ids,'one', '$.\"$aoiAreaId\"')", '=', 1);
            $aoiAreaIdCond->orWhere("JSON_CONTAINS_PATH(old_aoi_area_ids,'one', '$.\"$aoiAreaId\"')", '=', 1);
            $conds->andWhere($aoiAreaIdCond);
        }
```

#### column->path、column->>path

**获取指定路径的值**

**-> vs ->>**

Whereas the -> operator simply extracts a value, the ->> operator in addition unquotes the extracted result.

```
mysql> SELECT * FROM jemp WHERE g > 2;
+-------------------------------+------+
| c                             | g    |
+-------------------------------+------+
| {"id": "3", "name": "Barney"} |    3 |
| {"id": "4", "name": "Betty"}  |    4 |
+-------------------------------+------+
2 rows in set (0.01 sec)

mysql> SELECT c->'$.name' AS name
    ->     FROM jemp WHERE g > 2;
+----------+
| name     |
+----------+
| "Barney" |
| "Betty"  |
+----------+
2 rows in set (0.00 sec)

mysql> SELECT JSON_UNQUOTE(c->'$.name') AS name
    ->     FROM jemp WHERE g > 2;
+--------+
| name   |
+--------+
| Barney |
| Betty  |
+--------+
2 rows in set (0.00 sec)

mysql> SELECT c->>'$.name' AS name
    ->     FROM jemp WHERE g > 2;
+--------+
| name   |
+--------+
| Barney |
| Betty  |
+--------+
2 rows in set (0.00 sec)
```

实际使用：

```
$retTask = AoiAreaTaskOrm::findRows(['status', 'extra_info->>"$.new_aoi_area_infos" as new_aoi_area_infos', 'extra_info->>"$.old_aoi_area_infos" as old_aoi_area_infos'], $cond);
```











# ElasticSearch  

#### 安装  

Elasticsearch 需要 Java 8 环境。如果你的机器还没安装 Java，可以参考[这篇文章](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-get-on-debian-8)，注意要保证环境变量`JAVA_HOME`正确设置。Elastic 就会在默认的http://localhost:9200端口运行。

##### windows

1. 下载Elasticsearch6.2.2的zip包，并解压到指定目录，下载地址：https://www.elastic.co/cn/downloads/past-releases/elasticsearch-6-2-2 (**目前自己使用的是7.9.2，下同**)
2. 安装**中文分词**插件，在elasticsearch-6.2.2\bin目录下执行以下命令：elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v6.2.2/elasticsearch-analysis-ik-6.2.2.zip
3. 运行bin目录下的elasticsearch.bat启动Elasticsearch
4. 下载**Kibana**,作为访问Elasticsearch的客户端，请下载6.2.2版本的zip包，并解压到指定目录，下载地址：https://artifacts.elastic.co/downloads/kibana/kibana-6.2.2-windows-x86_64.zip
5. 运行bin目录下的kibana.bat，启动Kibana的用户界面
6. 访问http://localhost:5601 即可打开Kibana的用户界面
7. ![img](http://www.macrozheng.com/images/arch_screen_30.png)

# Zookeeper

#### [集群搭建](https://blog.51cto.com/14227204/2484928)

**2. zookeeper单机伪集群部署**
在一台主机上跑多个zk实例，每个zk实例对应一个独立的配置文件；但是每个配置文件的clientPort & dataDir & dataLogDir绝对不能相同，还需要在dataDir中创建myid文件来指定该dataDir对应的zk实例。
**环境如下：**
这里在一台物理服务器上，部署3个zk实例
![zookeeper（单机、伪集群、集群）部署](https://s4.51cto.com/images/blog/202004/04/2911e1655b4fa93eff6b4eda63353d82.png?x-oss-process=image/watermark,size_16,text_QDUxQ1RP5Y2a5a6i,color_FFFFFF,t_100,g_se,x_10,y_10,shadow_90,type_ZmFuZ3poZW5naGVpdGk=)
1）安装zookeeper

```shell
#安装好JDK，可参考之前单机安装
[root@zookeeper ~]# java -version 
java version "1.8.0_211"
Java(TM) SE Runtime Environment (build 1.8.0_211-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.211-b12, mixed mode)
#安装zookeeper
[root@zookeeper ~]# tar zxf zookeeper-3.4.14.tar.gz -C /usr/local/
[root@zookeeper ~]# vim /etc/profile
export ZOOKEEPER_HOME=/usr/local/zookeeper-3.4.14
export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$ZOOKEEPER_HOME/bin:$PATH                          
[root@zookeeper ~]# source /etc/profile
#创建数据目录
[root@zookeeper ~]# mkdir -p /usr/local/zookeeper-3.4.14/{data_0,data_1,data_2}
#创建myid文件，并填入ID值
[root@zookeeper ~]# echo 0 > /usr/local/zookeeper-3.4.14/data_0/myid
[root@zookeeper ~]# echo 1 > /usr/local/zookeeper-3.4.14/data_1/myid
[root@zookeeper ~]# echo 2 > /usr/local/zookeeper-3.4.14/data_2/myid
#创建事务日志目录，官方建立尽量给事务日志作单独的磁盘或挂载点，这会极大的提高zk性能
[root@zookeeper ~]# mkdir -p /usr/local/zookeeper-3.4.14/{logs_0,logs_1,logs_2}
#配置server0
[root@zookeeper ~]# cd /usr/local/zookeeper-3.4.14/conf/
[root@zookeeper conf]# cp zoo_sample.cfg zoo_0.cfg
[root@zookeeper conf]# egrep -v "^$|^#" zoo_0.cfg          # 修改配置文件为如下
tickTime=2000
initLimit=10
syncLimit=5
dataDir=/usr/local/zookeeper-3.4.14/data_0/
clientPort=2180
dataLogDir=/usr/local/zookeeper-3.4.14/logs_0/
server.0=127.0.0.1:2287:3387 
server.1=127.0.0.1:2288:3388 
server.2=127.0.0.1:2289:3389 
#配置server1
[root@zookeeper conf]# cp zoo_0.cfg zoo_1.cfg           # 复制之前的配置文件，修改个别参数
[root@zookeeper conf]# vim zoo_1.cfg
dataDir=/usr/local/zookeeper-3.4.14/data_1/
clientPort=2181
dataLogDir=/usr/local/zookeeper-3.4.14/logs_1/
#配置server2
[root@zookeeper conf]# cp zoo_0.cfg zoo_2.cfg
[root@zookeeper conf]# vim zoo_2.cfg
dataDir=/usr/local/zookeeper-3.4.14/data_2/
clientPort=2182
dataLogDir=/usr/local/zookeeper-3.4.14/logs_2/
[root@zookeeper conf]# zkServer.sh start zoo_0.cfg             # 我这里是在conf目录下，所以后面直接接着配置文件，如果不在conf下，则需写全路径
#启动各实例
[root@zookeeper conf]# zkServer.sh start zoo_1.cfg 
[root@zookeeper conf]# zkServer.sh start zoo_2.cfg 
[root@zookeeper conf]# netstat -anput | grep java 
tcp6       0      0 :::2180                 :::*                    LISTEN      9251/java           
tcp6       0      0 :::2181                 :::*                    LISTEN      9291/java           
tcp6       0      0 :::2182                 :::*                    LISTEN      9334/java    
#列出JVM
[root@zookeeper conf]# jps
9377 Jps
9251 QuorumPeerMain
9334 QuorumPeerMain
9291 QuorumPeerMain
#各实例都启动之后就可以使用客户端进行连接了
[root@zookeeper conf]# zkCli.sh -server 127.0.0.1:2180     # 例
```

**关于多个server的配置说明： 这些server表单服务器的条目。列出组成ZooKeeper服务的服务器。当服务器启动  时，它通过在数据目录中查找文件myid来知道它是哪个服务器。该文件包含服务器号。 最后，注意每个服务器  名后面的两个端口号:“2287”和“3387”。对等点使用前一个端口连接到其他对等点。这样的连接是必要的，以便  对等点可以通信，例如，就更新的顺序达成一致。更具体地说，ZooKeeper服务器使用这个端口将追随者连接  到leader。当一个新的领导者出现时，追随者使用这个端口打开一个TCP连接到领导者。由于默认的领导人选举  也使用TCP，我们目前需要另一个端口的领导人选举。这是服务器条目中的第二个端口。**



#### Zookeeper启动

```shell
cd /usr/local/apache-zookeeper-3.6.2-bin/conf
[root@zookeeper conf]# zkServer.sh start zoo_0.cfg  
[root@zookeeper conf]# zkServer.sh start zoo_1.cfg 
[root@zookeeper conf]# zkServer.sh start zoo_2.cfg 
#查看
[root@zookeeper conf]# netstat -anput | grep java 
#列出JVM
[root@zookeeper conf]# jps
#各实例都启动之后就可以使用客户端进行连接了
[root@zookeeper conf]# zkCli.sh -server 127.0.0.1:2180 
```





# Mongodb

服务相关命令

```
启动服务：net start MongoDB
关闭服务：net stop MongoDB
移除服务：D:\developer\env\MongoDB\bin\mongod.exe --remove
```

# RabbitMQ



# SpringCloud



# Hadoop/Spark

# 互联网工具

#### Jenkins

#### Git

#### Maven

#### Nginx

#### Docker









# 事务

## 事务的特性（ACID）

- **原子性(`Atomicity`)**：事务是不可分割的工作单元，要么都成功，要么都失败， 如果事务中一个sql语句执行失败，则已执行的语句也必须回滚，数据库退回到事务前的状态。
- **一致性(`Consistency`)**：事务不能破坏数据的完整性和业务的一致性 。例如在银行转账时，不管事务成功还是失败，双方钱的总额不变
- **隔离性(`Isolation`)**：一个事务所操作的数据在提交之前，对其他事务的可见性设定（一般是不可见）
- **持久性(`Durability`)**：事务提交之后，所做的修改就会永久保存，不会因为系统故障导致数据丢失



**隔离性(`Isolation`)**

以下概念是事务隔离级别要实际解决的问题。

**脏读**

脏读指的是读到了其他事务未提交的数据，未提交意味着这些数据可能会回滚，也就是可能最终不会存到数据库中，也就是不存在的数据。读到了并一定最终存在的数据，这就是脏读。

**不可重复读**

对比可重复读，不可重复读指的是在同一事务内，不同的时刻读到的同一批数据可能是不一样的，可能会受到其他事务的影响，比如其他事务改了这批数据并提交了。通常针对数据**更新（UPDATE）**操作。

**可重复读**

可重复读指的是在一个事务内，最开始读到的数据和事务结束前的任意时刻读到的同一批数据都是一致的。通常针对数据**更新（UPDATE）**操作。

**幻读**

幻读是针对数据**插入（INSERT）**操作来说的。假设事务A对某些行的内容作了更改，但是还未提交，此时事务B插入了与事务A更改前的记录相同的记录行，并且在事务A提交之前先提交了，而这时，在事务A中查询，会发现好像刚刚的更改对于某些数据未起作用，但其实是事务B刚插入进来的，让用户感觉很魔幻，感觉出现了幻觉，这就叫幻读。



当然,   从总的结果来看,   不可重复读和幻读似乎两者都表现为两次读取的结果不一致.

但如果你从控制的角度来看,   两者的区别就比较大
对于前者,   只需要锁住满足条件的记录
对于后者,   要锁住满足条件及其相近的记录
避免不可重复读需要锁行就行
避免幻影读则需要锁表







**事务的传播特性**：是Spring在当前线程内，处理多个数据库操作方法事务时所作的一种事务应用策略。指的是多个事务相互调用时，事务如何在这些方法间传播。

事务本身并不存在什么传播特性，不要混淆事务本身和Spring的事务应用策略。Spring提供了7种传播行为。

| 传播行为                  | 描述                                                         |
| ------------------------- | ------------------------------------------------------------ |
| **PROPAGATION_REQUIRED**  | 默认事务类型，如果没有，就新建一个事务；如果有，就加入当前事务。适合绝大多数情况。 |
| PROPAGATION_REQUIRES_NEW  | 如果没有，就新建一个事务；如果有，就将当前事务挂起。         |
| PROPAGATION_NESTED        | 如果没有，就新建一个事务；如果有，就在当前事务中嵌套其他事务。 |
| PROPAGATION_SUPPORTS      | 如果没有，就以非事务方式执行；如果有，就使用当前事务。       |
| PROPAGATION_NOT_SUPPORTED | 如果没有，就以非事务方式执行；如果有，就将当前事务挂起。即无论如何不支持事务。 |
| PROPAGATION_NEVER         | 如果没有，就以非事务方式执行；如果有，就抛出异常。           |
| PROPAGATION_MANDATORY     | 如果没有，就抛出异常；如果有，就使用当前事务。               |







# JVM

[**史上JVM最最最完整深入解析**](https://mp.weixin.qq.com/s/Pse77Fd2obAdr_q0BJOeRw)

[classloader加载class文件的原理和机制](https://www.jianshu.com/p/52c38cf2e3d4)

## JVM整体架构

![img](https://upload-images.jianshu.io/upload_images/1833901-3a7aa00aa498d8e3.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

JVM被分为三个主要的子系统

（1）类加载器子系统（2）运行时数据区（3）执行引擎



### 类加载器子系统

![img](https://upload-images.jianshu.io/upload_images/1833901-1f90cd995e4e1666.png?imageMogr2/auto-orient/strip|imageView2/2/w/878)

Java的动态类加载功能是由类加载器子系统处理。当它在**运行时**（不是编译时）首次引用一个类时，它加载、链接并初始化该类文件。

#### **类加载器ClassLoader加载**

1. **启动类加载器(BootStrap class Loader)**

   – 由C++实现，负责加载%JAVA_HOME%/lib目录中或-Xbootclasspath中参数指定的路径中的，并且是虚拟机识别的（按名称）类库。这个加载器会被赋予最高优先级。

2. **扩展类加载器 (Extension class Loader)**

   – 由启动类加载器加载，负责加载目录%JRE_HOME%/lib/ext目录中或-Djava.ext.dirs中参数指定的路径中的jar包和class文件负责加载ext 目录(jre\lib)内的类.

3.  **应用程序类加载器(Application class Loader)**

    – 负责加载应用程序级别类路径，涉及到路径的环境变量等etc.上述的类加载器会遵循委托层次算法（Delegation Hierarchy Algorithm）加载类文件，这个在后面进行讲解。

**加载过程**主要完成三件事情：

- **通过类的全限定名来获取定义此类的二进制字节流**
- 将这个类字节流代表的**静态存储结构转为方法区**的运行时数据结构
- 在**堆中生成一个代表此类的java.lang.Class对象**，作为访问方法区这些数据结构的入口。



#### **链接**

- 验证

  文件格式、元数据、字节码验证、符号引用验证

- 准备

  分配内存，并初始化默认值给所有的静态变量。

- 解析

  解析所有符号内存引用被方法区(Method Area)的原始引用所替代。

  举个例子来说明，在com.sbbic.Person类中引用了com.sbbic.Animal类，在编译阶段，Person类并不知道Animal的实际内存地址，因此只能用com.sbbic.Animal来代表Animal真实的内存地址。在解析阶段，JVM可以通过解析该符号引用，来确定com.sbbic.Animal类的真实内存地址（如果该类未被加载过，则先加载）。



#### **初始化**

这是类加载的最后阶段，这里所有的**静态变量会被赋初始值**, 并且**静态块将被执行。**



### Java运行时数据区

![img](https://mmbiz.qpic.cn/mmbiz_png/JdLkEI9sZfdCa89KZ4Ls04tTqXvgxWViaNzBh1nVFhpnSd7jrEWoRLN5c5rf9vdqkSN5CvtnsZSN1oKWvMlYk2g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



1、**程序计数器**：指向当前线程正在执行的字节码指令。线程私有的。

2、**虚拟机栈**：虚拟机栈是Java执行方法的内存模型。每个方法被执行的时候，都会创建一个栈帧，把栈帧压人栈，当方法正常返回或者抛出未捕获的异常时，栈帧就会出栈。

（1）栈帧：栈帧存储方法的相关信息，包含局部变量数表、返回值、操作数栈、动态链接

​		a、局部变量表：包含了方法执行过程中的所有变量。局部变量数组所需要的空间在编译期间完成分配，在方法运行期间不会改变局部变量数组的大小。

​		b、返回值：如果有返回值的话，压入调用者栈帧中的操作数栈中，并且把PC的值指向 方法调用指令 后面的一条指令地址。

​		c、操作数栈：操作变量的内存模型。操作数栈的最大深度在编译的时候已经确定（写入方法区code属性的max_stacks项中）。操作数栈的的元素可以是任意Java类型，包括long和double，32位数据占用栈空间为1，64位数据占用2。方法刚开始执行的时候，栈是空的，当方法执行过程中，各种字节码指令往栈中存取数据。

​		d、动态链接：每个栈帧都持有在运行时常量池中该栈帧所属方法的引用，持有这个引用是为了支持方法调用过程中的动态链接。

​	（2）线程私有

3、**本地方法栈**：（1）调用本地native的内存模型（2）线程独享。

4、**方法区**：用于存储已被虚拟机加载的类信息、常量、静态变量、即时编译后的代码等数据

​	（1）线程共享的

​	（2）运行时常量池：

```
A、是方法区的一部分
B、存放编译期生成的各种字面量和符号引用
C、Class文件中除了存有类的版本、字段、方法、接口等描述信息，还有一项是常量池，存有这个类的 编译期生成的各种字面量和符号引用，这部分内容将在类加载后，存放到方法区的运行时常量池中。
```

5、**堆（Heap）**：Java对象存储的地方

​	（1）Java堆是虚拟机管理的内存中最大的一块

​	（2）Java堆是所有线程共享的区域

​	（3）在虚拟机启动时创建

​	（4）此内存区域的唯一目的就是存放对象实例，几乎所有对象实例都在这里分配内存。存放new生成的对象和数组

​	（5）Java堆是垃圾收集器管理的内存区域，因此很多时候称为“GC堆”



### 执行引擎

分配给运行时数据区的字节码将由执行引擎执行。执行引擎读取字节码并逐段执行。

- **解释器**: 解释器能快速的**解释字节码**，但执行却很慢。  解释器的缺点就是,当一个方法被调用多次，每次都需要重新解释。

- **编译器：**JIT编译器消除了解释器的缺点。执行引擎利用解释器转换字节码，但如果是重复的代码则使用**JIT编译器将全部字节码编译成本机代码**。本机代码将直接用于重复的方法调用，这提高了系统的性能。a. 中间代码生成器– 生成中间代码b. 代码优化器– 负责优化上面生成的中间代码c. 目标代码生成器– 负责生成机器代码或本机代码d. 探测器(Profiler) – 一个特殊的组件，负责寻找被多次调用的方法。

- **垃圾回收器**: 收集并删除未引用的对象。可以通过调用"System.gc()"来触发垃圾回收，但并不保证会确实进行垃圾回收。JVM的垃圾回收只收集哪些由new关键字创建的对象。所以，如果不是用new创建的对象，你可以使用finalize函数来执行清理。Java本地接口 (JNI): JNI会与本地方法库进行交互并提供执行引擎所需的本地库。本地方法库:它是一个执行引擎所需的本地库的集合。



### 常见问题

**Java中new一个对象的步骤：**

1. 当虚拟机遇到一条new指令时候，首先去检查这个指令的参数是否能 **在常量池中能否定位到一个类的符号引用** （即类的带路径全名），并且检查这个符号引用代表的类是否已被加载、解析和初始化过，即**验证是否是第一次使用该类**。如果没有（不是第一次使用），那必须先执行相应的类加载过程（class.forname()）。
2. 在类加载检查通过后，接下来虚拟机将 **为新生的对象分配内存** 。对象所需的内存的大小在类加载完成后便可以完全确定，为对象分配空间的任务等同于把一块确定大小的内存从Java堆中划分出来，目前常用的有两种方式，根据使用的垃圾收集器的不同使用不同的分配机制：
   1.  **指针碰撞**（Bump the Pointer）：假设Java堆的内存是绝对规整的，所有用过的内存都放一边，空闲的内存放在另一边，中间放着一个指针作为分界点的指示器，那所分配内存就仅仅把那个指针向空闲空间那边挪动一段与对象大小相等的距离。
   2. **空闲列表**（Free List）：如果Java堆中的内存并不是规整的，已使用的内存和空间的内存是相互交错的，虚拟机必须维护一个空闲列表，记录上哪些内存块是可用的，在分配时候从列表中找到一块足够大的空间划分给对象使用。
3. 内存分配完后，虚拟机需要将分配到的内存空间中的数据类型都 **初始化为零值（不包括对象头）**；
4. 虚拟机要 **对对象头进行必要的设置** ，例如这个对象是哪个类的实例（即所属类）、如何才能找到类的元数据信息、对象的哈希码、对象的GC分代年龄等信息，这些信息都存放在对象的对象头中。
5. **调用对象的init()方法** ,根据传入的属性值给对象属性赋值。
6. 在线程 **栈中新建对象引用** ，并指向堆中刚刚新建的对象实例。





## **JMM Java内存模型**

1、 Java的并发采用“共享内存”模型，线程之间通过读写内存的公共状态进行通讯。**多个线程之间是不能通过直接传递数据交互的，它们之间交互只能通过共享变量实现。**
2、 主要目的是定义程序中各个变量的访问规则。

**线程之间的通讯只能通过共享变量实现。**

（1） 线程的工作内存中保存了被该线程使用到的变量的拷贝（从主内存中拷贝过来），线程对变量的所有操作都必须在工作内存中执行，而不能直接访问主内存中的变量。
（2） 不同线程之间无法直接访问对方工作内存的变量，线程间变量值的传递都要通过主内存来完成。
（3） 主内存主要对应Java堆中实例数据部分。工作内存对应于虚拟机栈中部分区域。

![clipboard.png](https://mmbiz.qpic.cn/mmbiz_png/YUYc62VIvE36KofZicVtibicnsFTfVn1T8CcZVibWtQiaIib0bFhribBm2vLSjmlCsCNtSOYEicYoQw84pdH0uzWXv2qbg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

4、Java线程之间的通信由内存模型JMM（Java Memory Model）控制。
（1）JMM决定一个线程对变量的写入何时对另一个线程可见。
（2）线程之间共享变量存储在主内存中
（3）每个线程有一个私有的本地内存，里面存储了读/写共享变量的副本。
（4）JMM通过控制每个线程的本地内存之间的交互，来为程序员提供内存可见性保证。



**堆的内存划分：**

![clipboard.png](https://mmbiz.qpic.cn/mmbiz_png/YUYc62VIvE36KofZicVtibicnsFTfVn1T8CEakvseciaNT0fMOoknwyxOwX7O7ZESvqXrps4AOGrT1fIJqkpKquGpg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
Java堆的内存划分如图所示，分别为年轻代、Old Memory（老年代）、Perm（永久代）。其中在Jdk1.8中，永久代被移除，使用MetaSpace代替。
1、新生代：
（1）使用复制清除算法（Copinng算法），原因是年轻代每次GC都要回收大部分对象。新生代里面分成一份较大的Eden空间和两份较小的Survivor空间。每次只使用Eden和其中一块Survivor空间，然后垃圾回收的时候，把存活对象放到未使用的Survivor（划分出from、to）空间中，清空Eden和刚才使用过的Survivor空间。
（2）分为Eden、Survivor From、Survivor To，比例默认为8：1：1
（3）内存不足时发生Minor GC
2、老年代：
（1）采用标记-整理算法（mark-compact），原因是老年代每次GC只会回收少部分对象。
3、Perm：用来存储类的元数据，也就是方法区。
（1）Perm的废除：在jdk1.8中，Perm被替换成MetaSpace，MetaSpace存放在本地内存中。原因是永久代进场内存不够用，或者发生内存泄漏。
（2）MetaSpace（元空间）：元空间的本质和永久代类似，都是对JVM规范中方法区的实现。不过元空间与永久代之间最大的区别在于：元空间并不在虚拟机中，而是使用本地内存。
4、堆内存的划分在JVM里面的示意图：
![clipboard.png](https://mmbiz.qpic.cn/mmbiz_png/YUYc62VIvE36KofZicVtibicnsFTfVn1T8C4hWl8Cf9RS6R9iaRd2fN9wX6E889f2OO9ic3gBvagS1cUzxfMkTODGfw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



## **GC垃圾回收**

一、 判断对象是否要回收的方法：可达性分析法
1、 **可达性分析法**：通过一系列“GC Roots”对象作为起点进行搜索，如果在“GC Roots”和一个对象之间没有可达路径，则称该对象是不可达的。不可达对象不一定会成为可回收对象。进入DEAD状态的线程还可以恢复，GC不会回收它的内存。（把一些对象当做root对象，JVM认为root对象是不可回收的，并且root对象引用的对象也是不可回收的）
2、 以下对象会被认为是root对象：
（1） 虚拟机栈（栈帧中本地变量表）中引用的对象
（2） 方法区中静态属性引用的对象
（3） 方法区中常量引用的对象
（4） 本地方法栈中Native方法引用的对象
3、 对象被判定可被回收，需要经历两个阶段：
（1） 第一个阶段是可达性分析，分析该对象是否可达
（2） 第二个阶段是当对象没有重写finalize()方法或者finalize()方法已经被调用过，虚拟机认为该对象不可以被救活，因此回收该对象。（finalize()方法在垃圾回收中的作用是，给该对象一次救活的机会）
4、 方法区中的垃圾回收：
（1） 常量池中一些常量、符号引用没有被引用，则会被清理出常量池
（2） 无用的类：被判定为无用的类，会被清理出方法区。判定方法如下：
A、 该类的所有实例被回收
B、 加载该类的ClassLoader被回收
C、 该类的Class对象没有被引用
5、 finalize():
（1） GC垃圾回收要回收一个对象的时候，调用该对象的finalize()方法。然后在下一次垃圾回收的时候，才去回收这个对象的内存。
（2） 可以在该方法里面，指定一些对象在释放前必须执行的操作。

二、 **发现虚拟机频繁full GC时应该怎么办**：
（full GC指的是清理整个堆空间，包括年轻代和永久代）
（1） 首先用命令查看触发GC的原因是什么 jstat –gccause 进程id
（2） 如果是System.gc()，则看下代码哪里调用了这个方法
（3） 如果是heap inspection(内存检查)，可能是哪里执行jmap –histo[:live]命令
（4） 如果是GC locker，可能是程序依赖的JNI库的原因

三、**常见的垃圾回收算法**：
1、Mark-Sweep（标记-清除算法）：
（1）思想：标记清除算法分为两个阶段，标记阶段和清除阶段。标记阶段任务是标记出所有需要回收的对象，清除阶段就是清除被标记对象的空间。
（2）优缺点：实现简单，容易产生内存碎片
2、Copying（复制清除算法）：
（1）思想：将可用内存划分为大小相等的两块，每次只使用其中的一块。当进行垃圾回收的时候了，把其中存活对象全部复制到另外一块中，然后把已使用的内存空间一次清空掉。
（2）优缺点：不容易产生内存碎片；可用内存空间少；存活对象多的话，效率低下。
3、Mark-Compact（标记-整理算法）：
（1）思想：先标记存活对象，然后把存活对象向一边移动，然后清理掉端边界以外的内存。
（2）优缺点：不容易产生内存碎片；内存利用率高；存活对象多并且分散的时候，移动次数多，效率低下

4、**分代收集算法**：（目前大部分JVM的垃圾收集器所采用的算法）：

```
思想：把堆分成新生代和老年代。（永久代指的是方法区）
```

（1） 因为新生代每次垃圾回收都要回收大部分对象，所以新生代采用Copying算法。新生代里面分成一份较大的Eden空间和两份较小的Survivor空间。每次只使用Eden和其中一块Survivor空间，然后垃圾回收的时候，把存活对象放到未使用的Survivor（划分出from、to）空间中，清空Eden和刚才使用过的Survivor空间。
（2） 由于老年代每次只回收少量的对象，因此采用mark-compact算法。
（3） 在堆区外有一个永久代。对永久代的回收主要是无效的类和常量
5、GC使用时对程序的影响？
垃圾回收会影响程序的性能，Java虚拟机必须要追踪运行程序中的有用对象，然后释放没用对象，这个过程消耗处理器时间
6、几种不同的垃圾回收类型：
（1）Minor GC：从年轻代（包括Eden、Survivor区）回收内存。

```
A、当JVM无法为一个新的对象分配内存的时候，越容易触发Minor GC。所以分配率越高，内存越来越少，越频繁执行Minor GC
B、执行Minor GC操作的时候，不会影响到永久代（Tenured）。从永久代到年轻代的引用，被当成GC Roots，从年轻代到老年代的引用在标记阶段直接被忽略掉。
```

（2）Major GC：清理整个老年代，当eden区内存不足时触发。
（3）Full GC：清理整个堆空间，包括年轻代和老年代。当老年代内存不足时触发



### GC参数

- 串行回收器

  - SerialGC

    - -XX:+UseSerialGC

      - 新生代、老年代使用串行回收
      - 新生代复制清除算法
      - 老年代标记压缩

      效率高，稳定，可能产生较长时间停顿（GC时应用线程挂起）

- 并行收集器

  - ParNew

    - -XX:+UseParNewGC
      - 新生代并行、老年代串行
      - Serial收集器新生代的并行版本，需要多核支持（GC时应用线程挂起）
      - -XX:ParallelGCThreads限制线程数量

  - Parallel收集器

    类似ParNew

    - -XX:+UseParallelGC
      - 使用Parallel收集器+老年代串行
    - -XX:+UseParallelOldGC
      - 使用Parallel收集器+老年代并行

  - CMS收集器（并行，不会Stop the world）

    - Concurrent Mark Sweep 并发标记清除
    - 降低吞吐量
    - -XX:+UseConcMarkSweepGC
    - 老年代收集器，不会作用在新生代

  





## 常用JVM配置参数

- Trace跟踪参数

  ​		查看GC日志

  - -XX:+printGC

  - -XX:+PrintGCDetails

    指定GC日志位置

  - -Xloggc:log/gc.log

    每一次GC后，都打印堆信息

  - -XX:+PrintHeapAtGC

    监控类的加载

  - -XX:+TraceClassLoading

- 堆的分配参数

  - -Xmx -Xms

    --指定最大堆和最小堆

  - -Xmn

    --设置新生代大小

  - -XX:NewRatio

    --老年代与新生代的比值

  - -XX:SurvivorRatio

    --eden与两个Servivor区的比值，默认8

- 栈的分配参数

  - -Xss

    通常只有几百K



- 



## 性能监控工具

### 命令

uptime

top

vmstat 

pidstat

pslist

jsp

jinfo

jmap

jstack

JConsole



# 分布式

## 分布式锁与分布式事务

### 分布式锁

针对分布式锁，目前有以下几种实现方案（From: http://www.hollischuang.com/a...）

- **基于数据库实现分布式锁**
- **基于缓存实现分布式锁**
- **基于zookeeper实现分布式锁**



##### 基于缓存实现分布式锁

###### Redis

谈起redis锁，下面三个，算是出现最多的高频词汇：

- setnx
- redLock
- redisson



**实现思路**

锁的实现主要基于redis的SETNX命令（SETNX详细解释参考这里），我们来看SETNX的解释

    SETNX key value
    将 key 的值设为 value ，当且仅当 key 不存在。
    若给定的 key 已经存在，则 SETNX 不做任何动作。
    SETNX 是『SET if Not eXists』(如果不存在，则 SET)的简写。
    
    返回值：
    设置成功，返回 1 。
    设置失败，返回 0 。

使用SETNX完成同步锁的流程及事项如下：

    使用SETNX命令获取锁，若返回0（key已存在，锁已存在）则获取失败，反之获取成功
    为了防止获取锁后程序出现异常，导致其他线程/进程调用SETNX命令总是返回0而进入死锁状态，需要为该key设置一个“合理”的过期时间
    释放锁，使用DEL命令将锁数据删除

------

**这个命令是可以保证原子性的。**

因为redis本身是单例队列处理的，你再多高并发请求获取锁都是排队进行，也就是只有前边第一个获取成功，后边的都获取失败。

这使得`SET {key} {value} EX {expiry} NX`非常适合简单的锁定。

[**实现过程**](https://segmentfault.com/a/1190000012919740)



**那么为什么要使用`PX 30000`去设置一个超时时间？**

进程故障，没人能拿到锁，锁一直挂着。

**设置超时时间的问题呢？**

进程A set成功拿到锁，去操作资源，但是操作的时间太久，这时key超时了，另外的线程Bsetc成功拿到锁，然后A回来反手一个del将锁删除，B就懵逼了。又或者，A操作B的锁，B操作C的锁，...禁止套娃啊。

所以在用**setnx**的时候，key虽然是主要作用，但是**value**也不能闲着，可以设置一个**唯一的客户端ID**，或者用**UUID**这种随机数。

当解锁的时候，先获取value判断是否是当前进程加的锁，再去删除。**伪代码**：

```java
String uuid = xxxx;
// 伪代码，具体实现看项目中用的连接工具
// 有的提供的方法名为set 有的叫setIfAbsent
set Test uuid NX PX 3000
**try**{
// biz handle....
} **finally** {
  // unlock
  **if**(uuid.equals(redisTool.get('Test')){
    redisTool.del('Test');
  }
}
```

但是在finally代码块中，**get和del并非原子操作**，还是有进程安全问题。

那么删除锁的正确姿势之一，就是可以使用**lua**脚本，通过redis的**eval**/**evalsha**命令来运行：

```lua
-- lua删除锁：
-- KEYS和ARGV分别是以集合方式传入的参数，对应上文的Test和uuid。
-- 如果对应的value等于传入的uuid。
**if** redis.call('get', KEYS[1]) == ARGV[1]
  then
 -- 执行删除操作
    **return** redis.call('del', KEYS[1])
  **else**
 -- 不成功，返回0
    **return** 0
end
```

通过**lua**脚本能保证原子性的原因说的通俗一点：

就算你在**lua**里写出花，执行也是一个命令(**eval**/**evalsha**)去执行的，一条命令没执行完，其他客户端是看不到的。



那么既然这么麻烦，有没有比较好的工具呢？就要说到**redisson**了。



***Redisson***

Redisson是**java的redis客户端之一**，提供了一些api方便操作redis。

Redisson普通的锁实现源码主要是**RedissonLock**这个类。

源码中**加锁/释放锁**操作都是用**lua**脚本完成的，封装的非常完善，开箱即用。

加锁解锁的lua脚本考虑的非常全面，其中就包括**锁的重入性**，这点可以说是考虑非常周全



**RedLock**

红锁并非是一个工具，而是redis官方提出的一种分布式锁的**算法**。







# 数据结构和算法



## 排序

### 冒泡排序

```java
private static void bubbleSort(int[] array) {
    //从后开始遍历len-1次，每次都将最大的放在最后
    for (int i = array.length-1;i>0;i--) {
        //每次都交换最大的数在最后位
        for (int j = 0;j<i;j++) {
            if (array[j]>array[j+1]) {
                int temp = array[j];
                array[j]=array[j+1];
                array[j+1]=temp;
            }
        }
    }
}
```

### 快速排序

**挖坑填数法**

下图中单词有两处拼写错误，pviot和pvoit应该为pivot

![img](https://img2018.cnblogs.com/blog/562030/201812/562030-20181206172133907-1934167112.png)

原理：

1.维护左右2个指针，目的是使数组局部有序（左边小于基准点，右边大于基准点）

2.取第一个为基准值，记录，从right指针开始往左遍历，直到遇到比基准小的数时停止,将arr[left]赋值为arr[right]，然后推动left指针，left指针往右遍历，遇到大于基准值时停止，然后赋值arr[right]=arr[left]，直到指针完成碰撞。最后将基准值赋值给交界点的位置。此时交界点左边的值全部小于等于基准值，右边的值全部大于等于基准值。

3.这时交界点将数组分为左右2支，递归排序即可。

注意：

1.推动指针时要注意边界条件，不能一次循坏将left与right指针推过了left>right。

2.递归调用时一定要注意被调用的数组要减小，否则会没有终止条件，比如数组本来就是有序的。



```java
private static void quickSort(int[] arr, int start, int end) {
        if (start >= end) {
            return;
        }
        int temp = arr[start];
        int low = start;
        int high = end;
        while (low < high) {
            //从后面开始找
            //后面大于基准数的数不动
            //这里low < high条件必不可少，不然有可能会让high--一直执行下去，这里结束如果携程low<=high，那么赋值这步虽然没影响，但是low会继续向前推进，导致low>high
            while (arr[high] >= temp&&low < high) {
                high--;
            }
            //找到小于基准的数了，那就赋值给前面的坑.这里arr[low++]下标不可以随意向前推进，因为循环里面一次不能同时推进2次，否则会导致low>high
            arr[low]=arr[high];
            //再从前面开始找，推进前面坑位
            while (arr[low]<=temp&&low < high) {
                low++;
            }
            //找到大于基准的数了，那就赋值给后面的坑
            arr[high]=arr[low];
        }
        //循环出来时再将基准值赋给最后的坑，也就是分界线
        arr[high]=temp;
        //此时已经完成工作，左边小于等于base，右边大于等于base
        //递归时必须要让排序的数组变小，不让没办法走到数组的长度为1这个结束条件
        quickSort(arr,start,low-1);
        quickSort(arr,low+1,end);

    }
```

### 归并排序

思路：采用分治的思想，将大问题分区，分区结束后再合并时排序，这样合并完成之后数组有序，往上合并后仍有序。也就是先拆，拆到不可再分之后再合。所有栈都在等待merge调用。而merge函数所作的事就是合起来排序。

[[图解]](https://www.jianshu.com/p/33cffa1ce613) 

![img](https://upload-images.jianshu.io/upload_images/7789414-b410a7c0fea50eba.png?imageMogr2/auto-orient/strip|imageView2/2/w/1141)![img](https://upload-images.jianshu.io/upload_images/7789414-4b8f4cb3cb5f0a9f.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

```java
private static void mergeSort(int[] arr) {
        sort(arr,0,arr.length-1);
    }

    private static void sort(int[] arr, int left, int right) {
        //递归终止条件，分区只有一个元素时栈帧不再push，开始pop。
        if (left>=right) {
            return;
        }
        //中间元素指针
        int mid = (left+right)/2;
        //分别将左右分区排序
        sort(arr,left,mid);
        sort(arr,mid+1,right);
        //实际上上面只做了分区，没有做排序，现在只需要将分区排序好，那么就可以保证下一次的调用每个分区有序
        merge(arr,left,mid,right);
    }

    private static void merge(int[] arr, int left, int mid, int right) {

        int[] tmpArr = new int[arr.length];
        int rStart = mid+1;
        int lStart = left;
        int tmpIndex= left;
        while (lStart<=mid && rStart<=right) {
            if (arr[lStart]<=arr[rStart]) {
                tmpArr[tmpIndex++] = arr[lStart++];
            }else {
                tmpArr[tmpIndex++] = arr[rStart++];
            }
        }
        while (lStart<=mid){
            tmpArr[tmpIndex++]=arr[lStart++];
        }
        while (rStart<=right){
            tmpArr[tmpIndex++]=arr[rStart++];
        }
        //tmpArr为有序数组，再赋值回原数组
        while (left<=right){
            //这个位置不能++2次
            arr[left]=tmpArr[left++];
        }
    }
```

### 插入排序

```java
private static void insertSort(int[] arr) {
    for (int i=1;i<arr.length;i++) {
        int temp = arr[i];
        int j;
        //待排序元素比前一个小时才插入，否则不插入
        if (arr[i]<arr[i-1]){
            for (j=i-1;j>=0;j--) {
                if (arr[j]>temp){
                    arr[j+1]=arr[j];
                }else {
                    break;
                }
            }
            arr[j+1]=temp;
        }
    }
}
```

### 希尔排序

[图解](https://www.cnblogs.com/chengxiao/p/6104371.html)

在希尔排序的理解时，我们倾向于对于每一个分组，逐组进行处理，但在代码实现中，我们可以不用这么按部就班地处理完一组再调转回来处理下一组（这样还得加个for循环去处理分组）比如[5,4,3,2,1,0] ，首次增量设gap=length/2=3,则为3组[5,2] [4,1]  [3,0]，实现时不用循环按组处理，我们可以从第gap个元素开始，逐个跨组处理。同时，在插入数据时，可以采用元素交换法寻找最终位置，也可以采用数组元素移动法寻觅。

```java
 private static void shellSort(int[] arr) {

        for (int gap = arr.length/2;gap>0;gap=gap/2){
            for (int i = gap;i<arr.length;i++) {
                if (arr[i-gap]>arr[i]) {
                    int tmp = arr[i];
                    int j;
                    for (j=i-gap;j>=0;j=j-gap) {
                        if (arr[j]>tmp) {
                            arr[j+gap]=arr[j];
                        }else {
                            break;
                        }
                    }
                    arr[j+gap]=tmp;
                }
            }
        }
    }
```



### 堆排序

**[图解](https://www.cnblogs.com/chengxiao/p/6129630.html)**

思路：

将待排序序列构造成一个大顶堆，此时，整个序列的最大值就是堆顶的根节点。将其与末尾元素进行交换，此时末尾就为最大值。然后将剩余n-1个元素重新构造成一个堆，这样会得到n个元素的次小值。如此反复执行，便能得到一个有序序列了

注意：

调整堆时，当前节点交换后需要再次调整其子节点；

本次处理完后当前节点的指针需要指向其子节点；

堆构建后以后只需要调整堆顶arr[0]节点就行了

```java
private static void heapSort(int[] arr) {
        //构建大顶堆
        for (int i = arr.length/2-1;i>=0;i--) {
            adjustHeap(arr,i,arr.length);
        }
        //调整
        for (int j = arr.length-1;j>0;j--) {
            swap(arr,0,j);
            //已经是大顶堆了，那么只需将堆顶元素下沉就可以了，仍然是大顶堆
            adjustHeap(arr,0,j);
        }
    }
    
    private static void adjustHeap(int[] arr, int i, int len) {
        int tmp = arr[i];
        for (int k = 2*i+1;k<len;k=2*k+1) {
            if (k+1<len && arr[k+1] >arr[k]) {
                k++;
            }
            if (tmp<arr[k]) {
                arr[i]=arr[k];
                //这个的目的在于将起始位重置
                i=k;
            }
        }
        arr[i]=tmp;
    }
```



### 桶排序

**算法过程**

1. 根据待排序集合中最大元素和最小元素的差值范围和映射规则，确定申请的桶个数；
2. 遍历待排序集合，将每一个元素移动到对应的桶中；
3. 对每一个桶中元素进行排序，并移动到已排序集合中。

**实质就是将元素已合理的规则映射到桶中，使得不同桶元素是有序的，然后桶内再按照其他方式排序。**



```java
private static void buckedSort(int[] arr) {
    int max=arr[0];
    int min=arr[0];
    for (int i: arr) {
        if (max<i){
            max=i;
        }
        if (min>i){
            min=i;
        }
    }
    //桶个数
    //映射规则为：f(x)=\frac x{10}-c，其中常量位：c=\frac {min}{10}，即以间隔大小 10 来区分不同值域
    int buckedNum=(max-min)/10+1;
    ArrayList<ArrayList<Integer>> buckedList = new ArrayList<>(buckedNum);
    for (int i=0;i<buckedNum;i++) {
        buckedList.add(new ArrayList<>());
    }
    // 将每个元素放入桶
    for (int value: arr) {
        buckedList.get((value-min)/10).add(value);
    }
    // 对每个桶进行排序
    for (ArrayList list : buckedList) {
        Collections.sort(list);
    }
    // 将桶中的元素赋值到原序列
    int tmp=0;
    for (int i=0;i<buckedList.size();i++){
        for (int j : buckedList.get(i)){
            arr[tmp++]=j;
        }
    }
}
```



### 基数排序

原理：
类似桶排序,这里总是需要10个桶,多次使用

首先以个位数的值进行装桶,即个位数为1则放入1号桶,为9则放入9号桶,暂时忽视十位数

**例如**

待排序数组[62,14,59,88,16]简单点五个数字

分配10个桶,桶编号为0-9,以个位数数字为桶编号依次入桶,变成下边这样

| 0 | 0 | 62 | 0 | 14 | 0 | 16 | 0 | 88 | 59 |

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |桶编号

将桶里的数字顺序取出来,

输出结果:[62,14,16,88,59]

再次入桶,不过这次以十位数的数字为准,进入相应的桶,变成下边这样:

由于前边做了个位数的排序,所以当十位数相等时,个位数字是由小到大的顺序入桶的,就是说,入完桶还是有序。

**所以只要每次将位数上排完赋值给元素组就好了。**

```java
 private static void radixSort(int[] arr) {
        //获取最大值
        int max = getMax(arr);
        //获取最大值位数；
        int digit = getMaxDigit(max);
        List<ArrayList<Integer>> queue = new ArrayList<>();//多维数组
        initList(queue);
        for (int i=0;i<digit;i++) {
            for (int j=0;j<arr.length;j++) {
                //获取对应位的值（i为0是个位，1是十位，2是百位）
                int digitValue = arr[j]%(int)Math.pow(10,i+1)/(int)Math.pow(10,i);
                ArrayList list = queue.get(digitValue);
                list.add(arr[j]);
            }
            //开始收集，赋值到原数组
            int count = 0;
            for (int k=0;k<10;k++){
                for (int tmp: queue.get(k)){
                    arr[count++]=tmp;
                }
                queue.get(k).clear();
            }
        }
    }
```



## 算法

**分治思想**

**动态规划**

**贪心算法**

**回溯算法**

**分支限界法**

**遗传算法**

# 计算机网络

[两大分析网络的利器](https://mp.weixin.qq.com/s/n1O4zrbt1nnF3GKhHFPA5g)：**tcpdump 和 Wireshark**

tcpdump 和 Wireshark 就是最常用的网络抓包和分析工具，更是分析网络性能必不可少的利器。

- tcpdump 仅支持命令行格式使用，常用在 Linux 服务器中抓取和分析网络包。
- Wireshark 除了可以抓包外，还提供了可视化分析网络包的图形页面。

所以，这两者实际上是搭配使用的，先用 tcpdump 命令在 Linux 服务器上抓包，接着把抓包的文件拖出到 Windows 电脑后，用 Wireshark 可视化分析。

当然，如果你是在 Windows 上抓包，只需要用 Wireshark 工具就可以。



**TCP协议**

TCP 进行握手初始化一个连接的目标是：分配资源、初始化序列号(通知 peer 对端我的初始序列号是多少)

三次握手可以简化理解为：

1. Client端首先发送一个SYN包告诉Server端要开始连接，并告诉自己的序列号x；
2. Server端收到后会发送一个ACK确认包告诉Client说自己收到了，并发送一个SYN包并告诉对方自己的序列号y
3. Client收到后，回复Server一个ACK确认包告诉对方说我知道了。



TCP 进行断开连接的目标是：回收资源、终止数据传输。由于 TCP 是全双工的，需要 Peer 两端分别各自拆除自己通向 Peer 对端的方向的通信信道。

四次挥手可以简化理解为：

1. Client发送一个FIN包告诉Server自己已经没有数据需要发送给Server了；
2. Server收到后回复一个ACK确认包说我知道了；
3. 然后Server端自己也没数据发送给Client时，会发送一个FIN包给Client告诉对方自己也没数据发送了
4. Client收到后恢复ACK确认包说自己知道了，双方拆除信道。



为什么TIME_WAIT状态需要经过2MSL(最大报文段生存时间)才能返回到CLOSE状态？

答：虽然按道理，四个报文都发送完毕，我们可以直接进入CLOSE状态了，但是我们必须假象网络是不可靠的，有可以最后一个ACK丢失。所以TIME_WAIT状态就是用来重发可能丢失的ACK报文。在Client发送出最后的ACK回复，但该ACK可能丢失。Server如果没有收到ACK，将不断重复发送FIN片段。所以Client不能立即关闭，它必须确认Server接收到了该ACK。Client会在发送出ACK之后进入到TIME_WAIT状态。Client会设置一个计时器，等待2MSL的时间。如果在该时间内再次收到FIN，那么Client会重发ACK并再次等待2MSL。所谓的2MSL是两倍的MSL(Maximum Segment  Lifetime)。MSL指一个片段在网络中最大的存活时间，2MSL就是一个发送和一个回复所需的最大时间。如果直到2MSL，Client都没有再次收到FIN，那么Client推断ACK已经被成功接收，则结束TCP连接。



# IDEA

## 快捷键

查看接口实现：ctrl + h 

查看类所有方法：Alt+7



# 实用工具

## 文档编辑

### Typora 

Markdown编辑器



# 技能

- 熟悉Java语法，集合、多线程等基础框架
- 熟悉数据结构与算法
- 熟悉Spring,SpringMVC,MyBatis等开源框架技术
- 熟悉SpringBoot+SpringCloud微服务架构
- 熟悉Mysql数据库及其优化
- 熟悉Redis缓存
- 了解Kafka，ES，MongoDB
- 了解Linux常用命令及一些故障排查
- 了解Docker,Nginx,Jenkins





熟悉微服务架构，了解分布式、缓存、消息等常见开源框架

了解Linux常用命令及一些故障排查，了解python/shell脚本

