---
layout: post
title:  "git的简单使用"
date:   2015-07-31 17:57:38
categories: The-use-of-git
---

## git的安装 ##

- 官方的下载地址 [http://git-scm.com/download/](http://git-scm.com/download/ "git download")

- 安装完毕在本地创建git 的目录
- 
## git的常用命令使用 ##

- mkdir git_WorkSpace

- cd git_WorkSpace
 
- git init  初始化git 目录

- 实际开发中，我们通常是直接用别人的仓库来进行进一步的开发，那么下面的流程就是必须要看的了：
因为是团队合作，所以每个人在使用git时，要先进行类似的配置。

-  git config --global user.name "ningy1009"

-  git config --global user.email "1309958989@qq.com"

- 这样的配置文件也可以在/home/ningy1009/.gitconfig中看到。

- 回到自己的 /home/ningy1009/ 目录下
-  mkdir project
- cd  project
- 首先从服务器上克隆（clone出完整的工作树到本地）：
-  git clone  https://github.com/ningy1009   (外网用户)
- git clone 命令是将别的仓库克隆（clone）过来，后面是别人仓库的源地址，你可以直接用上面的地址试试。
- 接下来是在git 目录下创建自己的文件，创建完文件如何将文件传输到服务器端呢，可以使用下面的命令
- 首先使用git status 查看一下git 当前的状态

	On branch master </br>
	Initial commit </br>
	Changes to be committed: </br>
		(use "git rm --cached <file>..." to unstage) </br>
		new file: example </br>
		new file: hello </br>
- 我们能看到 git 的状态提示。提示信息告诉我们版本库中加入了两个新的文件，并且 git 提示我们提交这些文件，我们可以通过 git-commit 命令来提交，这里我们有两种输入方式</br>
- （1）带参数 m </br>
git commit -m "Initial commit of gittest reposistory" </br>
引号中的内容就是类似于SVN中每次提交代码前，都要填写的message信息，以便于以后自己或者别人能明白你这次更改的原因，及相关改动的信息。
- （2）不带参数 m </br>
git commit  </br>
系统会自动调用一个叫GNU nano的编辑器，来让你输入与上面类似的信息，在编辑器的下面会出现^G  ^X  ^O   ^J等等，^表示ctrl键，所以他们分别是“ctrl键+G”（获取帮助），“ctrl键+X”（Exit 退出），“ctrl键+O”（WriteOut 写保存），“ctrl键+J”（Justify），具体就不详述了。

- git  push origin master </br>
将本地的更改最后push到服务器上，使服务器上也同步保留了自己的更改

- git status 再次查看git的状态 </br>
返回 no changes added to commit (use "git add" and/or "git commit -a") 这样的提示信息 说明现在 没有任何文件需要提交

- git pull </br>
将服务器的所有文件都更新到本地
- 上面降到是git 最常用的一些命令和操作