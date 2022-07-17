# Redis

## 前述

1、本篇分六个部分来介绍Redis，分别为以下：

【1】概述：Redis概述、文件、数据类型、基本功能、基本管理、基本命令。

【2】架构：主从模式、哨兵模式、集群模式。

【3】配置：Redis相关配置文件。

【4】工具：Redis相关工具（CLI、GUI、Proxy）及Redis Client等。

【5】场景：缓存、消息队列、分布式锁

【6】其他：其他相关重要部分

2、使用版本：Redis 7.0.3

3、官方手册：https://redis.io/docs/

## 概述

### 概述

### 文件

### 数据类型

###### 基本介绍

Redis is not a plain key-value store,it is actually a data structures server, supporting different kinds of values.

###### 数据类型

1、Strings ：

【1】Strings are the most basic kind of Redis value. Redis Strings are binary safe, this means that a Redis string can contain any kind of data, for instance a JPEG image or a serialized Ruby object.

【2】A String value can be at max 512 Megabytes in length.

2、Lists ： 

【1】Redis Lists are simply lists of strings, sorted by insertion order. 

3、Sets ： 

【1】Redis Sets are an unordered collection of Strings. 

4、Hashes ： 

【1】Redis Hashes are maps between string fields and string values, so they are the perfect data type to represent objects.

【2】Every hash can store up to 2^32 - 1 field-value pairs (more than 4 billion).

5、Sorted Sets

【1】Redis Sorted Sets are, similarly to Redis Sets, non repeating collections of Strings. 

【2】The difference is that every member of a Sorted Set is associated with a score, that is used to keep the Sorted Set in order, from the smallest to the greatest score. 

【3】 While members are unique, scores may be repeated.

6、Bitmaps

【1】待补

7、HyperLogLogs

【1】待补

8、Streams

【1】待补

9、Geospatial indexes

【1】待补

### 基本功能

###### Transactions

1、Redis Transactions allow the execution of a group of commands in a single step, they are centered around the commands MULTI, EXEC, DISCARD and WATCH. 

2、Redis Transactions make two important guarantees

【1】All the commands in a transaction are serialized and executed sequentially.

【2】The EXEC command triggers the execution of all the commands in the transaction, so if a client loses the connection to the server in the context of a transaction before calling the EXEC command none of the operations are performed, instead if the EXEC command is called, all the operations are performed.

3、rollbacks

【1】Redis does not support rollbacks of transactions since supporting rollbacks would have a significant impact on the simplicity and performance of Redis.

###### Pub/sub

1、SUBSCRIBE, UNSUBSCRIBE and PUBLISH implement the Publish/Subscribe messaging paradigm where (citing Wikipedia) senders (publishers) are not programmed to send their messages to specific receivers (subscribers).

2、Once the client enters the subscribed state it is not supposed to issue any other commands, except for additional SUBSCRIBE, SSUBSCRIBE, PSUBSCRIBE, UNSUBSCRIBE, SUNSUBSCRIBE, PUNSUBSCRIBE, PING, RESET and QUIT commands

###### programmability

1、Redis provides a programming interface that lets you execute custom scripts on the server itself. 

2、Redis provides two means for running scripts.

【1】Firstly, and ever since Redis 2.6.0, the EVAL command enables running server-side scripts. 

【2】Secondly, added in v7.0, Redis Functions are essentially scripts that are first-class database elements. 

### 基本管理

######  Persistence

1、Persistence refers to the writing of data to durable storage, such as a solid-state disk (SSD).

2、Redis itself provides a range of persistence options

【1】RDB (Redis Database)

- 配置项：save

【2】AOF (Append Only File)

- 配置项：appendonly

- 配置项：appendfsync 

  always ： every time new commands are appended to the AOF.

  everysec ： fsync every second.

  no ：  just put your data in the hands of the Operating System. 

【3】No persistence

【4】RDB + AOF

###### Key eviction

1、policy

【1】noeviction ：New values aren’t saved when memory limit is reached. When a database uses replication, this applies to the primary database

【2】allkeys-random ： Randomly removes keys to make space for the new data added.

【3】allkeys-lru ： Keeps most recently used keys; removes least recently used (LRU) keys

【4】allkeys-lfu ： Keeps frequently used keys; removes least frequently used (LFU) keys

【5】volatile-random ： Randomly removes keys with expire field set to true.

【6】volatile-ttl ： Removes keys with expire field set to true and the shortest remaining time-to-live (TTL) value.

【7】volatile-lru ： Removes least recently used keys with the expire field set to true.

【8】volatile-lfu ： Removes least frequently used keys with the expire field set to true.

2、配置项

【1】maxmemory

【2】maxmemory-policy

###### security

1、ACL

2、TLS

### 基本命令

## 架构

### 主从复制

### 哨兵模式

### 集群模式

## 配置

## 工具

## 场景

## 其他



