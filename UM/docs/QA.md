---
layout: default
title: Q&A
nav_order: 6
---

# Q&A



---

1. 如何查看当前磁盘剩余空间？

   答：使用quota命令，block即为已使用空间。

2. 模型训练过程中出现[Cuda runtime error (48) : no kernel image is available for execution的问题？](https://www.cnblogs.com/liuke-note/p/10149530.html)

   答：该问题是由于3090的GPU不支持cuda11.0之前的cuda，换用更高版本的cuda即可。

3. 没有存放大文件，但是home目录下磁盘空间占用量变大？

   答：使用pip安装python库会默认安装到home目录的.local隐藏目录下，建议使用conda进行安装，或者手动指定安装路径。如有需求可以申请提升磁盘配额。

4. 提交了作业显示了任务号但是没有输出，squeue也没有显示？

   答：sbatch提交脚本有误，请按照群中的标准提交脚本修改，注意使用python3，行尾的注释\#号前要有空格。

