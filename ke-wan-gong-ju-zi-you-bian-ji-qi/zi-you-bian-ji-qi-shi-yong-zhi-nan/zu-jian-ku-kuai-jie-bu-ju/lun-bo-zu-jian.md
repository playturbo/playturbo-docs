---
description: '#自由编辑器 #模板自由制作 #空白制作'
---

# 轮播组件

✨模板自由制作入口：作品预览区>>>轮播组件按钮 或 图层区>>>Carousel Component

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

✨空白制作入口：玩法模板>>>组件库>>>轮播组件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">一、轮播组件通俗介绍</mark>

* 适用玩法：适用于 要素自动/手动轮播类的玩法
  * [示例1-抓住优惠券](https://tinyurl.com/y2ztadf8) / [示例2-多要素点击切换](https://tinyurl.com/5bp6yfvc) / [示例3-循环展示](https://tinyurl.com/2n9nh5w8)
* 轮播组件支持在【空白制作】和【模板自由制作】中使用
* 对于新增的轮播组件，最少需完成组件的 「轮播样式选择」、「资源组」、「坑位设置」、「交互方式」、「高级设置」等参数设置，轮播组件才可正式生效
* <mark style="color:red;">注意：同个场景仅支持添加一个组件，但可跨场景添加组件 或 复制组件</mark>



## <mark style="color:blue;">二、轮播组件使用说明</mark>

「轮播组件」可调整的参数分四部分：外观、动画、**轮播设置**、事件

### 1.外观

* 组件是否启用：可在「外观」参数下通过调节此开关来启用/禁用轮播组件（默认启用）
* 超出范围是否裁剪：若打开「超出范围是否裁剪」，则超出组件范围的图片不予展示（默认不裁剪）
* 其他参数的使用同常规图层一样，在此不作说明。需注意：当调整轮播组件的外观参数(如位置大小)时，轮播组件内的所有图层会跟着一起变化

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2015).png" alt=""><figcaption></figcaption></figure>

</div>



### 2.动画

在此处设置的动画是对整个轮播组件生效的，具体的使用同常规图层一样，在此不作说明



### 3.轮播设置

轮播设置包含五部分参数，需先进行「样式选择」设置，再进行「资源组」、「坑位设置」、「交互方式」、「高级设置」等参数的设置

<mark style="color:red;">注意：「轮播设置」为轮播组件最核心的参数，请务必将各部分设置完成</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2016).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:red;">3.1 样式选择</mark>

当前支持五种轮播样式（每种轮播样式的具体效果可参考缩略图的动画）

* **常规轮播：**卡片默认间隔排列 同时展示多张，交互后/自动 进行**移动**的轮播切换
* **原地缩放轮播：**卡片默认处于相同位置 单次展示一张，交互后/自动 进行**原地缩放**的轮播切换
* **滚动缩放轮播：**卡片默认密集排列，交互后/自动 进行**缩放&移动**的轮播切换
* **透明度轮播：**卡片默认间隔排列 单次展示一张，交互后/自动 进行**移动&透明度变化**的轮播切换
* **渐隐缩放轮播：**卡片默认间隔排列 单次展示一张，交互后/自动 进行**缩放&移动&透明度变化**的轮播切换

<div align="left">

<figure><img src="../../../.gitbook/assets/Animation1 (6).gif" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:red;">3.2 资源组</mark>

「资源组」用来添加所要展示的要素 及 设置要素参数。

<mark style="color:red;">一个资源组可包含一个或多个轮播组；一个轮播组支持添加一张或多张图片</mark>

<mark style="background-color:red;">**3.2.1 单个轮播组**</mark>

* 上传轮播图片：点击+号，可从资产库或项目资产中选择图片加入轮播组
* 替换轮播图片：点击图示按钮(蓝色)，可替换当前轮播图片

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2019).png" alt=""><figcaption></figcaption></figure>

</div>

* 支持设置 「显示」/「隐藏」 轮播组或轮播图片
* 支持 删除 轮播组或轮播图片
* 支持 拖拽移动 轮播组或轮播图片的位置

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2020).png" alt=""><figcaption></figcaption></figure>

</div>

* 点击轮播组，调起轮播组的「外观」参数弹窗，可调整轮播组的整体尺寸及「坑位尺寸」和「坑位间隔」
  * 坑位尺寸：即每个图片坑位的尺寸大小。放在其中的图片按最长边进行适配
  * 坑位间隔：决定了每个坑位中心点之间的间距

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2021).png" alt="" width="515"><figcaption></figcaption></figure>

</div>

效果示例：

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2022).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2023).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

* 点击单个轮播图片调起弹窗，可设置该图片的「资源类别」及「事件」
* 需先【添加类别】，自定义类别后，再选择对应类别
* 资源类别用于后续事件判定成功or失败

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2024).png" alt=""><figcaption></figcaption></figure>

</div>

示例：如[本示例素材](https://tinyurl.com/5evemtcd)，就是添加了三种资源类别：「粉色」、「灰色」、「绿色」三套造型

可设置：切换轮播，当角色的头部、身体、脚部变为同一套造型（即同一种资源类别）时，触发后续事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2026).png" alt=""><figcaption></figcaption></figure>

</div>



<mark style="background-color:red;">**3.2.2 添加轮播组**</mark>

* 添加轮播组：点击图示按钮，都可新建一个轮播组
* 轮播组之间支持拖动调整位置
* 添加多个轮播组的使用场景：如[本示例素材](https://tinyurl.com/5evemtcd)，用多个轮播组控制不同身体部位造型的轮播切换

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2027).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:red;">3.3 坑位设置</mark>

坑位设置包含「排列方式」和「坑位数」

* **排列方式：**单选。可选水平或垂直
  * 若选择水平，则轮播为左右方向轮播
  * 若选择垂直，则轮播为上下方向轮播
* <mark style="color:red;">**坑位数：**</mark><mark style="color:red;">决定了轮播时的坑位数量</mark>
  * 注意：最中间的为坑位1。如坑位数量为5，则从左到右坑位数对应分别为4-5-1-2-3

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2028).png" alt=""><figcaption></figcaption></figure>

</div>

💡"**坑位数"与"已上传的图片数量"的关系**

* 当图片数量>坑位数时：部分图片会被隐藏。随着轮播的进行，一部分图片隐藏，另一部分图片被展示出来进行轮播
* 当图片数量=坑位数时：所有图片都被展示在对应坑位上进行轮播
* 当图片数量<坑位数时：所有图片都被展示在每一个坑位上，由于图片数较少，会用已有图片随机填满所有坑位

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2030).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:red;">3.4 交互方式</mark>

交互方式包含「播放设置」和「交互方式」

* **播放设置：**自动或手动，最少选择一项，支持多选
  * 只选择【自动】：无需再设置「交互方式」。轮播会自动播放
  * 只选择【手动】：需继续选择「交互方式」。轮播需通过玩家手动进行切换
  * 同时选择：需继续选择「交互方式」。既会自动轮播，又支持手动切换轮播

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2033).png" alt=""><figcaption></figcaption></figure>

</div>

* **交互方式**(播放设置勾选"手动"后选择)：点击或拖拽，最少选择一项，支持多选
  * 只选择【拖拽】：支持拖拽切换
  * 只选择【点击】：通过点击切换按钮进行切换
  * 同时选择：既支持点击按钮切换 同时支持拖拽切换

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2034).png" alt=""><figcaption></figcaption></figure>

</div>

* **切换按钮**(勾选"点击"后进行设置)
  * 支持 显示/隐藏 按钮
  * 点击替换按钮，支持从资产库或项目资产中选取图片替换按钮样式
  * 点击单张按钮图片，调起弹窗，可设置按钮的外观

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2035).png" alt="" width="515"><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:red;">3.5 高级设置</mark>

可对轮播动画的参数进行调整

* **动画停留时间：**当设置为自动轮播时，该参数决定了间隔多久切换下一张图片（如设置为1s，则每切换完成后再过1s，切换下一张图片）
* **动画播放时长：**当设置为自动轮播或点击轮播时，该参数决定了动画播放的时长（如设置为0.5s，则切换图片的动画过程时长为0.5s）
* **透明度：**最大值、最小值决定该动画播放过程中的透明度最大、最小值
* **缩放值：**最大值、最小值决定该动画播放过程中的缩放度最大、最小值

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2036).png" alt=""><figcaption></figcaption></figure>

</div>



### 4.事件

「轮播组件」存在独特的触发事件和响应事件

**触发事件**包含：「切换轮播时」、「轮播到某一资源」、「轮播到某一类别的资源」

相关的**响应事件**包含：「启用/禁用轮播组件」、「启用/禁用轮播组」、「暂停/播放轮播组」、「重新轮播」、「删除轮播资源」、「停留时间」

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2037).png" alt=""><figcaption><p>触发事件</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2038).png" alt=""><figcaption><p>响应事件</p></figcaption></figure>

</div>

#### <mark style="background-color:red;">4.1 触发事件</mark>切换轮播时

切换轮播时：需选择对应的轮播组，触发时机为选择的轮播组，切换轮播完成时



轮播完成停住时，触发响应事件

轮播到某一资源

轮播到某一类别的资源

#### <mark style="background-color:red;">4.2 响应事件</mark>

