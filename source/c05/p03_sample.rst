=======================
阶段实例
=======================


------------------
应用：猜拳游戏
------------------

需求分析：

- 参与游戏的角色

  - 玩家
  
    - 手动出拳
    
  - 电脑
  
    - 随机出拳

- 判断输赢

  - 玩家获胜

  | 玩家 | 电脑 |
  | ---- | ---- |
  | 石头 | 剪刀 |
  | 剪刀 | 布   |
  | 布   | 石头 |

  - 平局
    - 玩家出拳 和 电脑出拳相同
  - 电脑获胜

随机做法：

   1. 导出random模块
   2. random.randint(开始,结束)

.. code-block:: python

   """
   提示：0-石头，1-剪刀，2-布
   1. 出拳
   玩家输入出拳
   电脑随机出拳
   
   2. 判断输赢
   玩家获胜
   平局
   电脑获胜
   """
   
   # 导入random模块
   import random
   
   # 计算电脑出拳的随机数字
   computer = random.randint(0, 2)
   print(computer)
   
   player = int(input('请出拳：0-石头，1-剪刀，2-布：'))
   
   # 玩家胜利 p0:c1 或 p1:c2 或 p2:c0
   if (player == 0 and computer == 1) or (player == 1 and computer == 2) or (player == 2 and computer == 0):
       print('玩家获胜')
   
   # 平局：玩家 == 电脑
   elif player == computer:
       print('平局')
   else:
       print('电脑获胜')








 