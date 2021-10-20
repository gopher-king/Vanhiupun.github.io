## 使用ssh连接Git仓库（Github）
通过ssh命令连接远程服务器进行操作

## 在本机生成一个公钥和私钥对
一般放在``~/.ssh/``，即用户的``.ssh``目录下。

这个目录下有一个``known_hosts``文件，本用户曾经ssh连接过的主机的公钥都会保存在这里。

在命令行中使用`ssh-keygen`工具来生成密钥对：


```` bash
ssh-keygen          #mac系统命令
ssh-keygen.exe      #win系统命令
````
生成过程中会让你指定生成位置，以及给它再设一个密码。我们使用默认位置，不再设定密码。也就是一路Enter就行。


## 打开存放密钥的文件夹查看
````bash
cd .ssh/          #打开存放密钥的文件夹
ls                #查看文件
cat id_rsa        #查看私钥
cat id_rsa.pub    #查看公钥
````
**在`.ssh/`中可以看到`cat id_rsa`  `cat id_rsa.pub`两个文件**

**`cat id_rsa`为私钥，一般自己保存即可**

**`cat id_rsa.pub`为公钥，添加到服务器上**

## 添加密钥至Github

复制一下生成的公钥，从（包括）ssh-rsa到最后。最后的计算机名和它前面的空格不用复制，复制也可以。

登录Github，点右上角自己的头像，选择Settings，然后在新页面中的左侧边栏选择SSH and GPG Key。给这个ssh公钥起一个名字，然后把公钥复制进去。

添加上之后就可以用本机SSH连接Github了。

然后复制Clone地址的时候就可以选择`Use SSH`了。

clone方法跟HTTPS的一样。


然后使用`git remote set-url origin git@github.com:xxxxxx更新url`


##如何免密码使用SSH连接服务器
在目标服务器的``~/.ssh/``目录下有一个`authorized_keys`文件

这个文件中的所有ssh公钥是可以无条件连接到这台服务器上的

把自己生成的公钥粘贴进去就可以了。

## 通过SSH命令连接
````bash
ssh git@github.com     
````

当出现**_``Hi username! You’ve successfully authenticated, but GitHub does not provide shell access.``_**的时候就说明连接成功


## 将本机中已经clone下的项目由HTTPS方式更改为SSH方式

在目标项目的目录中打开Git Bash终端，

输入`git remote -v`可以查看remote仓库

去Github中复制下该仓库的SSH URL
