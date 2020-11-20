======================
调用其他包内的函数
======================

同一文件夹下的调用调用函数，针对一个模块的函数调用

第一种： import 模块名
模块名.函数名

第二种： from 模块名 import 函数名 （as 别名）
python调用另一个.py文件中的类和函数

我们有两个python文件，一个是A.py一个是B.py。

A.py文件如下：

.. code-block:: python

   def add(x,y):
      print('和为：%d'%(x+y))

在B.py文件中调用A.py的add函数如下：

.. code-block:: python

   import A
   A.add(1,2)

或

.. code-block:: python

   from A import add
   add(1,2)

以上内容，就是实现了对其他包内的函数进行调用。



