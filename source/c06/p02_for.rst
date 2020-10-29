===================
循环语句
===================
 
-----------
目标
-----------

- 了解循环
- for循环

--------------
循环简介
--------------

**循环的作用**

思考：假如我有个女朋友，有一天我们闹矛盾生气了，女朋友说：道歉，说100遍“媳妇儿，我错了”。这个时候程序员会怎么做？

答：100遍`print('媳妇儿，我错了')`

思考：复制粘贴100次吗？

答：重复执行100次一样的代码，程序中循环即可

循环的作用：让代码更高效的重复执行。


**循环的分类**

在Python中，循环分为`while`和`for`两种，最终实现效果相同。


--------------------
列表的循环遍历
--------------------

需求：依次打印列表中的各个数据。

**while**

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   
   i = 0
   while i < len(name_list):
       print(name_list[i])
       i += 1


 

**for**

.. code-block:: python

   name_list = ['Tom', 'Lily', 'Rose']
   
   for i in name_list:
       print(i)
       


----------------------
字典的循环遍历
----------------------

**遍历字典的key**

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   for key in dict1.keys():
       print(key)

 


**遍历字典的value**

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   for value in dict1.values():
       print(value)

 


**遍历字典的元素**

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   for item in dict1.items():
       print(item)


**遍历字典的键值对**

.. code-block:: python

   dict1 = {'name': 'Tom', 'age': 20, 'gender': '男'}
   for key, value in dict1.items():
       print(f'{key} = {value}')

 
 

---------------
for循环
---------------

**语法**

.. code-block:: python

   for 临时变量 in 序列:
      #重复执行的代码1
      #重复执行的代码2
      #......
 

**快速体验**

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
      print(i)


 
**break**

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
       if i == 'e':
           print('遇到e不打印')
           break
       print(i)
 
 
**continue**

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
       if i == 'e':
           print('遇到e不打印')
           continue
       print(i)
 
 

**退出循环的方式**

需求：女朋友生气，要求道歉5遍：媳妇儿，我错了。
道歉到第三遍的时候，媳妇埋怨这一遍说的不真诚，是不是就是要退出循环了？
这个退出有两种可能性：

   - 更生气，不打算原谅，也不需要道歉了，程序如何书写？
   - 只一遍不真诚，可以忍受，继续下一遍道歉，程序如何书写？

**break**

.. code-block:: python

   i = 1
   while i <= 5:
       if i == 3:
           print('这遍说的不真诚')
           break
       print('媳妇儿，我错了')
       i += 1
   else:
       print('媳妇原谅我了，真开心，哈哈哈哈')



> 所谓else指的是循环正常结束之后要执行的代码，即如果是break终止循环的情况，else下方缩进的代码将不执行。

**continue**

.. code-block:: python

   i = 1
   while i <= 5:
       if i == 3:
           print('这遍说的不真诚')
           i += 1
           continue
       print('媳妇儿，我错了')
       i += 1
   else:
       print('媳妇原谅我了，真开心，哈哈哈哈')


 
因为continue是退出当前一次循环，继续下一次循环，所以该循环在continue控制下是可以正常结束的，当循环结束后，则执行了else缩进的代码。

-----------------
for...else
-----------------

**语法**

.. code-block:: python

   for 临时变量 in 序列:
      #重复执行的代码
       ...
   else:
      #循环正常结束之后要执行的代码


所谓else指的是循环正常结束之后要执行的代码，即如果是break终止循环的情况，else下方缩进的代码将不执行。

**示例**

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
       print(i)
   else:
       print('循环正常结束之后执行的代码')


**退出循环的方式**

*break终止循环*

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
       if i == 'e':
           print('遇到e不打印')
           break
       print(i)
   else:
       print('循环正常结束之后执行的代码')



没有执行else缩进的代码。

*continue控制循环*

.. code-block:: python

   str1 = 'itheima'
   for i in str1:
       if i == 'e':
           print('遇到e不打印')
           continue
       print(i)
   else:
       print('循环正常结束之后执行的代码')

 

因为continue是退出当前一次循环，继续下一次循环，所以该循环在continue控制下是可以正常结束的，当循环结束后，则执行了else缩进的代码。



---------
总结
---------

- 循环的作用：控制代码重复执行
- while语法

.. code-block:: python

   while 条件:
      #条件成立重复执行的代码1
      #条件成立重复执行的代码2
      #......


- while循环嵌套语法

.. code-block:: python

   while 条件1:
      #条件1成立执行的代码
      #......
      while 条件2:
         #条件2成立执行的代码
         #......


- for循环语法

.. code-block:: python

   for 临时变量 in 序列:
      #重复执行的代码1
      #重复执行的代码2
      #......


- break退出整个循环
- continue退出本次循环，继续执行下一次重复执行的代码
- else

  + while和for都可以配合else使用
  + else下方缩进的代码含义：当循环正常结束后执行的代码
  + break终止循环不会执行else下方缩进的代码
  + continue退出循环的方式执行else下方缩进的代码
 
 
 