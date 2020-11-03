=======================
阶段实例
=======================

----------
目标
----------
 

使用面向对象，简化代码。
此时可以开发复杂实例。





  
 
-----------------
综合应用:烤地瓜
-----------------

**需求**

需求主线：

 1. 被烤的时间和对应的地瓜状态：

    0-3分钟：生的

    3-5分钟：半生不熟

    5-8分钟：熟的

    超过8分钟：烤糊了

    

 2. 添加的调料：

    用户可以按自己的意愿添加调料

    

**步骤分析**

需求涉及一个事物： 地瓜，故案例涉及一个类：地瓜类。

定义类

- 地瓜的属性

  - 被烤的时间
  - 地瓜的状态
  - 添加的调料
  
- 地瓜的方法

  - 被烤
  
    - 用户根据意愿设定每次烤地瓜的时间
    - 判断地瓜被烤的总时间是在哪个区间，修改地瓜状态
    
  - 添加调料
  
    - 用户根据意愿设定添加的调料
    - 将用户添加的调料存储

- 显示对象信息


创建对象，调用相关实例方法



**代码实现**

定义类

- 地瓜属性

  - 定义地瓜初始化属性，后期根据程序推进更新实例属性

.. code-block:: python

   class SweetPotato():
       def __init__(self):
           # 被烤的时间
           self.cook_time = 0
           # 地瓜的状态
           self.cook_static = '生的'
           # 调料列表
           self.condiments = []
 


定义烤地瓜方法

.. code-block:: python

   class SweetPotato():
       ......
       
       def cook(self, time):
           """烤地瓜的方法"""
           self.cook_time += time
           if 0 <= self.cook_time < 3:
               self.cook_static = '生的'
           elif 3 <= self.cook_time < 5:
               self.cook_static = '半生不熟'
           elif 5 <= self.cook_time < 8:
               self.cook_static = '熟了'
           elif self.cook_time >= 8:
               self.cook_static = '烤糊了'
 

书写str魔法方法，用于输出对象状态

.. code-block:: python

   class SweetPotato():
      #......
   
      def __str__(self):
         return f'这个地瓜烤了{self.cook_time}分钟, 状态是{self.cook_static}'


创建对象，测试实例属性和实例方法

.. code-block:: python

   digua1 = SweetPotato()
   print(digua1)
   digua1.cook(2)
   print(digua1)


定义添加调料方法，并调用该实例方法

.. code-block:: python

   class SweetPotato():
         ......
   
       def add_condiments(self, condiment):
           """添加调料"""
           self.condiments.append(condiment)
       def __str__(self):
           return f'这个地瓜烤了{self.cook_time}分钟, 状态是{self.cook_static}, 添加的调料有{self.condiments}'
         
   
   digua1 = SweetPotato()
   print(digua1)
   
   digua1.cook(2)
   digua1.add_condiments('酱油')
   print(digua1)
   
   digua1.cook(2)
   digua1.add_condiments('辣椒面儿')
   print(digua1)
   
   digua1.cook(2)
   print(digua1)
   
   digua1.cook(2)
   print(digua1)
 

**代码总览**

.. code-block:: python

   # 定义类
   class SweetPotato():
       def __init__(self):
           # 被烤的时间
           self.cook_time = 0
           # 地瓜的状态
           self.cook_static = '生的'
           # 调料列表
           self.condiments = []
   
       def cook(self, time):
           """烤地瓜的方法"""
           self.cook_time += time
           if 0 <= self.cook_time < 3:
               self.cook_static = '生的'
           elif 3 <= self.cook_time < 5:
               self.cook_static = '半生不熟'
           elif 5 <= self.cook_time < 8:
               self.cook_static = '熟了'
           elif self.cook_time >= 8:
               self.cook_static = '烤糊了'
   
       def add_condiments(self, condiment):
           """添加调料"""
           self.condiments.append(condiment)
   
       def __str__(self):
           return f'这个地瓜烤了{self.cook_time}分钟, 状态是{self.cook_static}, 添加的调料有{self.condiments}'
   
   
   digua1 = SweetPotato()
   print(digua1)
   
   digua1.cook(2)
   digua1.add_condiments('酱油')
   print(digua1)
   
   digua1.cook(2)
   digua1.add_condiments('辣椒面儿')
   print(digua1)
   
   digua1.cook(2)
   print(digua1)
   
   digua1.cook(2)
   print(digua1)


-----------------
综合应用:搬家具
-----------------
 

**需求**

将小于房子剩余面积的家具摆放到房子中



**步骤分析**

需求涉及两个事物：房子 和 家具，故被案例涉及两个类：房子类 和 家具类。

定义类

- 房子类
  - 实例属性
    - 房子地理位置
    - 房子占地面积
    - 房子剩余面积
    - 房子内家具列表
  - 实例方法
    - 容纳家具
  - 显示房屋信息



- 家具类
  - 家具名称
  - 家具占地面积

创建对象并调用相关方法



**代码实现**

定义类

家具类

.. code-block:: python

   class Furniture():
       def __init__(self, name, area):
           # 家具名字
           self.name = name
           # 家具占地面积
           self.area = area
    



房子类

.. code-block:: python

   class Home():
       def __init__(self, address, area):
           # 地理位置
           self.address = address
           # 房屋面积
           self.area = area
           # 剩余面积
           self.free_area = area
           # 家具列表
           self.furniture = []
   
       def __str__(self):
           return f'房子坐落于{self.address}, 占地面积{self.area}, 剩余面积{self.free_area}, 家具有{self.furniture}'
   
       def add_furniture(self, item):
           """容纳家具"""
           if self.free_area >= item.area:
               self.furniture.append(item.name)
               # 家具搬入后，房屋剩余面积 = 之前剩余面积 - 该家具面积
               self.free_area -= item.area
           else:
               print('家具太大，剩余面积不足，无法容纳')
 



创建对象并调用实例属性和方法

.. code-block:: python

   bed = Furniture('双人床', 6)
   jia1 = Home('北京', 1200)
   print(jia1)
   
   jia1.add_furniture(bed)
   print(jia1)
   
   sofa = Furniture('沙发', 10)
   jia1.add_furniture(sofa)
   print(jia1)
   
   ball = Furniture('篮球场', 1500)
   jia1.add_furniture(ball)
   print(jia1)




------------
总结
------------

- 面向对象重要组成部分

   - 创建类:  ``class 类名():``
   - 创建对象:  ``对象名 = 类名()``

- 添加对象属性

   - 类外面:  ``对象名.属性名 = 值  ```
   - 类里面:  ``self.属性名 = 值``

- 获取对象属性

   - 类外面:  ``对象名.属性名``
   - 类里面:  ``self.属性名``

- 魔法方法

   - ``__init__()`` : 初始化
   - ``__str__()`` :输出对象信息
   - ``__del__()`` :删除对象时调用






 