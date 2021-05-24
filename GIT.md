下载  https: //git-scm.com/downloads

安装  全部next 

配置信息
电脑空白处右键-->Git Bash Here 进入git终端-->输入命令
git config --global user.name "sxc"
git config --global user.email "www.1260010547@qq.com"

查看配置信息
1. 本地查看   C:\Users\sxc\'.gitconfig' 文件打开
2. 进入git终端-->输入命令 git config --list --global
进入git终端-->输入命令 git config user.name  查看用户名
进入git终端-->输入命令 git config user.email 查看用户邮箱

获取帮助信息
git help config  在本地上的git里面的文件查看
git config -h   在git终端里面查看

初始化仓库
在本地
项目文件的根目录  -->  git终端  -->  输入命令 git init  --> 会创建一个名为.git的隐藏目录，这个.git目录就是当前项目的Git仓库

查看状态报告
git status  -->  Untracked files(未跟踪管理的文件)  --> Git在之前的快照(提交)中没有这些文件
            -->  Changes to be committed(已跟踪管理的文件)  -->  已暂存状态
            -->  Changes not staged for commit(已修改，但还没放入暂存区中)   modified 文件名 绿字已修改已放入暂存区   红字已修改未放入暂存区
git status -s  --> 红??(未跟踪的文件)     -->  精简版的报告 同 git status 一样
               --> 绿A(已跟踪管理的文件)  -->  已暂存状态
               --> 红M(已修改，但还没放入暂存区中)
               --> 绿M(已修改，已放入暂存区中)

跟踪新文件  -->  git add index.html  -->  就可以跟踪index.html这个文件了   加入暂存区

对多个文件添加到暂存区  -->  git add .

清空  -->  clear 清空终端记录

提交  -->  git commit -m "添加此次提交的描述信息"  -->  加入到了git仓库里面了

提交  -->  git commit -a -m "添加此次提交的描述信息"  -->  跳过添加暂存区的步骤直接添加到了git仓库里面了

撤销对文件的修改  -->  git checkout -- index.html  -->  撤销对index.html文件的修改  本质 git仓库中所保存的文件来覆盖工作区的指定文件

移除暂存区里的文件  -->  git reset HEAD index1.html  -->  移除暂存区里面的index1.html

移除所有的暂存区里的文件  -->  git reset HEAD .

移除仓库里面的文件
从git仓库和工作区同时移除  -->  git rm index2.html

只从git仓库中移除  -->  git rm --cached index2.html

