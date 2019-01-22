---
layout: post
title:  "Anaconda"
date:   2018-01-23 15:32:49 +1200
categories: Learning Python
---
Python目前有两个主版本并存，这很让人苦恼。

虽然Python 3有许多优于Python 2的特性，但是Python 2的生态系统更为完善，支持的包更多。因为生态系统内部的依赖关系，许多软件包的运行说明会直接指定“仅适用于Python 2.7版本”。
所以，你会在不同的应用场景下切换这两种Python版本。

解决方法，安装虚拟环境。

在虚拟环境里，各种软件包的版本，都由你来指定。它们和系统默认Python环境是相互隔离的，因此互不干扰。

进入终端环境，使用Anaconda的环境创建命令，一行代码就可以创建成功。

conda create -n tfpy3 python=3
