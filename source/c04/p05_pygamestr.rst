=======================
用pygame绘制字符串
=======================



--------------
pygame输出文本
--------------

pygame支持使用pygame.font对象将文本打印到窗口上。
要打印文本的话，首先需要创建一个字体对象，Font的第一个参数为None是告诉pygame获得系统默认字体，也可以是具体的字体名称。
Font的第二个参数指明字体大小。

.. code-block:: python

   myfont = pygame.font.Font(None,60)

文本绘制过程比较耗费时间，常用的做法是先在内存中创建文本图像，然后将文本当作一个图像来渲染。

.. code-block:: python

   textImage = myfont.render("pygame", True, WHITE)

textImage 对象可以使用screen.blit()来绘制。
上面代码中的render函数第一个参数是要绘制的文本，第二个参数是启用抗锯齿能力，第三个参数是文本的颜色。

下面的代码，将刚刚产生文本图像绘制到屏幕的坐标（10，100）处。

.. code-block:: python

   screen.fill(BLACK)
   screen.blit(textImage, (10,100))
   pygame.display.flip()


 
------------
思考与练习
------------

绘制标靶

------------
你学到了什么
------------

- 了解pygame
- 学会了安装pygame
- 运行基本的pygame程序

 












