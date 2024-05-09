---
description: '#自由编辑器 #空白制作 #自由画线组件 #初级难度'
---

# 自由画线组件-空白制作教程

温馨提示：本篇教程主要讲解空白制作如何**通过自由画线组件制作出"画线玩法"的可玩素材**，建议搭配[DEMO](https://tinyurl.com/3k5zasma)和[功能介绍文档](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/zu-jian-ku/zi-you-hua-xian-zu-jian.md)食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：画线玩法
* 【交互方式】：开始画线/画线完成
* 【自由度】：固定流程
* 【核心资产】：图片
* 【核心功能】：开始画线-隐藏指引；画线完成-跳转到下一场景



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                          | 竖屏                                                                         | 横屏                                                                         |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1636).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/1 (3).gif" alt="" data-size="original"> | <img src="../../../.gitbook/assets/2 (7).gif" alt="" data-size="original"> |
| 扫码试玩                                                                              | [点击试玩](https://tinyurl.com/3k5zasma)                                       | [点击试玩](https://tinyurl.com/3k5zasma)                                       |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示"一个额头有痘的女孩"和"操作指引"，引导玩家在额头位置画线挤痘痘

2）玩家在额头位置画出任意线条，播放【成功反馈】，然后进入结束页面

3）结束页玩家任意按下，跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1637).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据上一环节的玩法梳理，我们可将本案例拆分为3个场景来制作

<table data-full-width="false"><thead><tr><th width="120">场景名称</th><th width="226">场景1-核心玩法</th><th>场景2-结果反馈</th><th>场景3-结束页面</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/image (1639).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1640).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1638).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>引导玩家在额头位置画线挤痘</td><td>玩家画线完成后播放成功反馈</td><td>产品信息+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>痘痘女孩、指引光圈和粉刺针</p><p><strong>视听包装：</strong>点击音效</p></td><td><p><strong>静帧图片：</strong>无痘女孩、反馈文本</p><p><strong>视听包装：</strong>成功音效、彩带粒子、星星粒子</p></td><td><p><strong>静帧图片：</strong>产品信息、跳转按钮</p><p><strong>视听包装：</strong>星星粒子</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>粉刺针：位移缓动</p><p>指引文本：位移缓动</p><p>指引光圈：透明度缓动</p></td><td>反馈文本：缩小出现</td><td>跳转按钮：脉冲向前</td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：自由画线组件</p><p>Draw Lines Component</p><p>触发事件：画线完成</p><p>响应事件：跳转到下一场景</p></td><td><p>触发对象：场景2</p><p>触发事件：定时触发</p><p>响应事件：跳转到下一场景</p></td><td><p>触发对象：场景3</p><p>触发事件：按下</p><p>响应事件：跳转应用商店</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step4【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整位置大小

<figure><img src="../../../.gitbook/assets/image (1642).png" alt=""><figcaption></figcaption></figure>

#### **2.普通场景**

**2-1）场景1**

1）在场景1中添加核心玩法相关资产：痘痘女孩/指引光圈/粉刺针/指引文本/点击音效

2）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名

<mark style="color:red;">**3）添加组件：**</mark>点击【玩法模板】，在【组件库】下添加 自由画线组件&#x20;

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1643).png" alt="" width="476"><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**4）调整组件参数：**</mark>可直接 拖拽/拉伸 画布中的绿色矩形，将组件的位置大小调整到额头位置。然后设置画出线条的颜色和粗细即可

<figure><img src="../../../.gitbook/assets/image (1644).png" alt=""><figcaption></figcaption></figure>

**2-2）场景2**

1）在场景2中添加结果反馈相关资产

2）调整各资产到合适的位置大小

<figure><img src="../../../.gitbook/assets/image (1647).png" alt=""><figcaption></figcaption></figure>

**2-3）场景3**

1）新建场景3，并添加产品信息相关资产

2）勾选场景3为【结束场景】，以便上报试玩结束

3）取消启用场景3的【全局场景】

<figure><img src="../../../.gitbook/assets/image (1648).png" alt=""><figcaption></figcaption></figure>



### Step2 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### 1.调整横屏排版

1）在场景1中切换到横屏模式，选中所有最高层级的图层(包含自由画线组件图层)

2）使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整各图层的【位置】和【缩放比例】，让画面展示出完整的核心玩法相关内容

<figure><img src="../../../.gitbook/assets/image (1649).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1650).png" alt=""><figcaption></figcaption></figure>

3）同理，我们再依次切换到场景2、场景3和【全局场景】，使用【复用竖屏位置尺寸配置】功能一键排版，再微调其位置大小



#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的常驻信息组始终位于各机型屏幕的顶部，所以我们调整其"屏幕适配方式"为贴顶适配（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1651).png" alt=""><figcaption></figcaption></figure>



### Step3 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，用到的动画和粒子特效如下，我们依次展开介绍：

场景1：粉刺针移动动画、指引文本移动动画、指引光圈闪烁动画

场景2：反馈文本入场动画、彩带粒子、星星粒子

场景3：跳转按钮缩放动画、星星粒子

#### **1.粉刺针：位移缓动**

1）在擦除组件中点击底图层（Bottom image）的美女序列帧，在弹窗面板中选择【动画】

2）然后我们依次添加缩放动画和位移动画，作为角色擦除成功后的展示动画效果

3）动画参数设置如下：

#### **2.**指引文本**：位移缓动**

在图层区选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，作为指引动画，参数设置如下：

#### **3.**指引光圈：透明度缓动

1）选中重玩按钮组\[group\_retry\_btn]，添加透明度动画，作为重玩按钮的渐显出场效果，然后添加缩放动画，引导用户点击重玩

2）动画参数设置如下：

#### 4.反馈文本：缩小出现

#### 5.跳转按钮：脉冲向前

#### 6.粒子特效：彩带粒子&星星粒子

1）打开公共粒子库，选择添加爱心粒子，以增强露出美女图片后的画面氛围

2）

3）调整好竖屏的位置，还需切换到横屏进行调整











### <mark style="color:red;">Step4 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例与事件设置相关的内容有：开始擦除时隐藏操作指引并播放擦除音效；抬手时暂停播放擦除音效；当擦除区域达到60%时擦除层消失，同时显示并播放相关反馈。接下来，我们按顺序依次讲解

#### <mark style="color:red;">1.图层: 擦除组件</mark>

1）选中擦除组件图层，点击【添加事件】，选择触发事件为**【开始擦除】**

* 依次添加响应事件：隐藏指引文本组、隐藏指引手指组、从头播放擦除音效
* 擦除音效的参数设置为【无限循环】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (18) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）继续【添加事件】，选择触发事件为**【抬手时】**

* 添加响应事件：暂停播放擦除音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (19) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）继续【添加事件】，选择触发事件为**【到达某一阶段】**

* 注意：因为擦除面积达到目标后，反馈只需触发一次，所以在这里我们勾选该事件"只生效一次"
* 选择【事件判定1】，然后选择【阶段1: 60%】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (22) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 依次添加响应事件：隐藏擦除组Mask、播放美女序列帧分组的全部动画、从头播放重玩按钮组的全部动画、显示并播放爱心粒子特效、从头播放美女害羞音效
* 音效的参数设置为【关闭无限循环】，并【禁用其他音效】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (21) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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





### Step5 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/擦除组件空白制作_资源.zip" %}
