=======================
安装使用pygame的模块
=======================

什么是Pygame？

Pygame是一个“游戏开发库” - 一组帮助程序员制作游戏的代码库。包含：

- 图形和动画
- 声音（包括音乐）
- 控制（键盘，鼠标，游戏手柄等）

Pygame已经存在很多时间了，许多优秀的程序员加入其中，把Pygame做得越来越好。

.. image:: ../_static/c04/c04p01_i01_pygamelogo.png

你可以从www.pygame.org下载Pygame，选择合适你的操作系统和合适的版本，然后安装就可以了。

当然，推荐大家用pip的方式安装pygame，输入 pip install pygame命令：

.. code-block:: console

   pip install pygame
   
通过上述命令，pygame模块就会被安装在当前的python解释器环境内。可以通过``pip list`` 命令进行查看,这个命令是列出已安装的包。

.. note::
   
   pip 是 Python 包管理工具，该工具提供了对Python 包的查找、下载、安装、卸载的功能。目前如果你在 python.org 下载最新版本的安装包，则是已经自带了该工具。 Python 3.4+ 以上版本都自带 pip 工具。

-----------------
使用pygame
-----------------

下面我们看一下pygame的第一个程序：

**如何启动pygame**

.. code-block:: python

   import pygame
   
   pygame.init() #模块初始化，任何pygame程序运行前，均需要初始化
   screen = pygame.display.set_mode((300,480)) #定义窗口大小为640*480

类似于第二章的math模块调用，本章是使用pygame模块进行简单的画图。
类似于之前引入math模块的方法：``import math`` 。
我们在这里也需要引入pygame模块：``import pygame`` 。
下一行的 ``pygame.init()`` 命令，是调用一个pygame程序模块下面的init函数。
含义是启动pygame，并“初始化”它的命令。实际上，在pygame支持库的下面，有一个init()函数，此函数是对整个pygame环境进行准备。
screen指的是游戏屏幕。

运行效果是：

.. image:: ../_static/c04/c04p01_i02_pygamestart.png

**如何停止pygame程序**

正确的设置停止pygame程序将在后面详细讲解。
现在阶段还不能正常停止pygame程序窗口，只能点击集成开发环境Thonny的关闭按钮来关闭程序：

.. image:: ../_static/c04/c04p01_i03_pygameclose.png

.. note::

   关于报错，现在我们很多知识还没有学习，所以暂时用上述的方法关闭pygame程序，到后面的章节会展开详细讲述如何使pygame程序不报错和如何正确关闭pygame程序。


------------
思考与练习
------------

安装pygame环境。

