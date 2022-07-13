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

###### Pub/sub

###### programmability

### 基本管理

######  Persistence

###### Key eviction

###### Pipelining

### 基本命令

## 架构

### 主从复制

### 哨兵模式

### 集群模式

## 配置

## 工具

## 场景

## 其他



