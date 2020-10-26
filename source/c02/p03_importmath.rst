===========================
使用math包进行简单科学计算
===========================

--------------
目标
--------------

- 了解如何引用python支持包，学会引入python支持包。
- 了解math包
- 进行简单的数学计算


----------------------
什么是pyton模块
----------------------

Python 模块(Module)，也叫支持包，是一个 Python 文件，以 .py 结尾，包含了 Python 对象定义和Python语句。

模块能定义函数，类和变量，模块里也能包含可执行的代码。

------------------------------------------
以math包为例，学习如何引入和使用python模块
------------------------------------------

math包是python的数学包，一些数学函数常用程序，包含在这个包内。
下面我们就利用math包，来说明如何引入包和使用包。

导入模块的方式：

   - import 模块名
   - from 模块名 import 功能名
   - from 模块名 import *
   - import 模块名 as 别名
   - from 模块名 import 功能名 as 别名



**方式一：import方式**

语法

.. code-block:: python

   # 1. 导入模块
   import 模块名
   import 模块名1, 模块名2...
   
   # 2. 调用功能
   #模块名.函数名()


体验math包调用，我们调用math包的取绝对值函数fabs()，对一个负数取绝对值计算：

.. code-block:: python

   >>> import math
   >>> print(math.fabs(-100))
   100.0

**方式二：from..import..方式**

语法： 

.. code-block:: python

   from 模块名 import 功能1, 功能2, 功能3... 

体验

.. code-block:: python

   >>> from math import fabs
   >>> print(fabs(-100))
   100.0

**方式三：from .. import * 方式**

语法： 

.. code-block:: python

   from 模块名 import *

此处的星号，代表任意名称。

体验

.. code-block:: python

   from math import *
   print(fabs(-100))
 

**方式四：用 as 定义别名的方式**

语法

.. code-block:: python

   # 模块定义别名
   import 模块名 as 别名
   
   # 功能定义别名
   from 模块名 import 功能 as 别名


体验：

.. code-block:: python

   >>> import math as m
   >>> print(m.fabs(-100))
   100.0
   
   >>> from math import fabs as abs
   >>> print(abs(-100))
   100.0





------------
你学到了什么
------------








