---
description: '#自由编辑器'
---

# 资产相关

## <mark style="color:blue;">一、资产编组</mark>

建议您在将资产添加到画布后，在图层区按照类别或作用对资产进行编组整合，方便后续制作

<figure><img src="../../../.gitbook/assets/image (1234).png" alt=""><figcaption></figcaption></figure>

**编组有什么作用？**

首先要知道，组的级别是高于单个资产的，小组之上的大组级别又是高于小组的，这就意味着对组的调整会作用于其下的各个资产，对大组的调整会作用于其下的各个小组和资产

举个例子：当隐藏左侧道具组时，其下的文本和图片会被一起隐藏；当隐藏整个选项大组时，其下的指引文案和手指以及两个道具组都会随之隐藏

<figure><img src="../../../.gitbook/assets/image (1235).png" alt=""><figcaption></figcaption></figure>

所以，合理地为资产编组：

1）方便在资产冗杂时，通过组别快速查找相应的资产，快速定位哪部分资产有问题；

2）能够更加高效地设置动画和事件，无需将同样的动画/事件一一设置在资产上，仅在组上设置即可；

3）方便为整个组的资产做屏幕适配，以及调整横屏布局（在做好竖屏排版后进入横屏，选中大组，点击“复用竖屏位置尺寸配置”按钮一键布局）



## <mark style="color:blue;">二、效果实现</mark>

### 1.如何制作“镜像&倒影”？

制作思路：镜像=水平翻转，倒影=垂直翻转，在外观参数调整对应图层的缩放比例即可

1）选中需要调整的图层

2）右侧参数设置区，修改缩放比例：

* 镜像：将【缩放比例】中的【 水平缩放】数值调整为-1

<figure><img src="../../../.gitbook/assets/image (1266).png" alt=""><figcaption></figcaption></figure>

* 倒影：将【缩放比例】中的【 垂直缩放】数值调整为-1

<figure><img src="../../../.gitbook/assets/image (1267).png" alt=""><figcaption></figcaption></figure>
