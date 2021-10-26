git 命令

cd 
cd ..：返回上一级
pwd

touch ：创建一个文件
rm：删除一个文件
mkdir：新建一个文件夹
rm -r “”:删除一个文件夹
mv ：移动文件

reset：重新初始化屏幕
clear
history

git配置：
git config -l 查看配置
git config --system -l  查看系统配置
git config --global --list 查看自己的配置

设置配置
git config --global user.name "" 
git config --global user.email  "" 

克隆
git  clone ""

git add . 提交到暂存区
git commin "备注" 提交本地仓库
git push 推送到远程

git pull 拉去代码 



# git

- git branch	查看本地分支
- git branch -r 查看远程分支
- git branch -a 查看所有分支
- git branch [brnachName] 创建分支
- git branch -d 删除分支
- git push origin :newbranch  删除远程分支
- git inti 初始本地仓库
- git  remote add origin git@github.com:youname/仓库名.git
- git add . 
- git commit -m "" 提交代码



删除已经提交的文件

**1、git rm -rf 已经提交的文件或文件夹**

**2、git commit  -a -m "删除不必要的文件"**



设置token提交代码

git remote set-url origin https://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@github.com/chengleigit/RoutineApi.git

 

合并分支

合并分支：git merge