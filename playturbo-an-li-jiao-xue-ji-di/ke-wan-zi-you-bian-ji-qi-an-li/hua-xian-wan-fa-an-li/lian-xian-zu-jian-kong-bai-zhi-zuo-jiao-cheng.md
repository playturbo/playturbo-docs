---
description: '#自由编辑器 #空白制作 #连线组件 #初级难度'
---

# 连线组件-空白制作教程

温馨提示：本篇教程主要讲解空白制作如何**通过连线组件制作出"连线玩法"的可玩素材**，建议搭配[DEMO](https://tinyurl.com/mwfduke2)和[功能介绍文档](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/zu-jian-ku-kuai-jie-bu-ju/lian-xian-zu-jian.md)食用效果更佳哦！



## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐⭐
* 【适用产品】：连线玩法
* 【交互方式】：开始画线/画线完成
* 【自由度】：全自由
* 【核心资产】：图片
* 【核心功能】：开始画线-隐藏指引；画线完成-播放反馈；全局变量累计次数



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

<table><thead><tr><th width="218.33333333333331">手机试玩效果最佳</th><th width="243">竖屏</th><th>横屏</th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (1652).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/1 (4).gif" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/2 (8).gif" alt="" data-size="original"></td></tr><tr><td>扫码试玩</td><td><a href="https://tinyurl.com/mwfduke2">点击试玩</a></td><td><a href="https://tinyurl.com/mwfduke2">点击试玩</a></td></tr></tbody></table>



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示三组待连线的元素

2）出现操作指引，引导玩家对其中一组元素进行连线配对

3）玩家可从任一元素出发，进行连线。配对成功，播放【正确反馈】，同时进度条前进一段；配对失败，播放【错误反馈】

4）成功完成三组连线配对后，进入结束页面

5）结束页玩家按下即跳转商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1654).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据上一环节的玩法梳理，我们可将本案例拆分为2个场景来制作

<table data-full-width="false"><thead><tr><th width="142">场景名称</th><th>场景1-核心玩法</th><th>场景2-结束页面</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/image (1655).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1656).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>引导玩家连线解谜</td><td>胜利反馈+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>多个连线元素、进度条、操作指引</p><p><strong>视听包装：</strong>按下音效、正确反馈音效、错误反馈音效</p></td><td><p><strong>静帧图片：</strong>胜利反馈面板、跳转按钮</p><p><strong>视听包装：</strong>彩带&#x26;烟花粒子、胜利音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>指引手指：位移缓动+透明度缓动</p><p>指引文本：位移缓动</p><p>正确/错误反馈：缩小出现+淡出</p><p>进度条：缩放缓动</p></td><td><p>胜利反馈面板：缩小出现</p><p>跳转按钮：脉冲向前</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：连线组件</p><p>触发事件：画线完成</p><p>响应事件：播放反馈/禁用起止区域</p></td><td><p>触发对象：场景2</p><p>触发事件：按下</p><p>响应事件：跳转应用商店</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step4【组件参数设置】和Step5 【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整位置大小

<figure><img src="../../../.gitbook/assets/image (1663).png" alt=""><figcaption></figcaption></figure>

#### **2.普通场景**

**2-1）场景1**

1）在场景1中添加核心玩法相关资产

2）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../.gitbook/assets/image (1662).png" alt=""><figcaption></figcaption></figure>

**2-2）场景2**

1）在场景2中添加胜利反馈相关资产和跳转按钮

2）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名

3）勾选场景2为【结束场景】，以便上报试玩结束

4）取消启用场景2的【全局场景】

<figure><img src="../../../.gitbook/assets/image (1661).png" alt=""><figcaption></figcaption></figure>



### Step2 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）在场景1中切换到横屏模式，选中所有最高层级的图层

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层的【位置】和【缩放比例】，让画面展示出完整的核心玩法相关内容

<figure><img src="../../../.gitbook/assets/image (1664).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1665).png" alt=""><figcaption></figcaption></figure>

3）同理，我们再依次切换到场景2和全局场景，使用【复用竖屏位置尺寸配置】功能一键排版，再微调其位置大小

<figure><img src="../../../.gitbook/assets/image (1666).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1667).png" alt=""><figcaption></figcaption></figure>

#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的常驻信息组始终位于各机型屏幕的底部，所以我们调整其"屏幕适配方式"为贴底适配（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1668).png" alt=""><figcaption></figcaption></figure>



### Step3 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，用到的动画和粒子特效如下，我们依次展开介绍：

场景1：手指连线指引动画、指引文本位移动画、进度条前进动画、正确/错误反馈的入场/退场动画

场景2：胜利反馈入场动画、跳转按钮指引动画、彩带粒子、烟花粒子

#### **1.指引手指：位移缓动&透明度缓动**

1）选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，作为手指移动的指引动画

2）选中手指和指引线所在的组图层\[group\_hand]，添加动画-通用-透明度缓动，作为手指过渡和指引线闪烁的动画

3）两个动画相结合，实现手指连线的循环指引动画。具体参数设置如下

<mark style="background-color:yellow;">注: 手指位移动画勾选了"\[位移距离]参数横竖屏拆分"，因此在完成竖屏的动画设置后，还需切换到横屏，对位移距离进行微调</mark>

<figure><img src="../../../.gitbook/assets/image (1669).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1670).png" alt=""><figcaption></figcaption></figure>

#### **2.**指引文本**：位移缓动**

选中指引文本\[text\_guide]，添加动画-通用-位移缓动，参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1671).png" alt=""><figcaption></figcaption></figure>

#### **3.进度条**：缩放缓动

1）选中进度条图片\[progress\_bar]，将其锚点修改为(0,50)，并重新调整位置

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1672).png" alt=""><figcaption></figcaption></figure>

</div>

2）添加动画-通用-缩放缓动，作为进度条的前进动画，参数设置如下

<mark style="background-color:yellow;">注: 因进度条需要播放3次才到终点，所以可将动画的"持续时间"设为0.9s，然后通过事件来控制每次动画的播放时长(0.3s)来实现目标效果</mark>

<figure><img src="../../../.gitbook/assets/image (1673).png" alt=""><figcaption></figcaption></figure>

#### 4.正确/错误反馈：缩小出现&淡出

1）选中正确反馈图片\[feedback\_right]，依次添加动画"缩小出现"&"淡出"，作为正确反馈的出现和消失动画，参数设置如下：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1674).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

2）因正确反馈和错误反馈的动画是相同的，因此可以复制动画到图层\[feedback\_wrong]，快速完成相同动画的制作

<figure><img src="../../../.gitbook/assets/image (1675).png" alt=""><figcaption></figcaption></figure>

#### 5.胜利反馈：缩小出现

选中场景2的胜利反馈组\[group\_end]，添加动画-进场动画-缩小出现，参数设置如下：

<figure><img src="../../../.gitbook/assets/image (18) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 6.跳转按钮：脉冲向前

选中跳转按钮组\[group\_ctat]，添加动画-强调动画-脉冲向前，作为按钮的循环指引动画。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 7.粒子特效：彩带粒子&烟花粒子

1）打开公共粒子库，选择并添加合适的粒子特效，以强化胜利的视觉效果

2）调整粒子到合适的位置

3）调整好竖屏粒子的位置，还需切换到横屏进行调整

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;">Step4 - 组件参数设置</mark> <a href="#umduz" id="umduz"></a>

完成以上内容的制作，我们开始对"连线玩法"最核心的内容——连线组件，进行添加和设置

#### 1.添加组件

在场景1中点击【玩法模板】，在【组件库】下添加 连线组件&#x20;

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="408"><figcaption></figcaption></figure>

</div>

#### **2.调整组件外观参数**

可在右侧参数区 或 直接拖拽/拉伸画布中的绿色矩形，来调整组件的位置大小（组件的大小等于可画出线 的区域范围）

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 3.设置起止区域

1）因本案例共有6个待连线元素，所以我们共添加6个起止区域

2）依次将起止区域调整到对应的位置和大小

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）设置"起止区域1"的线条样式，然后点击【应用到全部】，即可将6个区域的线条样式统一

<div align="left">

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="245"><figcaption></figcaption></figure>

</div>

#### 4.设置配对关系

1）点击【添加配对关系】，对"起止区域"的配对关系进行设置。本案例的配对关系如下：

* 正确配对：区域1 → 区域5 / 区域2 → 区域4  / 区域3 → 区域6&#x20;
* 错误配对：区域1 → 区域4&区域6 / 区域2 → 区域5&区域6  / 区域3 → 区域4&区域5

<mark style="background-color:yellow;">注：除"正确配对"和"错误配对"的配对关系外，其他区域不能进行连线配对(如区域1 → 区域2)，因此无需添加其他配对关系</mark>

2）以区域1为例，选择起止区域为"1 → 5"，并设置"配对类别"为TRUE；选择起止区域为"1 → 4&6"，并设置"配对类别"为FALSE

<div align="left">

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）依次完成六组配对关系的设置（前三组为正确配对，后三组为错误配对）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

4）在本案例中，我们选择连线配对为"双向"，连线类型为"直线"

<div align="left">

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



### <mark style="color:red;">Step5 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

完成组件的参数设置，我们开始用事件进行串联

本案例设置的主要事件有：开始画线时隐藏操作指引、正确画线完成时播放正确反馈、错误画线完成时播放错误反馈并修改线条样式、全局变量计算正确连线的次数、结束页按下跳转商店。接下来，我们按顺序依次讲解

#### 1.添加全局变量

1）点击上方【全局变量】图标，添加变量

2）填写变量名称如DrawTime，设置变量类型为"数值"，初始值为"0"，保存

<mark style="background-color:yellow;">注: 此变量仅用来计算正确连线的次数。因在玩家交互前，是没有完成任何一组连线的，所以初始值设为0</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="543"><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">2.图层事件: 连线组件Match Line Component</mark>

1）选中场景1中的连线组件图层，点击【添加事件】，选择触发事件为**【开始画线】**

* 全选所有起止区域 (因为前面我们选择了连线配对为"双向"，也就是从每个区域都可以画出线，所以这里我们全选所有起止区域)
* 添加响应事件：设置埋点1，编辑埋点名称为"玩家第一次按下"
* 添加响应事件：隐藏指引手指组、从头播放1次点击音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）继续【添加事件】，选择触发事件为**【画线完成】。**此事件我们对"正确配对关系1 → 5"进行设置

* 依次选择：匹配 - 配对关系 - "1 → 5"
* 添加响应事件：赋值。赋值变量DrawTime+1 (对应: 成功完成一组连线)
* 添加响应事件：禁用起止区域1和起止区域5
* 添加响应事件：从头播放正确反馈的全部动画、从头播放1次正确音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）复制并粘贴以上**【画线完成】**的事件，将"配对关系"和"禁用起止区域"的响应对象依次修改为"正确配对关系2 → 4""正确配对关系3 → 6"相关内容即可

<div align="left">

<figure><img src="../../../.gitbook/assets/image (18) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

4）最后添加触发事件**【画线完成】。**此事件我们统一对"三组错误配对关系"进行设置

* 依次选择：匹配 - 配对类别 - FALSE
* 添加响应事件：播放震屏效果、从头播放错误反馈的全部动画、从头播放1次错误音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (21) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 添加响应事件：修改已连线配对的线条样式，选择三组错误配对关系，并选择修改线条颜色为红色
* 添加响应事件：执行延迟0.5s后，抹除红色线条、修改连线线条样式为初始的绿色、启用三组错误配对关系

<div align="left">

<figure><img src="../../../.gitbook/assets/image (22) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### 3.场景事件：条件判断

1）在场景1下点击【添加事件】，选择触发事件为**【条件判断】**

2）编辑条件判断1：DrawTime=1（即成功完成一组连线时，会触发什么反馈）

3）勾选"只生效一次"

* 添加响应事件：设置埋点2，编辑埋点名称为"成功完成一组连线"
* 添加响应事件：播放进度条动画、执行延迟0.3s后暂停播放进度条动画

4）同理，我们再依次设置条件判断2、条件判断3

<mark style="background-color:yellow;">注: 当成功完成三组连线后需要进入结束页面，因此需要修改条件判断3最后的响应事件为"跳转到下一场景"</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (23) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### 4.场景2

选中场景2，点击【添加事件】，选择触发事件为**【按下】**

* 添加响应事件：设置埋点5，编辑埋点名称为"结束页触发跳转"
* 添加响应事件：从头播放1次点击音效、跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### 5.图层: 常驻下载按钮组

选中"全局场景"下的常驻下载按钮组，点击【添加事件】，选择触发事件为**【按下】**

* 添加响应事件：跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (25) (1).png" alt=""><figcaption></figcaption></figure>

</div>

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。



### Step6 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (1657).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/连线组件空白制作_资源.zip" %}
