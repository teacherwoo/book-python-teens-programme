===============================
对象的初始化
===============================

-----------
目标
-----------

- 理解面向对象
- 类和对象
- 添加和获取对象属性
- 魔法方法


-------------------
首先看一下self
-------------------
 
在类的定义时self指的是，改类被实例化之后的对象。
比如说，有个类叫做“人类”，那么self就是指“某人”，就是隶属于这个类的具体的某个对象。

比如下面的例子，洗衣工类在实例化的时候，self就被指定为具体的某个洗衣工人。

.. code-block:: python

   class Washer():
      def wash(self):
          print('我洗衣服')
          print(self)
     
   haier1 = Washer()
   print(haier1)
   haier1.wash()
     
   haier2 = Washer()
   print(haier2)
   haier2.wash()

注意：打印对象和self得到的结果是一致的，都是当前对象的内存中存储地址。



-----------------------
添加和获取对象属性
-----------------------


当我们创建对象时，我们会提前设置一些值，以便后续使用。属性即是特征，比如：一个事物的宽度、高度、重量...这些与生俱来的属性。
想要达到这一点，我们需要用到``__init__``函数，这个函数的开头和结尾都是双下划线。
比方说，我们创建一个长颈鹿类的对象时，我们可以预先设置他的名字和高度：

.. code-block:: python

   class Giraffes():
       def __init__(self,name,height):
           self.name=name
           self.height=height
 
这样，我们在创造这个长颈鹿对象的时候，我们就可以给他命名和设置高度：

.. code-block:: python
      
   jack=Giraffes('杰克',10)
   rose=Giraffes('罗丝',8)
           
   print(jack.name,jack.height)  
   print(rose.name,rose.height)          
        






 