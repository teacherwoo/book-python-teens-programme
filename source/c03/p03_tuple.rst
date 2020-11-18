=====================
元组:tuple 
=====================


什么是元组，元组就好像是使用圆括号的列表。

元组和列表的区别是，元组一旦创建，就不能再做任何的改动了。


-----------
定义元组
-----------

元组特点：定义元组使用``小括号`` ，且``逗号`` 隔开各个数据，数据可以是不同的数据类型。

.. code-block:: python

   # 多个数据元组
   t1 = (10, 20, 30)
   
   # 单个数据元组
   t2 = (10,)


注意：如果定义的元组只有一个数据，那么这个数据后面也好添加逗号，否则数据类型为唯一的这个数据的数据类型

.. code-block:: python

   t2 = (10,)
   print(type(t2))  # tuple
   
   t3 = (20)
   print(type(t3))  # int
   
   t4 = ('hello')
   print(type(t4))  # str




---------------------
元组的常见操作
---------------------

元组数据不支持修改，只支持查找，具体如下：

**按下标查找数据**

.. code-block:: python

   tuple1 = ('aa', 'bb', 'cc', 'bb')
   print(tuple1[0])  # aa

**获取元素个数**

统计元组中数据的个数，需要使用len()函数。

.. code-block:: python

   tuple1 = ('aa', 'bb', 'cc', 'bb')
   print(len(tuple1))  # 4


注意：元组内的直接数据如果修改则立即报错:

.. code-block:: python

   tuple1 = ('aa', 'bb', 'cc', 'bb')
   tuple1[0] = 'aaa'

.. code-block:: console

   TypeError: 'tuple' object does not support item assignment

------------
思考与练习
------------

新建一个元组，里面存储自己的所有课程。

------------
你学到了什么
------------
