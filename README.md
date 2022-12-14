# GameTheory
可恶的Java小组作业，居然这么难啊

一、“谁是卷王” 游戏背景

做“卷王”，还是“咸鱼”，这是个问题。说好的一起熬夜开黑，结果舍
友却偷偷去自习室通了宵；说好的一起泡图书馆，结果舍友却一觉睡到下午。

二、“谁是卷王” 游戏设计

1. 游戏模式概述

你将设计并实现一款“谁是卷王”的游戏，其中，你是第一人称玩家，可
以自己随意决策（“卷”or“躺”）；你的舍友、同学等是第二玩家，他们有
不同的身份：复读机、老油条、小粉红、刘皇叔，暂且称之为NPC（Non-Player
Character），相应地，他们对于“卷”还是“躺”有着不同的决策方案。
面对这个艰难的选择，你面前有一个黑盒子，暂且称之为内卷机器：其中，
任一玩家卷1小时，玩家自身学习时长增加2小时，另一玩家学习时长减少1小时；
任一玩家躺1小时，玩家自身学习时长减少2小时，另一玩家学习时长增加1小时。
游戏双方有且仅有两种选择：“卷”即学习一个小时、“躺”即摸鱼一个小时。
经过若干轮内卷之后，这场内卷之战终于诞生了真正的卷王：即总学习时长较
长的那位选手，收益矩阵如下：

![image](https://user-images.githubusercontent.com/104357032/197128144-e8f87005-5d07-4801-bcfc-fb19764a8c21.png)

提示：点击该链接可在线体验原版游戏：https://dccxi.com/trust/

2. 系统要求

本作业要求以“谁是卷王”游戏为背景，适当地进行游戏内容的修改和创新。
结合面向对象的知识，用 Java application 来模拟此游戏。
其中，作为基本要求，游戏核心就是一个用户玩家和一些NPC玩家对线，
NPC玩家每次的选择都是固定的；作为进阶要求，你可以根据4.评分标准，或进
行扩展，完善该游戏。

2.1 系统基本要求

（1）玩家注册与登录：在游戏开始之前，要求玩家登录系统。系统要求提
供注册功能，新玩家需要注册，已注册玩家可直接登录并加载历史数据，开始游
戏。（注：不熟悉数据库的同学可以采用本地文件存储）

（2）预游戏界面：第一次进入游戏，系统将出现一个进入游戏预界面，用
以指示玩家个人信息，历史数据，NPC介绍等信息，并且玩家可以和不同身份的
对手（NPC）进行游戏。

（3）游戏主界面：

（a）NPC设计：设计不同的玩家身份及内卷策略，具体如下：
我们将双方玩家都完成一次决策过程，叫做“一轮”。

（i）小粉红：每一轮总是选择“卷”

（ii）老油条：每一轮总是选择“躺”

（b）内卷机器设计：包括图形展示和核心逻辑，具体如下：

（i）逻辑：见上述收益矩阵

![image](https://user-images.githubusercontent.com/104357032/197128499-568dc1f2-0f77-4ccc-8497-a910a11c1413.png)

（ii）图形展示：呈现一个学习时长收益规则矩阵，收益值随着游戏进行，
根据该规则不断变化（体现在x, y之上），如下：

（4）道具设计：为了提高内卷胜率，你需要设计以下道具功能：

（a）加时器：加大内卷轮数，例如由原先设定的N轮，加大到2N轮
其中，道具需要用学习时长购买，购买后，在玩家的每一轮决策开始前均
可使用，价格等规则请自行设计（当然，NPC玩家是不能使用道具的）。

（5）人机交互：游戏应该根据当前玩家所处状态，给出一定的交互信息
（例如：玩家当前学习时长足够，提示是否购买道具）

（6）主界面其他要素：①状态栏：实时显式玩家当前学习时长、道具等信
息；②商店：用于购买道具

（7）游戏结束条件（仅供参考，可适当扩展）：①玩家未保存即退出游戏；

②每局内卷最多只能进行N轮（例如10）

2.2 系统进阶要求（附加题，可自行扩展）

（1）实现剩余的NPC：

（a）复读机：第一轮总是选择“卷，后续的轮次里，他的选择都是对手
上一轮的选择

（b）刘皇叔：先一直“卷”，直到对方“躺”一次，后续全部“躺”

（2）找出该游戏规则目前存在的BUG，或不合理的地方，尝试修改规则并
实现

（3）其他附加功能：例如游戏计时、游戏排行、背景音乐、声音效果、界面优
化等功能。

（4）二人对战：支持两个用户玩家（而不是用户玩家和NPC玩）同时在线
对战，各玩家可自由选择“卷”还是“躺

3. 评分标准

![image](https://user-images.githubusercontent.com/104357032/197128413-d966d947-863b-488c-b23b-21c9d344811c.png)
