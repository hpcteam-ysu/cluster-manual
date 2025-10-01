# Q&A
## 1. 为什么我之前能通过ssh连接到计算节点，现在不行了，提示：Access denied by pam_slurm_adopt: you have no active jobs on this node
这是因为集群更新后封掉了所有用户对于计算节点的ssh直连权限，若需要连接到计算节点调试程序，请先使用`salloc`申请一个计算节点，然后使用`srun`连接到该节点，详细方法请参考 [4.3 交互式任务提交](./slurm/#interactive) 或 [4.4 独占式任务提交](./slurm/#exclusive)。

## 2. 为什么我的脚本式任务提交成功了，但任务状态是PD，同时NODELIST(REASON)栏显示(QOSMaxWallDurationPerJobLimit)
这是因为任务时长超过了QOS的限制，具体可能是时间限制（任务最大运行时间不能超过6天0时0分0秒）或单用户最大任务限制（每个用户同时运行的任务数不能超过5个）。
