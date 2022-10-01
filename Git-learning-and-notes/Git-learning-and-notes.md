## 基本命令

### git status

查看仓库状态



### git init

初始化Git仓库



### git add

```
git add <file>
```

将文件添加到Git仓库

`git add`命令并没有把文件提交到 Git 仓库，而是把文件添加到了「临时缓冲区」，这个命令有效防止了我们错误提交的可能性



### git commit

```
git commit -m "message"
```

将文件提交到Git仓库



### git log

打印Git仓库提交日志



### git branch

查看仓库分支情况，分支前带`*`表示当前所在分支

输入命令`git branch "name"`创建一个名为`name`的分支

输入命令`git branch -d "name"`删除一个名为`name`的分支

有的时候会出现通过`git branch -d`命令可以出现删除不了现象，如分支`name`的代码没有合并到主分支等，这时如果我们一定要删除该分支，那么我们可以通过命令`git branch -D`进行强制删除



### git checkout

输入命令`git checkout "name"`切换到`name`分支

输入命令`git checkout -b "name"`在创建`name`分支的同时切换到`name`分支

输入命令`git checkout <messsage>`切换到`<message>`标签



### git merge

输入命令`git merge "name"`将`name`分支合并到当前分支

**在合并分支的时候，要考虑到两个分支是否有冲突，如果有冲突，则不能直接合并，需要先解决冲突；反之，则可以直接合并**



### git tag

输入`git tag <message>`命令，为当前分支添加标签，如`git tag v1.0`



## 将代码提交到 GitHub

### git pull

如果远程仓库的代码有更新，为了保持本地与远程的代码同步，我们需要把远程的代码拉到本地

```
git pull origin master
```

其中origin为远程仓库名称，master为分支名称



### git push

如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库

```
git push origin master
```



### 建立联系

#### 第一种

本地没有 Git 仓库，这时我们就可以直接将远程仓库`clone`到本地。通过`clone`命令创建的本地仓库，其本身就是一个 Git 仓库了，不用我们再进行`init`初始化操作啦，而且自动关联远程仓库。我们只需要在这个仓库进行修改或者添加等操作，然后`commit`即可

输入命令将远程仓库克隆至本地

```
git clone url
```



#### 第二种

本地有 Git 仓库，并且我们已经进行了多次`commit`操作

进入该仓库，进入`init`初始化操作

输入命令，关联远程仓库

```
git remote add url
```

