---
description: '#自由编辑器 #模板自由制作 #空白制作'
---

# 自由画线组件

✨模板自由制作入口：作品预览区>>>自由画线按钮 或 图层区>>>Draw Lines Component

<figure><img src="../../../.gitbook/assets/image (1869).png" alt=""><figcaption></figcaption></figure>

✨空白制作入口：玩法模板>>>组件库>>>自由画线组件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="416"><figcaption></figcaption></figure>

</div>

相关案例教学可查阅 [zi-you-hua-xian-zu-jian-kong-bai-zhi-zuo-jiao-cheng.md](../../../playturbo-an-li-jiao-xue-ji-di/ke-wan-zi-you-bian-ji-qi-an-li/hua-xian-wan-fa-an-li/zi-you-hua-xian-zu-jian-kong-bai-zhi-zuo-jiao-cheng.md "mention")



## <mark style="color:blue;">一、自由画线组件通俗介绍</mark>

* 适用于如模板"画线救它"等能够**在区域内自由画线**的玩法。通过「自由画线组件」，实现在指定区域内自由画线，并根据线条触发各种效果
* 当前，<mark style="color:red;">【模板自由制作】和【空白制作】都支持使用"自由画线组件"</mark>。使用【模板自由制作】，您可以基于原模板的玩法对组件进行调整；使用【空白制作】，可以从零开始制作画线玩法的素材
* 基于现有的「自由画线组件」，您可调整模板的可画线范围、线条样式等内容
* <mark style="color:red;">注意：同个场景仅支持添加一个组件，但可跨场景添加组件或复制组件</mark>



## <mark style="color:blue;">二、自由画线组件使用说明</mark>

「自由画线组件」可调整的参数分三部分：「外观」、「线条」、「事件」

我们将结合模板[【画线救它】](http://tinyurl.com/bdcm78r2)进行「自由画线组件」的使用说明

### 1. 外观

* \[显示隐藏参数]横竖屏拆分：和各图层的外观参数相同，可分别调整该画线组件在横/竖屏下是否显示
* 位置尺寸：可以修改该画线组件的宽高、位置。其宽高位置，决定了能够画出线的范围（如下图，绿色覆盖范围即是在试玩过程中可画出线的范围）
* 屏幕适配方式：和各图层的外观参数相同，可调整该画线组件的屏幕适配方式
* 缩放比例：和各图层的外观参数相同，可调整该画线组件的比例

<figure><img src="../../../.gitbook/assets/image (1410).png" alt=""><figcaption></figcaption></figure>



### 2.线条

「线条」参数包含“线条样式”和“刚体类型”两部分

#### 1）线条样式

* 可以设置画出的线条颜色及粗细
* 点击「预览线条」可在画布中预览所设置的线条样式

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1411).png" alt=""><figcaption></figcaption></figure>

</div>

#### 2）刚体类型(暂不支持调整)

「刚体类型」可以决定画出的线条，是否具有刚体属性。共有四种类型可以选择：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1412).png" alt=""><figcaption></figcaption></figure>

</div>

* 非刚体：不具有物理性质，仅作为图片展示
* 静态刚体：具有物理性质，会与其他的刚体发生碰撞，但静态刚体本身始终静止不动。如墙壁、地面等
* 动力学刚体：有一定质量并在外力作用下运动，遵循牛顿定律的物体，会与其他类型的刚体发生碰撞并改变其速度。如自由下落的小球
* 运动学刚体：不考虑物体受力情况和质量，以恒定的速度运动的物体，会与「动力学刚体」发生碰撞。如始终匀速运动的小球

<figure><img src="../../../.gitbook/assets/image (1413).png" alt=""><figcaption></figcaption></figure>



### 3.事件

「自由画线组件」包含两种**触发事件**：「开始画线」、「画线完成」

和「自由画线组件」相关的**响应事件**包含：「抹除画线线条」、「修改画线线条样式」、「启用/禁用自由画线组件」、「已画线条生成刚体」

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1414).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">1-1）</mark><mark style="background-color:orange;">**触发事件：开始画线**</mark>

设置「开始画线」，并添加所需的响应事件

**触发时机为：**<mark style="color:red;">**当玩家开始画线时**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1415).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">1-2）</mark><mark style="background-color:orange;">**触发事件：画线完成**</mark>

设置「画线完成」，并添加所需的响应事件

**触发时机为：**<mark style="color:red;">**当玩家完成画线时**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1416).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-1）</mark><mark style="background-color:orange;">**响应事件：抹除画线线条**</mark>

该事件的响应结果为：所有已画完成的线条会被抹除

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1417).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-2）</mark><mark style="background-color:orange;">**响应事件：修改画线线条样式**</mark>

该事件的响应结果为：画出的线条将被修改为指定样式

<mark style="color:red;">**注意：该响应事件仅对未画出的线生效，对已画出的不生效**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1418).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-3）</mark><mark style="background-color:orange;">**响应事件：**</mark><mark style="background-color:orange;">启用/禁用自由画线组件</mark>

需要选择启用/禁用：

* 若选择「禁用」，该事件的响应结果为：该组件不再能够开始画线和完成画线
* 若选择「启用」，该事件的响应结果为：取消「禁用」事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1419).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:orange;">**2-4）响应事件：已画线条生成刚体**</mark>

该事件的响应结果为：线条根据所选的「刚体类型」，变为刚体

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1420).png" alt=""><figcaption></figcaption></figure>

</div>
