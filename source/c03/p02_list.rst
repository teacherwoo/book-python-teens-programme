=====================
列表:list 
=====================

-------------
目标
-------------

- 学习使用列表
- 列表的格式
- 列表的常用操作
- 列表的循环遍历
- 列表的嵌套使用

------------------------------
什么是python的列表（list）
------------------------------

先思考一个问题，有一个人的姓名(TOM)，在程序内如何储存？

答：使用变量进行储存。

思考：如果一个班级100位学生，每个人的姓名都要存储，应该如何书写程序？声明100个变量吗？

答：列表即可， 一个列表变量，可以一次性存储多个数据。

那么列表是怎样储存数据的呢？列表储存数据的方式是：

``[数据1, 数据2, 数据3, 数据4......]``

列表可以一次性存储多个数据，且可以为不同数据类型。我们可以对这些数据进行的操作有：增、删、改、查。


------------------------------
列表的创建
------------------------------

我们用一对中括号``[]``来创建一个python列表。
零个，一个或一系列数据用逗号隔开，放在方括号[ ]内就是一个列表对象。具体做法是，只要把逗号分隔的不同的数据项使用方括号括起来即可。

.. code-block:: python

   list1 = ['苹果', '梨', '香蕉', '菠萝']
   list2 = [1, 2, 3, 4, 5 ]
   list3 = ["a", "b", "c", "d"]



------------------------
访问列表中的值
------------------------


与字符串的索引一样，列表索引从 0 开始，第二个索引是 1，依此类推。

通过索引列表可以进行截取、组合等操作。

.. image:: ../_static/c03/c03p02_i01_listindex.png

.. code-block:: python

   list = ['red', 'green', 'blue', 'yellow', 'white', 'black']
   print(list[0])
   print(list[1])
   print(list[2])

以上的输出结果是：

.. code-block:: console

   red
   green
   blue

索引也可以从尾部开始，最后一个元素的索引为 -1，往前一位为 -2，以此类推。

.. image:: ../_static/c03/c03p02_i02_listindexnegative.png

反向访问的代码是：

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



------------------------
列表的常用函数
------------------------
 
 

**count()**

统计指定数据在当前列表中出现的次数。

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   print(name_list.count('Lily'))  # 1


**len()**

访问列表长度，即列表中数据的个数。

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   print(len(name_list))  # 3





---------------------------------
列表操作：增加成员
---------------------------------
 

作用：增加指定数据到列表中。

**append()**

列表结尾追加数据。

1. 语法： ``列表序列.append(数据)``

2. 体验

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.append('xiaoming')
   
   # 结果：['Tom', 'Lily', 'Rose', 'xiaoming']
   print(name_list)
 
列表追加数据的时候，直接在原列表里面追加了指定数据，即修改了原列表，故列表为可变类型数据。

3. 注意点

如果append()追加的数据是一个序列，则追加整个序列到列表

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.append(['xiaoming', 'xiaohong'])
   
   # 结果：['Tom', 'Lily', 'Rose', ['xiaoming', 'xiaohong']]
   print(name_list)


**extend()**

列表结尾追加数据，如果数据是一个序列，则将这个序列的数据逐一添加到列表。

*语法*

``列表序列.extend(数据)``

*扩展单个数据*

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.extend('xiaoming')
   
   # 结果：['Tom', 'Lily', 'Rose', 'x', 'i', 'a', 'o', 'm', 'i', 'n', 'g']
   print(name_list)


*扩展序列数据*

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.extend(['xiaoming', 'xiaohong'])
   
   # 结果：['Tom', 'Lily', 'Rose', 'xiaoming', 'xiaohong']
   print(name_list)


**insert()**

指定位置新增数据。

1. 语法： ``列表序列.insert(位置下标, 数据)``

2. 快速体验

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list.insert(1, 'xiaoming')
   
   # 结果：['Tom', 'xiaoming', 'Lily', 'Rose']
   print(name_list)



---------------------------------
列表操作：删除元素
---------------------------------
 
*删除指定数据*

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   
   del name_list[0]
   
   # 结果：['Lily', 'Rose']
   print(name_list)

**清空列表**

我们用函数clear()来清空一个列表：

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   
   name_list.clear()
   print(name_list) # 结果： []


---------------------------------
列表的常用操作
---------------------------------
 

**修改指定下标数据**

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']   
   name_list[0] = 'aaa'
   
   # 结果：['aaa', 'Lily', 'Rose']
   print(name_list)


 


**排序：sort()**

*语法*

``列表序列.sort( key=None, reverse=False)``

注意：reverse表示排序规则，**reverse = True** 降序， **reverse = False** 升序（默认）

*快速体验*

.. code-block:: python

   num_list = [1, 5, 2, 3, 6, 8]
   
   num_list.sort()
   
   # 结果：[1, 2, 3, 5, 6, 8]
   print(num_list)








--------------------
列表嵌套
--------------------

所谓列表嵌套指的就是一个列表里面包含了其他的子列表。

应用场景：要存储班级一、二、三三个班级学生姓名，且每个班级的学生姓名在一个列表。

.. code-block:: python

   name_list = [['小明', '小红', '小绿'], ['Tom', 'Lily', 'Rose'], ['张三', '李四', '王五']]


思考： 如何查找到数据"李四"？

.. code-block:: python

   # 第一步：按下标查找到李四所在的列表
   print(name_list[2])
   
   # 第二步：从李四所在的列表里面，再按下标找到数据李四
   print(name_list[2][1])

-----------------------------
跟字符串相关的列表操作
-----------------------------


**字符串的切割**

我们可以使用``split()``函数，来实现按照指定字符分割字符串。

``字符串序列.split(分割字符, num)``

下面来看一下实例：

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"   
   
   print(mystr.split('and'))
   # 结果：['hello world ', ' itcast ', ' itheima ', ' Python']
   
   print(mystr.split(' '))
   # 结果：['hello', 'world', 'and', 'itcast', 'and', 'itheima', 'and', 'Python']
 

根据上面的例子我们可以看到，如果分割字符是原有字符串中的子串，分割后则丢失该子串。

**join()**

用一个字符或子串合并字符串，即是将多个字符串合并为一个新的字符串。

*语法*

``字符或子串.join(多字符串组成的序列)``


*快速体验*

.. code-block:: python

   list1 = ['chuan', 'zhi', 'bo', 'ke']
   t1 = ('aa', 'b', 'cc', 'ddd')
   # 结果：chuan_zhi_bo_ke
   print('_'.join(list1))
   # 结果：aa...b...cc...ddd
   print('...'.join(t1))










 




