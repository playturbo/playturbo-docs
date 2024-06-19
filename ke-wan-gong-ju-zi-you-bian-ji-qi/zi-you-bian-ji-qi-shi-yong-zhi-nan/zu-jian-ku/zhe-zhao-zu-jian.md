---
description: '#自由编辑器 #模板自由制作 #空白制作'
---

# 遮罩组件

✨模板自由制作入口：作品预览区>>>遮罩组件按钮 或 图层区>>>Mask Component

<figure><img src="../../../.gitbook/assets/image (1868).png" alt=""><figcaption></figcaption></figure>

✨空白制作入口：玩法模板>>>组件库>>>遮罩组件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1870).png" alt="" width="403"><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">一、遮罩组件通俗介绍</mark>

* 遮罩组件支持在【空白制作】和【模板自由制作】中使用
* 适用玩法：适用于 通过点击/拖拽等交互方式，调整遮罩蒙层，展示目标图片 的玩法
* 底层逻辑：通过「遮罩形状」来控制「被遮罩组」显示的部分，即「被遮罩组」内的图像，在「遮罩形状」覆盖范围内的部分会显示，覆盖范围外的部分会隐藏
* 对于新增的遮罩组件，最少需完成遮罩组件的 「外观」、「遮罩形状」、「被遮罩组」等参数设置，遮罩组件才可正式生效
* <mark style="color:red;">注意：同个场景仅支持添加一个组件，但可跨场景添加组件或复制组件</mark>



## <mark style="color:blue;">二、遮罩组件使用说明</mark>

「遮罩组件」可调整的参数分四部分：外观、动画、遮罩设置、事件

### 1.外观

* 组件是否启用：可在「外观」参数下通过调节此开关来启用/禁用遮罩组件（默认启用）
* 其他参数的使用同常规图层一样，在此不作说明。需注意：当调整遮罩组件的外观参数(如位置大小)时，遮罩组件内的所有图层会跟着一起变化

<figure><img src="../../../.gitbook/assets/image (1872).png" alt=""><figcaption></figcaption></figure>



### 2.动画

在此处设置的动画是对整个遮罩组件生效的，具体的使用同常规图层一样，在此不作说明



### 3.遮罩设置

一个「遮罩组件」最少包含一个「遮罩组」。遮罩组(遮罩设置)包含三部分：遮罩形状、被遮罩组、自定义分组（选做）

遮罩组：支持 添加遮罩组、添加动画(对组内所有元素生效)、调整遮罩组的显示/隐藏

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1874).png" alt=""><figcaption></figcaption></figure>

</div>

* 遮罩形状

<mark style="color:red;">注意：「遮罩设置」为遮罩组件最核心的参数，请务必将各部分设置完成</mark>













<div align="left">

<figure><img src="../../../.gitbook/assets/image (1873).png" alt=""><figcaption></figcaption></figure>

</div>





### 4.事件

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
