---
description: '#自由编辑器'
---

# 动画制作

## <mark style="color:blue;">一、效果实现</mark>

### 1.常用操作指引（手指动画）

<table data-full-width="true"><thead><tr><th width="132">手指动画</th><th width="163">图示</th><th width="453">制作步骤</th><th>图示</th></tr></thead><tbody><tr><td><strong>原地点击</strong></td><td><img src="../../../.gitbook/assets/image (1239).png" alt="" data-size="original"></td><td><ul><li>手指图片：添加动画-通用-缩放缓动，参数设置如右图1</li><li>点击特效图片（选做）：添加动画-通用-缩放缓动，参数设置如右图2；继续添加透明度缓动，参数设置如右图3；若想实现双层光圈效果，可再复制一个光圈图层，将两个动画的“延迟时间”改为0.2s即可</li></ul></td><td><p><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></p><p><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></p><p><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt="" data-size="original"></p></td></tr><tr><td><strong>移动点击</strong></td><td><img src="../../../.gitbook/assets/image (1243).png" alt="" data-size="original"></td><td><ul><li>手指图片：添加动画-通用-位移缓动，参数设置如右图</li></ul></td><td><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td></tr><tr><td><strong>按钮二选一</strong></td><td><img src="../../../.gitbook/assets/image (1245).png" alt="" data-size="original"></td><td><ul><li>手指图片：添加动画-通用-位移缓动，参数设置如右图1；继续添加缩放缓动，参数设置如右图2</li><li>选项按钮：为左侧按钮组添加动画-通用-缩放缓动，参数设置如右图3；复制该动画到右侧按钮组，调整动画曲线为反方向即可，参数设置如右图4</li></ul></td><td><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><img src="../../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><img src="../../../.gitbook/assets/image (7) (1) (1) (1).png" alt=""></td></tr><tr><td><strong>按钮四选一</strong></td><td><img src="../../../.gitbook/assets/image (1268).png" alt="" data-size="original"></td><td><ul><li>手指图片(横向运动)：添加动画-通用-位移缓动，参数设置如右图1；(选做)继续添加旋转缓动，参数设置如右图2</li><li>手指图片组(纵向运动)：添加动画-通用-位移缓动，参数设置如右图3；继续添加透明度缓动，参数设置如右图4</li></ul></td><td><img src="../../../.gitbook/assets/image (1269).png" alt="" data-size="original"><img src="../../../.gitbook/assets/image (1270).png" alt=""><img src="../../../.gitbook/assets/image (1271).png" alt=""><img src="../../../.gitbook/assets/image (1272).png" alt=""></td></tr><tr><td><strong>左右滑动</strong></td><td><img src="../../../.gitbook/assets/image (1250).png" alt="" data-size="original"></td><td><ul><li>手指图片：添加动画-通用-位移缓动，参数设置如右图</li></ul></td><td><img src="../../../.gitbook/assets/image (8) (1) (1) (1).png" alt="" data-size="original"></td></tr><tr><td><strong>滑动切割</strong></td><td><img src="../../../.gitbook/assets/image (1259).png" alt="" data-size="original"></td><td><ul><li>手指组：添加动画-通用-位移缓动，参数设置如右图1；继续添加透明度缓动，参数设置如右图2</li><li>拖尾效果（选做）：可直接将拖尾图片置于手指组内，跟随组动画一起运动</li></ul></td><td><img src="../../../.gitbook/assets/image (9) (1) (1) (1).png" alt=""><img src="../../../.gitbook/assets/image (10) (1) (1) (1).png" alt=""></td></tr><tr><td><strong>八字滑动</strong></td><td><img src="../../../.gitbook/assets/image (1252).png" alt="" data-size="original"></td><td><ul><li>手指图片(横向运动)：添加动画-通用-位移缓动，参数设置如右图1</li><li>手指图片组(纵向运动)：添加动画-通用-位移缓动，参数设置如右图2</li></ul></td><td><img src="../../../.gitbook/assets/image (11) (1) (1) (1).png" alt=""><img src="../../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""></td></tr><tr><td><strong>从A点拖到B点</strong></td><td><img src="../../../.gitbook/assets/image (1255).png" alt="" data-size="original"></td><td><ul><li>手指图片：添加动画-通用-位移缓动，参数设置如右图1</li><li>开头结尾透明度效果（选做）：在手指组上添加动画-通用-透明度缓动，参数设置如右图2；继续添加透明度缓动，参数设置如右图3</li></ul></td><td><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><img src="../../../.gitbook/assets/image (14) (1).png" alt=""><img src="../../../.gitbook/assets/image (1273).png" alt=""></td></tr></tbody></table>



### 2.如何设置人物呼吸感动画

1）选中人物图层，将锚点修改为（50,100）

<figure><img src="../../../.gitbook/assets/image (1262).png" alt=""><figcaption></figcaption></figure>

2）为人物图层添加动画-通用-缩放缓动，具体参数设置如下：

<figure><img src="../../../.gitbook/assets/image (1263).png" alt=""><figcaption></figcaption></figure>

注：可根据实际需求，通过调整【结束比例】来控制人物缩放幅度的大小



### 3.如何制作进度条

1）准备两张图片：底图+进度条

2）选中进度条图层，将锚点修改为（0,50），并调整到合适位置

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

3）为进度条图层添加动画-通用-缩放缓动，重要参数设置：播放1次 / 起始比例X轴设为0，Y轴不变默认为1，结束比例不变默认为1。

具体参数设置如下：

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>



### 4.如何制作血条

1）准备两张图片：底图+血条

2）选中血条图层，将锚点修改为（0,50），并调整到合适位置

<figure><img src="../../../.gitbook/assets/image (1264).png" alt=""><figcaption></figcaption></figure>

3）为血条图层添加动画-通用-缩放缓动，重要参数设置：播放1次 / 起始比例不变，结束比例Y轴不变，都默认为1，仅调整结束比例X轴的数值即可（此处的数值代表最终血量）。

具体参数设置如下：

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
