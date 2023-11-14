---
description: '#自由编辑器'
---

# 变化曲线

## 变化曲线动画参数说明

<table><thead><tr><th width="123">参数类型</th><th width="166">说明</th><th width="237">操作步骤</th><th width="197" align="center">图片</th></tr></thead><tbody><tr><td><strong>变化曲线</strong></td><td><p><br>1. 支持编辑动画曲线</p><p><br>2. 提供6种缓动基础样式</p><p><br>3. 支持编辑/删除/复用自定义曲线<br></p></td><td><p><strong>【选择曲线模版】</strong><br>1. 点击变化曲线缩略图，进入曲线编辑器面板<br>2. 选择曲线模版</p><p>3.双击曲线可添加关键帧，选中关键帧可进行删除或调整曲线弧度<br>4.点击保存即可完成变化曲线设置<br><br><strong>【自定义编辑变化曲线】</strong><br>1. 点击变化曲线缩略图，进入曲线编辑器面板<br>2. 自定义编辑变化曲线<br>3. 双击曲线可添加关键帧，选中关键帧可进行删除或调整曲线弧度<br>4. 点击【保存当前曲线】<br>5. 选择已保存的变化曲线，点击保存即可完成变化曲线设置</p></td><td align="center"><br><br>缓动基础样式<br><img src="../../../../../../../.gitbook/assets/image (92) (1).png" alt=""><br><br>曲线编辑器面板<br><img src="../../../../../../../.gitbook/assets/image (93) (1).png" alt=""></td></tr></tbody></table>

## 调整动画曲线

⭐曲线可以在“曲线编辑器”中进行调整（点击曲线即可打开编辑器）:

* 横轴代表时间，纵轴代表动画对应的各种变量（位移、透明度、缩放比例、旋转角度等）；
* 起点(0, 0)为动画运动的默认初始状态，终点(1, 1)为动画运动的默认结束状态；
* 横向移动锚点会直接改变物体运动时间，调整曲线斜率会直接改变物体运动速度的分布（曲线越陡峭速度越快，曲线越平缓速度越慢）；

<figure><img src="../../../../../../../.gitbook/assets/2 (17).png" alt=""><figcaption></figcaption></figure>

⭐举例说明：以位移缓动为例，横轴代表时间，纵轴代表位移距离，下面将列举一些常见效果调整方法

**a. 物体在起点停留一段时间后，再开始运动：**

① 将曲线起点向右移动（延迟动画开始时间），物体会在红框时间段内完成移动；

<div align="left">

<figure><img src="../../../../../../../.gitbook/assets/3 (16).png" alt="" width="375"><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../../../../../.gitbook/assets/常见问题1.gif" alt=""><figcaption></figcaption></figure>

</div>

**b. 物体在始末位置停留一段时间，并来回运动：**

① 动画【循环次数】选择：双向循环；

② 将曲线起点向右移动+ 将曲线终点向左移动（延迟动画开始时间并提早结束动画），物体会在在红框时间段内完成移动；

<div align="left">

<figure><img src="../../../../../../../.gitbook/assets/5 (14).png" alt="" width="375"><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../../../../../.gitbook/assets/常见问题2.gif" alt=""><figcaption></figcaption></figure>

</div>
