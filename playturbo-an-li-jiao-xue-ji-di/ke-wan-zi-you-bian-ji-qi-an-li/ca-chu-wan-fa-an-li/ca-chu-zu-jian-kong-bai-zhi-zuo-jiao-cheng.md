---
description: '#自由编辑器 #空白制作 #擦除组件 #初级难度'
---

# 擦除组件-空白制作教程

温馨提示：本篇教程主要讲解空白制作如何**通过擦除组件制作出"擦除玩法"的可玩素材**，建议搭配[DEMO](https://tinyurl.com/4xby5rvh)和[功能介绍文档](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/zu-jian-ku/ca-chu-zu-jian.md)食用效果更佳哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：擦除玩法
* 【交互方式】：开始擦除/到达某一阶段
* 【自由度】：固定流程
* 【核心资产】：图片
* 【核心功能】：到达某一阶段-隐藏蒙层



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                          | 竖屏                                                                                  | 横屏                                                                                  |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1504).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation1 (1).gif" alt="" data-size="original"> | <img src="../../../.gitbook/assets/Animation2 (2).gif" alt="" data-size="original"> |
| 扫码试玩                                                                              | [点击试玩](https://tinyurl.com/4xby5rvh)                                                | [点击试玩](https://tinyurl.com/4xby5rvh)                                                |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前先对本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示【美女被遮挡画面】，美女角色默认进行序列帧播放

2）出现【操作指引】，引导玩家滑动擦除遮罩

3）玩家在遮罩位置任意滑动，遮罩即被实时擦除，露出美女身体

4）当遮罩区域被擦除60%，遮罩消失，并出现完整的美女图片和重玩按钮

5）玩家按下按钮，跳转应用商店

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1506).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**因本案例玩法较简单，我们只需用 1 个场景来制作即可

<table data-full-width="false"><thead><tr><th width="164">场景名称</th><th>场景1-核心玩法</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/Animation1 (1).gif" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>玩家在遮罩位置任意滑动擦除遮罩，来显示出完整的美女图片</td></tr><tr><td><strong>核心资产</strong></td><td><p><strong>静帧图片：</strong><mark style="color:red;">遮罩</mark>、操作指引、下载按钮</p><p><strong>序列帧：</strong><mark style="color:red;">美女底图</mark></p><p><strong>视听包装：</strong>爱心粒子特效、擦除音效、美女害羞音效</p></td></tr><tr><td><strong>核心动画</strong></td><td><p>手指指引：位移缓动</p><p>美女放大出现：缩放缓动+位移缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：擦除组件Erase Component</p><p>触发事件：到达某一阶段</p><p>响应事件：隐藏蒙层</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*核心内容为Step3【事件设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

建议您在创建项目后，先将所有资产上传进【项目资产】内，方便后续添加使用

#### **1.全局场景**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息，并调整排版与适配

<figure><img src="../../../.gitbook/assets/image (1507).png" alt=""><figcaption></figcaption></figure>

#### **2.普通场景**

1）<mark style="color:red;">添加擦除组件：</mark>点击【玩法模板】，在【组件库】下将擦除组件添加进场景1

<figure><img src="../../../.gitbook/assets/image (1509).png" alt=""><figcaption></figcaption></figure>

2）将指引手、指引文案和底板、重玩按钮、音效相继添加进场景1

3）调整各资产到合适的位置大小，并根据资产类型对资产进行编组、排序、命名

4）将爱心粒子特效先设为"隐藏"状态，在后续我们通过事件来控制粒子的显示和播放

<figure><img src="../../../.gitbook/assets/image (1510).png" alt=""><figcaption></figcaption></figure>

5）调整横屏排版：可选中所有最高层级的图层，使用【复用竖屏位置尺寸配置】功能一键排版，然后再适当调整【位置】和【缩放比例】即可

<figure><img src="../../../.gitbook/assets/image (1511).png" alt=""><figcaption></figcaption></figure>

6）调整屏幕适配方式：在本案例中，我们想要横屏下的重玩按钮组和指引文本组始终位于屏幕底部，所以我们要调整其适配方式。依次选中图层，在右侧【屏幕适配方式】处点击向下图标即可（其他图层默认居中适配，无需调整）

<figure><img src="../../../.gitbook/assets/image (1512).png" alt=""><figcaption></figcaption></figure>



### Step2 - 组件参数设置 <a href="#tpuup" id="tpuup"></a>

1. 点击右上方【擦除设置】，进入擦除组件参数编辑面板

<figure><img src="../../../.gitbook/assets/image (1513).png" alt=""><figcaption></figcaption></figure>

2. 依次在**擦除层（Mask）**中添加擦除飘带图片，在**底图层（Bottom image）**中添加角色序列帧图片，然后将资产调整到合适的位置大小

<figure><img src="../../../.gitbook/assets/image (1514).png" alt=""><figcaption></figcaption></figure>

3. 然后我们根据实际需求，调整【擦除笔触设置】。在本案例中，我们选择使用60\*60大小的圆形笔触，不添加跟手图片

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1515).png" alt=""><figcaption></figcaption></figure>

</div>





### 动画设置 <a href="#tpuup" id="tpuup"></a>

在本案例中，需要设置动画的资产有：指引手指、指引文案、进度条(选做)、角色(选做)

<mark style="color:red;">温馨提示：若您使用了预设，则无需自己设置动画！</mark>

#### **1.指引手指**

1）选中手指图片\[gf\_hand]，添加动画-通用-位移缓动，参数设置如下(手指横向移动动画)：

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

2）选中手指组\[gf\_1]，添加动画-通用-位移缓动，参数设置如下(手指纵向移动动画)：

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

#### **2.指引文案**

选中指引文本\[tguidelines]，添加动画-强调动画-上下来回，参数设置如下（设置完成后可隐藏整个指引组，在后续通过事件控制）：

<figure><img src="../../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

#### 3.进度条(选做)

1）选中进度条图片\[progress\_bar]，将其【锚点】修改为（0,50），并取消勾选【参数横竖屏拆分】

注意：进度条图片左右需贴边，不能留空

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

2）添加动画-通用-缩放缓动，参数设置如下：

注意：这里的【持续时间】代表的是进度条加载到头所需的总时长。在本案例中，我们设定了"在进度条快加载完时，玩家不能再交互"，也就是当所有视频播放结束后，进度条需要差一截才到头，所以就需要"进度条播放的总时长＞所有视频加起来的总时长"。本案例的三段视频总时长为8.7s左右，所以在这里我们可以将进度条的【持续时间】设置为10s或更长

<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

#### 4.角色(选做)

1）选中角色图片\[role\_1]，将其【锚点】修改为（50,100），并取消勾选【参数横竖屏拆分】

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

2）添加动画-通用-缩放缓动，参数设置如下（设置完成后可隐藏该图层，在后续通过事件控制）：

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>



### <mark style="background-color:red;">Step3 - 事件设置</mark> <a href="#umduz" id="umduz"></a>

本案例的所有事件集中设置在三个视频图层上以及场景1上，我们按操作顺序依次讲解

#### <mark style="color:red;">1.图层: video\_01（初始视频1）</mark>

1）选中图层\[video\_01]，添加事件-开始时

* 添加响应事件：从头播放进度条动画

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

2）添加事件-结束时

* 添加响应事件：隐藏初始视频1；显示核心视频2、显示角色图片、显示操作指引组
* 添加响应事件：从头播放所有指引相关动画；同时暂停播放进度条动画

<div align="left">

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">2.图层: video\_02（核心视频2）</mark>

1）选中图层\[video\_02]，添加事件-按下

* 添加响应事件：设置埋点，修改埋点名称为"玩家第一次按下"
* 添加响应事件：隐藏角色图片、隐藏操作指引组
* 添加响应事件：继续播放核心视频2；并播放进度条动画和一次点击音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

</div>

2）添加事件-抬起

* 添加响应事件：暂停播放视频核心视频2
* 添加响应事件：显示操作指引组；并从头播放操作指引相关动画；同时暂停播放进度条动画

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

3）复制事件：复制\[video\_01]的"结束时"事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

粘贴事件：选中\[video\_02]，粘贴 - 仅粘贴图层事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 修改响应事件为：隐藏核心视频2；显示核心视频3；并删除显示角色图片
* 添加响应事件：跳转应用商店（此步骤就是前面提到的"强制跳转"）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">3.图层: video\_03（核心视频3）</mark>

1）复制事件：复制整个图层\[video\_02]

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2）粘贴事件：选中\[video\_03]，粘贴 - 仅粘贴图层事件（即一键粘贴该图层的所有事件）

<figure><img src="../../../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>

3）事件-按下

* 修改响应事件为：继续播放视频\[video\_03]；删除埋点事件、删除隐藏角色图片；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

</div>

4）事件-抬起

* 修改响应事件为：暂停播放视频\[video\_03]

<div align="left">

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

</div>

5）事件-结束时

* 删除响应事件：删除隐藏视频\[video\_02]、删除显示视频\[video\_03]、删除跳转应用商店
* 添加响应事件：禁用\[video\_03]的按下事件、禁用\[video\_03]的抬起事件（在设置完下一步的场景事件后，还需在这里添加一个响应事件"启用场景1的按下事件"）

<mark style="background-color:yellow;">注：这代表当最后一段视频播放结束，该视频的"按下/抬起"事件将不再生效，场景1的"按下"事件(即跳转事件)开始生效</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">4.场景: Scene 1</mark>

1）点击场景1 ，添加事件-按下

* 添加响应事件：跳转应用商店
* 添加响应事件：上报试玩结束
* 添加响应事件：从头播放一次点击音效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

</div>

2）添加事件-定时触发

* 设置执行延迟时间为0s
* 添加响应事件：禁用场景1的按下事件

<mark style="background-color:yellow;">注：这代表一进入试玩，场景1的"按下"事件(即跳转事件)即被禁用，不会生效。然后我们在核心视频3的"结束时"事件下添加"启用场景1的按下事件"</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

</div>

以上，就是本案例用到的全部事件。完成所有事件设置，我们的素材就制作完成了。



### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）建议在制作过程中，每完成一部分操作，就及时预览，检查设置是否正确

2）全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览，确认无误

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器制作此类素材

{% file src="../../../.gitbook/assets/模拟移动交互视频_资源.zip" %}
