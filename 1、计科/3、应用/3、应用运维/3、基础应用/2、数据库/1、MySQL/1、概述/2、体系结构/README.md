# 体系结构

一、MySQL的体系结构（如图，图版本为5.5）

![](MySQl Architecture（版本5.5）.png)

二、MySQL体系结构的分层解析

1、连接层：Connection Pool

2、SQL层：

（1）SQL Interface： SQL接口

（2）Caches&Buffers：缓存

（3）Parser：解析器

（4）Optimizer：优化器

（5）actuator ：执行器

3、存储引擎层：可插拔式的存储引擎

（1）InnoDB：

（2）MyISAM：

（3）NBD：

4、物理文件层：

（1）支持的文件系统

（2）存储的物理文件

【1】数据文件

【2】日志文件

三、MySQL体系结构语句流程分析

1、流程图示例1：

![image-20221015171206738](流程图1.png)

2、流程图示例2（分层建议按上述文字描述）：

![](MySQL流程图2.jpg)

四：MySQL体系结构语句流程动态演示（存储引擎部分后续讲解）：

![](MySQL流程图.gif)
