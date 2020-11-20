===============================
设置对象属性
===============================

当我们表述下列一段话：所有的人都有一个名字，这个人叫什么名字？

我们针对这句话，用面向对象程序设计的思想来看，所有的人就是指人类，那么这个人就是人类的一个对象实例。
那么，当我们定义人类这个类的过程中，我们需要使用“这个人”的概念，意思就是人类这个类的一个实例。
在python中，这个人就用self来指代。

-------------------
首先看一下self
-------------------
 
在类的定义时self指的是，改类被实例化之后的对象。
比如说，有个类叫做“人类”，那么self就是指“某人”，就是隶属于这个类的具体的某个对象。
比如下面的例子，程序定义了一个洗衣工类，这个类在实例化的时候，self就被指定为具体的某个洗衣工人。

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

------------------------
用类存储数据
------------------------

类实际上就是一个数据结构，对于python而言，它是一个类似于字典的结构。
当根据类创建了对象之后，这个对象就有了一个数据结构，包含一些赋值了的属性。
在这一点上，它和dict的作用是类似的：存储数据并提供数据检索功能。
例如，下面是最简单的类：

.. code-block:: python

   class Person: 
      pass

pass关键字表示这个类没有实际的逻辑体。
这里只是定义了一个类，这个类的对象初始化时不会存放任何数据。
现在，构造一个对象，让它和dict一样存放一些数据：

.. code-block:: python

   p = Person()    # 构造对象
   p.name = "张三"  # 创建对象的属性name
   p.age = 16            # 创建对象的属性age

现在，Person的实例对象p中就存放了两个属性：p.name和p.age。可以直接去检索存放在p中的数据：

.. code-block:: python

   print(p.name)  # 输出"张三"
   print(p.age)   # 输出16


换一种形式，也可以使用dict来存储这些数据：

.. code-block:: python

   >>> d={}
   >>> d["name"]="张三"
   >>> d["age"]=16
   
   >>> print(d["name"])
   张三
   >>> print(d["age"])
   16

在数据存储方面，它们的作用是完全等价的。实际上对象/类在内部就是使用一个名为__dict__的dict类型来存放它所拥有的数据的。

.. code-block:: python

   >>> p.__dict__
   {'name': '张三', 'age': 16}

---------------------------------
__init__()构造对象初始数据
---------------------------------

上面的name和age属性是在构建了对象之后附加上去的。
如果想要创建对象时就存放好数据，可以定义类的构造函数__init__()。例如：

.. code-block:: python

   class Person:
       def __init__(self,name,age):
           self.name = name
           self.age = age

然后创建对象的时候，传递name参数和age参数即可。

.. code-block:: python

   >>> p = Person("张三",16)
   >>> p.__dict__
   {'name': '张三', 'age': 16}
   >>> print(p.__dict__['age'])
   16

如果想定义这个类公有的数据，可以将公有属性定义为类的属性。比如中国人都是黄皮肤：

.. code-block:: python

   class Person:
       skin = "yellow"
       def __init__(self,name,age):
           self.name = name
           self.age = age

这样每次创建Person的对象实例时，每个对象都会有相同的肤色：yellow。
但注意，这个skin属性是类属性，不是对象属性，它是存放在类的名称空间中的。
当对象真的需要这个属性的时候，会临时去检索类的名称空间来获取。
看下面的__dict__字典即可知道：

.. code-block:: python

   >>> p = Person("longshuai",23)
   >>> p.__dict__
   {'name': 'longshuai', 'age': 23}
   >>> p.skin
   'yellow'

也就是说，类变量没有放到对外的dict立面。
但注意，如果我们强行把类属性加上self进行定义，会报错：NameError: name 'self' is not defined
那python为什么会支持这种方式呢？
按照面向对象的封装原则，在类中定义类变量的目的不是对外，是给本类中计算时使用的一些常量或者是某些类内函数都要用到的公用属性。
因为要在外部访问它需要通过x.y的方式，这意味着打开了封装好的"黑匣子"，暴露了类属性。
除非真的有需要，否则最好将类变量的定义放进构造函数__init__()中。

------------
思考与练习
------------

------------
你学到了什么
------------
