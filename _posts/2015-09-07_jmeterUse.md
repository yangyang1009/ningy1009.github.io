---
layout: post
title:  "Jmeter 的安装与使用"
date:   2015-09-07 17:57:38
categories: The-use-of-jmeter
---

## jmeter的安装 ##

- 官方的下载地址 [http://jmeter.apache.org/](http://jmeter.apache.org/)

- jmeter 是Apache JMeter 是Apache组织的开放源代码项目，是一个100%纯Java桌面应用，用于压力测试和性能测量。它最初被设计用于Web应用测试但后来扩展到其它测试领域。
- jmeter 不需要安装 直接在环境变量中配置
- 首先在系统变量中新增一个JMETER_HOME 变量，存入JMETER的 解压包文件地址 D:\Program\apache-jmeter-2.13
- 接着在再 classpath 中添加jmeter 的jar 文件
- %JMETER_HOME%\lib\ext\ApacheJMeter_core.jar;%JMETER_HOME%\lib\jorphan.jar;%JMETER_HOME%\lib\logkit-2.0.jar; 
- 注意这里的logkit-2.0.jar 要以自己本机的版本为主。
- 配置结束后，运行jmeter 的bin 文件夹下的jmeter.bat 
- 如果出现 
- ![](https://github.com/ningy1009/ningy1009.github.io/blob/master/_posts/jmeter_success.jpg)
## jmeter的常用命令使用 ##

