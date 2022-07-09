# 网络服务

## 前述

### 本篇内容

本人暂时将网络服务分类网络支撑服务、网络系统服务、网络应用服务。

不一定绝对准确，只是对常用的网络服务进行某种程度某种类型的归类。

现在只是对掌握的和掌握到一定程度的服务简单整理，后续会不断补充。

## 正篇

### 网络支撑服务

#### DNS

#### DHCP

### 网络系统服务

#### 时间同步

#### 网络监控

### 网络应用服务

#### 远程会话

##### SSH---OpenSSH

###### 介绍

###### 包名

1、openssh-server

2、openssh

3、openssh-clients

###### 文件

###### 服务

###### 配置

###### 工具

1、ssh

【1】介绍：

简述：OpenSSH SSH client (remote login program)

来源：软件包openssh-clients

【2】格式：

ssh [......] [user@]hostname [command]

【3】选项：

- -p port：Port to connect to on the remote host.

​    `ssh -p 22 root@192.168.1.137`

- -v：Verbose mode.

​    ` ssh -v -p 22 root@192.168.1.137 `

- -o option：Can be used to give options in the format used in the configuration file.

​    `ssh -o ConnectTimeout 10 root@192.168.1.137`

2、scp

【1】介绍：

简述： secure copy (remote file copy program)

来源： 软件包openssh-clients

【2】格式：

scp [......] [[user@]host1:]file1 ...  [[user@]host2:]file2

【3】选项：

- -o ssh_option
- -P port

3、pssh

【1】介绍：

简述：Parallel SSH tools

来源：pssh软件包

【2】格式：

pssh   [......]    command ...

【3】选项

- -h   host_file：Read  hosts  from  the given host_file.

- -H  [user@]host[:port]： Add the given host strings to the list of hosts.

  -H  "[user@]host[:port] [ [user@]host[:port ] ... ]"

- -i：Display standard output and standard error as each host completes.

  `pssh -iH 192.168.1.137 'cat /etc/passed' `

#### 网络存储

##### NFS

##### Samba

#### 文件传输

##### FTP













