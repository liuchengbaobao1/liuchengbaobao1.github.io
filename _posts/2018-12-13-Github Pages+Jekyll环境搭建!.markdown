---
layout: post
title:  "Github Pages+Jekyll环境搭建!"
date:   2018-12-13 10:08:24 +0800
categories: jekyll update
---
1、安装Ruby

	下载地址:http://rubyinstaller.org/downloads/
	
![](/assets/2018-12-13/img/1.jpg)

	本文使用的是：rubyinstaller-2.3.3-x64
	
![](/assets/2018-12-13/img/2.jpg)

	安装的时候注意勾选把ruby添加到路径PATH
	安装目录：D:\software\rub\Ruby23-x64
	Ruby安装成功

2、安装DevKit

	下载地址:http://rubyinstaller.org/downloads/
	
![](/assets/2018-12-13/img/3.jpg)

	本文使用的是：DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe
	将后缀改成.zip并解压到D:\software\rub\DevKit目录下
	
	1）进入目录，执行初始化命令：ruby dk.rb init 生成config.yml文件(如下图)
	
![](/assets/2018-12-13/img/4.jpg)	

	2）打开config.yml文件，最后一行添加 - D:/software/rub/Ruby23-x64 路径(如下图)
	
![](/assets/2018-12-13/img/5.jpg)	

	3）依次执行以下命令(如下图)
		
		ruby dk.rb review # 审查（非必须）
		
		ruby dk.rb install # 安装

		gem -v  # 查看gem是否正常安装

![](/assets/2018-12-13/img/6.jpg)

3、安装Jekyll
	
	1）gem install jekyll
	
	2）jekyll --version
	
![](/assets/2018-12-13/img/7.jpg)

	3)新建项目，执行命令： jekyll new myblog
	
![](/assets/2018-12-13/img/8.jpg)	
	
4、运行服务器	
	
	进入 myblog 文件夹，运行服务器
	
	cd myblog
	
	jekyll serve
	
	注：D:\software\rub\DevKit\myblog目录下同时按下Shift+鼠标右键，选择在此处打开命令窗口

![](/assets/2018-12-13/img/9.jpg)

	访问测试：http://127.0.0.1:4000/(如下图)
	
![](/assets/2018-12-13/img/10.jpg)

至此环境安装完毕
	
5、github创建仓库		
	网站地址：https://github.com/
	
	第一步命名规则：username.github.com
	
	第二步直接创建即可
	
![](/assets/2018-12-13/img/11.jpg)	
	
6、将项目（代码）从GitHub上克隆（下载）到本地仓库	
	
	1)要将项目从GitHub上克隆到本地，首先你得下载并安装好git for window。
	
	下载地址:https://gitforwindows.org/
	
	安装时，直接next就行。
	
	2)配置Git：安装完后，右键单击桌面空白处，选择Git Gui Here，进去之后，选择左上角的help选项，
	会出现一个Show SSH Key，然后点击“Generate Key”得到秘钥。将其复制到剪切板。（如下图）

![](/assets/2018-12-13/img/12.jpg)	
	
	3)打开GitHub，登陆后，打开设置界面，在SSH Keys栏中点击“Add SSH key”按钮，
	然后复制上面生成的秘钥。
	
![](/assets/2018-12-13/img/13.jpg)		
	
	粘贴后，点击add key。
	
	4)此时便可以开始使用Git功能了，右键单击桌面空白处，选择Git Bash Here，进去后便可进入git控制台，
	对于首次安装git的机器，一定要首先进行用户账户信息的配置：

	git config --global user.name "你的github用户名"

	git config --global user.email "你的github邮箱地址"
	
	5)将项目从GitHub上克隆到本地，首先打开你要想项目存放到本地的目录，
	例如：我的Git安装在D盘中，而我想将项目存放到D:\software\rub目录下，操作如下：
	
	在空白处单击鼠标右键，Git Bash Here
	
	然后git clone +你想要克隆的项目的地址。如：
	
![](/assets/2018-12-13/img/14.jpg)	

	命令如下：
	
![](/assets/2018-12-13/img/15.jpg)	
	
	此时，打开你的目标文件，会发现新建了一个目录，里面便是你拷贝到本地的文件。
	
![](/assets/2018-12-13/img/16.jpg)	

7、本地博客发布到Github Pages

	1）将项目myblog文件夹下所有文件拷贝到D:\software\rub\liuchengbaobao1.github.io下

	2）接下来依次输入一下命令即可上传到github
		
		git add .        （注：别忘记后面的.，此操作是把liuchengbaobao1.github.io文件夹下面的文件都添加进来）

		git commit  -m  "提交信息"  （注：“提交信息”里面换成你需要，如“first commit”）

		git push -u origin master   （注：此操作目的是把本地仓库push到github上面，此步骤需要你输入帐号和密码）

![](/assets/2018-12-13/img/17.jpg)	

	项目已提交到github上

![](/assets/2018-12-13/img/18.jpg)	

8、写博客
	
	1)按照D:\software\rub\DevKit\myblog\_posts目录下文件格式编写（如下图）

![](/assets/2018-12-13/img/19.jpg)	
	
	2)文件内容红框中的内容按照此格式修改，其他内容按照markdown语法编写（如下图）
	
![](/assets/2018-12-13/img/20.jpg)		


至此，结束！有遗漏与不足欢迎补充！










