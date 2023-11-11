# GitHub入门学习笔记

注册登录什么的就没必要说了，我一学计算机的连这都不会那真没必要学了

~~毕竟这GitHub又不像OpenAI那样非得国外手机号才能注册~~



**Repository**，仓库，在这里可以存放代码文件和学习文档

**Profile**，个人档案，点个人头像再点`Your profile`进入

> 个人主页内容很多，主要为以下几个：
>
> 1. **Edit profile**，修改个人资料
> 2. **Star**，类似“赞”，“like”，“红心”，表示认可，同时也是收藏，可以在自己主页的星星图标处查看
> 3. **Pinned**，个人展示区，可以展示自己的作品
> 4. **活跃度表格**，展示用户的活跃程度，绿格子的数量和颜色代表了活跃度

**Fork**，意为“叉子”，这里指的是把别人的仓库复制到自己这来（相当于创建一个自己的分支，不会影响到原仓库，除非别人接受了你的***Pull request***）

> Fork来的仓库会备注“Forked from xxx”标明来源
>
> 原主同意了pull request后，做的修改就会反映到原仓库上，修改者也成了仓库贡献者（Contributors）

## GitHub 是 Git 软件用户的项目管理中心

Git是一款**分布式版本控制软件**，它记录了每次修改时的文件状态，也就是**时刻备份**

~~跟游戏里不断save/load好像~~

而Github，就是用于**托管文件和修改等信息**，方便Git的使用

右键文件夹，选择`Git Bash Here`就可以在这个文件夹中运行Git命令

> Git的常用命令：
>
> * `git add`和`git commit`
>
>   add提交了修改，但是是放在staging area，即暂存区中，commit是最终提交
>
>   类似电脑删除文件移动到回收站（add），只要不清空回收站（commit），文件就随时可以还原。
>
> * `git pull`和`git push`
>
>   pull是“**拉取**”，从远程仓库获取更新；push是“**推送**”，把本地文件推送到仓库中。
>
>   协作完成项目时，每天开始工作时先pull，跟上进度；结束工作时，先pull再push
>
> * `git clone`
>
>   下载仓库到本地。
>
>   先要复制仓库的ssh地址，在Git Bash窗口输入`git clone 复制的ssh地址`来下载仓库
>
>   当然也可以用HTTPS地址。

## 配置SSH Key

按照[GitHub入门指南 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/337959303)一下就配置好了，还挺简单的

试用了下clone与push，很方便

































