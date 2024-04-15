---
description: '#自由编辑器 #空白制作 #消除玩法 #进阶难度'
---

# 《货架三消》空白制作教程

温馨提示：本篇教程主要讲解**如何通过空白制作来做出三消玩法的2D素材**，建议搭配DEMO食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐⭐
* 【适用产品】：消除玩法产品
* 【交互方式】：拖拽到指定位置
* 【自由度】：半自由
* 【核心资产】：静帧图片
* 【核心功能】：拖拽到指定位置-隐藏/显示素材；全局变量



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                          | 竖屏                                                                                | 横屏                                                                                   |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| <img src="../../../.gitbook/assets/image (1522).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation001.gif" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation00 (1).gif" alt="" data-size="original"> |
| 扫码试玩                                                                              | [点击试玩](https://tinyurl.com/yf989yf6)                                              | [点击试玩](https://tinyurl.com/yf989yf6)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示图示【货架初始画面】

2）出现【操作指引】，引导玩家向下拖动白色盒子完成排序消除

3）玩家拖动白色盒子到指定位置，播放【成功反馈】；否则返回原位

注意：①所有物品都能被拖拽，但只有拖拽正确才放置；②当绿色瓶子完成排序消除，褐色瓶子的拖拽事件即生效

4）玩家每完成一组排序消除，星星数量+1；当玩家完成三组消除(即星星数量为"3/3")时，进入结束页面

5）结束页面玩家全屏任意按下，跳转商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1517).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据玩法梳理内容，我们可将本案例拆分为 2 个场景来制作，即核心玩法场景+结束页场景

<table data-full-width="false"><thead><tr><th width="136">场景名称</th><th width="321">场景1-核心玩法</th><th>场景2-结束页</th></tr></thead><tbody><tr><td><strong>效果预览</strong></td><td><img src="../../../.gitbook/assets/Animation001.gif" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/Animation3 (1).gif" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家依次拖动三个目标物品(白色盒子/绿色瓶子/褐色瓶子)到指定位置，即可成功放置完成消除；拖动其他物品则返回原位</td><td>结束页面: 奖励面板+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>货架、物品&#x26;物品外发光图片、指引手指</p><p><strong>粒子特效：</strong>消除反馈</p><p><strong>音效：</strong>按下拖拽音效、消除音效</p></td><td><p><strong>静帧图片：</strong>弹窗面板、奖励图片、跳转按钮</p><p><strong>粒子特效：</strong>胜利反馈</p><p><strong>音效：</strong>胜利音效</p></td></tr><tr><td><strong>核心动画</strong></td><td>手指指引：位移+透明度+旋转缓动</td><td><p>奖励面板：缩放+透明度缓动</p><p>跳转按钮：缩放+透明度缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：单个物品</p><p>触发事件：拖拽；拖拽到指定位置</p><p>响应事件：隐藏素材；显示素材；赋值(全局变量)</p></td><td><p>触发对象：场景2</p><p>触发事件：按下</p><p>响应事件：跳转应用商店；上报试玩结束</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step4【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局设置**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息

<figure><img src="../../../.gitbook/assets/image (1518).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1**

1）将与核心玩法相关的资产添加进场景1

2）调整各资产到合适的位置大小，根据资产类型对资产进行编组、排序、命名

<mark style="color:red;">**注意:**</mark>&#x20;

a. <mark style="color:red;">此类玩法(指在玩家交互后,物品位置发生改变的玩法)的制作逻辑为 "在不同位置添加相同的物品，然后先隐藏放置后的物品，再通过事件设置显示放置后的物品，隐藏原位置的物品"，以此来实现目标效果</mark>

因此，"可被拖拽并放置的物品"就需要准备两张相同的图片资源。在本案例中，我们想要物品在拖拽过程中有外发光效果，所以各准备了一张普通物品图片以及一张物品外发光图片

b. 此外在本案例中，我们想要实现"在拖拽起某个物品后，其层级是在其他所有物品之上的"。<mark style="color:red;">因图层有前后顺序的层级影响，所以每个物品也都需要准备两张相同的图片资源，将其中一张设为"可被拖动的物品"，另一张则设为"不可被拖动/仅在原地显示的物品"，然后将前者所有的图片编组，并将其层级置于后者的上方</mark>

c. 因为有三次不同位置的手指指引，所以手指图片也需要添加三个

<figure><img src="../../../.gitbook/assets/image (1523).png" alt=""><figcaption><p>示意图</p></figcaption></figure>

3）调整图层初始状态：将所有可被拖动的物品(即层级较高的)设为"隐藏"状态，将所有不可被拖动的物品(即层级较低的)设为"显示"状态；将指引手指1和3设为"隐藏"状态，指引手指2设为"显示"状态。后续我们将通过事件来控制这些图层的隐藏/显示

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1524).png" alt="" width="464"><figcaption></figcaption></figure>

</div>

#### **3.场景2**

1）将与结束页面相关的资产添加进场景2

2）同样的，调整各资产到合适的位置大小，根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../.gitbook/assets/image (1525).png" alt=""><figcaption></figcaption></figure>



### Step2 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成所有竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）切换到横屏模式，选中所有最高层级的图层

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层的【位置】和【缩放比例】即可

3）全局场景和场景2同理

<figure><img src="../../../.gitbook/assets/image (1526).png" alt=""><figcaption></figcaption></figure>

#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的产品信息始终位于屏幕最上方，所以我们要调整其适配方式。直接在竖屏模式下选中产品信息组\[group\_product]，在右侧【屏幕适配方式】处点击向上图标即可完成设置（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1527).png" alt=""><figcaption></figcaption></figure>



### Step3 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，使用到的动效如下：

动画：手指指引、奖励面板+跳转按钮

粒子特效：消除反馈(星星粒子)、结束页胜利反馈(星星/彩带粒子)

#### **1.动画:**&#x20;

**1-1）手指指引**

1）选中手指组\[hand\_1]，依次添加动画-通用-位移缓动、透明度缓动，来作为手指及物品的指引动画，参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1529).png" alt=""><figcaption><p>位移缓动</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1530).png" alt=""><figcaption><p>透明度缓动</p></figcaption></figure>

2）选做：再选中手指图片\[gf\_hand1]，添加动画-通用-旋转缓动，参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1528).png" alt=""><figcaption></figcaption></figure>

3）hand2 和hand3 的动画设置同理，可直接复制-粘贴，然后调整位移动画的"位移距离"即可



**1-2）奖励面板+跳转按钮**

1）选中奖励面板组\[board]，依次添加动画-通用-缩放缓动、透明度缓动，来作为入场动画

<figure><img src="../../../.gitbook/assets/image (1533).png" alt=""><figcaption></figcaption></figure>

2）参数设置如下：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1534).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

3）复制该组图层的动画到跳转按钮组\[btn\_download]，然后再添加一个缩放动画，作为入场后的循环指引动画

<figure><img src="../../../.gitbook/assets/image (1536).png" alt=""><figcaption></figcaption></figure>

#### **2.粒子特效**

**2-1）消除反馈**

1）在【公共资产库】中选择合适的粒子特效并添加

2）因本案例有3处不同的消除区域，所以需要再复制两个粒子图层

3）依次调整三个粒子特效的位置到对应区域，然后进行编组

4）将三个粒子特效设为"隐藏"状态，后续我们通过事件来控制粒子的显示和播放

<figure><img src="../../../.gitbook/assets/image (1531).png" alt=""><figcaption></figcaption></figure>

**2-2）结束页胜利反馈**

同理，对场景2中的胜利反馈粒子特效进行设置（注:场景2的粒子特效因为是入场自动播放的，也可以直接设为"显示"状态）

<figure><img src="../../../.gitbook/assets/image (1532).png" alt=""><figcaption></figcaption></figure>



### <mark style="background-color:red;">Step4 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例的所有事件集中设置在"所有可被拖动的物品组"以及"场景"上，我们按操作顺序依次讲解。

首先，因为要实现：

a. 计算成功操作次数：玩家每完成一组消除，星星数量+1；当完成三组消除(即星星数量为3)时，进入结束页面

b. 无操作指引：当玩家完成任意一组消除后，出现下一组手指指引；玩家每3秒钟内无任何操作时，出现手指指引

要想实现以上效果，就需要使用[【全局变量】](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/quan-ju-bian-liang.md)









#### <mark style="color:red;">1.场景: Scene 1</mark>

1）选中图层\[video\_01]，添加事件-开始时

* 添加响应事件：从头播放进度条动画

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1537).png" alt=""><figcaption></figcaption></figure>

</div>

2）添加事件-结束时

* 添加响应事件：隐藏初始视频1；显示核心视频2、显示角色图片、显示操作指引组
* 添加响应事件：从头播放所有指引相关动画；同时暂停播放进度条动画

#### <mark style="color:red;">2.图层: video\_02（核心视频2）</mark>

1）选中图层\[video\_02]，添加事件-按下

* 添加响应事件：设置埋点，修改埋点名称为"玩家第一次按下"
* 添加响应事件：隐藏角色图片、隐藏操作指引组
* 添加响应事件：继续播放核心视频2；并播放进度条动画和一次点击音效

2）添加事件-抬起

* 添加响应事件：暂停播放视频核心视频2
* 添加响应事件：显示操作指引组；并从头播放操作指引相关动画；同时暂停播放进度条动画

3）复制事件：复制\[video\_01]的"结束时"事件

粘贴事件：选中\[video\_02]，粘贴 - 仅粘贴图层事件

* 修改响应事件为：隐藏核心视频2；显示核心视频3；并删除显示角色图片
* 添加响应事件：跳转应用商店（此步骤就是前面提到的"强制跳转"）

#### <mark style="color:red;">3.图层: video\_03（核心视频3）</mark>

1）复制事件：复制整个图层\[video\_02]

2）粘贴事件：选中\[video\_03]，粘贴 - 仅粘贴图层事件（即一键粘贴该图层的所有事件）

3）事件-按下

* 修改响应事件为：继续播放视频\[video\_03]；删除埋点事件、删除隐藏角色图片；

4）事件-抬起

* 修改响应事件为：暂停播放视频\[video\_03]

5）事件-结束时

* 删除响应事件：删除隐藏视频\[video\_02]、删除显示视频\[video\_03]、删除跳转应用商店
* 添加响应事件：禁用\[video\_03]的按下事件、禁用\[video\_03]的抬起事件（在设置完下一步的场景事件后，还需在这里添加一个响应事件"启用场景1的按下事件"）

<mark style="background-color:yellow;">注：这代表当最后一段视频播放结束，该视频的"按下/抬起"事件将不再生效，场景1的"按下"事件(即跳转事件)开始生效</mark>

#### <mark style="color:red;">4.场景: Scene 1</mark>

1）点击场景1 ，添加事件-按下

* 添加响应事件：跳转应用商店
* 添加响应事件：上报试玩结束
* 添加响应事件：从头播放一次点击音效

2）添加事件-定时触发

* 设置执行延迟时间为0s
* 添加响应事件：禁用场景1的按下事件

<mark style="background-color:yellow;">注：这代表一进入试玩，场景1的"按下"事件(即跳转事件)即被禁用，不会生效。然后我们在核心视频3的"结束时"事件下添加"启用场景1的按下事件"</mark>

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。



### Step5 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/模拟移动交互视频_资源.zip" %}
