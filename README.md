###test
|a      |b  |c  |2    |
-----------------------
|asdfasf|adf|fff|1    |
|a      |2  |3  |44234|
<h1>一、git</h1>
  <h2>1. 安装和配置</h2><br>
    1. <a href="https://git-scm.com">官网</a>下载，根据自身OS下载git。<br>
      a. Windows：运行安装程序后配置环境变量，将安装git的目录定位到bin文件夹以后，复制bin的路径，将此路径添加到环境变量中，重启cmd即可运行git命令<br>
      b. MacOS：git version 查看git版本，如果报错请自行下载<br>
    2. 使用命令 "git config --global user.name "Your Name" " 配置用户名<br>
       使用命令 "git config --global user.email "email@example.com" " 配置邮箱<br>
       使用命令 "git config user.name" or "git config user.email" 查看当前用户名或邮箱<br>
    3. git version 查看git版本<br>
    4. git config --list 查看配置文件<br>
    5. vi .gitconfig 查看并编写git config文件<br>
  2. 常用命令<br>
    1. 常用命令，包括分支、提交、等<br>
      a. git clone yourGitProjectUrl  拉取远端仓库<br>
      b. git branch 查看分支<br>
        -a 查看所有分支包括远端(需要在本地项目跟目录运行此命令)<br>
        -v 查看所有分支的最后一次提交<br>
      c. git status 查看本地仓库状态<br>
      d. git add . 添加修改后的文件<br>
      e. git commit 提交代码到本地缓存区，命令执行后需要填写提交信息。尽量多次提交，容易回退。<br>
      f. git stash 将会把当前目录和index中的所有改动(但不包括未track的文件)压入一个栈,然后留给你一个<br>clean的工作状态,即处于上一次最新提交处。<br>
      g. git checkout branchname 切换分支 当改动未提交时不允许切换，可以先commit再切换<br>
    2. git commit message的格式，检查格式的插件，type(feat/fix/docs...)的说明，以及tag<br>
        git checkout -- README.md 撤销更改<br>
        git commit --amend 重新提交 使用场景：提交信息填写错误 更改提交信息<br>
    3. git恢复之前版本的两种方法：<br>
      方法一：使用reset，适用场景：如果想恢复到之前某个提交的版本，且那个版本之后提交的版本我们都不要<br>了，就可以用这种方法。<br>
        a. 查看版本号 git log<br>
        b. 使用 "git reset --hard 目标版本号" 命令将版本回退<br>
        c. 使用 "git push -f" 提交更改，-f 表示强制push<br>
      方法二：使用git revert，使用场景：如果我们想恢复之前的某一版本（该版本不是merge类型），但是又想<br>保留该目标版本后面的版本，记录下这整个版本变动流程，就可以用这种方法。<br>
        a. 查看版本号 git log<br>
        b. 使用"git revert -n 版本号"反做，并使用"git commit -m 版本名"提交。注意： 这里可能会出现<br>
           冲突，那么需要手动修改冲突的文件。而且要git add 文件名。<br>
        c. git push<br>
  3. change log<br>
    介绍插件和使用方法<br>
  4. copyright<br>
    修改vscode新建js的模板<br>
    可以修改JavaScript的模板 然后输入指定的词会自动输出<br>
    © 2018-2019 FCoE, DRC, Delta Electronics, Inc. All Rights Reserved.<br>
    All rights reserved表示保留所有权利。<br>
    2018—2019，意思是说代码完成时间是2018年，最近一次修订在2019年。<br>

<h2>二、gitflow</h2>
  1. 安装<br>
    通过命令方式安装git flow    (MacOS的命令  brew install git-flow)<br>
  2. 常用命令<br>
    init、publish、feature...<br>
  3. 分支的说明<br>
    master、develop、 release、 hotfix<br>
  4. git release<br>
    发布版本<br>
  5. test reset<br>
<a href="https://blog.csdn.net/yxlshk/article/details/79944535">git恢复之前的版本1</a><br>
<a href="https://git-scm.com/book/zh/v1/Git-基础-撤消操作">git恢复之前的版本2</a><br>