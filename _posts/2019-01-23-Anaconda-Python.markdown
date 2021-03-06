---
layout: post
title:  "Anaconda"
date:   2019-01-23 15:32:49 +1200
categories: jekyll update
---
Python目前有两个主版本并存，这很让人苦恼。

虽然Python 3有许多优于Python 2的特性，但是Python 2的生态系统更为完善，支持的包更多。因为生态系统内部的依赖关系，许多软件包的运行说明会直接指定“仅适用于Python 2.7版本”。
所以，你会在不同的应用场景下切换这两种Python版本。

# 解决方法，安装虚拟环境。

在虚拟环境里，各种软件包的版本，都由你来指定。它们和系统默认Python环境是相互隔离的，因此互不干扰。

1. 进入终端环境，使用Anaconda的环境创建命令，一行代码就可以创建成功。

创建一个名为python34的环境，指定Python版本是3.4（不用管是3.4.x，conda会为我们自动寻找3.4.x中的最新版本）

`conda create --name python34 python=3.4`

2. 呼唤创建的虚拟环境

`source activate python34`



3. 激活后，会发现terminal输入的地方多了python34的字样，实际上，此时系统做的事情就是把默认2.7环境从PATH中去除，再把3.4对应的命令加入PATH
此时，输入

`python --version`

4. 用户安装的不同python环境都会被放在目录~/anaconda/envs下，可以在命令中运行
`conda info -e`
查看已安装的环境，当前被激活的环境会显示有一个星号或者括号。

5. 在当前环境运行下列命令，安装插件，在jupyter notebook中加入新设环境

`conda install nb_conda`

6. 然后在当前环境打开jupyter notebook

`jupyter notebook`



# Conda的包管理

Conda的包管理就比较好理解了，这部分功能与pip类似。

例如，如果需要安装scipy：

1. 安装scipy

conda install scipy

2. 卸载scipy
conda remove scipy

# 在当前环境下安装anaconda包集合

conda install anaconda

# 更新anaconda

conda update anaconda

# 更新python

conda update python
