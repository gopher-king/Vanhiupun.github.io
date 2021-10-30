## Git 修改更新的代码上传到服务器的操作步骤：


### 打开终端`cd`到目标目录

使用命令 `git status` ，查看本地分支文件信息

````bash
 git status # 确保更新时不产生冲突 （ no changes added to commit (use "git add" and/or "git commit -a" 说明没有冲突）
````


### 添加修改更新过的代码

使用命令`git add .` 将更改或者新增的文件加入到Git的索引中

````bash
 git add .
````



### 确认提交当前工作目录的修改内容，并添加修改原因

直接调用 `git commit` 命令，会提示填写注释。

````bash
git commit -m "注释内容"
````


### 拉一下远端的仓
使用 `git pull origin master`

拉一下远端的仓代码，然后弹出的文件，`q!` 退出即可
````bash
git pull origin master
````


### 把代码推送到远端仓库
使用 `git push origin master`

等待一段时间，即可上传成功
````bash
git push origin master
````


### 登录 Github 即可看代码上传情况
