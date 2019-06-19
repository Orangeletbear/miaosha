![互联网 Java 秒杀系统设计与架构](https://raw.githubusercontent.com/qiurunze123/imageall/master/miaoshashejitu.png)

> 邮箱 : [QiuRunZe_key@163.com](QiuRunZe_key@163.com)

> Github : [https://github.com/qiurunze123](https://github.com/qiurunze123)

> QQ : [3341386488](3341386488)

[![GQ Welcome](https://raw.githubusercontent.com/qiurunze123/imageall/master/2018.png)](https://github.com/qiurunze123)
[![Travis](https://img.shields.io/badge/language-Java-yellow.svg)](https://github.com/qiurunze123)
高并发大流量如何进行秒杀架构，我对这部分知识做了一个系统的整理，写了一套系统。本GitHub还有许多其他的知识，随时欢迎探讨与骚扰！

一点小建议：学习本系列知识之前，如果你完全没接触过 `MQ`、`SpringBoot`、`Redis`、`Dubbo`、`ZK` 、`Maven`等，那么我建议你可以先在网上搜一下每一块知识的快速入门，也可以下载本项目边做边学习，然后再开始每一块知识的学习。这样效果更好噢~

### 秒杀高并发架构 -- 架构图

> 软件环境 : 请选择稳定版 

![整体流程](https://raw.githubusercontent.com/qiurunze123/imageall/master/miaosha.png)

> 软件环境 : mysql 数据库表设计

![整体流程](https://raw.githubusercontent.com/qiurunze123/imageall/master/miaoshasql.png)

>1.需注意 因为秒杀，大促，打折等活动进行频繁，所以需要单独建立秒杀_....表来管理否则会经常进行回归

>2.本sql只是进行模拟，现实情况比这个信息要复杂的多，你可以把它看作是一个简化版本的sql

>3.详情请看miaosha.sql

 
###  [如要提交代码请先看--提交合并代码规范](/docs/code-criterion.md)

| ID | Problem  | Article | 
| --- | ---   | :--- |
| 000 |如何解决卖超问题 | [解决思路](/docs/code-solve.md) |
| 001 |全局异常处理拦截 |[解决思路](/docs/code-solve.md)  |
| 002 |页面级缓存thymeleafViewResolver |[解决思路](/docs/code-solve.md)  |
| 003 |对象级缓存redis🙋🐓 |[解决思路](/docs/code-solve.md)  |
| 004 |订单处理队列rabbitmq |[解决思路](/docs/code-solve.md)  |
| 005 |解决分布式session |[解决思路](/docs/code-solve.md)  |
| 006 |秒杀安全 -- 安全性设计 |[解决思路](/docs/code-solve.md)  |
| 007 |通用缓存key的封装采用什么设计模式 |[解决思路](/docs/code-solve.md)  |
| 008 |redis的库存如何与数据库的库存保持一致 |[解决思路](/docs/code-solve.md)  |
| 009 |为什么redis数量会减少为负数 |[解决思路](/docs/code-solve.md)  |
| 010 |为什么要单独维护一个秒杀结束标志 |[解决思路](/docs/code-solve.md)  |
| 011 |rabbitmq如何做到消息不重复不丢失即使服务器重启 |[解决思路](/docs/code-solve.md)  |
| 012 |为什么threadlocal存储user对象，原理 |[解决思路](/docs/code-solve.md)  |
| 013 |maven 隔离 |[解决思路](/docs/code-solve.md)  |
| 014 |服务降级--服务熔断(过载保护)） |[解决思路](/docs/code-solve.md)  |
| 015 |redis 分布式锁实现方法 |[解决思路](/docs/code-solve.md)  |
| 016 |定时关单模拟与分布式锁 |[解决思路](/docs/code-solve.md)  |
| 017 |tomcat配置和优化  |[解决思路]((/docs/tomcat-good.md))  |
| 018 |tomcat集群配置 |[解决思路](/docs/tomcat-group.md)  |
| 019 |Nginx优化（前端缓存） |[解决思路](/docs/ngnix-good.md)  |
| 020 |RPC分布式补偿如何解决 |[解决思路](/docs/code-solve.md)   |
| 021 |mysql主从复制思路及节约 |[解决思路](/docs/mysql-master-slave.md)   |


#### [定时关单模拟与分布式锁](/docs/time-close.md)
#### [mybatis源码解析](/docs/mybatis-code.md)
#### [tomcat配置和优化](/docs/tomcat-good.md)
#### [tomcat集群配置](/docs/tomcat-group.md)
#### [Nginx优化（前端缓存）](/docs/ngnix-good.md)
#### [如何进行分库分表](/docs/ngnix-good.md)
     1.并发优化 2.Keepalive长连接 3.压缩优化 4.配置缓存5.监控工具
### [缓存](/docs/why-cache.md)
- [在项目中缓存是如何使用的？缓存如果使用不当会造成什么后果？](/docs/why-cache.md)
- [Redis 和 Memcached 有什么区别？Redis 的线程模型是什么？为什么单线程的 Redis 比多线程的 Memcached 效率要高得多？](/docs/redis-single-thread-model.md)
- [Redis 都有哪些数据类型？分别在哪些场景下使用比较合适？](/docs/redis-data-types.md)
- [Redis 的过期策略都有哪些？手写一下 LRU 代码实现？](/docs/redis-expiration-policies-and-lru.md)
- [如何保证 Redis 高并发、高可用？Redis 的主从复制原理能介绍一下么？Redis 的哨兵原理能介绍一下么？](/docs/how-to-ensure-high-concurrency-and-high-availability-of-redis.md)
- [Redis 的持久化有哪几种方式？不同的持久化机制都有什么优缺点？持久化机制具体底层是如何实现的？](/docs/redis-persistence.md)
- [Redis 集群模式的工作原理能说一下么？在集群模式下，Redis 的 key 是如何寻址的？分布式寻址都有哪些算法？了解一致性 hash 算法吗？如何动态增加和删除一个节点？](/docs/redis-cluster.md)
- [了解什么是 Redis 的雪崩和穿透？Redis 崩溃之后会怎么样？系统该如何应对这种情况？如何处理 Redis 的穿透？](/docs/redis-caching-avalanche-and-caching-penetration.md)
- [如何保证缓存与数据库的双写一致性？](/docs/redis-consistence.md)
- [Redis 的并发竞争问题是什么？如何解决这个问题？了解 Redis 事务的 CAS 方案吗？](/docs/redis-cas.md)
- [生产环境中的 Redis 是怎么部署的？](/docs/redis-production-environment.md)

## 高可用架构
- [Hystrix 介绍](/docs/hystrix-introduction.md)
- [电商网站详情页系统架构](/docs/e-commerce-website-detail-page-architecture.md)

### 高可用系统
- 如何设计一个高可用系统？

### 限流
- 如何限流？在工作中是怎么做的？说一下具体的实现？

### 熔断
- 如何进行熔断？
- 熔断框架都有哪些？具体实现原理知道吗？

### 降级
- 如何进行降级？