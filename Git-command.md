> @Author: xiaxs(xxs19910202@vip.qq.com)<br>
> @[markdown-兔清风的博客](http://blog.leanote.com/post/freewalk/Markdown-%E8%AF%AD%E6%B3%95%E6%89%8B%E5%86%8C#index)

##### GitHub注册信息:
    用户名: xiaxs
    邮 箱:  xxs19910202@vip.qq.com

##### MAC - 命令行方式:
###### 进入文件夹
    方式一
    cd /users/zsh/GitHub

    方式二:
    cd ~
    cd GitHub/xiaxs-study

##### 克隆GitHub远程仓库: git clone [url]
    HTTPS: git clone https://github.com/xiaxs/xiaxs-study.git
    SSH(需要配置SSH KEY): git clone git@github.com:xiaxs/xiaxs-study.git

##### 设置/切换作者信息: name email
    name:  git config --global user.name "xiaxs"
    email: git config --global user.email "xxs19910202@vip.qq.com"
> 没有提示即为设置成功

##### 同一台电脑切换不同的GitHub账户
    git config --global user.name "xxs19910202"
    git config --global user.email "xiaxiansheng@adinnet.cn"
>切换后需要登录GitHub账户,才能执行git相关操作

##### 查看当前设置的作者信息:
    name:  git config --global user.name
    email: git config --global user.email
>不填写用户名或者邮箱即可
>
##### 查看git下所有的文件
    git config --list

##### 查看工作区和缓存区状态:
    git status

##### 添加单个文件到git缓存区
    git add git.txt
    git add demo.html

##### 提交整个文件夹里的所有文件
    git add .

##### git提交
    git commit -m "注释内容"
    git commit -a -m "注释内容" --> 合并 git add . 和 git commit -m ""

##### 查看git操作文件记录
    git log: 查看git操作文件记录
    按下 Enter 键查看更多记录,按下 Q键 退出当前记录

##### git 对比:
    git diff: 工作区与缓存区之间的差异对比
    git diff --cached: 缓存区与版本库之间的差异对比
    git diff --staged: 缓存区与版本库之间的差异对比
    git diff 分支(git diff master): 工作区与版本库之间的差异对比

##### git 撤销:
    git reset HEAD <file name>: 从暂存区撤销回工作区
    git checkout -- <file name>: 工作区撤销返回到版本库的状态
    git commit --amend: 误提交后返回重新提交,比如需要提交a,b两个文件,但是只提交了一个,则把未提交的文件添加进缓存区,然后再一起提交
    example: 只提交了a.js -> git commit -m "modified a.js"
             添加另外一个a.js -> git add b.js
             撤销上次提交再一起提交: git commit "changes to commit a.js b.js" --amend

##### git 删除
    git rm <filename>: 将从工作区直接删除(如右键-删除)的文件同步到缓存区
    git rm -f <filename>: 从缓存区和工作区中直接强制删除对应的文件
    git rm --cached <filename>: 从缓存区中删除,并会保留工作区的文件

##### git 恢复(还原过去或未来版本的文件)
    git checkout id <filename> -- 还原指定文件 - id获取: git log --> 选取每条记录(commit) 后的字符串的一部分即可
    git reset --hard id --> 还原版本
    git reset --hard HEAD^ --> 逐步还原之前的版本
    git reset --hard HEAD~3 --> 还原之前的第三个版本
    git reflog --> 查看之前每次操作记录(获取每条记录开始的字符串) --> git reset --hard hjhgleg

##### git 同步到远程仓库
    git remote --> 查看远程仓库的名字(origin)
    git remote -v --> 查看远程仓库的地址
    git push origin master --> push到远程仓库

##### git 添加协作人员: 必须是已经注册的GitHub账号
    https://github.com/xiaxs/xiaxs-study -> Settings -> Collaborators -> 输入后 -> Add collaborators
    -> 被添加的人同意即可

##### git多人协作解决冲突
    在开发之前先拉取远程仓库的地址 git pull / git fetch, 开完之后及时进行提交
    git fetch --> 不会进行代码的merge操作,需要手动merge
        git fetch -> git diff master origin/master -> git merge origin/master -> 出现冲突 -> 在冲突文件中比对后删除冲突位置的代码 -> git commit -a -m "resolve conflict" -> git push origin master

    git pull --> 自动进行代码的合并操作
        git pull -> 在冲突文件中比对后删除冲突位置的代码 -> git commit -a -m "resolve conflict" -> git push origin master

##### git 分支
    git branch --> 查看分支, 带星号(*)的为当前分支
    git branch <branch name> --> 创建分支
    git checkout <branch name> --> 切换当前分支
    git checkout -b <branch name> --> 快速创建并切换到新分支
    git merge testBranch --> 合并分支,必须切换到需要做分支操作的那条主分支
        exmple: master分支合并testBranch分支,首先需要切换到master分支,然后再执行 git merge newBranch
    git branch --merged --> 查看当前分支所合并的分支
    git branch --no-merged --> 查看当前分支没有合并的分支
    git branch -d <branch name> --> 删除分支,没有合并的分支默认不删除
    git branch -D <branch name> --> 强制删除未合并的分支
    git branch -m <old_name> <new_name> --> 修改分支名称

    Git分支冲突的处理: 当合并多个分支时,每次合并一个分支(git merge newBranch),如果有冲突,手动处理冲突后,提交代码 git commit -a -m "resolve conflict"

##### GitHub上的分支
    git push origin newBranch --> 同步新分支到GitHub
    git push origin :<branch_name> --> 删除GitHub远程分支
    git push origin --delete <branch_name> --> 删除GitHub远程分支

    GitHub直接创建

##### GitHub上的标签(GitHub上的 release-版本信息)
    git tag --> 查看标签(release)
    git tag v1.0 --> 设置标签(release)
    git push origin v1.0 --> 将版本信息同步到远程GitHub

##### GitHub创建组织
    GitHub -> New orgination -> Adinnet

##### GitHub创建博客
    GitHub创建: https://pages.github.com
* [创建博客](https://pages.github.com)

##### Git资源
    http://git.oschina.net/progit/
    http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
* [proGit](http://git.oschina.net/progit/)
* [廖雪峰](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)



##### 开源项目的协作:

    fork: 将开源项目镜像到自己的GitHub,修改后按照正常方式提交提交推送 -> pull request -> New pull request -> Create pull request, 有权限的开发者收到请求后,确认无误后合并请求,(主开发回复贡献者: 复制comment后按下R同步注释)
