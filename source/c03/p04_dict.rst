=====================
字典:dict 
=====================

--------
目标
--------

- 创建字典的语法
- 字典常见操作
- 字典的循环遍历

------------------
什么是字典
------------------

python中的字典是dict，是单词dictionary的缩写。是Python 提供的一种常用的数据结构，它用于存放具有映射关系的数据。

比如有份成绩表数据，语文：79，数学：80，英语：92，这组数据看上去像两个列表，但这两个列表的元素之间有一定的关联关系。
如果单纯使用两个列表来保存这组数据，则无法记录两组数据之间的关联关系。

为了保存具有映射关系的数据，Python 提供了字典，字典相当于保存了两组数据，
其中一组数据是关键数据，被称为 key；另一组数据可通过 key 来访问，被称为 value。
形象地看，字典中 key 和 value 的关联关系如图所示：

.. image:: ../_static/c03/c03p04_i01_dict.png

由于字典中的 key 是非常关键的数据，而且程序需要通过 key 来访问 value，因此字典中的 key 不允许重复。



--------------------
如何创建字典
--------------------

程序既可使用花括号语法来创建字典，也可使用 dict() 函数来创建字典。
在使用花括号语法创建字典时，花括号中应包含多个 key-value 对，key 与 value 之间用英文冒号隔开；多个 key-value 对之间用英文逗号隔开。

字典创建的特点：

   - 符号为大括号
   - 数据为键值对形式出现
   - 各个键值对之间用逗号隔开

如下代码示范了使用花括号语法创建字典： 

.. code-block:: python
        
   scores = {'语文': 89, '数学': 92, '英语': 93}
   print(scores)
   
   # 空的花括号代表空的字典
   empty_dict = {}
   print(empty_dict)
   
   # 使用元组作为dict的key
   dict2 = {(20, 30):'good', 30:'bad'}
   print(dict2)  
 
注意：一般称冒号前面的为键(key)，简称k；冒号后面的为值(value)，简称v。
需要指出的是，元组可以作为 dict 的 key，但列表不能作为元组的 key。这是由于 dict 要求 key 必须是不可变类型，但列表是可变类型，因此列表不能作为元组的 key。


----------------
字典常见操作
----------------

**增**

写法： ``字典序列[key] = 值``

注意：如果key存在则修改这个key对应的值；如果key不存在则新增此键值对。
 

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   
   dict1['name'] = 'Rose'
   # 结果：{'name': 'Rose', 'age': 20, 'gender': '男'}
   print(dict1)
   
   dict1['id'] = 110
   
   # {'name': 'Rose', 'age': 20, 'gender': '男', 'id': 110}
   print(dict1)


注意：字典为可变类型。



**删**

*del() / del*

删除字典或删除字典中指定键值对。

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   
   del dict1['gender']
   # 结果：{'name': 'Tom', 'age': 20}
   print(dict1)




*清空字典*

用clear()函数清空一个字典。


.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   
   dict1.clear()
   print(dict1)  # {}


**改**

写法：``字典序列[key] = 值``

注意：如果key存在则修改这个key对应的值 ；如果key不存在则新增此键值对。

**查**

*key值查找*

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   print(dict1['name'])  # Tom
   print(dict1['id'])  # 报错


如果当前查找的key存在，则返回对应的值；否则则报错。



*get()*

- 语法: ``字典序列.get(key, 默认值)``

注意：如果当前查找的key不存在则返回第二个参数(默认值)，如果省略第二个参数，则返回None。

- 快速体验

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   print(dict1.get('name'))  # Tom
   print(dict1.get('id', 110))  # 110
   print(dict1.get('id'))  # None


*keys()*

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   print(dict1.keys())  # dict_keys(['name', 'age', 'gender'])




*values()*

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   print(dict1.values())  # dict_values(['Tom', 20, '男'])




*items()*

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   print(dict1.items())  # dict_items([('name', 'Tom'), ('age', 20), ('gender', '男')])




 
