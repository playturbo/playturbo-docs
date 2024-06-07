---
description: '#换肤编辑器'
---

# 3D模板

Playturbo现已支持3D类型的可玩素材产出，可通过模版换肤制作的方式对3D模版进行迭代

<mark style="color:red;">**注意：当前3D模版仅支持 【换肤制作-普通制作】**</mark>



## <mark style="color:blue;">一、项目创建</mark>

1）在「模版库」-「可玩模版」页面，筛选类型为「3D」的模板，即可展示所有3D模版

<div align="left">

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

2）点击模版进行预览。注意，一个模版中可能包含多套皮肤，不同皮肤可能对应不同的玩法、资源、游戏逻辑，可切换皮肤进行预览，并选择最适合的皮肤创建项目

3）确认皮肤后，点击「换肤制作」 - 「普通制作」 ，填写项目名称后即进入编辑页面

<div align="left">

<figure><img src="../../.gitbook/assets/image (1836).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">二、换肤制作</mark>

✨对比常规2D模板，创建3D模板换肤制作项目后，编辑页面新增了【预设及镜头】、【3D资源】、【玩法】这三个模块

✨建议操作流程：

* 先在「预设及镜头」，对预设值、屏幕适配、镜头参数进行调整
* 再依次进入「3D资源」、「常驻元素」、「场景」内，对3D模型资源及其他资源进行替换、调整

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



### 1.预设及镜头 <a href="#g3lte" id="g3lte"></a>

「预设及镜头」包含三部分：预设、屏幕适配、相机

#### <mark style="background-color:blue;">1-1）预设</mark>

* 「预设」是一系列游戏逻辑、素材模型的集合，可通过切换预设，实现不同游戏逻辑、不同场景、不同模型的素材产出
* 「预设」为单选切换
* 调整「预设」后可能会使用到不同的模型，可前往场景内调整具体资源及玩法

<div align="left">

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>示例：在该模板的「预设」中,可分别对模板内的人物模型、奖励项目、有无障碍进行调整</p></figcaption></figure>

</div>



#### <mark style="background-color:blue;">1-2）屏幕适配</mark>

在「屏幕适配」下，可分别调整横屏和竖屏的FOV偏移值

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>调整前</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>调整后</p></figcaption></figure>



#### <mark style="background-color:blue;">1-3）相机</mark>

* 每个模板可调整的相机参数数量不同，由模板的玩法决定。例如camera1用来观察场景， camera2用来跟随玩家，camera3用于ending页面

<div align="left">

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

</div>

* 展开「相机」下的参数，可对相机位置角度进行调整，以实现不同的视觉效果
* 可调整的参数包含：极角、方位角、径向距离、X轴视角偏移、Y轴视角偏移、Z轴视角偏移、阻尼系数

<figure><img src="../../.gitbook/assets/image (1839).png" alt=""><figcaption><p>调整前</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (1842).png" alt=""><figcaption><p>调整后</p></figcaption></figure>



### 2.3D资源

在项目编辑页面，左侧「3D资源」栏，可查看该项目内的所有3D模型资源。可对3D模型资源，进行「编辑」和「替换」操作

#### 2-1）模型替换

点击模型资源上的「替换」按钮，可打开替换模型资源弹窗，可选择资源进行替换。（仅支持同类型的资源替换，如人替换人、动物替换动物）

#### 2-2）模型编辑 <a href="#sobfc" id="sobfc"></a>

点击模型资源上的「编辑」按钮，可打开模型编辑弹窗。模型编辑包括三部分「基础」参数、「外观」参数和「动作」参数

三种「预览」模式：预览弹窗分别有三种预览模式，用以控制相机镜头。最后一个按钮为「重置镜头」按钮

1. 默认模式：当前的模式，左键拖拽旋转、中间位移
2. 平移模式：左键拖拽进行预览相机的平移
3. 缩放模式：左键拖拽进行缩放



「基础参数」：对模型的X、Y、Z位置、旋转、缩放进行修改。预览弹窗分为两块，分别预览修改前和修改后的模型

<div align="left">

<figure><img src="../../.gitbook/assets/image (1843).png" alt=""><figcaption></figcaption></figure>

</div>

「外观参数」：可对模型进行「部位颜色」和「材质」的修改。

可对该模型不同部位的「颜色」进行修改

<figure><img src="../../.gitbook/assets/image (1844).png" alt=""><figcaption></figcaption></figure>

并且可对整体模型的「材质」进行修改。可修改的材质参数包括，模型的「主颜色」、「环境遮蔽强度」、「粗糙度」、「金属光泽」、「镜面强度」、「自发光颜色」等参数进行修改。具体的修改效果可自行体验

<figure><img src="../../.gitbook/assets/image (1845).png" alt=""><figcaption></figcaption></figure>

「动作参数」：部分模型有对应的动作，则在模型编辑弹窗内有「动作」Tab页，展示该模型关联的所有动作资源。

对于动作资源，可以调整其播放「速率」，在右侧预览区可预览该动作

<figure><img src="../../.gitbook/assets/image (1846).png" alt=""><figcaption></figcaption></figure>

可以替换资产的动作资源

对于部分动作，动作播放到第n帧时会触发相应的其他事件，被称为关键帧。如「攻击」动作到第5帧时，触发「出血」事件。该关键帧的位置可以在右侧「预览进度条」区域通过滑块移动调整。（尤其注意替换动作之后，关键帧的位置可能需要调整）

<div align="left">

<figure><img src="../../.gitbook/assets/image (1847).png" alt=""><figcaption></figcaption></figure>

</div>
