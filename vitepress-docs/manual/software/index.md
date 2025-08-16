# 集群软件综述

## 2.1 系统介绍

集群使用 SCOW 集群管理系统，系统基于 Debian12 发行版构建，调度系统采用 SLURM。集群使用过程中只可登入主节点和作业所在的计算节点进行操作，作业的配置等预处理操作应在主节点完成，后提交至调度系统进行调度。计算节点系统环境通过nfs网络启动，完全一致。

## 2.2 系统存储结构

集群使用管理节点搭载的磁盘构建集群的文件存储系统。

| 硬盘 | 配额 | 挂载点 | RAID类型 | 用途 |
|-----|-----|-----|-----|-----|
| 机械硬盘 | 无限制 | /archive | RAID0 | 用户作业数据，用户家目录 |
| 固态硬盘 | Soft27G，Hard30G | /home | RAID5 | 部分用户家目录 |

### 注意事项

1. 如果用户磁盘配额需要提升磁盘配额，可以按照要求填写《燕山大学计算机学科 GPU 集群磁盘配额申请表》，管理员会根据用户使用情况，为用户提升磁盘配额。

## 2.3 软件环境

集群预装了以下软件环境：

### 开发环境
- GCC编译器 版本：15.2 12.2 11.4 
- cuda 版本: 11.7 11.8 12.0 12.2
- clang 版本：18.1.8
- icc 版本：2025.2.1（通过source /opt/intel/setvars.sh加载）

注：上文提到的版本是可通过module加载的版本，其中cuda最高支持到12.9，用户可自行安装
### 作业调度系统
- SLURM作业调度器
- SCOW可视化管理系统

### module 常用命令

- 查看所有可用模块：`module avail`
- 加载模块：`module load <module_name>`
- 卸载模块：`module unload <module_name>`
- 显示已加载模块：`module list`
- 切换模块：`module swap <old_module_name> <module_name>`

## 2.4 软件安装指南

**以下教程仅做参考，同学们也可以询问AI来帮助自己安装软件，集群的CPU架构是x86_64（也称为amd64）**

### conda的安装
Conda 是一个跨平台的开源包和环境管理工具，可管理 Python等语言的软件包和独立运行环境。
推荐大家安装Miniconda，Miniconda 是一个轻量级的 Conda 发行版，只包含 Conda 和 Python，不包含其他软件包，占用空间较小。

#### Anaconda的安装
首先，通过wget命令下载Anaconda安装包：
```bash
wget https://repo.anaconda.com/archive/Anaconda3-2025.06-0-Linux-x86_64.sh
```
然后，通过bash命令运行安装脚本：
```bash
bash Anaconda3-2025.06-0-Linux-x86_64.sh
```
运行后，根据提示进行安装，第一步是按下ENTER查看协议，查看完成后输入yes并按下ENTER，第二步是选择安装路径，默认安装在用户家目录的anaconda3目录下，第三步是是否初始化conda，输入yes并按下ENTER。

#### Miniconda的安装
首先，通过wget命令下载Miniconda安装包：
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
剩下的所有步骤与Anaconda的安装步骤相同，只是安装路径不同，默认安装在用户家目录的miniconda3目录下。
### pip换源
pip是Python的包管理工具，默认源为国外源，为提升下载速度，可使用以下命令将源切换为国内源，命令以中科大源为例：
```bash
pip config set global.index-url https://pypi.mirrors.ustc.edu.cn/simple
```
其余常用国内源：
- 阿里云：https://mirrors.aliyun.com/pypi/simple/
- 腾讯云：https://mirrors.cloud.tencent.com/pypi/simple/

### pip安装和conda安装的区别
pip只管理Python的软件包，较为轻量，而conda支持多语言管理，其依赖管理和环境隔离功能更加强大，但体积较大。
如需安装其他软件，请联系管理员或使用用户空间安装方式。
