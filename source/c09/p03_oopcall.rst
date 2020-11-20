=======================
调用其他包里面的类
=======================

同一文件夹下的调用调用其他包的类，有两个python文件A和B

A.py文件如下:

.. code-block:: python

   class M:
       def __init__(self,xx,yy):
           self.x=xx
           self.y=yy
       def add(self):
           print("x和y的和为：%d"%(self.x+self.y))

在B.py文件中调用A.py的add函数如下：

.. code-block:: python

   from A import M
   m=M(2,3)
   m.add()

或 

.. code-block:: python

   import A
   m=A.M(2,3)
   m.add()

以上内容，就是实现了对其他包内的类进行调用。





 