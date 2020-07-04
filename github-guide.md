title: 超完整Github开发指南
tags:
  - 计算机
  - Github
description: Github开发指南
date: 2020-04-03 00:00:00
---
# 0、目录
<a href="#first">1、注册GitHub 账户</a>
<a href="#second">2、创建第一个仓库 </a>
<a href="#third">3、上传至仓库</a>
<a name="#fourth">4、使用Github Pages创造自己的网站</a>
# 1、注册GitHub 账户
访问[Github](http://www.github.com/),若无意外，则效果为以下所示（Firefox)

![Github首页](/blogimages/github-mainpage.png)

输入**用户名**、**邮箱（确保可用）**、**密码**，点击Sign up for Github，再填写几个个人信息，就Well Done了！

注册完后点击Sign in,填写用户名及密码即可。

![Github 登录页](/blogimages/github-login.png)







然后就可以看到个人界面了！

![Github 个人主页](/blogimages/github-logined.png)
<a name="second"></a>
# 2、创建第一个仓库
点击Repositories右侧的New，即可跳转至仓库创造页！

​![仓库创造页](/blogimages/github-new.png)



可以填写Repository name(仓库名称）、Description（仓库描述）等。

注：关于license：请访问[Choose an open source license](https://choosealicense.com/)


<a name="third"></a>
# 3、上传至仓库
1、下载[GitHub Desktop](https://desktop.github.com/)

2、打开软件

3、克隆仓库

![Github Desktop](/blogimages/github-desktop.png)

编写，点击**COMMIT TO MASTER**和**PUSH ORIGN**即可！
<a name="fourth"></a>
# 4、使用Github Pages创造自己的网站
新建一个仓库，以**username.github.io** 命名（username是指你的用户名）
新建完成后，使用Github Desktop推送网页至该仓库。
Q&：万一网站做不好肿么办？
A：
1、使用Github主题：
访问**Settings->GitHub Pages->Theme Chooser->Change Theme** 选择样式，不过好像只适合写主页，并且必须使用**Markdown**格式。
2、使用模板网站，这里推荐[HTML5 UP](https://html5up.net/)
![HTML5UP](/blogimages/htmlup.png)
看到自己心仪的主题，可以选择**Free Download**，或者点击**Live Demo**查看预览。
注：大家可以看看我的网站：[xiezheyuan.github.io](http://xiezheyuan.github.io/)

<a name="fifth"></a>

# 5、为自己的项目创建Github Pages 网站
与*4、使用Github Pages创造自己的网站* 类似，不过需要选择Settings->GitHub Pages->Source选择上传地址，默认为None，建议为**master branch /docs folder**，这样可以将网站与程序分开（**master branch /docs folder**指仅上传docs目录）
首发于CSDN博客https://blog.csdn.net/pythonbilly