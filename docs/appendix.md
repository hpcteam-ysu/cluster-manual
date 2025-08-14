---
layout: default
title: 附录
nav_order: 7
---

# 附录


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## A 上网认证

集群默认不连接外网，如果需要联网下载请参考如下说明，使用校园网账号进行认证：

### 登录

```
netlogin <上网id> <密码> [运营商：校园网(def)|中国移动(1)|中国联通(2)|中国电信(3)] 
```

### 登出

```
 netlogin logout 
```

注意：集群所有用户共用一个校园网账号，为了避免流量被他人使用，请使用完后及时下线账号。

### 查看用户信息

在认证成功情况下，运行：（该命令暂时下线）

```
netlogin info
```

PS:该命令目前尚存BUG，第一次运行会出现错误，如确认已经认证成功结果显示“出现错误”，请再次运行。

### 确认是否联网

```
curl baidu.com 
```

## B 相关资源

SLURM官网：[**https://slurm.schedmd.com/**](https://slurm.schedmd.com/)

BrightComputing用户手册：[**https://support.brightcomputing.com/manuals/9.1/user-manual.pdf**](https://support.brightcomputing.com/manuals/9.1/user-manual.pdf/)

modules wiki:：**https://modules.readthedocs.io/en/stable/index.html**

## C 更新说明

### V4.3

1.  集群磁盘配置更新
2.  QA更新

Contributor:msprcli

### V4.2

1.  集群磁盘配置更新
2.  集群预装软件更新

Contributor:BeingGod

### V4.1

1.  集群IP地址更新
2.  集群磁盘配置更新

Contributor:BeingGod

### V4.0

1.  移除无法使用的MPI库
2.  补充MPI相关内容
3.  修补充了若干细节

Contributor:BeingGod

### v3.3

1.  移除部分深度学习包，推荐用户统一使用conda
2.  增加salloc独占式作业提交
3.  修正了若干细节错误

Contributor:BeingGod

### v3.2

1.  修正了若干细节错误

Contributor:BeingGod

### v3.1

1.  修改QOS服务部分错误
2.  修正了若干细节错误

Contributor: BeingGod

### v3.0

1.  重新组织手册结构
2.  更新集群硬件信息描述
3.  更新集群软件信息描述

Contributor: BeingGod

### v2.1

1.  补充使用堡垒机在外网访问GPU集群的内容；
2.  补充MPI任务提交的内容；
3.  补充查看当前认证用户信息的内容；
4.  补充并修正集群软件环境；
5.  修正sbatch脚本式任务提交选项；
6.  修正若干细节错误。

Contributor: BeingGod

### V2.0

Contributor: opluss