---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 交互视频《3步点击》教程

温馨提示：入门难度模板《3步点击交互视频》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：3步跳转
* 【线程】：单线程
* 【核心资产】：视频（5段/连贯的）
* 【功能】：动画-位移缓动、事件-按下从头播放视频、事件-视频结束时跳转到下一场景



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                                                                                                                                                                                                                                                                                                                                                       | 横屏                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1079).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1080).png" alt="" data-size="original">                                                                                                                                                                                                                                                                                                                                     | <img src="../../../../.gitbook/assets/image (1081).png" alt="" data-size="original">                                                                                                                                                                                                                                                                                                                                     |
| 扫码试玩                                                                                 | [点击试玩](https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fgm%2Ft%2F20000751%2F11662%2Fpv%2F23%2F09%2F13%2F6501901b8a614%2Fproject.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn\&mw\_test=0\&is\_browser\_tips=1\&track\_data=%7B%22pid%22%3A20000751%2C%22uid%22%3A9432%2C%22skin\_id%22%3A11662%2C%22sct%22%3A%22pt\_template\_index%22%2C%22env%22%3A%22p%22%7D) | [点击试玩](https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fgm%2Ft%2F20000751%2F11662%2Fpv%2F23%2F09%2F13%2F6501901b8a614%2Fproject.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn\&mw\_test=0\&is\_browser\_tips=1\&track\_data=%7B%22pid%22%3A20000751%2C%22uid%22%3A9432%2C%22skin\_id%22%3A11662%2C%22sct%22%3A%22pt\_template\_index%22%2C%22env%22%3A%22p%22%7D) |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【初始汽车移动-待发射】；
* 出现【操作指引】，提示玩家按下发射汽车；
* 玩家全屏任意按下，播放【汽车首次发射】视频；
* 播放【第二次待机】视频，再次出现【操作指引】，提示玩家按下发射汽车；
* 玩家全屏任意按下，播放【汽车第二次发射】视频；
* 播放【第三次待机】视频，再次出现【操作指引】，提示玩家按下发射汽车；
* 玩家全屏任意按下，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们可将本案例设置为3个场景来制作

（共5段视频，场景1和场景2分别包含一段循环视频和反馈视频，场景3作为结束页包含一段循环视频）

<table data-full-width="true"><thead><tr><th width="140">场景名称</th><th>场景1-诱导点击+播放视频</th><th>场景2-诱导点击+播放视频</th><th>场景3-结束页诱导点击</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1080).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1082).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1083).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>第一次待机视频循环播放，引导玩家点击合成汽车，玩家点击后播放汽车首次发射视频</td><td>第二次待机视频循环播放，引导玩家点击合成汽车，玩家点击后播放汽车第二次发射视频</td><td>第三次待机视频循环播放，引导玩家点击合成汽车，玩家点击后跳转应用商店</td></tr><tr><td><strong>动画</strong></td><td><p>【指引文案】：闪烁</p><p>【指引手指】：位移缓动</p><p>【指引箭头】：左右滑动</p></td><td><p>【指引文案】：闪烁</p><p>【指引手指】：位移缓动</p><p>【指引箭头】：左右滑动</p></td><td><p>【指引文案】：闪烁</p><p>【指引手指】：位移缓动</p><p>【指引箭头】：左右滑动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：场景-场景1</p><p>触发操作：按下</p><p>响应事件：从头播放视频</p><hr><p>触发对象：图层-视频</p><p>触发操作：结束时</p><p>响应事件：跳转到下一场景</p></td><td><p>触发对象：场景-场景2</p><p>触发操作：按下</p><p>响应事件：从头播放视频</p><hr><p>触发对象：图层-视频</p><p>触发操作：结束时</p><p>响应事件：跳转到下一场景</p></td><td><p>触发对象：场景-场景3</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【视频】：视频a循环（自动播放&#x26;无限循环）；视频a（关闭自动播放&#x26;无限循环）</p><p>【音频】：汽车发射音效、汽车撞击音效</p><p>【图片】：指引文案、指引手指、指引箭头</p></td><td><p>【视频】：视频b循环（自动播放&#x26;无限循环）；视频b（关闭自动播放&#x26;无限循环）</p><p>【音频】：汽车发射音效、汽车撞击音效</p><p>【图片】：指引文案、指引手指、指引箭头</p></td><td><p>【视频】：视频c循环（自动播放&#x26;无限循环）</p><p>【图片】：指引文案、指引手指、指引箭头</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1084).png" alt=""><figcaption></figcaption></figure>

#### **2.全局场景**

1）在【全局场景】中添加常驻信息：logo、CTA按钮、白色底图

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1085).png" alt=""><figcaption></figcaption></figure>

**3.场景1-3**

1）在【场景1】中添加视频、音效、指引手指、指引箭头、指引文案

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1088).png" alt=""><figcaption></figcaption></figure>

注：因三个场景资产分布大体相同，我们可以通过【复制场景】后微调来实现【场景2】【场景3】的快速制作。

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.指引文案**

在左侧图层处选中指引文本【text:guide】，添加动画-强调-闪烁。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1089).png" alt=""><figcaption></figcaption></figure>

#### **2.指引手指**

在左侧图层处选中手指组【hand】，添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1090).png" alt=""><figcaption></figcaption></figure>

#### **3.指引虚线**

在左侧图层处选中右箭头图片【rightarrow】，添加动画-强调-左右滑动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1091).png" alt=""><figcaption></figcaption></figure>

注：左箭头图片的动画可直接复制右箭头的，将X轴位移参数改为-22即可。



### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.**场景1/2：场景事件

1）在场景1下添加事件-按下；

2）添加响应事件-隐藏素材指引相关；隐藏素材视频a循环；

添加响应事件-从头播放视频a；从头播放音效；

3）添加响应事件-禁用事件“按下”（保证玩家仅可点击1次）；

4）其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1092).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1/2：图层事件-视频**

1）选中视频a图层；

2）添加事件-结束时；

3）添加响应事件-跳转到下一场景

<figure><img src="../../../../.gitbook/assets/image (1093).png" alt=""><figcaption></figcaption></figure>

注：场景2的事件设置同理场景1，仅需将相关资产替换为场景2的即可，因此我们可以通过【复制/粘贴事件】的方式来快速制作。

#### **3.**场景3：场景事件

1）在场景3下添加事件-按下；

2）添加响应事件-跳转应用商店；设置埋点信息；上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (1094).png" alt=""><figcaption></figcaption></figure>

#### **4.**全局场景：图层事件-CTA按钮

在【全局场景】中选中按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1095).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1096).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1097).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1098).png" alt=""><figcaption></figcaption></figure>
