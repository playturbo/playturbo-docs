---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# IEC《动态画面循环播放》教程

温馨提示：入门难度模板《动态画面循环播放》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：1步跳转
* 【线程】：单线程
* 【核心资产】：视频（1段/可循环播放）
* 【功能】：动画-闪烁、动画-位移缓动、事件-按下跳转应用商店



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1059).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1057).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1058).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/33r7xwhn)                                                 | [点击试玩](https://tinyurl.com/33r7xwhn)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，初始画面展示一段循环播放的动态画面，显示蛋糕周围爬满了虫子；
* 出现操作指引，引导玩家点击画面来喷射杀虫水；
* 玩家全屏任意按下，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们判断本案例只需设置1个场景即可

<table><thead><tr><th width="178">场景名称</th><th>场景1-诱导点击</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1057).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>动态画面循环播放，引导玩家点击驱赶虫子</td></tr><tr><td><strong>动画</strong></td><td><p>【杀虫水(即指引手指)】：位移缓动</p><p>【指引文案】：闪烁</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-组节点（画面需足够大）</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【视频】：视频（设置为入场自动播放、无限循环）</p><p>【音频】：背景音乐、点击音效</p><p>【图片】：背景图片、杀虫水(手指)、指引文案背景图、logo、CTA按钮</p><p>【文本】：指引文案、下载文案</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1055).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1**

1）在【场景1】中添加视频、音效、指引手指(杀虫水)、指引文案、logo、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.指引文案**

在左侧图层处选中指引文本【guidanceText】，添加动画-强调动画-闪烁。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

#### **2.杀虫水（手指）**

在左侧图层处选中杀虫水图片【hand】，添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.图层事件-组节点**

1）选中组节点（注：因需设置全屏按下跳转商店，所以组的范围需足够大；也可直接在场景1上设置场景事件，步骤同理）；

2）添加事件-按下；

3）添加响应事件-跳转应用商店；

4）其他响应事件：设置埋点信息/上报试玩结束/从头播放点击音效

<figure><img src="../../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

**2.图层事件-CTA按钮**

选中按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">**六、演示录屏**</mark> <a href="#ypqot" id="ypqot"></a>

注：本视频为以上图文教程的**演示录屏**，仅有画面内容，未添加配音；

视频详细记录了本案例空白制作的操作过程，演示速度基本没有调整，方便您查看学习（如果您已能对某一步骤熟悉操作，可酌情跳过）

此外，在演示录屏下方还为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器

{% embed url="https://mmp-cdn.rayjump.com/res_store/2110668/65eaae046dd0e.mp4" %}

{% file src="../../../../.gitbook/assets/动态画面循环播放_资源.zip" %}
