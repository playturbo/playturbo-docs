---
description: '#自由编辑器 #空白制作 #合成玩法 #初级难度'
---

# 《合成新元素》空白制作教程

温馨提示：本篇教程主要讲解**如何通过空白制作来做出"合成"玩法的2D素材**，建议搭配[DEMO](https://tinyurl.com/yt6uwvkn)食用效果更佳哦！



## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：成双匹配 合成玩法
* 【交互方式】：拖拽到指定位置
* 【自由度】：固定流程
* 【核心资产】：图片
* 【核心功能】：拖拽到指定位置 - 隐藏/显示素材；禁用事件/启用事件



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

<table><thead><tr><th width="222.33333333333331">手机试玩效果最佳</th><th>竖屏</th><th>横屏</th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (1789).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/Animation1 (4).gif" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/Animation2 (5).gif" alt="" data-size="original"></td></tr><tr><td>扫码试玩</td><td><a href="https://tinyurl.com/yt6uwvkn">点击试玩</a></td><td><a href="https://tinyurl.com/yt6uwvkn">点击试玩</a></td></tr></tbody></table>



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示图示【初始元素布局】，此时物品都不可被拖拽

2）出现【操作指引1】，引导玩家点击"添加元素"按钮。玩家按下按钮，第一个格子出现元素2，同时按钮不可点击

3）出现【操作指引2】，引导玩家拖动左侧元素2到右侧进行合成。玩家拖动左侧元素2到正确位置，播放【合成反馈】；否则播放【错误反馈】

4）同理，依次完成元素3和元素4的合成

5）完成元素4的合成(即钻石数量变为300)后，进入结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1790).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据上一环节的玩法梳理，我们可将本案例拆分为2个场景来制作

<table data-full-width="false"><thead><tr><th width="123">场景名称</th><th width="322">场景1-核心玩法</th><th>场景2-结束页面</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/image (1792).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1791).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td><p>1）引导玩家点击按钮，添加元素</p><p>2）引导玩家合成目标元素</p></td><td>奖励面板+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>棋盘底图、多种元素、操作指引、合成指引、目标面板</p><p><strong>视听包装：</strong>合成粒子特效、错误粒子特效、音效</p></td><td><p><strong>静帧图片：</strong>奖励面板、奖励物品、跳转按钮</p><p><strong>视听包装：</strong>彩带粒子、胜利音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>点击指引：缩放缓动</p><p>合成指引：位移缓动+缩放缓动+透明度缓动</p><p>目标元素：旋转缓动</p></td><td>奖励面板&#x26;跳转按钮：缩放缓动</td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象："添加元素"按钮</p><p>触发事件：按下</p><p>响应事件：显示素材；禁用事件/启用事件</p><hr><p>触发对象：元素2/3/4</p><p>触发事件：拖拽到指定位置</p><p>响应事件：显示素材/隐藏素材；禁用事件/启用事件</p></td><td><p>触发对象：场景2</p><p>触发事件：按下</p><p>响应事件：跳转应用商店</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step4【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整位置大小

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1793).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2.普通场景**

**2.1 场景1**

1）在场景1中添加核心玩法相关资产：棋盘底图/多种元素图片/合成指引/目标面板/操作指引/音效

2）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名（详细内容可进DEMO查看）

<figure><img src="../../../.gitbook/assets/image (1794).png" alt=""><figcaption></figcaption></figure>

**3）注意:** <mark style="color:orange;">此类玩法(指在玩家交互后,物品位置发生改变的玩法)的制作逻辑为 "在同一个位置添加可能出现的所有元素，然后先隐藏高级元素（即玩家交互后才会出现的元素），后续通过事件设置显示高级元素，隐藏低级元素"，以此来实现目标效果</mark>

因此，需要将以下图层的初始状态设为"隐藏"，后续我们再通过事件来控制这些图层的显示（需要隐藏的图层包含：棋盘上的高级元素；第2/3/4次操作指引；灰色按钮）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1796).png" alt=""><figcaption></figcaption></figure>

</div>

**2.2 场景2**

1）复制场景1的目标面板组\[group\_guidelines1]到场景2，并删除多余图层

2）添加奖励面板和跳转按钮相关资产，调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名（详细内容可进DEMO查看）

3）勾选场景2为【结束场景】，以便上报试玩结束

<figure><img src="../../../.gitbook/assets/image (1798).png" alt=""><figcaption></figcaption></figure>



### Step2 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）在场景1中切换到横屏模式，选中所有最高层级的图层

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层的【位置】和【缩放比例】，让画面展示出完整的核心玩法相关内容

3）同理，我们再依次切换到场景2和【全局场景】，使用【复用竖屏位置尺寸配置】功能一键排版，再微调其位置大小

<figure><img src="../../../.gitbook/assets/image (1800).png" alt=""><figcaption><p>场景1</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1801).png" alt=""><figcaption><p>场景2</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1802).png" alt=""><figcaption><p>全局场景</p></figcaption></figure>



#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的常驻信息组始终位于各机型屏幕的顶部，所以我们调整其"屏幕适配方式"为贴顶适配（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1803).png" alt=""><figcaption></figcaption></figure>



### Step3 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，用到的动画和粒子特效如下，我们依次展开介绍：

场景1：点击指引动画、目标指引动画、合成指引动画、目标元素旋转动画、合成粒子、错误粒子

场景2：奖励面板&跳转按钮的缩放动画、彩带粒子

#### **1.点击指引：缩放缓动**

1）选中指引手指1图片\[gf\_hand1]，添加动画-通用-缩放缓动，作为点击指引循环动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1804).png" alt=""><figcaption></figcaption></figure>

2）复制该缩放动画到按钮组\[btn\_add]，微调参数，作为按钮指引循环动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1806).png" alt=""><figcaption></figcaption></figure>

#### **2.目标指引：缩放缓动**

1）选中目标图片\[target]，添加动画-通用-缩放缓动，作为目标元素指引动画。参数设置如下

2）注意：该缩放动画可复制给其他\[target]图层，微调数值即可

<figure><img src="../../../.gitbook/assets/image (1805).png" alt=""><figcaption></figcaption></figure>

#### 3.合成指引：位移缓动&缩放缓动&透明度缓动

1）选中指引手指2图片\[gf\_hand2]，依次添加 位移缓动/缩放缓动/透明度缓动 动画，作为手指的合成指引动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1808).png" alt=""><figcaption></figcaption></figure>

2）注意：该图层动画可复制给\[gf\_hand3]&\[gf\_hand4]，调整位移距离即可

<figure><img src="../../../.gitbook/assets/image (1809).png" alt=""><figcaption></figcaption></figure>

#### 4.目标元素：旋转缓动

选中目标元素图片\[target\_ui]，添加动画-通用-旋转缓动，作为目标元素的突出展示动画。参数设置如下

<figure><img src="../../../.gitbook/assets/image (1810).png" alt=""><figcaption></figcaption></figure>

#### 5.奖励面板&跳转按钮：缩放缓动

1）选中组图层\[node\_reward]，添加动画-通用-缩放缓动，作为结束元素的入场动画。参数设置如下

<figure><img src="../../../.gitbook/assets/image (1811).png" alt=""><figcaption></figcaption></figure>

2）复制该动画到按钮组\[btn\_continue]，微调参数，作为跳转按钮的循环指引动画。参数设置如下

<figure><img src="../../../.gitbook/assets/image (1812).png" alt=""><figcaption></figcaption></figure>

#### 6.粒子特效：合成粒子&错误粒子&彩带粒子

1）打开公共粒子库，选择并添加合适的粒子特效。如在场景1中添加合成粒子、错误粒子；在场景2中添加彩带粒子

2）调整粒子到合适的位置（注意横竖屏都要调整）

3）将场景1中粒子的初始状态设为"隐藏"，后续我们通过事件来控制粒子的显示和播放

<figure><img src="../../../.gitbook/assets/image (1813).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;background-color:red;">Step4 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

完成所有动效的设置，我们对试玩的逻辑 也就是"事件"进行设置

本案例与事件设置相关的内容有：

* 按下"添加元素按钮"：隐藏原按钮，显示灰色按钮，显示元素2
* 拖拽并抬起"元素2"：播放错误粒子特效；拖拽"元素2"到正确位置：隐藏元素2，显示元素3
* "元素3"和"元素4"的事件设置同上
* 结束页按下：跳转应用商店

接下来，我们按顺序依次讲解

#### <mark style="color:red;">1.图层：元素2</mark>









#### <mark style="color:red;">2.图层：添加元素按钮</mark>

1）选中场景1中的自由画线组件图层，点击【添加事件】，选择触发事件为**【开始画线】**

* 添加响应事件：设置埋点，编辑埋点名称为"第一次有效操作"
* 添加响应事件：隐藏粉刺针组图层、隐藏指引光圈、从头播放1次点击音效

2）继续【添加事件】，选择触发事件为**【画线完成】**

* 添加响应事件：跳转到下一场景

#### 2.场景2

选中场景2，点击【添加事件】，选择触发事件为**【定时触发】**

* 设置执行延迟时长为1s
* 添加响应事件：跳转到下一场景

#### 3.场景3

选中场景3，点击【添加事件】，选择触发事件为**【按下】**

* 添加响应事件：设置埋点，编辑埋点名称为"结束页触发跳转"
* 添加响应事件：跳转应用商店

#### 4.图层: 常驻下载按钮组

选中"全局场景"下的常驻下载按钮组，点击【添加事件】，选择触发事件为**【按下】**

* 添加响应事件：跳转应用商店

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。





### Step5 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1788).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/自由画线组件空白制作_资源.zip" %}
