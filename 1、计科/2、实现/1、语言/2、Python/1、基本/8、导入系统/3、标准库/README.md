# 标准库



## 前述

1、参考来源：《Python语言参考手册》Python标准库

2、Python版本：3.10.5

3、Python手册版本：3.10.5

4、Python手册参考地址：

[ ]()https://docs.python.org/zh-cn/3.10/library/

5、本篇内容只解析Linux下适用的函数。

6、本篇内容主要解析并演示本人认为重要性偏高及使用率较高的。



## 标准库



## 通用操作系统服务

#### os

##### 进程参数

1、进程及进程间关系

【1】os.getpid() ： Return the current process id.

【2】os.getppid() ： Return the parent’s process id. 

【3】os.getpgrp() ： Return the id of the current process group.

【4】os.getpgid(pid) ： Return the process group id of the process with process id pid. 

![进程与进程间关系](进程与进程间关系.png)

2、进程属主属组

【1】os.getlogin() ： Return the name of the user logged in on the controlling terminal of the process.

【2】os.getuid() ： Return the current process’s real user id.

【3】os.getgid() ：Return the real group id of the current process.

【4】os.geteuid() ： Return the current process’s effective user id.

【5】os.getegid() ： Return the effective group id of the current process. 

【6】os.getgroups() ： Return list of supplemental group ids associated with the current process.

![进程属主属组](进程属主属组.png)

3、进程环境信息

【1】os.environ ：A mapping object where keys and values are strings that represent the process environment.

【2】os.uname() ： Returns information identifying the current operating system. 

【3】os.ctermid() ： Return the filename corresponding to the controlling terminal of the process.

【4】os.getenv(key, default=None) ： Return the value of the environment variable key if it exists, or default if it doesn’t.  

​                                                                    key, default and the result are str. 

![进程环境信息png](进程环境信息png.png)

##### 进程管理

##### 调度器接口

##### 文件名，命令行参数，以及环境变量

##### 文件和目录

#####  文件描述符操作

##### 其他系统信息

#### io

#### time

#### platform

#### argparse

#### loging



