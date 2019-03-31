# Git 学习


![git](https://git-scm.com/images/logo@2x.png "git")


Git(读音为/gɪt/。)是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。


### 一、安装git

##### 1.在Linux上安装git

ubuntu上的命令：

```
$ sudo apt-get install git
```

如果是其他版本的Linux可以通过源码安装。

先从官网下载源码，然后解压，依次输入：./config , make , sudo make install这几个命令。

##### 2.在Mac OS 上安装git

在Mac上安装推荐从APPSTORE安装。

##### 3.在Windows上安装git

1.  从git[官网下载程序](https://git-scm.com/downloads)安装，按默认一直点下一步就可以。

2.  安装完成后，在开始菜单或者右键里可以找到git/git bash here点击运行出现类似命令行窗口的东西，恭喜你git安装成功了！

3.  然后在命令行里配置你的用户名和email地址。

```
$ git config --global "youname"
$ git config --global "youemail" 
```

### 二、创建仓库

仓库就是版本库，英文名repository ，每个文件的修改、删除都在版本库里并且可以被追踪。

命令：
```
$ mkdir Learn   //创建文件夹
$ cd Learn      //进入文件夹Learn
$ git init      //初始化，把这个目录变成git仓库
```
这时文件夹里会出现一个.git目录，如果没有看到那就打开隐藏文件。

### 三、把文件添加到版本库

1.   首先我们建立一个文本文档命名为README.txt，用命令添加到仓库：

```
$ git add README.txt    //git add <file>可以多次使用，添加多个文件
```

2.   用命令git commit告诉git，把文件提交到仓库。-m后面的内容是本次提交的说明，可以是任意的内容：

```
$ git comnit -m "新建一个README.txt"
```

3.   可以使用命令git status 查看当前仓库的状态：

```
$ git status 
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   README.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

4.   使用命令git diff可以查看文件做了什么修改：

```
$ git diff README.txt
```
注：如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

5.   使用命令git log显示从最近到最远的提交日志：

```
$ git log   //如果嫌输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数
$ git log  --pretty=oneline
```
6.   HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭

```
$ git reset --hard commit_id    //commit_id是版本号
```

7.   使用git reflog查看命令历史，以便确定要回到未来的哪个版本

```
$ git reflog 
```

8.   使用git checkout 命令可以丢弃工作区的修改

```
$ git checkout -- file
```

9.   使用git rm命令用于删除一个文件

```
$ git rm README.txt
```


### 四、把文件添加到远程仓库

1.  由于你的本地Git仓库和GitHub仓库之间的传输是通过SSH加密的，所以第一步是创建SSH Key。

```
$ ssh-keygen -t rsa -C "youremail@example.com"  //一路回车，使用默认值即可

完成之后可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。
```

2.   登录GitHub 打开“Account settings”，“SSH Keys”页面：

然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容。

3.   要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git

```
$ git remote add origin git@github.com:zhaozhifu-catshak/Learn.git
```

4.   关联后，使用命令git push -u origin master第一次推送master分支的所有内容，此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改
   

5.   用命令git clone克隆一个远程库到本地

```
$ git clone git@github.com:zhaozhifu-catshak/Learn.git
```

