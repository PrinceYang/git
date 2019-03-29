# 一、git

## 1. 安装和配置
### 1.安装 
###   a. 根据自身OS从[官网](https://git-scm.com)下载git。
      b. Windows：运行安装程序后配置环境变量，将安装git的目录定位到bin文件夹以后，复制bin的路径，将此路径添加到环境变量中，重启cmd即可运行git命令
      c. MacOS：git version 查看git版本，如果报错请自行下载
### 1.配置 
##### 1. 
       使用命令 "git config --global user.name "Your Name" " 配置用户名
       使用命令 "git config --global user.email "Your Email" " 配置邮箱
       使用命令 "git config user.name" or "git config user.email" 查看当前用户名或邮箱
##### 2. git version 查看git版本
##### 3. git config --list 查看配置文件
##### 4. vi .gitconfig 查看并编写git config文件

## 2. 常用命令
    1. 常用命令，包括分支、提交、等
      open . 打开命令行当前路径文件夹
      a. git clone yourProjectUrl  拉取远端仓库
      b. git branch 查看分支
        -a 查看所有分支包括远端(需要在本地项目跟目录运行此命令)
        -v 查看所有分支的最后一次提交
      c. git status 查看本地仓库状态
      d. git add . 添加修改后的文件
      e. git commit 提交代码到本地缓存区，命令执行后需要填写提交信息。尽量多次提交
      f. git stash 将会把当前目录和index中的所有改动(但不包括未track的文件)压入一个栈,然后留给你一个clean的工作状态,即处于上一次最新提交处。
      g. git checkout branchname 切换分支 当改动未提交时不允许切换，可以先commit再切换，或者stash后再切
    2. git commit message的格式，检查格式的插件，type(feat/fix/docs...)的说明，以及tag
        git checkout -- README.md 撤销更改
        git commit --amend 重新提交 使用场景：提交信息填写错误 更改提交信息
    3. git恢复之前版本的两种方法：
      方法一：使用reset，适用场景：如果想恢复到之前某个提交的版本，且那个版本之后提交的版本我们都不要了，就可以用这种方法。
        a. 查看版本号 git log
        b. 使用 "git reset --hard 目标版本号" 命令将版本回退
        c. 使用 "git push -f" 提交更改，-f 表示强制push
      方法二：使用git revert，使用场景：如果我们想恢复之前的某一版本（该版本不是merge类型），但是又想保留该目标版本后面的版本，记录下这整个版本变动流程，就可以用这种方法。
        a. 查看版本号 git log
        b. 使用"git revert -n 版本号"反做，并使用"git commit -m 版本名"提交。注意： 这里可能会出现
           冲突，那么需要手动修改冲突的文件。而且要git add 文件名。
        c. git push
  3. change log
    介绍插件和使用方法
  4. copyright
    修改vscode新建js的模板
    可以修改JavaScript的模板 然后输入指定的词会自动输出
    © 2018-2019 FCoE, DRC, Delta Electronics, Inc. All Rights Reserved.
    All rights reserved表示保留所有权利。
    2018—2019，意思是说代码完成时间是2018年，最近一次修订在2019年。

二、gitflow
  1. 安装
    通过命令方式安装git flow    (MacOS的命令  brew install git-flow)
  2. 常用命令
    init、publish、feature...
  3. 分支的说明
    master、develop、 release、 hotfix
  4. git release
    发布版本
  5. test reset
<!-- <a href="https://blog.csdn.net/yxlshk/article/details/79944535">git恢复之前的版本1</a> -->
<!-- <a href="https://git-scm.com/book/zh/v1/Git-基础-撤消操作">git恢复之前的版本2</a> -->
commitlint https://www.cnblogs.com/liuming666/p/e3f10b69324d50518ef3a2ea71de6ed9.html
git cz,  http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html
git changelog https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-changelog-cli
test changelog9
tag 9