---
description: '#自由编辑器'
---

# 触发事件

触发事件，可以简单将其理解为"玩家的操作方式" 或 "到达某种时机就生效的事件"



## <mark style="color:blue;">一、触发事件的使用</mark>

### 1.添加触发事件

1）选中单个图层或单个场景

2）点击右侧【添加事件】按钮，调起触发事件类型选项卡

3）结合产品玩法和素材需要，点击选择适合的触发事件即可

4）添加触发事件后，可在其下方添加所需的响应事件

<mark style="color:red;">注意：通常，添加触发事件的</mark><mark style="color:red;">**对象**</mark><mark style="color:red;">取决于我们需要玩家在什么图层上进行交互</mark>

<mark style="color:red;">如想要玩家点击某个物品后出现xx效果，则可以</mark><mark style="color:red;">**选中该物品图层**</mark><mark style="color:red;">，添加"点击"的触发事件和对应响应事件；若想要玩家在全屏任意位置都可点击，则可直接</mark><mark style="color:red;">**选中场景**</mark><mark style="color:red;">，添加"点击"的触发事件和对应响应事件</mark>

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1678).png" alt=""><figcaption></figcaption></figure>

</div>

### 2.替换触发事件

点击图示按钮，可对已添加的触发事件进行替换（不会改变响应事件）

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1679).png" alt=""><figcaption></figcaption></figure>

</div>

### 3.复制事件

1）点击图示按钮，即可复制对应的触发事件及其响应事件

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1680).png" alt=""><figcaption></figcaption></figure>

</div>

2）复制该事件后，可选中想要粘贴该事件的图层或场景，进行事件的粘贴，即可快速实现相同事件的制作

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1682).png" alt=""><figcaption></figcaption></figure>

</div>

### 4.删除触发事件

点击图示按钮，即可删除对应的触发事件及其响应事件

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1683).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">二、触发事件的类别</mark> <a href="#mjnno" id="mjnno"></a>

当前触发事件包含六大类别：【点击】 【滑动】 【拖拽】 【媒体播放】 【定时器】 【条件判断】

<table data-full-width="false"><thead><tr><th width="241">截图</th><th width="190">事件属性</th><th width="123">事件类别</th><th>类别细分</th></tr></thead><tbody><tr><td><img src="../../../../../../.gitbook/assets/image (208).png" alt=""></td><td>通用事件</td><td><strong>点击</strong></td><td><p>点击</p><p>长按3s</p><p>按下</p><p>抬起</p><p>双击</p></td></tr><tr><td><img src="../../../../../../.gitbook/assets/image (713).png" alt=""></td><td>通用事件</td><td><strong>滑动</strong></td><td><p>上滑</p><p>下滑</p><p>左滑</p><p>右滑</p><p>任意滑动</p></td></tr><tr><td><img src="../../../../../../.gitbook/assets/image (213).png" alt=""></td><td>图层事件(常规图层)</td><td><strong>拖拽</strong></td><td><p>拖拽</p><p>拖拽到指定位置</p></td></tr><tr><td><img src="../../../../../../.gitbook/assets/image (286).png" alt=""></td><td>图层事件(视频/音频)</td><td><strong>媒体播放</strong></td><td><p>开始时</p><p>结束时</p></td></tr><tr><td><img src="../../../../../../.gitbook/assets/image (211).png" alt=""></td><td>场景事件</td><td><strong>定时器</strong></td><td>定时触发</td></tr><tr><td><img src="../../../../../../.gitbook/assets/image (920).png" alt=""></td><td>场景事件(全局变量)</td><td><strong>条件判断</strong></td><td>条件判断</td></tr></tbody></table>



### 1.通用事件: 点击

1）【点击】类事件包含：点击、长按3s、按下、抬起、双击

2）对应触发时机为：

* 点击：按下屏幕后抬手
* 长按3s：按住屏幕3s后抬手
* 按下：按下屏幕即触发，不管是否抬手
* 抬起：从屏幕抬手时触发，不管按下多久
* 双击：连续两次点击屏幕

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1687).png" alt=""><figcaption></figcaption></figure>

</div>



### 2.通用事件: 滑动

1）【滑动】类事件包含：上滑、下滑、左滑、右滑、任意滑动

2）对应触发时机为：

* 上滑：在屏幕上上滑，抬手时触发
* 下滑：在屏幕上下滑，抬手时触发
* 左滑：在屏幕上左滑，抬手时触发
* 右滑：在屏幕上右滑，抬手时触发
* 任意滑动：在屏幕上任意方向滑动，抬手时触发

<mark style="color:red;">注意：【滑动】类事件，图层不会跟随玩家手指的移动而移动</mark>

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1688).png" alt=""><figcaption></figcaption></figure>

</div>



### 3.图层事件: 拖拽

1）【拖拽】类事件包含：拖拽、拖拽到指定位置

2）对应触发时机为：

* 拖拽：拖拽某个图层，不抬手即触发
* <mark style="color:red;">拖拽到指定位置：</mark><mark style="color:red;">**拖拽某个图层，如果拖到指定的区域抬手，则触发事件；如果未拖到指定的区域抬手，则图层默认返回原位，不触发事件**</mark>

3）选择【拖拽】事件后，支持选择【拖拽方向】：可选择【任意方向】、【水平方向】、【垂直方向】

4）选择【拖拽到指定位置】事件后，需编辑【拖拽区域】：添加指定区域、调整区域位置大小、选择拖拽范围

同样，支持选择【拖拽方向】：可选择【任意方向】、【水平方向】、【垂直方向】

注意：【拖拽】类事件仅适用在常规图层上添加，即除了视频、音频以外的图层

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1676).png" alt=""><figcaption></figcaption></figure>

</div>



### 4.图层事件: 媒体播放

1）【媒体播放】类事件包含：开始时、结束时

2）对应触发时机为：

* 开始时：所选视频/音频开始播放时
* 结束时：所选视频/音频播放结束时

注意：【媒体播放】类事件仅适用在视频、音频图层上添加

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1686).png" alt=""><figcaption></figcaption></figure>

</div>



### 5.场景事件: 定时器

1）【定时器】类事件包含：定时触发

2）对应触发时机为：根据所设置的"延迟时长"定时触发(当延迟时长为0s则代表进入该场景时自动触发对应事件)

注意：【定时触发】仅支持在场景上添加

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1684).png" alt=""><figcaption></figcaption></figure>

</div>



### 6.场景事件: 条件判断

1）【条件判断】类事件包含：条件判断

2）对应触发时机为：当变量满足设定的条件判断时

3）添加【条件判断】后，在弹窗内点击【添加条件】，然后依次选择全局变量/运算方法/数值

4）支持勾选“只生效一次”

<mark style="color:red;">注意：只有当前项目添加</mark>[全局变量](../../../ding-bu-zi-chan-ku/quan-ju-bian-liang.md)<mark style="color:red;">后，才可使用这一触发事件</mark> (结合功能介绍文档查看 可以更快理解该触发事件哦)

<div align="left">

<figure><img src="../../../../../../.gitbook/assets/image (1685).png" alt=""><figcaption></figcaption></figure>

</div>
