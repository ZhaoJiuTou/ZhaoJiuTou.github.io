# ElasticStack

## 前述

###### ElasticStack官网：

[ ]()https://www.elastic.co/cn/

###### Elastic中文社区：

[ ]()https://elasticsearch.cn/

###### 本篇内容：

1、ElasticStack基本介绍

2、ElasticStack基本部署

3、ElasticStack基本使用



## 基本介绍

###### 什么是Elastic Stack？

Elastic Stack 由一系列产品组件构成，能够对数据进行采集、搜索、分析、可视化。

###### Elastic Stack与ElK Stack。

1、Elastic Stack 是 ELK Stack 的下一步演进。

2、ElK Stack 在2015年加入了一系列称之为beats的组件。 但是放弃了称之为BELK，而是称之为Elastic Stack。

3、The Elastic Stack is the ELK Stack, but with more flexibility to do great things.

<!--信息来源：https://www.elastic.co/what-is/elk-stack-->

###### Elastic Stack的基本组成与各自功能

1、Elasticsearch： Elasticsearch is a search and analytics engine.

2、Logstash：Logstash is a server‑side data processing pipeline.

3、Kibana：Kibana lets users visualize data with charts and graphs in Elasticsearch.

4、Beats：a family of lightweight, single-purpose data shippers.

【1】Filebeat : Log files and journals

【2】Auditbeat : Audit data

【3】Functionbeat : Cloud data 

【4】Heartbeat : Availability

【5】Metricbeat : Metrics

【6】Packetbeat : Network traffic

【7】Winlogbeat : Windows event logs



## 基本部署

###### 前述

1、Elastic Stack版本：8.2.2

2、部署环境 ：CentOS 7

3、

###### ElasticSeach
