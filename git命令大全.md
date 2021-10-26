





## 一、新建代码库

> 1.  
>
>     
>
> 2.  
>
>    \# 在当前目录新建一个Git代码库
>
> 3.  
>
>    $ git init
>
> 4.  
>
>     
>
> 5.  
>
>    \# 新建一个目录，将其初始化为Git代码库
>
> 6.  
>
>    $ git init [project-name]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 下载一个项目和它的整个代码历史
>
> 9.  
>
>    $ git clone [url]

## 二、配置

 

Git的设置文件为`.gitconfig`，它可以在用户主目录下（全局配置），也可以在项目目录下（项目配置）。

> 1.  
>
>     
>
> 2.  
>
>    \# 显示当前的Git配置
>
> 3.  
>
>    $ git config --list
>
> 4.  
>
>     
>
> 5.  
>
>    \# 编辑Git配置文件
>
> 6.  
>
>    $ git config -e [--global]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 设置提交代码时的用户信息
>
> 9.  
>
>    $ git config [--global] user.name "[name]"
>
> 10.  
>
>     $ git config [--global] user.email "[email address]"

## 三、增加/删除文件

> 1.  
>
>     
>
> 2.  
>
>    \# 添加指定文件到暂存区
>
> 3.  
>
>    $ git add [file1] [file2] ...
>
> 4.  
>
>     
>
> 5.  
>
>    \# 添加指定目录到暂存区，包括子目录
>
> 6.  
>
>    $ git add [dir]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 添加当前目录的所有文件到暂存区
>
> 9.  
>
>    $ git add .
>
> 10.  
>
>      
>
> 11.  
>
>     \# 添加每个变化前，都会要求确认
>
> 12.  
>
>     \# 对于同一个文件的多处变化，可以实现分次提交
>
> 13.  
>
>     $ git add -p
>
> 14.  
>
>      
>
> 15.  
>
>     \# 删除工作区文件，并且将这次删除放入暂存区
>
> 16.  
>
>     $ git rm [file1] [file2] ...
>
> 17.  
>
>      
>
> 18.  
>
>     \# 停止追踪指定文件，但该文件会保留在工作区
>
> 19.  
>
>     $ git rm --cached [file]
>
> 20.  
>
>      
>
> 21.  
>
>     \# 改名文件，并且将这个改名放入暂存区
>
> 22.  
>
>     $ git mv [file-original] [file-renamed]

## 四、代码提交

> 1.  
>
>     
>
> 2.  
>
>    \# 提交暂存区到仓库区
>
> 3.  
>
>    $ git commit -m [message]
>
> 4.  
>
>     
>
> 5.  
>
>    \# 提交暂存区的指定文件到仓库区
>
> 6.  
>
>    $ git commit [file1] [file2] ... -m [message]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 提交工作区自上次commit之后的变化，直接到仓库区
>
> 9.  
>
>    $ git commit -a
>
> 10.  
>
>      
>
> 11.  
>
>     \# 提交时显示所有diff信息
>
> 12.  
>
>     $ git commit -v
>
> 13.  
>
>      
>
> 14.  
>
>     \# 使用一次新的commit，替代上一次提交
>
> 15.  
>
>     \# 如果代码没有任何新变化，则用来改写上一次commit的提交信息
>
> 16.  
>
>     $ git commit --amend -m [message]
>
> 17.  
>
>      
>
> 18.  
>
>     \# 重做上一次commit，并包括指定文件的新变化
>
> 19.  
>
>     $ git commit --amend [file1] [file2] ...

## 五、分支

> 1.  
>
>     
>
> 2.  
>
>    \# 列出所有本地分支
>
> 3.  
>
>    $ git branch
>
> 4.  
>
>     
>
> 5.  
>
>    \# 列出所有远程分支
>
> 6.  
>
>    $ git branch -r
>
> 7.  
>
>     
>
> 8.  
>
>    \# 列出所有本地分支和远程分支
>
> 9.  
>
>    $ git branch -a
>
> 10.  
>
>      
>
> 11.  
>
>     \# 新建一个分支，但依然停留在当前分支
>
> 12.  
>
>     $ git branch [branch-name]
>
> 13.  
>
>      
>
> 14.  
>
>     \# 新建一个分支，并切换到该分支
>
> 15.  
>
>     $ git checkout -b [branch]
>
> 16.  
>
>      
>
> 17.  
>
>     \# 新建一个分支，指向指定commit
>
> 18.  
>
>     $ git branch [branch] [commit]
>
> 19.  
>
>      
>
> 20.  
>
>     \# 新建一个分支，与指定的远程分支建立追踪关系
>
> 21.  
>
>     $ git branch --track [branch] [remote-branch]
>
> 22.  
>
>      
>
> 23.  
>
>     \# 切换到指定分支，并更新工作区
>
> 24.  
>
>     $ git checkout [branch-name]
>
> 25.  
>
>      
>
> 26.  
>
>     \# 切换到上一个分支
>
> 27.  
>
>     $ git checkout -
>
> 28.  
>
>      
>
> 29.  
>
>     \# 建立追踪关系，在现有分支与指定的远程分支之间
>
> 30.  
>
>     $ git branch --set-upstream [branch] [remote-branch]
>
> 31.  
>
>      
>
> 32.  
>
>     \# 合并指定分支到当前分支
>
> 33.  
>
>     $ git merge [branch]
>
> 34.  
>
>      
>
> 35.  
>
>     \# 选择一个commit，合并进当前分支
>
> 36.  
>
>     $ git cherry-pick [commit]
>
> 37.  
>
>      
>
> 38.  
>
>     \# 删除分支
>
> 39.  
>
>     $ git branch -d [branch-name]
>
> 40.  
>
>      
>
> 41.  
>
>     \# 删除远程分支
>
> 42.  
>
>     $ git push origin --delete [branch-name]
>
> 43.  
>
>     $ git branch -dr [remote/branch]

## 六、标签

> 1.  
>
>     
>
> 2.  
>
>    \# 列出所有tag
>
> 3.  
>
>    $ git tag
>
> 4.  
>
>     
>
> 5.  
>
>    \# 新建一个tag在当前commit
>
> 6.  
>
>    $ git tag [tag]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 新建一个tag在指定commit
>
> 9.  
>
>    $ git tag [tag] [commit]
>
> 10.  
>
>      
>
> 11.  
>
>     \# 删除本地tag
>
> 12.  
>
>     $ git tag -d [tag]
>
> 13.  
>
>      
>
> 14.  
>
>     \# 删除远程tag
>
> 15.  
>
>     $ git push origin :refs/tags/[tagName]
>
> 16.  
>
>      
>
> 17.  
>
>     \# 查看tag信息
>
> 18.  
>
>     $ git show [tag]
>
> 19.  
>
>      
>
> 20.  
>
>     \# 提交指定tag
>
> 21.  
>
>     $ git push [remote] [tag]
>
> 22.  
>
>      
>
> 23.  
>
>     \# 提交所有tag
>
> 24.  
>
>     $ git push [remote] --tags
>
> 25.  
>
>      
>
> 26.  
>
>     \# 新建一个分支，指向某个tag
>
> 27.  
>
>     $ git checkout -b [branch] [tag]

## 七、查看信息

> 1.  
>
>     
>
> 2.  
>
>    \# 显示有变更的文件
>
> 3.  
>
>    $ git status
>
> 4.  
>
>     
>
> 5.  
>
>    \# 显示当前分支的版本历史
>
> 6.  
>
>    $ git log
>
> 7.  
>
>     
>
> 8.  
>
>    \# 显示commit历史，以及每次commit发生变更的文件
>
> 9.  
>
>    $ git log --stat
>
> 10.  
>
>      
>
> 11.  
>
>     \# 搜索提交历史，根据关键词
>
> 12.  
>
>     $ git log -S [keyword]
>
> 13.  
>
>      
>
> 14.  
>
>     \# 显示某个commit之后的所有变动，每个commit占据一行
>
> 15.  
>
>     $ git log [tag] HEAD --pretty=format:%s
>
> 16.  
>
>      
>
> 17.  
>
>     \# 显示某个commit之后的所有变动，其"提交说明"必须符合搜索条件
>
> 18.  
>
>     $ git log [tag] HEAD --grep feature
>
> 19.  
>
>      
>
> 20.  
>
>     \# 显示某个文件的版本历史，包括文件改名
>
> 21.  
>
>     $ git log --follow [file]
>
> 22.  
>
>     $ git whatchanged [file]
>
> 23.  
>
>      
>
> 24.  
>
>     \# 显示指定文件相关的每一次diff
>
> 25.  
>
>     $ git log -p [file]
>
> 26.  
>
>      
>
> 27.  
>
>     \# 显示过去5次提交
>
> 28.  
>
>     $ git log -5 --pretty --oneline
>
> 29.  
>
>      
>
> 30.  
>
>     \# 显示所有提交过的用户，按提交次数排序
>
> 31.  
>
>     $ git shortlog -sn
>
> 32.  
>
>      
>
> 33.  
>
>     \# 显示指定文件是什么人在什么时间修改过
>
> 34.  
>
>     $ git blame [file]
>
> 35.  
>
>      
>
> 36.  
>
>     \# 显示暂存区和工作区的差异
>
> 37.  
>
>     $ git diff
>
> 38.  
>
>      
>
> 39.  
>
>     \# 显示暂存区和上一个commit的差异
>
> 40.  
>
>     $ git diff --cached [file]
>
> 41.  
>
>      
>
> 42.  
>
>     \# 显示工作区与当前分支最新commit之间的差异
>
> 43.  
>
>     $ git diff HEAD
>
> 44.  
>
>      
>
> 45.  
>
>     \# 显示两次提交之间的差异
>
> 46.  
>
>     $ git diff [first-branch]...[second-branch]
>
> 47.  
>
>      
>
> 48.  
>
>     \# 显示今天你写了多少行代码
>
> 49.  
>
>     $ git diff --shortstat "@{0 day ago}"
>
> 50.  
>
>      
>
> 51.  
>
>     \# 显示某次提交的元数据和内容变化
>
> 52.  
>
>     $ git show [commit]
>
> 53.  
>
>      
>
> 54.  
>
>     \# 显示某次提交发生变化的文件
>
> 55.  
>
>     $ git show --name-only [commit]
>
> 56.  
>
>      
>
> 57.  
>
>     \# 显示某次提交时，某个文件的内容
>
> 58.  
>
>     $ git show [commit]:[filename]
>
> 59.  
>
>      
>
> 60.  
>
>     \# 显示当前分支的最近几次提交
>
> 61.  
>
>     $ git reflog

## 八、远程同步

> 1.  
>
>     
>
> 2.  
>
>    \# 下载远程仓库的所有变动
>
> 3.  
>
>    $ git fetch [remote]
>
> 4.  
>
>     
>
> 5.  
>
>    \# 显示所有远程仓库
>
> 6.  
>
>    $ git remote -v
>
> 7.  
>
>     
>
> 8.  
>
>    \# 显示某个远程仓库的信息
>
> 9.  
>
>    $ git remote show [remote]
>
> 10.  
>
>      
>
> 11.  
>
>     \# 增加一个新的远程仓库，并命名
>
> 12.  
>
>     $ git remote add [shortname] [url]
>
> 13.  
>
>      
>
> 14.  
>
>     \# 取回远程仓库的变化，并与本地分支合并
>
> 15.  
>
>     $ git pull [remote] [branch]
>
> 16.  
>
>      
>
> 17.  
>
>     \# 上传本地指定分支到远程仓库
>
> 18.  
>
>     $ git push [remote] [branch]
>
> 19.  
>
>      
>
> 20.  
>
>     \# 强行推送当前分支到远程仓库，即使有冲突
>
> 21.  
>
>     $ git push [remote] --force
>
> 22.  
>
>      
>
> 23.  
>
>     \# 推送所有分支到远程仓库
>
> 24.  
>
>     $ git push [remote] --all

## 九、撤销

> 1.  
>
>     
>
> 2.  
>
>    \# 恢复暂存区的指定文件到工作区
>
> 3.  
>
>    $ git checkout [file]
>
> 4.  
>
>     
>
> 5.  
>
>    \# 恢复某个commit的指定文件到暂存区和工作区
>
> 6.  
>
>    $ git checkout [commit] [file]
>
> 7.  
>
>     
>
> 8.  
>
>    \# 恢复暂存区的所有文件到工作区
>
> 9.  
>
>    $ git checkout .
>
> 10.  
>
>      
>
> 11.  
>
>     \# 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
>
> 12.  
>
>     $ git reset [file]
>
> 13.  
>
>      
>
> 14.  
>
>     \# 重置暂存区与工作区，与上一次commit保持一致
>
> 15.  
>
>     $ git reset --hard
>
> 16.  
>
>      
>
> 17.  
>
>     \# 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
>
> 18.  
>
>     $ git reset [commit]
>
> 19.  
>
>      
>
> 20.  
>
>     \# 重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
>
> 21.  
>
>     $ git reset --hard [commit]
>
> 22.  
>
>      
>
> 23.  
>
>     \# 重置当前HEAD为指定commit，但保持暂存区和工作区不变
>
> 24.  
>
>     $ git reset --keep [commit]
>
> 25.  
>
>      
>
> 26.  
>
>     \# 新建一个commit，用来撤销指定commit
>
> 27.  
>
>     \# 后者的所有变化都将被前者抵消，并且应用到当前分支
>
> 28.  
>
>     $ git revert [commit]
>
> 29.  
>
>      
>
> 30.  
>
>     \# 暂时将未提交的变化移除，稍后再移入
>
> 31.  
>
>     $ git stash
>
> 32.  
>
>     $ git stash pop



