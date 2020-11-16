=======================
阶段实例
=======================


--------------
函数应用
--------------

**函数计算**

1. 求三个数之和

.. code-block:: python

   def sum(a, b, c):
       return a + b + c
   
   
   result = sum(1, 2, 3)
   print(result)  # 6




2. 求三个数平均值

.. code-block:: python

   def average(a, b, c):
       sumResult = sum(a, b, c)
       return sumResult / 3
   
   result = average(1, 2, 3)
   print(result)  # 2.0




--------------------
一元二次方程
--------------------

.. math::

   \text{一元二次方程：}{a\mathop{{x}}\nolimits^{{2}}+bx+c=0}\text{的两根为：}\\
   \mathop{{x}}\nolimits_{{1}}=\frac{{-b+\sqrt{{\mathop{{b}}\nolimits^{{2}}-4ac}}}}{{2a}}\\
   \mathop{{x}}\nolimits_{{2}}=\frac{{-b-\sqrt{{\mathop{{b}}\nolimits^{{2}}-4ac}}}}{{2a}}

   x ={-b \pm \sqrt{b^2-4ac}\over 2a}
   
   
根据表达式的逻辑，进行下述编程：

.. code-block:: python

   import math
   def quadratic(a,b,c):
      p=b*b-4*a*c
      if p>=0 and a!=0:#一元二次方程有解的条件
         x1=(-b+math.sqrt(p))/(2*a)
         x2=(-b-math.sqrt(p))/(2*a)
         return x1,x2
      elif a==0:#a=0的情况下为一元一次方程
      x1=x2=-c/b
      return x1
      else:
         return('Wrong Number！')
   
   a=float(input('Please input a='))
   b=float(input('Please input b='))
   c=float(input('Please input c='))
   print(quadratic(a,b,c))

------------
思考与练习
------------

改造之前的代码。

使用函数，简化代码。

------------
你学到了什么
------------









 