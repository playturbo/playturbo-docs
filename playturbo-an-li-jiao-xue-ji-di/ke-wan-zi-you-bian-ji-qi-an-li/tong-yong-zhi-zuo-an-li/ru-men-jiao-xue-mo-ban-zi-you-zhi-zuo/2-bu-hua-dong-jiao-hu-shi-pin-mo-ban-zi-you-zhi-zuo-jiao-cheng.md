---
description: '#自由编辑器 #模板自由制作'
---

# 《2步滑动交互视频》模板自由制作教程

## <mark style="color:blue;">**一、对比展示**</mark> <a href="#aluje" id="aluje"></a>

我们先来看一下使用**模板自由制作**前后的对比：[迭代前](https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fgm%2Ft%2F20000734%2F11625%2Fpv%2F23%2F09%2F14%2F65026ea3e762a%2Fproject.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn\&mw\_test=0\&is\_browser\_tips=1\&track\_data=%7B%22pid%22%3A20000734%2C%22uid%22%3A109685%2C%22skin\_id%22%3A11625%2C%22sct%22%3A%22pt\_template\_index%22%2C%22env%22%3A%22p%22%7D) VS [迭代后](https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fps%2Fpreview%2F23%2F10%2F26%2F653a16b712270%2Findex.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn\&mw\_test=0\&is\_browser\_tips=1\&track\_data=%7B%22pid%22%3A1979925%2C%22uid%22%3A109685%2C%22sct%22%3A%22pt\_project\_ps%22%2C%22env%22%3A%22p%22%7D)

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

</div>

## <mark style="color:blue;">**二、迭代内容概括**</mark> <a href="#zxvfg" id="zxvfg"></a>

模板迭代后的改动，主要在以下几方面：

### 1.场景及资产 <a href="#yjysk" id="yjysk"></a>

1）替换资产——视频/音频/图片/文本

2）隐藏资产——隐藏或删除了不需要的资产，包含指引文本组及指引虚线

3）新增场景——原模板仅有一个场景，迭代后的素材新增了“场景2”，即结束页面

4）新增资产——全局场景新增产品名称文本；场景1增加金额面板相关资产及粒子特效；场景2结束页增加奖励面板相关资产及两个下载按钮

### 2.动画及特效 <a href="#hndzz" id="hndzz"></a>

1）修改动画——删减同时替换手指动画，并重新调整参数

2）新增动画——为新增资产添加相应动画，包括：金额文本、下载按钮

### 3.事件设置 <a href="#ylidl" id="ylidl"></a>

1）修改事件——将场景1手势区域2的“按下”事件整个复制到场景2，作为场景事件；修改场景1手势区域2“按下”的响应事件为“跳转应用商店”“跳转下一场景”；

2）新增事件——增加场景1视频“结束时”的响应事件“显示并播放粒子特效”“从头播放文本动画”；为场景2的下载按钮增加跳转事件

### 4.文本翻译 <a href="#cs5zi" id="cs5zi"></a>

将修改及新增后的中文文本翻译为英文，并微调格式

### 5.横屏适配 <a href="#gqxtf" id="gqxtf"></a>

对每个场景的横屏进行排版调整



## <mark style="color:blue;">**三、迭代内容详解**</mark> <a href="#ypqot" id="ypqot"></a>

接下来，我们将配图详细介绍每一步骤。

### 1.场景及资产 <a href="#aqu3j" id="aqu3j"></a>

<mark style="color:red;">**Tips：**</mark>在开始调整前，我们可先统一将新的资产上传到【项目资产】，方便后续替换或新增资产

<figure><img src="../../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

#### **1）替换资产**

主要替换的资产有：背景图/背景音乐/视频/音效/手指图片/logo/下载按钮/免责声明

* 选中需要替换的资产图层，点击右侧【替换】按钮，调起资产库弹窗
* 在【项目资产】一栏选择要替换的资产，点击【+】按钮即可完成替换

<figure><img src="../../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

* 文本可直接选中图层，在右侧文本框直接进行修改
* 调整完文本内容和样式，我们可顺便点击【应用到其他语言】按钮，后续调整其他语言样式时会更加方便快捷

<figure><img src="../../../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

#### **2）隐藏/删除资产**

在本案例中，因准备的视频资产已包含“抽奖”字样的指示，所以模板原有的指引文案就不需要了，指引虚线在迭代时也不需要，可以将其隐藏或删除；

<figure><img src="../../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

#### **3）新增场景**

在本案例中，我们希望场景2的结算画面是置于玩法画面之上的，因此我们可以通过【复制场景】的方式来保留玩法画面，在此基础上新增资产来完成场景2的快速制作。复制完成后，我们可删除无用图层。

<figure><img src="../../../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

同时，在场景2的【场景设置】中，我们选择将全局场景【置于场景底层】

<figure><img src="../../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

#### **4）新增资产**

全局场景：产品名称

场景1：金额面板/金额文本/提现按钮/金币粒子特效

场景2：遮罩/抽奖底图/奖励面板/奖励物品图片/奖励文本/下载按钮\*2/散射光粒子特效

* 点击打开【项目资产】窗口，添加所需资产
* 调整各资产位置及大小，并对同类资产进行编组
* <mark style="color:red;">**注意：**</mark>在新增资产时需关注是否要调整屏幕适配方式（默认居中），如需要，可在调整资产时一并调整

<figure><img src="../../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

### 2.动画及特效 <a href="#ssrbm" id="ssrbm"></a>

#### **1）修改动画**

在本案例中，我们需要将手指做成点击效果，因此我们将“旋转缓动”替换为“缩放缓动”，并删除“透明度缓动”“位移缓动”这两个不需要的动画，并重新调整位置及参数。具体参数设置如下：

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2）新增动画**

2-1）为金额文本“¥0”增加“退场动画-淡出”，关闭自动播放，具体参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

2-2）为金额文本“¥999”增加“入场动画-淡入”，关闭自动播放，具体参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

2-3）为结束页下载按钮1增加“缩放缓动”动画。参数设置如下：

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

</div>

#### **3）新增粒子特效**

调整完动画，我们对粒子特效进行添加和调整。

3-1）金币爆出特效

场景1：点击【资产库】，调起资产库弹窗，在粒子分类下添加需要的粒子特效

<figure><img src="../../../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

简单调整粒子的位置及参数后，我们将其隐藏掉，在后续通过事件触发显示粒子

<figure><img src="../../../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

3-2）背景散射光特效

场景2：点击【资产库】，调起资产库弹窗，在粒子分类下添加需要的粒子特效

<figure><img src="../../../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

简单调整粒子的位置及参数，并将其图层拖拽到奖励面板之下，作为背景显示

<figure><img src="../../../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

### 3.事件设置 <a href="#xhudq" id="xhudq"></a>

#### **1）修改事件**

1-1）将场景1手势区域2的“按下”事件整个复制到场景2，作为场景事件（可根据需要在场景2添加“按下播放点击音效”的响应事件）：

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

</div>

1-2）将场景1手势区域2“按下”的响应事件修改为“跳转应用商店”“跳转下一场景”

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2）新增事件**

2-1）为场景1视频事件“结束时”增加响应事件“显示并播放粒子特效”“从头播放文本的淡入淡出动画”；增加响应事件“执行延迟1.5s”，并将其拖拽到原本的显示手指指引与手势区域2的响应事件前（即在视频播放完成后再出现操作指引，才可继续点击）

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

</div>

2-2)为场景1的提现按钮添加手势区域及“按下-跳转应用商店”的事件

<figure><img src="../../../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

2-3)为场景2的两个下载按钮分别添加“按下-跳转应用商店”的事件

<figure><img src="../../../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

### 4.文本翻译 <a href="#fgprf" id="fgprf"></a>

* 点击【全局设置】，在【默认语言】处点击笔刷图标，调起文本翻译窗口

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

</div>

* 选择目标语言英语，并勾选所有文本，点击【翻译(内测)】按钮进行智能翻译
* 若对翻译结果不满意，我们可直接在文本框内进行微调
* 调整完毕后，点击【提交】，多语言翻译即生效

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (72).png" alt="" width="475"><figcaption></figcaption></figure>

</div>

* 然后我们点击切换到英语版本下预览，对英语文本的样式进行微调

<figure><img src="../../../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

### 5.横屏适配 <a href="#sl2ai" id="sl2ai"></a>

* <mark style="color:red;">注意：每个场景竖屏调整完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）</mark>
* <mark style="color:red;">同时需注意横屏下各图层的屏幕适配方式是否正确</mark>

<figure><img src="../../../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

### 6.**整体预览** <a href="#ozdcc" id="ozdcc"></a>

全部调整完成后，我们对不同机型/不同语言/横竖屏进行整体预览试玩

<figure><img src="../../../../.gitbook/assets/image (1219).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">**四、演示录屏**</mark> <a href="#ypqot" id="ypqot"></a>

注：本视频为以上图文教程的**演示录屏**，仅有画面内容，未添加配音；

视频详细记录了模板自由制作的迭代过程，演示速度基本没有调整，以方便您可以跟着视频一步步操作（如果已能对某一步骤熟悉操作，可酌情跳过）

{% embed url="https://mmp-cdn.rayjump.com/res_store/1985012/65431e829d47e.mp4" %}
