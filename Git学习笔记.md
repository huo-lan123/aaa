![](C:\Users\pc\Pictures\重要图片\1716463609-5bf0fbfc7c3aa_articlex.jpg)

​                                                                  工作区、暂存区、版本库（本地仓库）

### 命令

**仓库（Repository）**

**收藏（Star）**：收藏项目，方便下次查看

**复制（克隆）项目（Fork）**

**发送请求（Pull Request**）：Fork者发起，原创者接受请求，合并到原项目中去

**关注（Watch ）**：关注项目，当项目更新可以接受到通知

**事务卡片（Issue）**：发现代码BUG，但是目前没有成型的代码，需要讨论时用（提出问题，一起来讨论）

### 基本信息设置

进入你要存放文件的文件夹，右击点击进入Git Bash Here
注意：这里填写的是你的Github用户名和邮箱，这样在你提交的时候仓库里面就可以看到

设置用户名：
git config --global user.name ‘huo-lan123’
设置用户名邮箱
git config --global user.email ‘XXX@163.com'
注意空格

### 工作区域（上传文件到Github）

进入暂存区：git add 文件名
进入本地Git 仓库 ：git commit -m “提交描述”
上传远程仓库 ：git push 

### 删除文件（三种方式）

1、rm  文件名       #工作区 
     git rm 文件名       #暂存区
     git commit -m '提交描述 ’    #本地仓库

2、rm a.txt       #工作区

​     git add a.txt     #暂存区

​     git commit -m '描述'  #本地仓库

3、git rm -f a.txt     #暂存区

git commit -m '描述'   #本地仓库

<u>注意：第一步操作删除工作区文件同时提交到暂存区中</u>

**删除后撤回**

工作区（执行了第一步想撤回）

1、git checkout 文件名 

2、git checkout .

3、git reset  -hard head

暂存区（执行了第二步想撤回）

git reset  -hard head

暂存区-->本地仓库（已提交）

git reset --hard HEAD^ 

### 修改文件

vi 文件名（a 进入编译，Esc切换，然后在左下角输:wq就可以退出）

### 将Github文件克隆到Git上

git clone 仓库地址

### 遇到的问题

##### 1.上传时要输入账号密码（私有项目，没有权限）

解决：

1、在 .git文件 里面找到config 打开（.git文件在你本地仓库创建的文件夹里面，默认隐藏）

2、将 [remote “origin”]
url = https://github.com/用户名/仓库名.git
改为
[remote “origin”]
url = https://用户名:密码@github.com/用户名/仓库名.git
保存就解决了

##### 2.上传错误 （git push）

```
输入：git pull --rebase origin master
```

##### 3.查找问题经验

> 可以输入`git status` 查看当前状态，你在删除或者上传时漏了那一步操作

### 需要记住的基本操作命令

<u>注意每个单词后都有空格</u>

新建文件 touch 文件名
创建文件夹：mkdir 文件名
进入文件 ： cd 文件名
查看文件 ： ls
创建本地Git仓库：git init
查看仓库状态： git status
编辑文件 ： vi
查看设置：git config --list
history 显示历史输入过的命令
clear 清屏