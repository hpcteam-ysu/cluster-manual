# SCOW系统使用

## 5.1 连接方式
保持自己处于校园网环境下，使用浏览器访问SCOW控制台。   
SCOW控制台：http://10.21.22.100/portal/
使用超算账号登录即可
![登录页面](/images/login.avif)

## 5.2 系统介绍
SCOW是由北京大学研发的可视化集群管理系统，在使用算力资源的时候，用户只需要一个浏览器即可管理集群上的文件、访问终端及桌面、提交和管理作业，以及执行带 GUI 的交互式任务。

## 5.3 目前支持功能
1. [仪表盘](#dashboard)
2. [文件操作](#file)
3. [任务管理](#job)
4. [SHELL连接](#shell)
5. [交互式任务-VSCode](#vscode)
6. [交互式任务-桌面](#desktop)

## 5.4 功能介绍及使用方法
### 5.4.1 仪表盘 {#dashboard}
在SCOW控制台内，点击"仪表盘"选项卡，即可查看集群的空闲情况，剩余CPU、GPU数量等信息。
![仪表盘](/images/dashboard.avif)

### 5.4.2 文件操作 {#file}
在SCOW控制台内，点击"文件管理"选项卡，即可查看当前用户的文件目录。
![文件管理](/images/file.avif)
在这里可以进行文件夹、文件的创建、下载、重命名、复制、移动、删除等操作，并可提交slurm脚本至任务队列。

### 5.4.3 任务管理 {#job}
在SCOW控制台内，点击"作业"选项卡，即可进入任务管理页，在这里可以查看当前登录用户的正在运行的和历史任务列表，并可进入任务对应的文件夹内，对于正在运行的任务，可取消任务、查看任务详情。
![正在运行的任务](/images/running_job.avif)
![所有任务](/images/all_job.avif)
![任务详情](/images/job_detail.avif)
同时，还可在任务管理页进行作业的提交和保存的模版的查看和使用。
![提交作业1](/images/submit1.avif)
![提交作业2](/images/submit2.avif)
![作业模板](/images/template.avif)

### 5.4.4 Shell连接 {#shell}
在SCOW控制台内，点击"Shell"选项卡，即可连接到集群的login节点，可直接输入命令进行操作。
![Shell](/images/shell.avif)

### 5.4.5 交互式任务-VSCode {#vscode}
在SCOW控制台内，点击"交互式任务"选项卡，即可进入交互式任务页，在这里可以查看创建过的交互式任务，也可创建新的交互式任务。
![VSCode1](/images/VSCode_1.avif)
![VSCode2](/images/VSCode_2.avif)
点击VSCode选项，即可跳转至任务创建页面，在这里可以设置任务的名称，分区，节点数（推荐设置为1），每个节点所用GPU数，最长运行时间，以及其他的参数，如内存等。
![VSCode3](/images/VSCode_3.avif)
点击提交后，页面自动跳转回"已创建应用"页，该页面可以查看任务的运行状态（排队中，运行中），当任务处于运行中状态时，可选择连接VSCode页面，结束任务和进入任务对应目录。
![VSCode4](/images/VSCode_4.avif)
点击连接后，即可进入web端的VSCode页面。
![VSCode5](/images/VSCode_5.avif)
**在使用web端的VSCode时，请严格注意任务运行剩余时间，避免任务结束造成的数据丢失**  
**目前的VSCode暂时不支持插件的安装，运维团队将尽快完善**
### 5.4.6 交互式任务-桌面 {#desktop}
在SCOW控制台内，点击"桌面"选项卡，即可进入创建桌面页，在这里可以设置桌面的名称。
![桌面1](/images/desktop_1.avif)
![桌面2](/images/desktop_2.avif)
确定创建后，会自动跳转至桌面页面，同时，先前的桌面页面也会刷新，显示新创建的桌面。
![桌面3](/images/desktop_3.avif)
![桌面4](/images/desktop_4.avif)
**请注意，桌面不会随页面关闭而关闭，请在使用完成后及时关闭，避免影响他人使用**  
**当前桌面创建数量上限为10个，且只能连接login节点的桌面**
