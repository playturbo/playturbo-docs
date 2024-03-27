---
description: '#自由编辑器 #空白制作 #通用制作 #简单难度'
---

# 交互视频《模拟移动》教程

温馨提示：本篇教程主要讲解**如何通过交互视频来实现"模拟玩家实时操作"的效果**，建议搭配DEMO食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：普遍适用(尤其是摇杆玩法产品)
* 【交互方式】：按下/抬起
* 【自由度】：固定流程
* 【核心资产】：视频
* 【核心功能】：按下-继续播放视频；抬起-暂停播放视频



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                           | 竖屏                                                                                | 横屏                                                                                 |
| ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| <img src="../../../../.gitbook/assets/image (13).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/Animation.gif" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/Animation2.gif" alt="" data-size="original"> |
| 扫码试玩                                                                               | [点击试玩](https://tinyurl.com/3tndebp6)                                              | [点击试玩](https://tinyurl.com/3tndebp6)                                               |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，自动播放【丧失围攻视频】<mark style="background-color:yellow;">（初始视频1）</mark>

2）视频播放结束，出现【操作指引】，引导玩家按下继续对抗丧尸

3）玩家全屏任意按下，播放【对抗丧尸视频】<mark style="background-color:yellow;">（核心视频2）</mark>，同时加载进度条；每当玩家抬起，暂停播放【对抗丧尸视频】，同时进度条停止加载，并出现【操作指引】

4）视频播放结束，自动跳转商店，玩家从商店返回可继续试玩

5）玩家全屏任意按下，播放【对抗丧尸视频】<mark style="background-color:yellow;">（核心视频3）</mark>，同时加载进度条；每当玩家抬起，暂停播放【对抗丧尸视频】，同时进度条停止加载，并出现【操作指引】

6）视频播放结束，进度条停止加载，并出现【操作指引】，玩家按下即跳转商店

<div align="left">

<figure><img src="../../../../.gitbook/assets/Animation2.gif" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**因本案例玩法较简单，我们只需用 1 个场景来制作即可

<table data-full-width="false"><thead><tr><th width="164">场景名称</th><th>场景1-核心玩法</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/Animation.gif" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家按下就播放视频，抬手就暂停播放视频，以此来模拟玩家实时交互的效果</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong>进度条、操作指引</p><p><strong>视频：</strong>初始视频1、核心视频2、核心视频3</p><p><mark style="color:red;">注：因为我们对本案例的DEMO有"核心视频播放4s后,有一次强制跳转"的设定，为了便于理解和制作，将核心视频拆分成了两段(核心视频2总时长为4s)。若您不需要中途的强制跳转，只需准备一段核心视频即可</mark></p></td></tr><tr><td><strong>核心动画</strong></td><td><p>进度条：缩放缓动</p><p>手指指引：位移缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：视频图层</p><p>触发事件：按下；抬起</p><p>响应事件：继续播放视频；暂停播放视频</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心部分为Step3【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局设置**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息

#### **2.场景1**

1）将所需视频、图片添加进场景1

<mark style="color:red;">温馨提示："进度条"和"操作指引"相关资产，都可从【预设库】直接获取哦！</mark>

<figure><img src="../../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

4）调整横屏排版：可选中所有最高层级的图层，使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整【位置】和【缩放比例】即可

<figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

5）调整屏幕适配方式：在本案例中，我们想要竖屏下的产品信息始终位于屏幕底部，所以我们要调整其适配方式。直接选中该图层，在右侧【屏幕适配方式】处点击向下图标即可（其他图层默认居中适配，无需调整）

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



### Step2 - 动画设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，需要设置动画的资产有：指引手指、指引文案、进度条(选做)、角色(选做)

<mark style="color:red;">温馨提示：若您使用了预设，则无需自己设置动画！</mark>

#### **1.指引手指**

1）选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，参数设置如下(手指横向移动动画)：

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

2）选中手指组\[gf\_1]，添加动画-通用-位移缓动，参数设置如下(手指纵向移动动画)：

<figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

#### **2.指引文案**

选中指引文本\[tguidelines]，添加动画-强调动画-上下来回，参数设置如下（设置完成后可隐藏整个指引组，在后续通过事件控制）：

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

#### 3.进度条(选做)

1）选中进度条图片\[progress\_bar]，将其【锚点】修改为（0,50），并取消勾选【参数横竖屏拆分】

注意：进度条图片左右需贴边，不能留空

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

2）添加动画-通用-缩放缓动，参数设置如下：

注意：这里的【持续时间】代表的是进度条加载到头所需的总时长。在本案例中，我们设定了"在进度条快加载完时，玩家不能再交互"，也就是当所有视频播放结束后，进度条需要差一截才到头，所以就需要"进度条播放的总时长＞所有视频加起来的总时长"。本案例的三段视频总时长为8.7s左右，所以在这里我们可以将进度条的【持续时间】设置为10s或更长

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

#### 4.角色(选做)

1）选中角色图片\[role\_1]，将其【锚点】修改为（50,100），并取消勾选【参数横竖屏拆分】

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

2）添加动画-通用-缩放缓动，参数设置如下（设置完成后可隐藏该图层，在后续通过事件控制）：

<figure><img src="../../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



### <mark style="background-color:red;">Step3 - 事件设置</mark> <a href="#umduz" id="umduz"></a>



####









\




### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../../.gitbook/assets/模拟移动交互视频_资源.zip" %}
