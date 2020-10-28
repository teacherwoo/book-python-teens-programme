=====================
字符串
=====================

------------
目标
------------

- 认识字符串
- 学习下标操作
- 了解切片

------------------
认识字符串
------------------

字符串是 Python 中最常用的数据类型。我们一般使用引号来创建字符串。创建字符串很简单，只要为变量分配一个值即可。

.. code-block:: python

   a = 'hello world'
   b = "abcdefg"
   print(type(a))
   print(type(b))


注意:控制台显示结果为 ``<class 'str'>`` ， 即数据类型为str(字符串)。
创建一个字符串可以用单引号，双引号，也可以用一对三个单引号或者双引号创建一个字符串，这种字符串支撑换行。

一对引号字创建的符串：

.. code-block:: python

   name1 = 'Tom'
   name2 = "Rose"


用三个引号创建的字符串：

.. code-block:: python

   name3 = ''' Tom '''
   name4 = """ Rose """
   a = ''' i am Tom, 
           nice to meet you! '''
   
   b = """ i am Rose, 
           nice to meet you! """

思考：如果创建一个字符串 ``I'm Tom`` ?

.. code-block:: python

   c = "I'm Tom"
   d = 'I\'m Tom'

这里使用了反斜杠，反斜杠加字符的形式叫做``转义字符``，转义字符的目的是表达一些无法用字符表达的含义。

------------------
字符串的输入输出
------------------

字符串输出的方法，之前介绍过，使用print函数，向控制台终端，打印出你想看到的字符串：

.. code-block:: python

   print('hello world')   
   name = 'Tom'
   print('我的名字是%s' % name)
   print(f'我的名字是{name}')

那么字符串输入如何实现呢？
在Python中，使用``input()``函数，来接收用户的输入： 

.. code-block:: python

   >>> name=input('请输入名字：\n')
   请输入名字：
   woo
   >>> name
   'woo'

-------------
下标
-------------

“下标”又叫“索引”，就是编号。比如火车座位号，座位号的作用：按照编号快速找到对应的座位。
这个下表或者索引，类似数学数列中的编号。下标的作用即是，当我们使用字符串时，通过下标快速找到对应的数据。

比如，有一个字符串``name = "abcdef"``，我们如何快速的取到name这个字符串里面，不同位置对应的字符串呢?

.. code-block:: python

   name = "abcdef"   
   print(name[1])
   print(name[0])
   print(name[2])
 
注意：下标从``0``开始。

 
----------------------
字符串的修改
----------------------
 
**字符串替换**

所谓修改字符串，指的就是通过函数的形式修改字符串中的数据。
我们使用``replace()``函数，来实现对字符串的替换：

.. code-block:: python

   字符串序列.replace(旧子串, 新子串)

我们看一下例子：

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：hello world he itcast he itheima he Python
   print(mystr.replace('and', 'he'))
   # 结果：hello world he itcast he itheima he Python
   print(mystr.replace('and', 'he', 10))
   # 结果：hello world and itcast and itheima and Python
   print(mystr)
 




**capitalize()**

将字符串第一个字符转换成大写。

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：Hello world and itcast and itheima and python
   print(mystr.capitalize())


*注意*

capitalize()函数转换后，只字符串第一个字符大写，其他的字符全都小写。



**title()**

将字符串每个单词首字母转换成大写。

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：Hello World And Itcast And Itheima And Python
   print(mystr.title())


**lower()**

将字符串中大写转小写。

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：hello world and itcast and itheima and python
   print(mystr.lower())


**upper()**

将字符串中小写转大写。

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：HELLO WORLD AND ITCAST AND ITHEIMA AND PYTHON
   print(mystr.upper())



**lstrip()**

删除字符串左侧空白字符。

**rstrip()**

删除字符串右侧空白字符。


**strip()**

删除字符串两侧空白字符。

**ljust()**

返回一个原字符串左对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串。

*语法*

``字符串序列.ljust(长度, 填充字符)``


**rjust()**

返回一个原字符串右对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串，语法和ljust()相同。

**center()**

返回一个原字符串居中对齐,并使用指定字符(默认空格)填充至对应长度 的新字符串，语法和ljust()相同。


----------------------
常用操作:判断
----------------------
 


所谓判断即是判断真假，返回的结果是布尔型数据类型：True 或 False。

**startswith()**

检查字符串是否是以指定子串开头，是则返回 True，否则返回 False。如果设置开始和结束位置下标，则在指定范围内检查。

*语法*

``字符串序列.startswith(子串, 开始位置下标, 结束位置下标)``

*快速体验*

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python   "
   
   # 结果：True
   print(mystr.startswith('hello'))
   
   # 结果False
   print(mystr.startswith('hello', 5, 20))




**endswith()**

检查字符串是否是以指定子串结尾，是则返回 True，否则返回 False。如果设置开始和结束位置下标，则在指定范围内检查。

*语法*

``字符串序列.endswith(子串, 开始位置下标, 结束位置下标)``


*快速体验*

.. code-block:: python

   mystr = "hello world and itcast and itheima and Python"
   
   # 结果：True
   print(mystr.endswith('Python'))
   
   # 结果：False
   print(mystr.endswith('python'))
   
   # 结果：False
   print(mystr.endswith('Python', 2, 20))
 



**isalpha()**

如果字符串至少有一个字符并且所有字符都是字母则返回 True, 否则返回 False。

.. code-block:: python

   mystr1 = 'hello'
   mystr2 = 'hello12345'
   
   # 结果：True
   print(mystr1.isalpha())
   
   # 结果：False
   print(mystr2.isalpha())
 



**isdigit()**

如果字符串只包含数字则返回 True 否则返回 False。

.. code-block:: python

   mystr1 = 'aaa12345'
   mystr2 = '12345'
   
   # 结果： False
   print(mystr1.isdigit())
   
   # 结果：False
   print(mystr2.isdigit())
 



**isalnum()**

如果字符串至少有一个字符并且所有字符都是字母或数字则返 回 True,否则返回 False。

.. code-block:: python

   mystr1 = 'aaa12345'
   mystr2 = '12345-'
   
   # 结果：True
   print(mystr1.isalnum())
   
   # 结果：False
   print(mystr2.isalnum())
 



**isspace()**

如果字符串中只包含空白，则返回 True，否则返回 False。

.. code-block:: python

   mystr1 = '1 2 3 4 5'
   mystr2 = '     '
   
   # 结果：False
   print(mystr1.isspace())
   
   # 结果：True
   print(mystr2.isspace())




-------------
总结
-------------

- 下标

  - 计算机为数据序列中每个元素分配的从0开始的编号
  
- 切片： ``序列名[开始位置下标:结束位置下标:步长]``


- 常用操作方法

  - find()
  - index()









