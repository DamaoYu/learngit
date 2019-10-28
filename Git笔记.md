# Git笔记

## Git简介

 Git是目前世界上最先进的分布式版本控制系统。 

## 创建版本库

版本库又名仓库，英文名**repository**，你可以简单理解成一个目录，这个目录里面的所有文件都可以被Git管理起来，每个文件的修改、删除，Git都能跟踪，以便任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。 

选择一个合适的地方，创建一个空目录： 

```powershell
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit
```

第二步，通过`git init`命令把这个目录变成Git可以管理的仓库： 

```powershell
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
```

当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的 。

所有的版本控制系统，其实只能跟踪文本文件的改动，比如TXT文件，网页，所有的程序代码等等，Git也不例外。 

### 把文件添加到版本库

1.编写一个`readme.txt`文件 

2.用命令`git add`告诉Git，把文件添加到仓库 

```powershell
$ git add readme.txt
```

3.用命令`git commit`告诉Git，把文件提交到仓库 

```powershell
$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```

`-m`后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的 。

`git commit`命令执行成功后会告诉你，`1 file changed`：1个文件被改动（我们新添加的readme.txt文件）；`2 insertions`：插入了两行内容（readme.txt有两行内容）。 

`commit`可以一次提交很多文件，所以你可以多次`add`不同的文件 。

## 时光机穿梭

- 要随时掌握工作区的状态，使用`git status`命令。
- 如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。

