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
//第一步 提交到本地仓库 
git add ./demo.js   // ./具体文件名  
// git add ./   	// ./当前目录下所有修改的文件

//第二部 提交到远程版本仓库  -m  message 
git commit -m '说明0.1v版本'  //  
// git commit --all -m ''    // 直接提交到 远程仓库
```

- 代码检查

```js
git status
```

- 查看日志

```js
git log
// 谁提交了   Author
// 提交的时间 Date

git log --oneline   // 查看简洁版本的日志
// 版本号   备注
```

- 版本回退

```js
git reset -- hard head ~0   //从最近一次索引  0上一次  1上上次提交的代码


// git reset -- hart 797a51d  //精确回到某一个版本     版本号  797a51d

git  reflog  // 可以看到每一次版本切换的记录
```

- 分支处理

```js
// 创建分支
git branch dev   // dev 是分支名称，在刚创建时dev分支的东西和master分支一样的

// 查看分支 
git branch

// 切换分支
git checkout dev    // 切换之前要创建分支

// 分支合并
git merge dev      // 合并分支的内容，把当前分支于指定的分支合并
// 从主分支进入合并  单分支 

// 删除分支 
git branch -d dev   // 注意不能删除  当前分支
```

- 冲突解决

```js
// 原因  devs修改完功能 提交了   masters修改了功能也提交了  在master中  合并分支
<<<<<<< HEAD
这是在 master  分支中的功能
=======
devs 分支的一半
>>>>>>> devs


// head  指向当前最新的提交
```



- 代码提交

  拿到 githup的地址

  ```js
  git push 
  // https://gitee.com/xhwork/blok.git
  ```

  

`clear  清屏`

#### 常见问题

1. 没有添加 说明 `-m  ''`这时候需要退出  `esc`  `:q!` 回车

2. 如果已经提交 `git add `可使用 `git status ` 检查状态

   ```js
   git status 
   // working directory clean 工作环境是干净的 已经提交过了
   
   // modified 红色 修改过的文件还没有到本地仓库 需使用  git add
   // modified 绿色 修改过的文件还没有到远程仓库 需使用  git  commit -m '';
   // nothing to commit, working tree clean 绿色  提交完成过了
   
   ```

   



1. 先确认当前分支是你的工作分支
   - git checkout working    --force 
2. 把本地代码提交到本地仓库
   - git add .  
   - git commit -m"$1" -a 
3. 切换到主分支
   - git checkout master 
4. 并将默认分支和中央最新版本合并  
   - git pull origin master 
5. 本地仓库和主分支(默认分支)进行合并
   - git merge working    
6. 提交到中央版本库
   - git push origin master   
7. 切回到你的工作分支
   - git checkout working   --force   
8. 如果不小心动了生产环境（就是只从中央版本库pull到本地）的文件，只好将本地版本退回一个，再从中央代码库pull代码合并 
   - git reset --hard HEAD   





# 使用命令行操作流程

1. 执行命令 切换到master分支
    `git checkout master` 
2. 执行命令 拉取master最新稳定代码分支
    ` git pull master` 
3. 执行命令 新建一个分支并切换到该分支
    ` git checkout -b newbranch` 
4. 执行命令 将新的分支推送到远程服务器
    ` git push --set-upstream origin newbranch` 
5. 代码开发中 ，开发完成，提交代码操作如下
    5.1 将不需要提交，无用的修改文件还原（尽量保持少的修改文件）
    ` git checkout -- fileName`
    5.2 将本地需要提交的文件隐藏（因为如果有文件冲突，将会拉取不了主分支代码）
    ` git stash`
    5.3 拉取主分支代码
    ` git pull origin master`
    5.4 还原隐藏的文件
    ` git stash pop`
    5.5 将需要提交的代码添加到暂存区
    ` git add fileName`
    5.6 将需要提交的代码提交到本地仓库
    ` git commit -m "提交代码功能描述信息"`
    5.6 将需要提交的代码提交到远程仓库
    ` git push`
    5.7 在浏览器客户端新建PR请求

 

 

 

 

 









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



