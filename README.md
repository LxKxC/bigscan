# bigscan
这是一个大网段端口扫描器，使用场景是产品经理丢给你上千IP段让你一天完成检查端口开放情况。。。

我不是专业程序员，代码写的烂请谅解

调用内嵌的masscan进行扫描，所以很快，还可以多线程。

依赖python3,使用环境是windows，**不支持linux**

需要安装依赖包：

python：xlwt,xlrd,xlutils

winpcap：[https://www.winpcap.org/install/default.htm](https://www.winpcap.org/install/default.htm)

你可以试着用下面的pip命令安装，请注意pip要用python3的pip：

	pip install -r requirements.txt
	或者：
	pip install xlrd xlrd xlutils

什么？使用方法？

其实挺简单，直接运行bigscan.py文件就好啦！

第一次运行会自动生成配置文件，你需要做的就是把需要检查的IP段一行一段的放进本程序自动生成的IP.txt里面，然后再次运行bigscan.py就好啦！

bigscan.exe是懒人版程序，依赖都打包好了，不需要准备环境。

线程设置在scan.config文件里。

懒人版没法改扫描速率，想改要在bigscan.py里面改，位置是:

	--rate 3000
一般家用路由器用3000正合适，5000容易死机，当然这个速率是单线程3000，默认使用5个线程那就是15000的速率。。。

顺便说一下，masscan威力非常大，举个例子：

	如果你在你的公司里，以每秒十几万的rate扫描主机，那么你整个公司的网络将瞬间堵塞
	（自杀式DOS攻击，奇效）

所以！扫描要小心啊！