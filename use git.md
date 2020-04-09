# 我的git使用

新建一个房子，给房子起一个名字，想要进去打开门（放到本地），进去（提交远程），关上门

#### 初始化本地仓库

```js
// 右键 git bash here
get init
// 生成 .git文件仓库
```

#### 配置git信息

- 每一次提交都会记录当前备份者

```js
git config --global  user.name 'name'
// 当前的用户名
git config -- global user.email 'ceshi.@qq.com'
// 当前用户名的邮箱

```

#### 把代码放到仓库

- 提交代码

```js
// 提交到本地仓库 
git add ./demo.js
// 提交到远程仓库  -m  message 
git commit -m '说明0.1v版本'
```



















start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Reapply commits on top of another base tip
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects



