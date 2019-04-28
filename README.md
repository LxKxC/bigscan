# bigscan
这是一个大网段端口扫描器，使用场景是产品经理丢给你上千IP段让你一天完成检查端口开放情况。。。

调用内嵌的masscan进行扫描，所以很快，还可以多线程。

依赖python3,使用环境是windows，**不支持linux**

需要安装依赖包：

python：
xlwt,
xlrd,
xlutils

winpcap：[https://www.winpcap.org/install/default.htm](https://www.winpcap.org/install/default.htm)

你可以试着用下面的pip命令安装，请注意pip要用python3的pip：
``` 
pip install -r requirements.txt
或者：
pip install xlrd xlrd xlutils
```

什么？使用方法？

其实挺简单，直接运行bigscan.py文件就好啦！

第一次运行会自动生成配置文件，你需要做的就是把需要检查的IP段一行一段的放进本程序自动生成的IP.txt里面。

