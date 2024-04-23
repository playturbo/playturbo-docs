---
description: '#自由编辑器 #空白制作 #擦除组件 #初级难度'
---

# 擦除组件-空白制作教程

温馨提示：本篇教程主要讲解空白制作如何**通过擦除组件制作出"擦除玩法"的可玩素材**，建议搭配[DEMO](https://tinyurl.com/4xby5rvh)和[功能介绍文档](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/zu-jian-ku/ca-chu-zu-jian.md)食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：擦除玩法
* 【交互方式】：开始擦除/到达某一阶段
* 【自由度】：固定流程
* 【核心资产】：图片
* 【核心功能】：到达某一阶段-隐藏擦除层



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                          | 竖屏                                                                                  | 横屏                                                                                  |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1504).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation1 (1).gif" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation2 (2).gif" alt="" data-size="original"> |
| 扫码试玩                                                                              | [点击试玩](https://tinyurl.com/4xby5rvh)                                                | [点击试玩](https://tinyurl.com/4xby5rvh)                                                |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示【美女被遮挡画面】，美女角色默认进行序列帧播放

2）出现【操作指引】，引导玩家滑动擦除遮罩

3）玩家在遮罩位置任意滑动，遮罩即被实时擦除，露出美女身体

4）当遮罩区域被擦除60%，遮罩消失，并出现完整的美女图片和重玩按钮

5）玩家按下按钮，跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1506).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**因本案例玩法较简单，我们只需用 1 个场景来制作即可

<table data-full-width="false"><thead><tr><th width="164">场景名称</th><th>场景1-核心玩法</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/Animation1 (1).gif" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家在遮罩位置任意滑动擦除遮罩，来显示出完整的美女图片</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong><mark style="color:red;">遮罩(擦除层)</mark>、操作指引、重玩按钮</p><p><strong>序列帧：</strong><mark style="color:red;">美女底图</mark></p><p><strong>视听包装：</strong>爱心粒子特效、擦除音效、美女害羞音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>手指指引：位移缓动</p><p>美女放大出现：缩放缓动+位移缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：擦除组件Erase Component</p><p>触发事件：到达某一阶段</p><p>响应事件：隐藏擦除层</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step2【组件参数设置】和Step5【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整位置大小

<figure><img src="../../../.gitbook/assets/image (1507).png" alt=""><figcaption></figcaption></figure>

#### **2.普通场景**

1）添加擦除组件：点击【玩法模板】，在【组件库】下将擦除组件添加进场景1

<figure><img src="../../../.gitbook/assets/image (1509).png" alt=""><figcaption></figcaption></figure>

2）将指引手、指引文案和底板、重玩按钮、音效相继添加进场景1

3）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名

4）在本案例中，我们只需要一个普通场景，所以可以删除场景2

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;">Step2 - 组件参数设置</mark> <a href="#tpuup" id="tpuup"></a>

1.点击右上方【擦除设置】，进入擦除组件参数编辑面板

<figure><img src="../../../.gitbook/assets/image (1513).png" alt=""><figcaption></figcaption></figure>

2.依次在**擦除层（Mask）**中添加擦除飘带图片，在**底图层（Bottom image）**中添加角色序列帧图片，然后将资产调整到合适的位置大小

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3.然后我们根据实际需求，调整【擦除笔触设置】。在本案例中，我们选择使用60\*60大小的圆形笔触，不添加跟手图片

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1515).png" alt=""><figcaption></figcaption></figure>

</div>

4.针对擦除层进行**事件判定**设置

1）判断时机：在本案例中，我们想要在擦除过程中实时判定擦除进度，所以我们选择判断时机为【擦除过程实时判定】

2）添加事件判定：在本案例中，我们想要实现"当擦除面积达到60%时，触发相应反馈"，所以在这里，我们选择要判定的区域为擦除层"erase\_mask"，然后点击【新增阶段】，将阶段1设置为60%

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

完成以上，我们擦除组件的基本参数就设置好了。





### Step3 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）切换到横屏模式，选中所有最高层级的图层(包含擦除组件图层)

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层的【位置】和【缩放比例】，让画面展示出完整的擦除组件相关内容

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）同理，我们再切换到【全局场景】，选择LOGO和常驻下载按钮组，使用【复用竖屏位置尺寸配置】功能一键排版，再微调其位置大小

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

1）在本案例中，我们想让常驻信息在竖屏下依次贴顶、贴底适配，在横屏下靠左上角适配，所以我们分别调整横竖屏下的屏幕适配方式

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）在场景1中，我们想要横屏下的重玩按钮组和指引文本组始终位于屏幕底部，所以我们依次将其屏幕适配方式调整为贴底适配（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1512).png" alt=""><figcaption></figcaption></figure>



### Step4 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们用到的动画和粒子特效有：美女序列帧(底图层)动画、指引手指动画、重玩按钮组动画、爱心粒子特效

#### **1.美女序列帧**

1）在擦除组件中点击底图层（Bottom image）的美女序列帧，在弹窗面板中选择【动画】

2）然后我们依次添加缩放动画和位移动画，作为角色擦除成功后的展示动画效果

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）动画参数设置如下：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1).png" alt="" width="556"><figcaption></figcaption></figure>

</div>

#### **2.指引手指**

在图层区选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，作为指引动画，参数设置如下：

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **3.重玩按钮组**

1）选中重玩按钮组\[group\_retry\_btn]，添加透明度动画，作为重玩按钮的渐显出场效果，然后添加缩放动画，引导用户点击重玩

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2）动画参数设置如下：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

#### 4.爱心粒子特效

1）打开公共粒子库，选择添加爱心粒子，以增强露出美女图片后的画面氛围

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2）然后将爱心粒子特效设为"隐藏"状态，在后续我们通过事件来控制粒子的显示和播放

<div align="left">

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



### <mark style="color:red;">Step5 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例与事件设置相关的内容有：开始擦除时隐藏操作指引并播放擦除音效；抬手时暂停播放擦除音效；当擦除区域达到60%时擦除层消失，同时显示并播放相关反馈。接下来，我们按顺序依次讲解

#### <mark style="color:red;">1.图层: 擦除组件</mark>

1）选中擦除组件图层，点击【添加事件】，选择触发事件为**【开始擦除】**

* 依次添加响应事件：隐藏指引文本组、隐藏指引手指组、从头播放擦除音效
* 擦除音效的参数设置为【无限循环】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (18) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）继续【添加事件】，选择触发事件为**【抬手时】**

* 添加响应事件：暂停播放擦除音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (19) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）继续【添加事件】，选择触发事件为**【到达某一阶段】**

* 注意：因为擦除面积达到目标后，反馈只需触发一次，所以在这里我们勾选该事件"只生效一次"
* 选择【事件判定1】，然后选择【阶段1: 60%】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (22) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 依次添加响应事件：隐藏擦除组Mask、播放美女序列帧分组的全部动画、从头播放重玩按钮组的全部动画、显示并播放爱心粒子特效、从头播放美女害羞音效
* 音效的参数设置为【关闭无限循环】，并【禁用其他音效】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (21) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">2.图层: 重玩按钮组</mark>

选中重玩按钮组，点击【添加事件】，选择触发事件为**【按下】**

依次添加响应事件：跳转应用商店、上报试玩结束

<figure><img src="../../../.gitbook/assets/image (23) (1) (1).png" alt=""><figcaption></figcaption></figure>



#### <mark style="color:red;">3.图层: 常驻下载按钮组</mark>

选中常驻下载按钮组，点击【添加事件】，选择触发事件为**【按下】**

添加响应事件：跳转应用商店

<figure><img src="../../../.gitbook/assets/image (24) (1) (1).png" alt=""><figcaption></figcaption></figure>

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。





### Step6 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/擦除组件空白制作_资源.zip" %}
