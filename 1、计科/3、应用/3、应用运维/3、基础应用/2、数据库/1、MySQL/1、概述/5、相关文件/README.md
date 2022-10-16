# 相关文件



1、配置文件

2、日志文件

（1）错误日志

【1】概述：错误日志文件对MySQL的启动、运行、关闭过程进行记录。

【2】位置：show VARIABLES like 'log_error' \G

![](log_error.png)

（2）查询日志

【1】查询日志记录了所有对MySQl的请求信息，不论这些信息是否得到了正确的执行。

<1>日志名为：主机名.log

【2】相关查询与操作

<1>show variables like '%general_log%';

<2>set global general_log=ON;

![](查询日志1.png)

【3】将此日志记录存放到general_log表中

<1>show variables like '%log_output%';

<2>set global log_output='table';

![](查询日志2.png)

![](查询日志三.png)

（3）慢查询日志

（4）二进制日志

3、PID文件



4、套接字文件

5、表结构定义文件

6、存储引擎相关文件
