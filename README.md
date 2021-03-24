# git bash常用命令
### 一、准备：
1、安装git官网：https://git-scm.com 下载下来直接下一步。。。。。
2、申请GitHub帐号（过程忽略，作为程序员这个是必备的哦 _）;
3、配置GitHub秘钥：

        下载安装好git在桌边或者新建个文件夹右击选择Git Bash Here，
        打开后输入:ssh-keygen -t rsa -C 你的邮箱   回车下一步
        下图红色箭头是.ssh/id_rsa文件在你电脑上的位置(之前我已经配置好了)


下图箭头如果需要重新配置原则y 不需要选择n（只要配置过都选n）

打开github登录你的账号，点击 右上角头像选择settings

在电脑上找到你的.ssh/id_rsa文件，用记事本打开id_rsa.pub文件，将文件的内容复制粘贴在下图的Key里，Title随便起个标（这里我以添加不做展示）；最后点击Add SSH Key，完成这一步就ssh就配置完成了 

### 二、建立仓库：
在本地新建一个文件夹；
进入文件夹，右击打开git bash Here, 输入
> git init

此时文件夹里生成一个.git的文件夹（如果没有是默认隐藏了）；

登录github帐号，点击右上角+号，点击New repository，进入填写名称，说明，勾选Initialize this repository with a README,
在点击Create repository点击确认创建仓库。

然后在打开的git Bash Here中输入 git clone 项目地址

回车之后项目就被克隆在本地仓库里了。

### 三、将项目托管到github上：
> cd demo
进入到项目目录，再把要托管的项目放在目录里

下面是要托管的项目

> 运行：git init

> 运行：git add .

> 运行：git commit -m "提交项目的备注"

> 运行：git remote add origin "仓库地址"，让本地仓库和远程仓库关联

> 运行：git push origin main 本地仓库代码提交到github上（运行这一步要输入用户名和密码，用户名是github帐号，密码就是github的密码）


### 四、创建分支，提交到分支在合并分支到主干
> 运行：git branch dev 创建分支

> 运行：git checkout dev|main 进入创建的分支(也可以切换到main主干)

> 运行：git add .

> 运行：git commit -m "提交代码说明"

> 运行：git remote add origin url(demo仓库地址)，让本地仓库和远程仓库关联

> 运行：git push origin dev|main 本地dev分支仓库提交到github上（运行这一步要输入用户名和密码，用户名是github帐号，密码就是github的密码）；

### 五、代码比对

> 运行：git diff  分支名1 主干名     dev对比main

> 运行：git diff  分支名称 分支名称  dev1对比dev2

### 六、解决冲突

> 运行：git add .

> 运行：git commit -m "提交代码说明"

> 运行：git pull  提交代码前一定要拉代码

> 运行：git push origin dev|main  提交代码此时出现冲突

### 七、dev（分支）合并到 main（主干）

> 运行：git checkout main   先切换到主干来

> 运行：git merge dev    运行要合并的分支

> 运行：git push -u origin main  推到远程仓库  
