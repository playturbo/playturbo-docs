---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 2D playable《拖拽放置》教程

温馨提示：入门难度模板《拖拽到指定位置放置》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：拖拽
* 【交互次数】：2步跳转
* 【线程】：单线程
* 【核心资产】：静态图片
* 【功能】：动画-通用、动画-淡入、事件-拖拽到指定位置、事件-拖拽



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1141).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1142).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1143).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/46t968a2)                                                 | [点击试玩](https://tinyurl.com/46t968a2)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【待拼图案轮廓】和【两块碎片按钮】；
* 出现【第一次操作指引】，提示玩家拖动碎片A到待拼图案中；
* 玩家拖动碎片A到指定区域，触发【成功反馈】；
* 出现【第二次操作指引】，提示玩家拖动碎片B到待拼图案中；
* 玩家拖动碎片B，抬起即跳转商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们判断本案例设置1个场景即可

<table><thead><tr><th width="178">场景名称</th><th>场景1-诱导拖拽</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1142).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>显示灰色底图和两个拼图碎片，引导玩家拖拽完成拼图</td></tr><tr><td><strong>动画</strong></td><td><p>【指引文案】：缩放缓动</p><p>【操作指引】：旋转缓动+位移缓动+透明度缓动</p><p>【拼图碎片】：缩放缓动；淡入</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-碎片A</p><p>触发操作：拖拽到指定位置</p><p>响应事件：隐藏素材；禁用事件；启用事件</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【音频】：背景音乐、音效（点击音效/成功放置音效）</p><p>【图片】：背景图片、拼图灰色底图、拼图碎片、拼图碎片拖拽版、指引手指、logo、CTA按钮</p><p>【文本】：指引文案、产品名称、下载文案</p><p>【粒子特效】</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1144).png" alt=""><figcaption></figcaption></figure>

#### **2.全局场景**

1）在【全局场景】中添加常驻信息：logo、产品名称、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1145).png" alt=""><figcaption></figcaption></figure>

#### **3.场景1**

1）在【场景1】中添加音效、拼图灰色底图、拼图碎片、拼图碎片拖拽版、指引手指、指引文案、粒子特效

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1146).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.第一次操作指引**

1）在左侧图层处选中拼图碎片A剪影【cat\_A\_silhouette】，添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1147).png" alt=""><figcaption></figcaption></figure>

2）选中手指组【group\_hand】，添加动画-通用-旋转缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1148).png" alt=""><figcaption></figcaption></figure>

3）选中整个操作指引组【cat\_A\_guide】，添加动画-通用-位移缓动与透明度缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1149).png" alt=""><figcaption></figcaption></figure>

注：第二次操作指引同理第一次操作指引，可通过【复制/粘贴动画】来快速完成制作。

#### **2.拼图碎片A被按下/松开**

由模板可知，当按下碎片A时，碎片A呈放大状态；当松开碎片A且碎片A未被放置到正确位置上时，碎片A呈缩小状态。因此，我们要为碎片A设置两个缩放缓动动画。

1）选中碎片A选项图片【cat\_A\_Options】，添加动画-通用-缩放缓动，并命名为“放大”。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1150).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-缩放缓动，并命名为“缩小”。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1151).png" alt=""><figcaption></figcaption></figure>

#### **3.拼图碎片A正确放置**

选中正确放置后的拼图碎片A【cat\_A】，添加动画-进场动画-淡入。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1152).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.图层事件-碎片A**

我们需要为碎片A添加三个触发事件，分别为：按下碎片时、碎片未被放置到正确位置时、碎片被成功放置到正确位置时，即对应的触发事件为“按下”、“抬起”、“拖拽到指定位置”。

<mark style="background-color:orange;">**按下**</mark>

1）选中碎片A图层，添加事件-按下；

2）添加响应事件-从头播放点击音效；播放碎片A“放大”的单个动画；

3）添加响应事件-隐藏素材操作指引相关，并暂停播放相关指引动画；

4）其他响应事件：设置埋点信息；取消执行延迟（在“抬起”事件中讲解）

<figure><img src="../../../../.gitbook/assets/image (1153).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:orange;">**抬起**</mark>

1）选中碎片A图层，添加事件-抬起；

2）添加响应事件-播放碎片A“缩小”的单个动画；

3）添加响应事件-执行延迟0.2s，显示素材操作指引相关，并从头播放相关指引动画；

_（因为我们设置了“抬起”碎片后重新出现操作指引的定时器，因此我们要在“按下”的响应事件中取消该定时器，否则会出现当我们按下碎片的同时出现操作指引）_

<figure><img src="../../../../.gitbook/assets/image (1154).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:orange;">**拖拽到指定位置**</mark>

1）选中碎片A图层，添加事件-拖拽到指定位置；

2）点击【编辑拖拽区域】，将区域调整到合适位置大小后保存，并选择拖拽方向为【任意方向】；

<figure><img src="../../../../.gitbook/assets/image (1155).png" alt=""><figcaption></figcaption></figure>

3）添加响应事件-禁用事件“抬起”；禁用事件“按下”；

4）添加响应事件-隐藏素材碎片A；隐藏素材灰色碎片B，并播放碎片B透明度动画；

5）添加响应事件-播放正确放置后的碎片A的淡入动画；播放相关音效与粒子特效；

6）添加响应事件-执行延迟0.2s，显示第二次操作指引组；启用碎片B的“拖拽”事件；

7）其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1156).png" alt=""><figcaption></figcaption></figure>

#### **2.图层事件-碎片B**

<mark style="background-color:orange;">**拖拽**</mark>

1）选中碎片B图层，添加事件-拖拽，选择拖拽方向为【任意方向】；

2）添加响应事件-从头播放点击音效；播放碎片B放大的单个动画；隐藏素材操作指引相关；

3）其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1157).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:orange;">**抬起**</mark>

1）选中碎片B图层，添加事件-抬起

2）添加响应事件-隐藏素材碎片B；隐藏素材第二次操作指引相关；播放碎片B“缩小”的单个动画；

3）添加响应事件-执行延迟0.2s，重新显示素材碎片B；显示素材操作指引相关

4）其他响应事件：跳转应用商店；设置埋点信息；上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (1158).png" alt=""><figcaption></figcaption></figure>

#### **3.图层事件-CTA按钮**

选中【全局场景】中的下载按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1159).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1160).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1161).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1162).png" alt=""><figcaption></figcaption></figure>
