---
description: '#自由编辑器 #空白制作 #消除玩法 #进阶难度'
---

# 《方块三消》空白制作教程

温馨提示：本篇教程主要讲解**如何通过空白制作来做出"点击"三消玩法的2D素材**，建议搭配DEMO食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐⭐
* 【适用产品】：消除玩法产品
* 【交互方式】：按下
* 【自由度】：全自由
* 【核心资产】：静帧图片
* 【核心功能】：按下-隐藏/显示素材；全局变量



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                          | 竖屏                                                                                  | 横屏                                                                                  |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1629).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation1 (3).gif" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation2 (4).gif" alt="" data-size="original"> |
| 扫码试玩                                                                              | [点击试玩](https://tinyurl.com/bdhea2kb)                                                | [点击试玩](https://tinyurl.com/bdhea2kb)                                                |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示图示【方块初始画面】

2）出现【操作指引】，引导玩家按下西瓜方块

3）玩家可按下任一明亮方块，按下后该方块即按顺序显示在【消除坑位】

4）当【消除坑位】出现3个相同图案的方块时，播放【消除成功反馈】，同时进度条前进一段

5-1）当玩家成功完成三组消除(进度条加载满)，进入胜利结束页

5-2）当【消除坑位】已满同时未出现3个相同图案的方块时，进入失败结束页

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1631).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据玩法梳理内容，我们可将本案例拆分为 3 个场景来制作，即1个核心玩法场景+2个结束场景

<table data-full-width="false"><thead><tr><th width="117">场景名称</th><th width="243">场景1-核心玩法</th><th>场景2-胜利结束页</th><th>场景3-失败结束页</th></tr></thead><tbody><tr><td><strong>效果预览</strong></td><td><img src="../../../.gitbook/assets/image (1632).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1633).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1634).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家可点击任意方块，满足消除条件即原地消除；完成三组消除即成功，坑位已满未消除三组即失败</td><td>胜利页面: 开心gif+奖励文本+跳转按钮</td><td>失败页面: 哭泣gif+失败文本+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>多种方块、消除坑位、进度条</p><p><strong>粒子特效：</strong>消除反馈</p><p><strong>音效：</strong>点击音效、消除音效</p></td><td><p><strong>静帧图片：</strong>跳转按钮</p><p><strong>序列帧：</strong>开心表情</p><p><strong>粒子特效：</strong>彩带反馈</p><p><strong>音效：</strong>胜利音效</p></td><td><p><strong>静帧图片：</strong>跳转按钮</p><p><strong>序列帧：</strong>哭泣表情</p><p><strong>音效：</strong>失败音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>手指指引：位移缓动</p><p>进度条：缩放缓动</p></td><td>胜利反馈组：缩放缓动</td><td>失败反馈组：缩放缓动</td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：单个物品</p><p>触发事件：按下</p><p>响应事件：隐藏素材；显示素材；赋值(全局变量)</p></td><td><p>触发对象：跳转按钮</p><p>触发事件：按下</p><p>响应事件：跳转应用商店</p></td><td><p>触发对象：跳转按钮</p><p>触发事件：按下</p><p>响应事件：跳转应用商店</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step4【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../.gitbook/assets/image (22) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1**

1）将与核心玩法相关的资产添加进场景1

2）调整各资产到合适的位置大小，根据资产类型对资产进行编组、排序、命名

**注意:**  此类玩法(指在玩家交互后,物品位置发生改变的玩法)的制作逻辑为 "在不同位置添加相同的物品，然后先隐藏消除坑位上可能出现的物品，再通过事件设置显示消除坑位上的物品，隐藏原位置的物品"，以此来实现目标效果

<mark style="color:orange;">因此，除了初始界面要展示的方块外，每个消除坑位上都应添加所有可能出现的结果，也就是5张不同图案的方块图片；同理，上方6张灰色不可点击的图片也应该在同样的位置各添加一张正常图案的图片，来作为解除限制后方块变明亮的效果</mark>

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）调整图层初始状态：将消除坑位上的所有方块图片(4\*5=20个)设为"隐藏"状态；将所有灰色方块对应的明亮方块(6个)设为"隐藏"状态。后续我们将通过事件来控制这些图层的隐藏/显示。

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>其中一组图层示例</p></figcaption></figure>

</div>

#### **3.场景2 & 场景3**

1）将与结束页面相关的资产分别添加进场景2、场景3

2）同样的，调整各资产到合适的位置大小，根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>场景2</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>场景3</p></figcaption></figure>



### Step2 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成所有竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）切换到横屏模式，选中所有最高层级的图层

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层组的【位置】和【缩放比例】即可

3）场景2和场景3同理

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的产品信息始终位于屏幕最上方，所以我们要调整其适配方式。直接在竖屏模式下选中产品信息组\[group\_information]，在右侧【屏幕适配方式】处点击向上图标即可完成设置（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



### Step3 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，使用到的动效如下：

动画：手指指引、进度条、胜利/失败反馈组

粒子特效：消除反馈(星星粒子)、结束页胜利反馈(彩带粒子)

#### **1.动画:**&#x20;

**1-1）手指指引**

1）选中手指图片\[hand]，添加动画-通用-位移缓动，来作为手指的循环指引动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2）再选中手指组\[group\_gf]，添加动画-退场动画-淡出，作为玩家有效操作后手指退场的动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**1-2）进度条**

1）选中进度条图片\[progress]，将其锚点设为（0,50）

2）添加动画-通用-缩放缓动，来作为进度条的前进动画。参数设置如下：

<mark style="color:orange;">注意: 因进度条需要播放3次才到终点，所以可将动画的"持续时间"设为0.9s，然后通过事件控制动画的播放时间(每次播0.3s)来实现目标效果</mark>

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）然后选中跟随进度条同步前进的星星图片\[progress]，添加动画-通用-位移缓动，同样将动画的持续时间设置为0.9s。具体参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1635).png" alt=""><figcaption></figcaption></figure>

**1-3）胜利/失败反馈组**

1）选中场景2的胜利反馈组\[group\_emojiAndText]，添加动画-通用-缩放缓动，来作为入场动画

2）然后再选中跳转按钮组\[group\_btn]，添加缩放缓动动画，作为入场后的按钮循环指引动画

3）依次复制两个动画到场景3对应的失败反馈组\[group\_emoji]和跳转按钮组\[group\_btn]即可

参数设置如下：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="548"><figcaption></figcaption></figure>

</div>



#### **2.粒子特效**

**2-1）消除反馈**

1）在【公共资产库】中选择合适的粒子特效并添加

2）因本案例有4个不同的消除坑位，所以需要再复制三个粒子图层

3）依次调整四个粒子特效的位置到对应区域，然后进行编组

4）将四个粒子特效设为"隐藏"状态，后续我们通过事件来控制粒子的显示和播放

<div align="left">

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

**2-2）结束页胜利反馈**

在场景2中添加彩带粒子特效，开启【自动播放】即可

<div align="left">

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



### <mark style="background-color:red;">Step4 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例的核心事件集中设置在"所有可被点击的方块图片"以及"场景1"上，我们按操作顺序依次讲解

<mark style="background-color:green;">**Part1：全局变量**</mark>

首先，因为要实现：

a. 放置坑位显示：判断玩家所有操作的可能性，来显示对应的结果

b. 底层方块是否启用：判断底层方块状态，有遮挡时不可点击，无遮挡时可点击

c. 交互开关：消除中禁止点击方块，同时清空消除坑位

d. 计算成功消除次数：玩家每完成一组消除，进度条前进一段；完成三组消除后，进入结束页面

要想实现以上效果，就需要使用[【全局变量】](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/quan-ju-bian-liang.md)，以下是对本案例所使用到的全局变量的梳理，我们以其中一个方块为例，展开介绍

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">1.添加全局变量</mark>

1）点击上方【全局变量】图标，添加变量

2）填写变量名称，如blockchose1，并设置变量类型与初始值，保存

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）按照同样的方法，依次添加其他类型的变量

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">2.为其中一个"可被点击的方块"添加事件与条件判断</mark>

以其中一个方块为例，选中方块2图层\[block2\_4]，添加事件-按下

<mark style="background-color:yellow;">因消除坑位共有4个，我们需要给每个方块设置4个条件判断来区分方块该被放置在哪个位置</mark>

1）添加条件判断1：blockchose1=0 且 eliminate=false (对应: 方块可点击，同时坑位1无方块)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="347"><figcaption></figcaption></figure>

</div>

* 添加响应事件：赋值，赋值blockchose1=2(对应: 坑位1已放置方块2)
* 添加响应事件：隐藏原位置方块2；显示坑位1上的方块2
* 添加响应事件：从头播放1次按下音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）继续添加条件判断2：blockchose1≠0 且 blockchose2=0 且 eliminate=false (对应: 方块可点击，同时坑位1已有方块，坑位2无方块)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="403"><figcaption></figcaption></figure>

</div>

* 同理，添加响应事件：赋值，赋值blockchose2=2(对应: 坑位2已放置方块2)
* 添加响应事件：隐藏原位置方块2；显示坑位2上的方块2
* 添加响应事件：从头播放1次按下音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）同理，继续完成条件判断3和条件判断4的设置

条件判断3对应: 方块可点击，同时坑位1、坑位2都已有方块，坑位3无方块

条件判断4对应: 方块可点击，同时坑位1、坑位2、坑位3都已有方块，坑位4无方块

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### <mark style="color:red;">3.快速复制事件给其他"所有可被点击的方块"</mark>

在本案例中，每个方块的事件设置都是相同的逻辑，所以在按照上面步骤完成一个方块的事件设置后：

1）我们点击"复制"按钮复制整个"按下"事件

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2）按住Ctrl键，全选所有可被点击的图片图层（包含灰色方块下的明亮方块）

3）点击上方"粘贴"按钮，选择【仅粘贴图层事件】。这样，所有"可被点击的图片"都有了同一套逻辑的事件与条件判断

4）然后逐一将每个方块的响应事件对应的响应对象进行微调即可

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**5）需注意：**因上方的\[block4\_1]和\[block3\_2]两个方块直接影响"底层方块是否被启用"，所以需额外给这两个方块添加与之变量相关的响应事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

分别给\[block3\_2]的每个条件判断下添加响应事件：赋值，赋值block3\_2=false (对应: block3\_2已不在场上,已放置到坑位)

同理，给\[block4\_1]的每个条件判断下添加响应事件：赋值，赋值block4\_1=false (对应: block4\_1已不在场上,已放置到坑位)

后续，我们将通过场景1下的条件判断和响应事件来触发对应结果

<div align="left">

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

以上，我们就完成了"所有可被点击的方块"的事件设置。接下来，我们在场景1上添加条件判断



#### <mark style="color:red;">4.在"场景1"添加条件判断与响应事件</mark>

选中场景1 - 添加事件 - 条件判断

**1）条件判断1-4：消除中禁止点击方块，同时清空消除坑位**

* 编辑条件判断1为：blockchose1=0 且 eliminate=true (对应: 方块不可点击，同时坑位1方块已消除)
* 添加响应事件：逐一隐藏坑位1上五个不同图案的方块
* 条件判断2/3/4同理

<div align="left">

<figure><img src="../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



**2）条件判断5-8：消除结果与对应反馈**

* 编辑条件判断5：blockchose1≠0 且 blockchose1=blockchose2 且 blockchose1=blockchose3 (对应: 坑位1已有方块，同时坑位2/坑位3的方块图案与坑位1相同)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>示例</p></figcaption></figure>

</div>

* 添加响应事件：赋值，赋值elimination\_time+1 (对应: 已完成一组消除)
* 添加响应事件：赋值，赋值blockchose1/blockchose2/blockchose3=0、eliminate=true  (对应: 方块不可点击，同时清空前三个坑位)
* 添加响应事件：显示并播放对应坑位的消除粒子特效、从头播放1次消除音效
* 添加响应事件：执行延迟0.5s后，赋值，eliminate=false (对应: 方块可点击）

<mark style="background-color:yellow;">注意：因消除清空的逻辑和点击放置的逻辑同时判断可能会出错，所以需要做个时间差(即延迟0.5s)在禁用点击的同时控制已消除的元素清空</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (19) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 按照同样的逻辑，还需添加三个条件判断，即当消除坑位为 "1-2-4"、"1-3-4"、"2-3-4"时
* 所以，我们依次设置条件判断6/7/8

<figure><img src="../../../.gitbook/assets/image (20) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



**3）条件判断9：消除失败**

* 编辑条件判断9：blockchose1≠0 且 blockchose2≠0 且 blockchose3≠0 且blockchose4≠0  (对应: 四个坑位都已放置方块)

<mark style="background-color:yellow;">注意：因为我们在前面设置了"条件判断5-8：消除结果与对应反馈"，已经包含了可能出现的四种正确消除的结果，所以错误消除的条件判断，只需将所有坑位的变量设置为"≠0"即可</mark>

* 注意，因"错误消除"只发生一次就要进入失败结束页，所以这里需要勾选"只生效一次"
* 添加响应事件：赋值，赋值eliminate=true (对应: 不可点击)
* 添加响应事件：播放震屏效果、从头播放1次错误音效
* 添加响应事件：执行延迟0.5s后，跳转失败结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



**4）条件判断10-12：消除成功次数对应反馈**

* 编辑条件判断10为：elimination\_time=1  (对应: 完成一组消除)
* 勾选"只生效一次"
* 添加响应事件：设置埋点，编辑埋点名称为"成功消除一组方块"
* 添加响应事件：从头播放进度条前进动画；执行延迟0.3s后，暂停播放进度条前进动画
* 条件判断11/12同理，分别对应：完成两组消除、完成三组消除

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



**5）条件判断13-15：底层方块是否可点击**

* 编辑条件判断13为：block4\_1=false (对应: 方块block4\_1已被放到坑位)
* 勾选"只生效一次"
* 添加响应事件：隐藏两个左边底层的灰色方块；显示两个左边底层的明亮方块
* 条件判断14/15同理，分别对应：方块block3\_2已被放到坑位、方块block4\_1和block3\_2都已被放到坑位

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



**6）条件判断16：埋点1相关**

* 编辑条件判断16为：blockchose1≠0  (对应: 坑位1已有方块，即玩家第一次有效操作)
* 勾选"只生效一次"
* 添加响应事件：设置埋点，编辑埋点名称为"玩家按下第一个方块"
* 添加响应事件：播放指引手指的淡出动画

<div align="left">

<figure><img src="../../../.gitbook/assets/image (21) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



<mark style="background-color:green;">**Part2：普通事件**</mark>

#### <mark style="color:red;">1.场景1：常驻下载按钮组</mark>

1）选中场景1中的常驻下载按钮组\[ctat]

2）添加事件 - 按下

3）添加响应事件：跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">2.场景2/3：跳转按钮组</mark>

1）选中场景2中的跳转按钮组\[group\_btn]

2）添加事件 - 按下

3）添加响应事件：设置埋点"结束页触发跳转"、跳转应用商店

4）复制该事件到场景3的跳转按钮组

<div align="left">

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。



### Step5 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/方块三消空白制作_资源.zip" %}
