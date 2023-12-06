---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 交互视频《2步滑动》教程

温馨提示：入门难度模板《2步滑动交互视频》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：滑动
* 【交互次数】：2步跳转
* 【线程】：单线程
* 【核心资产】：视频（1段/连贯的）
* 【功能】：动画-旋转缓动、事件-按下从头播放视频、事件-按下隐藏素材、事件-视频结束时显示素材



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1060).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1061).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1062).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/3n6bk64j)                                                 | [点击试玩](https://tinyurl.com/3n6bk64j)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【初始指引画面】，引导玩家滑动抓羊；
* 玩家全屏任意滑动，播放【羊羊飞到车里视频】；
* 视频播放结束，再次出现【手指指引】，引导玩家继续滑动抓羊；
* 玩家全屏任意按下，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们判断本案例只需设置1个场景即可

<table><thead><tr><th width="178">场景名称</th><th>场景1-诱导滑动</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1063).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>视频暂停状态，引导玩家滑动抓羊</td></tr><tr><td><strong>动画</strong></td><td><p>【指引文案】：位移缓动</p><p>【指引虚线】：透明度缓动</p><p>【指引手指】：旋转缓动+透明度缓动+位移缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-手势区域（画面需足够大）</p><p>触发操作：按下（或任意滑动）</p><p>响应事件：从头播放视频</p><hr><p>触发对象：图层-视频</p><p>触发操作：结束时</p><p>响应事件：显示素材</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【视频】：视频（关闭自动播放、无限循环）</p><p>【音频】：背景音乐、滑动音效、羊羊入车音效</p><p>【图片】：背景图片、手指、指引虚线、指引文案背景图、logo、CTA按钮</p><p>【文本】：指引文案、下载文案</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1064).png" alt=""><figcaption></figcaption></figure>

#### **2.全局场景**

1）在【全局场景】中添加常驻信息：logo、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1065).png" alt=""><figcaption></figcaption></figure>

**3.场景1**

1）在【场景1】中添加视频、音效、指引手指、指引虚线、指引文案

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1066).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.指引文案**

在左侧图层处选中指引文本组【group\_guide】，添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1067).png" alt=""><figcaption></figcaption></figure>

#### **2.指引虚线**

在左侧图层处选中指引虚线图片【hand\_line】，添加动画-通用-透明度缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1068).png" alt=""><figcaption></figcaption></figure>

#### **3.指引手指**

因手指在引导滑动时，需要进行旋转和位移，因此我们为手指设置2个通用动画，分别为：旋转缓动、位移缓动；为使手指效果更加自然，还可添加透明度缓动动画。

1）在左侧图层处选中手指图片【gf\_hand】，添加动画-通用-旋转缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1069).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1070).png" alt=""><figcaption></figcaption></figure>

3）继续添加动画-通用-透明度缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1071).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.**图层事件-手势区域1

因我们想要玩家全屏可滑动，且要区分第一次滑动与第二次滑动的区域，因此我们添加2个较大范围的手势区域，来分别作为第一次滑动与第二次滑动的区域，并在手势区域上设置事件。

1）选中手势区域1图层；

2）添加事件-按下；

_（说明：此玩法也可将触发事件改为“任意滑动”，但使用“按下”会更容易触发事件）_

3）添加响应事件-从头播放视频；从头播放滑动音效；

4）添加响应事件-隐藏素材指引相关；隐藏素材手指区域1；

_（说明：当视频播放后，我们需将指引手指与文案隐藏掉，同时隐藏掉手势区域1，因为在第一次滑动过后，手势区域1就无存在的意义了，第二次滑动是在手势区域2上进行的）_

5）其他响应事件：设置埋点信息；执行延迟0.5秒后播放羊羊入车音效

<figure><img src="../../../../.gitbook/assets/image (1072).png" alt=""><figcaption></figcaption></figure>

**2.图层事件-视频**

1）选中视频图层；

2）添加事件-结束时；

3）添加响应事件-显示素材指引相关；显示素材手指区域2；

<figure><img src="../../../../.gitbook/assets/image (1073).png" alt=""><figcaption></figcaption></figure>

#### **3.图层事件-手势区域2**

1）选中手势区域2图层；

2）添加事件-按下；

3）添加响应事件-跳转应用商店；设置埋点信息；上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (1074).png" alt=""><figcaption></figcaption></figure>

**4.图层事件-CTA按钮**

选中按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1075).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1076).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1077).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1078).png" alt=""><figcaption></figcaption></figure>
