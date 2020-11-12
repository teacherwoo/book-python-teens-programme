=======================
让事物移动
=======================

上一个小节，是使得矩形的边的厚度改变，来改变图形。
这一小节，我们通过改变图形的位置，让图像动起来。



-------------------------
Pygame游戏结构框架
-------------------------
所以现在，制作一个简单的pygame程序框架，需要把绘制逻辑部分：``pygame.draw.rect(screen, BLUE, shape, width)`` 
放到了while循环体立面，动态的绘制,再动态的更新当前的屏幕： ``pygame.display.update()``

所以，上述代码就变为：

.. code-block:: python

   import pygame
   import sys
   
   # Colors (R, G, B)
   BLACK = (0, 0, 0)
   WHITE = (255, 255, 255)
   RED = (255, 0, 0)
   GREEN = (0, 255, 0)
   BLUE = (0, 0, 255)
      
   WIDTH = 360  # 游戏窗口的宽度
   HEIGHT = 480 # 游戏窗口的高度
    
   pygame.init()
   screen = pygame.display.set_mode((WIDTH, HEIGHT))
   screen.fill(WHITE)
   pygame.display.set_caption("我的游戏窗口")#设置游戏窗口标题栏文字
   
   #定义初始位置
   pos_x= 130
   pos_y= 100
   width= 2 
   while True:
       for event in pygame.event.get():
           if event.type == pygame.QUIT:
               sys.exit()
       shape= pos_x, pos_y, 100, 100
       pygame.draw.rect(screen, BLUE, shape, width)
       pygame.display.update()

绘制出的效果是一样的:

.. image:: ../_static/c07/c07p01_i02_rect.png

虽然效果和之前的一样，但是本质却是不一样的，因为绘制逻辑变为每次刷新前动态绘制，并且不停刷新。
那么我们如何看到刷新的效果呢？
就让宽度增加1，也就是说，每次刷新，就增加一个像素的宽度：``width=width+1``
那么，while循环部分的代码变为

.. code-block:: python

   while True:
       for event in pygame.event.get():
           if event.type == pygame.QUIT:
               sys.exit()       
         
       width= width+1       
       shape= pos_x, pos_y, 100, 100       
       pygame.draw.rect(screen, BLUE, shape, width)       
       pygame.display.update()

这样一来，矩形的边变得越来越宽，这样，一个矩形就变成了一个十字架：

.. image:: ../_static/c07/c07p01_i03_cross.png

-------------------------
控制时间
-------------------------

上述的程序运行过程是动态的，但是比较快速，那么我们想延缓这种过称怎么办呢？
我们开始控制时间。
上述的程序运行较快，我们就让他慢下来，具体的，采用 ``pygame.time.delay()``
函数，来使得程序可以暂停一段时间，入参是暂停的毫秒数。
Pygame中的时间以毫秒（1/1000秒）表示。大多数平台的时间分辨率有限，大约为10毫秒。所以我们控制最好是10毫秒的倍数。
具体的：

.. code-block:: python

   while True:
       for event in pygame.event.get():
           if event.type == pygame.QUIT:
               sys.exit()
       pygame.time.delay(20)        
       width=width+1
       shape= pos_x, pos_y, 100, 100
       pygame.draw.rect(screen, BLUE, shape, width)
       pygame.display.update()

上述程序中的 ``pygame.time.delay(20)`` 就是让成型等待20个毫秒。
这时，我们就可以看到图形的演化过程了:

.. image:: ../_static/c07/c07p01_i04_animate.png




>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>








 