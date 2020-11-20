=====================
列表:list 
=====================

我们开始学习什么是python的列表，先思考一个问题，有一个人的姓名(TOM)，在程序内如何储存？

答：使用变量进行储存。

思考：如果一个班级100位学生，每个人的姓名都要存储，应该如何书写程序？声明100个变量吗？

答：列表即可， 一个列表变量，可以一次性存储多个数据。

那么列表是怎样储存数据的呢？
列表储存数据的方式是： ``[数据1, 数据2, 数据3, 数据4......]`` 类似于这样，把一系列数据放到一个中括号里面，并用逗号隔开。
列表可以一次性存储多个数据，且可以为不同数据类型。我们可以对这些数据进行的操作有：增、删、改、查。

------------------------------
列表的创建
------------------------------

我们用一对中括号``[]``来创建一个python列表。零个，一个或一系列数据用逗号隔开，放在方括号[ ]内就是一个列表对象。
具体做法是，只要把逗号分隔的不同的数据项使用方括号括起来即可。

.. code-block:: python

   list1 = ['苹果', '梨', '香蕉', '菠萝']
   list2 = [1, 2, 3, 4, 5 ]
   list3 = ["a", "b", "c", "d"]
   numbers_and_strings = ['Why', 'was', 6, 'afraid', 'of', 7,'because', 7, 8, 9]

从上面可以看出，列表可以存放数字，和字符串等数据类型，也可以混合存储。

------------------------
访问列表中的值
------------------------


对于一个储存了各种颜色的列表，我们如何访问其中的各个颜色呢？

我们通过索引的方式，访问具体的颜色：

.. code-block:: python

   list = ['red', 'green', 'blue', 'yellow', 'white', 'black']
   print(list[0])
   print(list[1])
   print(list[2])

与字符串的索引一样，列表索引从 0 开始，第二个索引是 1，依此类推。

通过索引列表可以进行截取、组合等操作。

.. image:: ../_static/c03/c03p02_i01_listindex.png

所以，上述程序的输出结果是：

.. code-block:: console

   red
   green
   blue

索引也可以从尾部开始计算，最后一个元素的索引为 -1，往前一位为 -2，以此类推。这样的话，各个元素的索引变为如下形式：

.. image:: ../_static/c03/c03p02_i02_listindexnegative.png

所以，按照反向索引方式，访问颜色列表的访问方式变为：

.. code-block:: python

   list = ['red', 'green', 'blue', 'yellow', 'white', 'black']
   print(list[-1])
   print(list[-2])
   print(list[-3])

以上实例输出结果：

.. code-block:: console

   black
   white
   yellow


---------------------------------
给列表添加元素
---------------------------------
 
 
**指定位置新增数据**

用insert()函数，向列表添加元素的方法： ``列表.insert(位置下标, 数据)``

实例：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.insert(1, 'xiaoming')   
   
   print(name_list)
   # 结果：['Tom', 'xiaoming', 'Lily', 'Rose']



---------------------------------
列表的修改
---------------------------------
 

**修改指定下标数据**

既然我们可以按照列表的下标，找到对应的列表内的元素，那么我们就可以对其进行修改：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list[0] = 'aaa'   

   print(name_list)
   # 结果：['aaa', 'Lily', 'Rose']




---------------------------------
删除列表内的元素
---------------------------------
 
*删除指定数据*

我们用del命令，对列表内的元素进行删除

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   del name_list[0]   
   
   print(name_list)
   # 结果：['Lily', 'Rose']

**清空列表**

我们用函数clear()来清空一个列表：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   
   name_list.clear()
   print(name_list) # 结果： []

------------------------
列表的常用函数
------------------------
 
 

**统计指定数据在列表中出现的次数**

我们用count()函数，来统计指定数据在当前列表中出现的次数：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   print(name_list.count('Lily'))  # 1


**获取列表长度**

我们用len()函数，获取一个列表的长度，即列表中数据的个数：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   print(len(name_list))  # 3

------------
思考与练习
------------

新建一个列表，里面存储自己的所有爱好。

------------
你学到了什么
------------
