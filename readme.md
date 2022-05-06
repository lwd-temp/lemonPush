# Push To PC
## 介绍
一个基于局域网内Android手机简单快捷发送剪切板内容到Windows电脑剪切板的项目，项目包括Android和Windows软件

## 下载地址
- [Windows 7.5K](https://gitee.com/ishare20/msglistener/attach_files/1052158/download/pushToPCServer.exe)
- [Android 1.78M](https://gitee.com/ishare20/msglistener/attach_files/1052159/download/push-v1.0-app-release.apk) 

## 配置教程
电脑双击启动pushToPC程序后显示电脑的IP，手机安装Push App后，点击设置电脑IP，填写电脑IP点击发送剪切版即可将
手机的剪切板发送到电脑的剪切板。

支持扫描设置电脑IP（速度较慢，部分手机无法扫描）

如电脑无法接收手机剪切板，需要配置电脑防火墙（教程待补充）

## 功能特性
- 手机的剪切板直接发送到电脑的剪切板，电脑直接粘贴可用
- 剪切板中的文本如包含网址可自动识别并使用默认浏览器打开
- 支持多台手机发送到电脑


## 开发背景
日常手机与电脑互发消息频率较多，使用微信或QQ来发消息步骤略显繁琐。

举例如手机查看的网页需发送电脑查看时传统步骤：
1.复制或分享链接    
2.选择QQ或微信打开  
3.QQ直接点击链接打开，微信还需复制链接到浏览器

使用Push To PC就可以减少以上步骤。电脑端启动pushToPC服务，在Android手机安装Push App，完成基本配置（配置教程在下面）后
。在浏览器中点分享，选择Push，电脑就会自动使用默认浏览器打开网页。

以上的痛点在手机厂商推出的[跨屏联网](https://www.36kr.com/p/1384344509332613)方案得以改善，但有所限制，如只支持部分手机或自家笔记本等。

## 开发技术
电脑端使用固定端口作为服务端，基于局域网的socket编程实现信息交互


## 已知问题
受限于作者的开发水平，软件还有许多未完善的地方。如使用固定端口、传输内容未加密会存在安全性问题，除了局域网内有人主动攻击，这个问题对于多数的场景下是安全的

## 建议反馈
欢迎在兔小槽建议反馈
[https://support.qq.com/products/405982](https://support.qq.com/products/405982)

## 免责声明
- 软件所有代码开源，不连互联网，仅在局域网内使用，不收集个人信息
- 软件使用固定端口、传输内容未加密会存在安全性问题。因使用软件造成信息泄露等，作者不负任何责任

## Windows软件代码
[软件源码](https://gitee.com/ishare20/msglistener/blob/master/pushToPCServer.cs)