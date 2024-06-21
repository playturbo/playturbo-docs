---
description: '#自由编辑器 #空白制作 #遮罩组件 #初级难度'
---

# 遮罩组件-空白制作教程

温馨提示：本篇教程主要讲解如何**通过遮罩组件制作出此类玩法（通过点击/拖拽等交互方式，来展示目标图片）的可玩素材，**建议搭配[DEMO](https://tinyurl.com/4j5t5z3u)和[功能介绍文档](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/zu-jian-ku/zhe-zhao-zu-jian.md)食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：通用
* 【交互方式】：拖拽到指定位置
* 【自由度】：固定流程
* 【核心资产】：图片
* 【核心功能】：遮罩形状、被遮罩组、拖拽事件



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

<table><thead><tr><th width="205.33333333333331">手机试玩效果最佳</th><th>竖屏</th><th>横屏</th></tr></thead><tbody><tr><td><img src="../../../.gitbook/assets/image (1892).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/Animation1 (5).gif" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/Animation2 (6).gif" alt="" data-size="original"></td></tr><tr><td>扫码试玩</td><td><a href="https://tinyurl.com/4j5t5z3u">点击试玩</a></td><td><a href="https://tinyurl.com/4j5t5z3u">点击试玩</a></td></tr></tbody></table>



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【黑白底图】和【操作指引】，引导玩家滑动进行涂色；
* 玩家拖动彩虹条
  * 若未拖拽到指定位置，彩虹条返回原位；
  * 若拖拽到指定位置，则涂色成功 跳转结束场景；
* 结束场景 玩家按下按钮跳转商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1893).png" alt="" width="504"><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据上一环节的玩法梳理，我们可将本案例拆分为2个场景来制作

<table data-full-width="false"><thead><tr><th width="133">场景名称</th><th>场景1-核心玩法</th><th>场景2-结束场景</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/image (1905).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1906).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家拖动彩虹条，对图片进行涂色</td><td>成功反馈+跳转按钮</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong><mark style="color:red;">彩色图片(被遮罩组)</mark>、<mark style="color:red;">彩虹条(跟随元素）</mark>、黑白底图、指引手指</p><p><strong>视听包装：</strong>彩虹粒子特效条(跟随元素）、点击音效</p></td><td><p><strong>静帧图片：</strong>彩色图片、跳转按钮</p><p><strong>视听包装：</strong>星星粒子特效、成功音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p><strong>指引手指：</strong>位移缓动</p><p><strong>指引文本：</strong>闪烁</p></td><td><p><strong>反馈文本&#x26;跳转按钮：</strong>脉冲向前</p><p><strong>背景光：</strong>旋转缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p><strong>触发对象：</strong>遮罩形状</p><p><strong>触发事件：</strong>拖拽到指定位置</p><p><strong>响应事件：</strong>跳转到下一场景</p></td><td><p><strong>触发对象：</strong>跳转按钮</p><p><strong>触发事件：</strong>按下</p><p><strong>响应事件：</strong>跳转应用商店</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为**Step2【组件参数设置】**和**Step5【事件设置】**

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进<mark style="color:red;">【项目资产】</mark>内，方便后续添加使用

#### **1. 全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整各资产的位置大小，对资产进行合理编组、排序

<figure><img src="../../../.gitbook/assets/image (1907).png" alt=""><figcaption></figcaption></figure>

#### **2. 普通场景**

1）添加遮罩组件：在场景1中点击【玩法模板】，选择【组件库】下的遮罩组件并添加

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1908).png" alt="" width="404"><figcaption></figcaption></figure>

</div>

2）添加指引手指、指引文案、点击音效，并调整各资产的位置大小

<div align="left">

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

3）在场景2中添加相应反馈资产，并调整各资产的位置大小（可将所有资产编进一个组内，方面后续做横屏适配）

4）将反馈音效的参数设为"入场自动播放1次"

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>

5）勾选场景2为【结束场景】

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;">Step2 - 组件参数设置</mark> <a href="#tpuup" id="tpuup"></a>

#### 1.外观

选中遮罩组件Mask Component，在外观参数下将其尺寸调整到合适

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

#### 2.遮罩设置

<mark style="color:red;">**2.1 被遮罩组**</mark>

【被遮罩组】是【遮罩形状】所覆盖范围内，会显示出的内容

首先，将最后需要展示的图片（彩色图）添加进【被遮罩组】

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**2.2 自定义分组**</mark>

1）添加遮罩分组1（命名为background\_image），将初始展示的图片（黑白图）添加进分组，并拖动调整其层级至最低

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

2）添加遮罩分组2（命名为outer\_frame），将画框图片添加进分组，并拖动调整其层级至最高（装饰图片，需要始终置顶）

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**2.3 遮罩形状**</mark>

1）在本案例中，我们选择遮罩形状为矩形

2）点击【矩形】调起参数弹窗，将遮罩形状的尺寸调整为能够遮住最后展示图片的大小

3）将遮罩形状移动至右侧（不覆盖被遮罩组即可）

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption><p>点击【预览遮罩效果】可查看实际效果</p></figcaption></figure>

<mark style="color:red;">**2.4 跟随元素**</mark>

在【跟随元素】下添加彩虹条和彩虹粒子，并调整其位置大小到合适

<div align="left">

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

</div>

完成以上，我们遮罩组件的参数就设置好了。



### Step3 - 横竖屏适配 <a href="#tpuup" id="tpuup"></a>

完成竖屏的排版后，我们还需对"横屏的排版"以及"横竖屏的屏幕适配方式"进行调整

#### **1.调整横屏排版**

1）在场景1中切换到横屏模式，选中所有最高层级的图层(包含遮罩组件)，使用【复用竖屏位置尺寸配置】功能一键排版

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

2）再分别调整各图层的【位置】和【缩放比例】，让画面展示出完整的核心玩法相关内容

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

3）同理，我们再依次切换到【场景2】和【全局场景】，完成横屏的排版

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

#### 2.调整屏幕适配方式 <a href="#tpuup" id="tpuup"></a>

在本案例中，我们想要竖屏下的产品信息组\[group\_icon]始终位于各机型屏幕的顶部，所以我们调整其"屏幕适配方式"为贴顶适配（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



### Step4 - 动效设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，用到的动画和粒子特效如下，我们依次展开介绍：

场景1：点击指引动画、目标指引动画、合成指引动画、目标元素旋转动画、合成粒子、错误粒子

场景2：奖励面板&跳转按钮的缩放动画、彩带粒子

#### **1.美女序列帧**

1）在擦除组件中点击底图层（Bottom image）的美女序列帧，在弹窗面板中选择【动画】

2）然后我们依次添加缩放动画和位移动画，作为角色擦除成功后的展示动画效果

3）动画参数设置如下：

#### **2.指引手指**

在图层区选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，作为指引动画，参数设置如下：

#### **3.重玩按钮组**

1）选中重玩按钮组\[group\_retry\_btn]，添加透明度动画，作为重玩按钮的渐显出场效果，然后添加缩放动画，引导用户点击重玩

2）动画参数设置如下：

#### 4.爱心粒子特效

1）打开公共粒子库，选择添加爱心粒子，以增强露出美女图片后的画面氛围

2）然后将爱心粒子特效设为"隐藏"状态，在后续我们通过事件来控制粒子的显示和播放



### <mark style="color:red;">Step5 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例与事件设置相关的内容有：开始擦除时隐藏操作指引并播放擦除音效；抬手时暂停播放擦除音效；当擦除区域达到60%时擦除层消失，同时显示并播放相关反馈。接下来，我们按顺序依次讲解

#### <mark style="color:red;">1.图层: 擦除组件</mark>

1）选中擦除组件图层，点击【添加事件】，选择触发事件为**【开始擦除】**

* 依次添加响应事件：隐藏指引文本组、隐藏指引手指组、从头播放擦除音效
* 擦除音效的参数设置为【无限循环】

2）继续【添加事件】，选择触发事件为**【抬手时】**

* 添加响应事件：暂停播放擦除音效

3）继续【添加事件】，选择触发事件为**【到达某一阶段】**

* 注意：因为擦除面积达到目标后，反馈只需触发一次，所以在这里我们勾选该事件"只生效一次"
* 选择【事件判定1】，然后选择【阶段1: 60%】
* 依次添加响应事件：隐藏擦除组Mask、播放美女序列帧分组的全部动画、从头播放重玩按钮组的全部动画、显示并播放爱心粒子特效、从头播放美女害羞音效
* 音效的参数设置为【关闭无限循环】，并【禁用其他音效】



#### <mark style="color:red;">2.图层: 重玩按钮组</mark>

选中重玩按钮组，点击【添加事件】，选择触发事件为**【按下】**

依次添加响应事件：跳转应用商店、上报试玩结束



#### <mark style="color:red;">3.图层: 常驻下载按钮组</mark>

选中常驻下载按钮组，点击【添加事件】，选择触发事件为**【按下】**

添加响应事件：跳转应用商店

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。





### Step6 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (1891).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/擦除组件空白制作_资源.zip" %}
