# Unity入门学习笔记（上）

> :smiley:

## 学习背景

* 制作**[Ruby's Adventure](https://www.sikiedu.com/my/course/650)**，过程中注意学习以下内容

1. 了解unity工程面板
2. 组件的概念与理解
3. 物体的物理系统
4. 动画系统，粒子系统，Cinemachine工具包
5. 敌人AI的制作
6. UGUI
7. 完整游戏流程梳理

## 目录

unity界面的熟悉

主角ruby的制作

场景制作

装饰制作



## 学习内容

### 1.unity界面的熟悉

一般通过**Unity Hub**来管理unity游戏项目和unity版本

* unity版本管理

在**安装**这一窗口选项下可进行unity版本的管理

![uh1](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/uh1.png)

“安装编译器”，可以免费下载unity的最新版本及公开的测试版本

“选择位置”，可导入自行安装的unity版本

* 游戏项目管理

在**项目**这一窗口选项下可进行游戏项目的管理

![uh2](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/uh2.png)

“打开”，可以直接添加已经创建好的项目

若要新建项目，点击“新项目”，然后选择编译器版本及项目模板，确定名称和保存路径后点击创建就可以了。

![uh3](D:\1\github\geek\Tasks\阶段4学习笔记\图片素材\uh3.png)

（2023版的unity有好多模板）

创建好项目后就进入到游戏的实际开发界面

![uw](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/uw.png)

有很多功能性窗口，大致和vs这些编译器一样，只不过unity是图像可视化与代码结合编辑的

因为是学习游戏开发，所以首先在“Asset Store”中找到素材导入

跟教程不一样的是，2023版不能直接在编译器里打开素材商店了，只能网页开

![uweb](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/uweb.png)

（说是为了编译器界面更流畅简洁，~~我感觉没啥用~~）

通过“package manager”窗口下载导入好素材后，就可以开始创作了

首先，熟悉一下各窗口的功能

* scene![scene](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/scene.png)

编辑游戏主要展现给玩家的界面

* project

![project](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/project.png)

资源文件

* inspector

<img src="https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/inspector.png" alt="inspector" style="zoom:50%;" />

对象编辑，可以修改各项参数和添加各种组件

* hierarchy

![hierarchy](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/hierarchy.png)

游戏项目使用的各种资源对象

### 2.主角Ruby的创建

#### 1.坐标

场景中的所有物体都有3个坐标。分别是Horizontal水平轴向（x）,Vertical垂直轴向（y），depth深度（z）。
如果游戏对象无父对象，则坐标是GameObject距场景中心的距离。
如果游戏对象有父对象，则坐标是GameObject距其父对象的距离。

#### 2.脚本

包含命名空间，类（组件），函数（功能），其中两个重要的函数。

**Start()**:当游戏开始时，Unity只在Start中执行一次代码,且在第一帧更新之前调用。

帧：为了给人留下运动的印象，游戏（就像电影）是高速播放的静止图像。通常在游戏中，30或60个图像显示在
一秒钟内，这些图像都称为帧。

**Update()**:在创建该图像（帧）之前，Unity会执行在所有游戏对象的Update函数中编写的代码。1秒钟大约调用60次。在此函数中，可以编写任何希望在游戏中连续发生的事情（例如，读取玩家的输入、移动游戏对象或计算累计时间）。

**Vector2变量类型**：一种存储两个数字的数据类型，存贮在Inspector面板里关于transform组件中positon的x,y值。（vector3则是xyz三个坐标值）

将ruby的角色图片形象导入unity工程文件，新建`RubyController`脚本,将代码与ruby绑定即可

### 3.移动控制

可以在unity中`Edit > Project Settings > Input Manager`查找和修改键盘输入对应游戏操作。

（photo）

先监听玩家的键入，根据键入来进行相应移动

![spy](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/spy.png)

![move](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/move.png)

如果想要游戏物体以每秒多少的速度移动可以乘上`Time.deltaTime`

### 4.场景制作

运用unity自带的**TileMap**工具快速进行场景制作

TileMap创建：Hirerachy>右键>2D Object>TileMap

相关概念：

* 网格(Grid)：可以用来将游戏对象均匀地放置在其单元格中。
* 瓦片地图（Tilemap）：是网格的子游戏对象。由Tiles（瓦片）组成的。
* 精灵（Sprite）:纹理的容器。大型纹理图集可以转换为精灵图集(Sprite Sheet)。
* 瓦片（Tile）：一种特殊的精灵。使用瓦片就像在画布上画画一样，画画时可以设置一些颜色和属性。
* 调色板(Palette)：保存瓦片，将它们绘制到网格上。
* 笔刷(Brush)：用于将画好的东西绘制到画布上。使用Tilemap时，可以在多个笔刷中任意选择，绘制出线条、方块等各种形状。

![mapres](https://raw.githubusercontent.com/chlorine22/Tasks/main/阶段4学习笔记/图片素材/mapres.png)

存在一种图片资源叫**图集**，包含多种张贴图（多为角色动作）

**切割图集**：选中一张精灵图片资源，将SpriteMode从single改为mutiple，可制作成图集，点击SpriteEditor可进行

**切割**：切割有三种形式：自动，按像素切割，按行列切割。

`Edit`决定瓦片的操作范围，按下是对调色板内编辑，未按下是对scene内场景编辑

**层级(Layer)**：可以在2D游戏物体中的SpriteRenderer和地形TilemapRenderer组件中的Order in layer属性中去设置层级的大小，值越大，越后渲染，值越小，越先渲染，值大的游戏物体会覆盖值小的游戏物体。

### 5.装饰制作

每一个精灵资源放入scene使用时都有着**轴心点（Pivot）**。这个点是可以自定义的特殊点，充当精灵的“锚点”。精灵以此为支点进行旋转，坐标点位置则是指轴心点的位置。         可以合理修改轴心点来达成模拟遮蔽的渲染效果。

**预制体(Prefab)**

Unity中的一种特殊资源。预制体就是一个或者一系列组件的集合体，可以使用预制体实例化克隆体，后续可对克隆体属性进行统一修改。

.进入预制体编辑模式的方法：1.双击 2.选中预制体资源，点击openPrefab选项 3.点击蓝色克隆体名称右边的小箭头 4.点击选中克隆体，点击检视面板中的Open按钮





































