# Bilibili-Download-Util
用java实现的简易版b站视频下载器

# 介绍

因为朋友昨天突然要了这个需求，所以今天通过一上午来写了个简易版。


# java版本 1.8



# 使用方法

因为是用java编写的，并且就一个文件，所以也没有进行打包和编译。打包嘛，没意义。编译呢，还是让使用的程序员看看源码，然后有其它需求自己改改，总共200多行，还有那么多空行，没什么技术难度。

总共文件为一个启动文件（java格式），一个配置文件（properties格式），共两个文件。

使用前，没有java的需要java，我是基于java1.8进行开发的。

有java的，然后就在命令行工具里。 输入 javac 这个java文件的全路径名（包含.java）。你先换到java文件的目录也成，然后直接javac 文件名。进行编译

编译后，产生一个同名class文件。然后还是在命令行输入 java 文件全路径名(不包含.class)。还是你也可以先换到java文件的目录，然后直接java 文件名进行启动。

不过启动前要做一些事。

请将配置文件和启动文件放到同一目录下。

然后进行配置文件配置

配置文件有两个参数

一个是下载路径，这个大家都懂，想下载到哪里就配一下。不要忘记在路径结尾加个斜线。什么斜线根据你的系统来。

另外一个是cookie，正是因为这个cookie，所以才能模仿真实访问来获取到根据你的账号设置的默认清晰度来获取改清晰度的视频地址。


以google浏览器为例，先进入到一个视频，然后 鼠标右键 -> 检查 -> application -> Cookies -> https://www.bilibili.com 

然后出现一个 cookie列表，你就找 _uuid 开头的 后面一长串就是这个key的值，复制，然后粘贴到配置文件里，就okay了。

有人可能问，我每次都要配置嘛？，其实这涉及到cookie原理。 cookie的保存期是很长的，虽然我没查看 b站的保存期限，那也得有一周吧。

你这中途再次访问b站。他的时间会刷新。也不知道b站的机制是什么，但应该差不多。复制完成放心用。

你遇到过，你每天登陆b站，都不用登陆账号密码吧，然后偶尔会需要，可能是因为b站服务器的问题，或者，你很久没有登陆了，过期了。

这个和上面的情况是一样的。


然后就可以通过之前 讲过的 java 文件名（不包含后缀）来启动了。

先输入av号（必选），然后输入p号，如不输入p号直接回车，则默认为p=1。

然后进入下载序列，请耐心等待。



# 文件格式

B站的视频格式是为flv格式的，我也没有进行更改，因为我个人觉得，这个格式很好。很清晰

