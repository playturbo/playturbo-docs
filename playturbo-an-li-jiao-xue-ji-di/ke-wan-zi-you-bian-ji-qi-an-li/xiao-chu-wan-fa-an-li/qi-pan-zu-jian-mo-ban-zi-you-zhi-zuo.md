---
description: '#自由编辑器 #模板自由制作 #棋盘组件 #初级难度'
---

# 棋盘组件-模板自由制作

## <mark style="color:blue;">一、对比展示</mark>

我们先来看一下使用**棋盘组件**进行模板自由制作前后的对比：[迭代前](http://tinyurl.com/dft2378n) VS [迭代后](http://tinyurl.com/yzrj25yt)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1303).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">二、迭代内容概括</mark>

本案例使用模板【方正点消】进行迭代，主要展示<mark style="color:red;">如何通过棋盘组件功能调整</mark><mark style="color:red;">**消除玩法**</mark><mark style="color:red;">模板的棋盘与元素布局</mark>

迭代内容主要包含以下步骤：

**1.编辑网格**

即棋盘样式，包含：调整行列数、选择排布形式、是否开启统一格子背景、替换统一格子背景图片

**2.编辑元素**

包含：选用或关闭某元素、替换某元素图片、按权重排版元素

**3.替换棋盘背景图片**

在【玩法模板】替换整个棋盘的背景图片

**4.新增资产**

新增礼盒图片及外发光图片

**5.新增动画**

为新增的礼盒添加通用动画及退场动画

**6.调整事件**

为新增的礼盒增加退场事件

**7.横屏排版**

调整完竖屏，需切换至横屏对排版进行微调

关于棋盘组件的功能介绍可查看[wan-fa-mo-ban](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/wan-fa-mo-ban/ "mention")

<figure><img src="../../../.gitbook/assets/image (1327).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">三、迭代步骤详解</mark>

### **1.编辑网格**

点击【快捷排版】，进入棋盘组件

<figure><img src="../../../.gitbook/assets/image (1305).png" alt=""><figcaption></figcaption></figure>

* 将行列数由（10 x 10）调整为（8 x 8）
* 排布形式有【行列对齐】【行列错位】两种，在本案例中，我们不做改动，保持【行列对齐】
* 点击替换【统一格子背景】，从本地选择我们提前准备好的格子背景图，完成替换

<figure><img src="../../../.gitbook/assets/image (1306).png" alt=""><figcaption></figcaption></figure>

点击上方的【全选】按钮，我们启用全部格子

<figure><img src="../../../.gitbook/assets/image (1307).png" alt=""><figcaption></figcaption></figure>

再通过【橡皮擦】，擦除我们不需要的格子

<figure><img src="../../../.gitbook/assets/image (1308).png" alt=""><figcaption></figcaption></figure>

这样，棋盘的布局我们就调整好了。

### 2.编辑元素

点击进入【元素】编辑界面，我们依次替换5种元素。同样是从本地选择我们提前准备好的元素图片，完成替换

<figure><img src="../../../.gitbook/assets/image (1309).png" alt=""><figcaption></figcaption></figure>

替换完5种元素的图片，我们选中【消除元素1】，然后点击上方的【选择】按钮，在棋盘**已启用的格子上**进行拖动或点击，即可调整**该元素**的布局。然后再依次选中其他消除元素进行布局调整

<figure><img src="../../../.gitbook/assets/image (1313).png" alt=""><figcaption></figcaption></figure>

注：若使用【按权重排版】功能，系统将会按照您填写的权重快速随机生成元素布局，在本案例中，我们不使用该功能

<figure><img src="../../../.gitbook/assets/image (1311).png" alt=""><figcaption></figcaption></figure>

完成所有元素的布局后，点击【确认】即可保存以上调整

<figure><img src="../../../.gitbook/assets/image (1312).png" alt=""><figcaption></figcaption></figure>

### 3.**替换棋盘背景图片**

棋盘属于核心玩法内容，相关资产若不在左侧图层区，则位于【玩法模板】的【玩法编辑】中。我们点击进入【玩法编辑】

<figure><img src="../../../.gitbook/assets/image (1315).png" alt=""><figcaption></figcaption></figure>

选中棋盘背景图层【checkboard】，点击【替换】，上传本地图片到【项目资产】内进行图片替换。完成替换后，我们点击左上角【返回项目编辑】

<figure><img src="../../../.gitbook/assets/image (1316).png" alt=""><figcaption></figcaption></figure>

### 4.新增资产

* 新增礼盒与外发光图片，并调整其位置和大小
* 为了方便后续横屏排版与动画设置，我们分别为“礼盒”以及“礼盒+外发光图片”进行编组
* 然后将整个组移动至图层最下方

<figure><img src="../../../.gitbook/assets/image (1322).png" alt=""><figcaption></figcaption></figure>

### 5.新增动画

选中礼盒图层【box】，添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1323).png" alt=""><figcaption></figcaption></figure>

选中礼盒组图层【Box】，添加动画-退场动画-放大消失。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1324).png" alt=""><figcaption></figcaption></figure>

### 6.调整事件

点击场景1的【事件】，在【奖励反馈】处添加响应事件【从头播放全部动画】，选择组图层【Box】，即礼盒的退场动画

<figure><img src="../../../.gitbook/assets/image (1325).png" alt=""><figcaption></figcaption></figure>

### 7.横屏排版

完成以上内容的调整，我们切换至横屏对新增的资产进行排版调整。直接选中大组【group\_box】，点击【复用竖屏位置尺寸配置】按钮即可一键排版

<figure><img src="../../../.gitbook/assets/image (1326).png" alt=""><figcaption></figcaption></figure>

到此，本案例模板自由制作的全部内容就完成了。
