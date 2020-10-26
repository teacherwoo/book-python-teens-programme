=======================
Python集成开发环境准备
=======================

------------
目标
------------

- 了解什么是IDE
- 常用IDE介绍
- 学习和使用

------------
什么是IDE
------------

集成开发环境（IDE，Integrated Development Environment ）是用于提供程序开发环境的应用程序，一般包括代码编辑器、编译器、调试器和图形用户界面等工具。
集成了代码编写功能、分析功能、编译功能、调试功能等一体化的开发软件服务套。所有具备这一特性的软件或者软件套（组）都可以叫集成开发环境。

常用的python集成开发环境很多，专业用户经常使用pycharm和pydev。对初学者来说，thonny比较简洁高效。

--------------
下载thonny
--------------

`[Thonny—— https://thonny.org/] <https://thonny.org/>`_

.. image:: ../_static/c01/c01p03_i01_thonnydownload.png
 

--------
安装
--------

下载后，双击安装包，按照下述步骤进行安装。

.. image:: ../_static/c01/c01p03_i02_thonnyinstall.png

.. image:: ../_static/c01/c01p03_i03_thonnyinstall2.png

.. image:: ../_static/c01/c01p03_i04_thonnyinstall3.png

.. image:: ../_static/c01/c01p03_i05_thonnyinstall4.png

--------------------------------
设置Thonny编辑器的语言为中文
--------------------------------

在Thonny首次运行时，可以设置语言.
如果错过了设置，也可以在的设置内，可以设置整个编辑器的语言为中文。
在菜单栏内选择Tools选项：

.. image:: ../_static/c01/c01p03_i06_setting.png

打开Option选项，打开设置窗口，在Language下拉选择框内，选择简体中文选项：

.. image:: ../_static/c01/c01p03_i07_setting2.png

点击OK按钮确认设置，然后重启Thonny编辑器，即可设置编辑器为中文。

----------------------------
Thonny编辑器的基本使用
----------------------------

接着，即可开始使用Thonny进行编程开发了。

**创建python文件**

点击 “文件” 选择“新文件”，这时，tab页编辑区，就打了一个新的待编辑python文件。

编辑第一个python程序，并保存为first.py，python文件都是以py为后缀结尾。

双击打开文件，并书写一个最简单的helloworld代码：

.. code-block:: python

   print("hello world")

点击绿色的运行按钮，或者点击快捷键‘F5’，运行这个python程序。运行效果会出现在Shell区域。
下面是运行效果：

.. image:: ../_static/c01/c01p03_i08_helloworld.png

print是打印函数。在python中，调用函数的方式是函数名称加括号。此段程序命令的含义，是在终端中，打印出字符串``hello world``。

**载入python文件**

那么程序的特点是什么？
程序的特点是一次编写，多处使用。
所以，程序编辑完成后，需要进行打开操作，并可以再次执行。

点击 “文件” 选择“打开”，这时，会打开文件选择对话框，从里面选择我们要进行编辑的python文件，打开后，就可以进行再次编辑。


------------
你学到了什么
------------

- 什么是集成开发环境
- Thonny环境如何安装
- Thonny环境如何开发第一个python程序

 

   
 
