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

* 适用玩法：适用于 通过点击/拖拽等交互方式，调整遮罩蒙层，展示目标图片 的玩法
  * [示例1-点击涂色](https://tinyurl.com/ykrebstj) / [示例2-透视](https://tinyurl.com/bde7wycx) / [示例3-点击涂色](https://tinyurl.com/2eemxpa9) / [示例4-拖动涂色](https://tinyurl.com/27ejnt5a)
* 底层逻辑：通过「遮罩形状」来控制「被遮罩组」显示的部分，即「被遮罩组」内的图像，在「遮罩形状」覆盖范围内的部分会显示，覆盖范围外的部分会隐藏
* 遮罩组件支持在【空白制作】和【模板自由制作】中使用。对于新增的遮罩组件，最少需完成遮罩组件的 「外观」、「遮罩形状」、「被遮罩组」等参数设置，遮罩组件才可正式生效
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

<mark style="color:red;">注意：「遮罩设置」为遮罩组件最核心的参数，请务必将各部分设置完成</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1873).png" alt=""><figcaption></figcaption></figure>

</div>

#### 3.1 遮罩组

新增：支持新增遮罩组，点击后输入新遮罩组名称即可创建遮罩组

添加动画：可为遮罩组添加动画，添加后动画对组内所有元素生效

显示/隐藏：可调整遮罩组的显示/隐藏，对组内所有元素生效（默认显示）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1882).png" alt=""><figcaption></figcaption></figure>

</div>



#### 3.2 遮罩形状

<mark style="background-color:red;">**形状**</mark>：「遮罩形状」覆盖到「被遮罩组」的部分会显示，未覆盖到的部分会隐藏

* 形状支持设置「矩形」或「圆形」，并可调整其「外观」、「动画」、「事件」参数
  * 外观：可调整该形状的位置尺寸、缩放比例、旋转角度
  * 动画：可对该形状设置动画
  * 事件：可对遮罩形状设置事件(可设置「拖拽」事件，使遮罩在实际试玩中可拖动)
* 可点击「预览遮罩效果」，在画布内预览当前遮罩形状的位置大小

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1876).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:red;">**跟随元素**</mark>（非必须添加）：设置跟随元素后，需为形状添加「拖拽」事件。设置完成后，跟随元素将会跟随形状的拖拽同步移动

* 支持添加多个跟随元素，点击右侧"+"按钮即可从资产库中添加
* 点击可调整「跟随元素」的「外观」、「动画」、「事件」参数（使用同常规图层一样）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1878).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:red;">3.3 被遮罩组</mark>

「被遮罩组」内的图像，在「遮罩形状」覆盖范围内的部分会显示，覆盖范围外的部分会隐藏

* 支持添加多个 被遮罩元素，点击右侧"+"按钮即可从资产库中添加
* 点击可调整「被遮罩元素」的「外观」、「动画」、「事件」参数（使用同常规图层一样）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1880).png" alt=""><figcaption></figcaption></figure>

</div>



#### 3.4 自定义分组

<mark style="color:red;">「自定义分组」</mark>作为遮罩组件的一部分，可随着遮罩组件一起缩放和调整位置，但<mark style="color:red;">不受遮罩的影响，不会被遮罩</mark> （如下图所示，将"被遮罩组"对应的黑白底图加入到自定义分组中，当"遮罩形状"覆盖"被遮罩组"时，展示"被遮罩组"的彩色图片，其他部分则展示该黑白底片）

**用户可根据自身创意，决定是否要添加「自定义分组」**

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1881).png" alt=""><figcaption></figcaption></figure>

</div>



### 4.事件

「遮罩组件」独特的**响应事件**包含：启用/禁用遮罩组件、启用/禁用遮罩组、显示/隐藏遮罩组、显示/隐藏遮罩分组、启用/禁用遮罩效果

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1884).png" alt=""><figcaption></figcaption></figure>

</div>

#### 4.1 启用/禁用遮罩组件

需选择启用/禁用

若被禁用，等同于禁用所有的遮罩组。遮罩组下的所有遮罩层、被遮罩层事件将不再生效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1885).png" alt="的" width="314"><figcaption></figcaption></figure>

</div>

#### 4.2 启用/禁用遮罩组

需选择启用/禁用和某个遮罩组

若被禁用，遮罩组下的所有遮罩层、被遮罩层事件将不再生效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1886).png" alt=""><figcaption></figcaption></figure>

</div>

#### 4.3 显示/隐藏遮罩组

需选择显示/隐藏和某个遮罩组

选择后，将显示/隐藏某个遮罩组内的所有元素

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1887).png" alt=""><figcaption></figcaption></figure>

</div>

#### 4.4 显示/隐藏遮罩分组

需选择显示/隐藏和某个遮罩分组

选择后，将显示/隐藏某个遮罩分组内的所有元素

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1888).png" alt=""><figcaption></figcaption></figure>

</div>

#### 4.5 启用/禁用遮罩效果

需选择启用/禁用和某个遮罩组

若启用，则「被遮罩组」会受「遮罩形状」的影响而展示；若禁用，则「被遮罩组」不受「遮罩形状」影响，直接展示

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1889).png" alt=""><figcaption></figcaption></figure>

</div>
