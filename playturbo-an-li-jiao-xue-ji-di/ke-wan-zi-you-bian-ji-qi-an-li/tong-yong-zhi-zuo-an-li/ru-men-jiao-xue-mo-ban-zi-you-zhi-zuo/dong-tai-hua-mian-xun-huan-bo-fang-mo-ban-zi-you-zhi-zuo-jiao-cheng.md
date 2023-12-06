---
description: '#自由编辑器 #模板自由制作'
---

# 《动态画面循环播放》模板自由制作教程

## <mark style="color:blue;">**一、对比展示**</mark> <a href="#aluje" id="aluje"></a>

我们先来看一下使用**模板自由制作**前后的对比：[迭代前](https://tinyurl.com/27txy7jm) VS[ 迭代后](https://tinyurl.com/saktyf7h)

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

</div>

## <mark style="color:blue;">**二、迭代内容概括**</mark> <a href="#zxvfg" id="zxvfg"></a>

模板迭代后的改动，主要在以下几方面：

### 1.场景及资产 <a href="#yjysk" id="yjysk"></a>

1）替换资产——视频/音频/图片/文本

2）新增场景——原模板仅有一个场景，迭代后的素材新增了“场景2”，即结束页面

3）新增资产——场景1求救相关资产：图片/文本/音效；场景2结束页相关资产：图片/文本

### 2.动画及特效 <a href="#hndzz" id="hndzz"></a>

1）修改动画——替换手指动画，并重新调整参数

2）新增动画——为新增资产添加相应动画

### 3.事件设置 <a href="#ylidl" id="ylidl"></a>

1）修改事件——将场景1的“按下”事件整个复制到场景2，作为场景事件；修改场景1“按下”的响应事件为“跳转下一场景”“暂停播放求救音效”

2）新增事件——为场景2的下载按钮增加跳转事件

### 4.文本翻译 <a href="#cs5zi" id="cs5zi"></a>

将修改及新增后的中文文本翻译为英文，并微调格式

### 5.横屏适配 <a href="#gqxtf" id="gqxtf"></a>

对每个场景的横屏进行排版调整



## <mark style="color:blue;">**三、迭代内容详解**</mark> <a href="#ypqot" id="ypqot"></a>

接下来，我们将配图详细介绍每一步骤。

### 1.场景及资产 <a href="#aqu3j" id="aqu3j"></a>

<mark style="color:red;">**Tips：**</mark>在开始调整前，我们可先统一将新的资产上传到【项目资产】，方便后续替换或新增资产

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

</div>

#### **1）替换资产**

主要替换的资产有：背景图/背景音乐/视频/音效/手指图片(杀虫水)/指引文本/logo/下载按钮

* 选中需要替换的资产图层，点击右侧【替换】按钮，调起资产库弹窗
* 在【项目资产】一栏选择要替换的资产，点击【+】按钮即可完成替换

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

</div>

* 文本可直接选中图层，在右侧文本框直接进行修改
* 调整完文本内容和样式，我们可顺便点击【应用到其他语言】按钮，后续调整其他语言样式时会更加方便快捷

<figure><img src="../../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

#### **2）新增场景**

在场景缩略图处右键选择【新建场景】或直接点击【+】按钮，即可在当前场景下增加一个新的场景

<figure><img src="../../../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

#### **3）新增资产**

场景1：警示图片/求救文案/求救音效

场景2：logo/下载按钮

* 点击打开【项目资产】窗口，添加所需资产
* 调整位置及大小
* <mark style="color:red;">**注意：**</mark>在新增资产时需关注是否要调整屏幕适配方式（默认居中），如需要，可在调整资产时一并调整

<figure><img src="../../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### 2.动画及特效 <a href="#ssrbm" id="ssrbm"></a>

#### **1）修改动画**

将手指（杀虫水）动画由“位移缓动”替换为“缩放缓动”，并重新调整位置及参数。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

#### **2）新增动画**

2-1）为一张警示图片增加“强调动画-闪烁”。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

设置完成后，我们点击复制动画按钮，将该闪烁动画粘贴到另外三张警示图片上：按住Ctrl键(苹果电脑需按钮Command键)，选中另外三张图片的图层，点击上方【粘贴-仅粘贴图层动画】即可

<figure><img src="../../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

2-2）为求救文本增加“位移缓动”动画。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

2-3）为结束页下载按钮增加“缩放缓动”动画。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### 3.事件设置 <a href="#xhudq" id="xhudq"></a>

#### **1）修改事件**

1-1）将场景1的图层事件“按下”整个复制到场景2，作为场景事件：

<figure><img src="../../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

1-2）将场景1的图层事件“按下”的响应事件修改为“跳转下一场景”，并添加响应事件“暂停播放求救音效”

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2）新增事件**

为场景2的下载按钮增加事件“按下-跳转应用商店”

<figure><img src="../../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

### 4.文本翻译 <a href="#fgprf" id="fgprf"></a>

* 点击【全局设置】，在【默认语言】处点击笔刷图标，调起文本翻译窗口

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

</div>

* 选择目标语言英语，并勾选所有文本，点击【翻译(内测)】按钮进行智能翻译
* 若对翻译结果不满意，我们可直接在文本框内进行微调
* 调整完毕后，点击【提交】，多语言翻译即生效

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (47).png" alt="" width="470"><figcaption></figcaption></figure>

</div>

* 然后我们点击切换到英语版本下预览，对英语文本的样式进行微调

<figure><img src="../../../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

### 5.横屏适配 <a href="#sl2ai" id="sl2ai"></a>

* <mark style="color:red;">注意：每个场景竖屏调整完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）</mark>
* <mark style="color:red;">同时需注意横屏下各图层的屏幕适配方式是否正确</mark>

<figure><img src="../../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

### 6.**整体预览** <a href="#ozdcc" id="ozdcc"></a>

全部调整完成后，我们对不同机型/不同语言/横竖屏进行整体预览试玩

<figure><img src="../../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">**四、演示录屏**</mark> <a href="#ypqot" id="ypqot"></a>

注：本视频为以上图文教程的**演示录屏**，仅有画面内容，未添加配音；

视频详细记录了模板自由制作的迭代过程，演示速度基本没有调整，以方便您可以跟着视频一步步操作（如果已能对某一步骤熟悉操作，可酌情跳过）

{% embed url="https://mmp-cdn.rayjump.com/res_store/1984991/654314b824f7d.mp4" %}
