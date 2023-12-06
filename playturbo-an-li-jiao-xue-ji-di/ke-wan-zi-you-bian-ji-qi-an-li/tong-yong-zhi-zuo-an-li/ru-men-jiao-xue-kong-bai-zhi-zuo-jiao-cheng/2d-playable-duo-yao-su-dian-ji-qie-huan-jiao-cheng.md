---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 2D playable《多要素点击切换》教程

温馨提示：入门难度模板《多要素点击切换》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：不限
* 【线程】：多线程
* 【核心资产】：静态图片
* 【功能】：动画-缩放缓动、事件-按下跳转指定场景、事件-定时触发



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1163).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1164).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1165).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/mr3fmh45)                                                 | [点击试玩](https://tinyurl.com/mr3fmh45)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【美女造型A】和【左右切换按钮】；
* 出现【操作指引】，提示玩家按下【右侧切换按钮】；
* 此时玩家可按下左右任一按钮，玩家第一次按下任一按钮后，播放【换装反馈】；
* 再次出现【操作指引】，提示玩家按下【确认按钮】；
  * 在玩家按下【确认按钮】前，可自由按下左右任一按钮切换造型，无次数限制
* 玩家按下【确认按钮】，跳转商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们可将本案例设置为4个场景来制作。

（场景1-3分别对应1套美女造型；场景4为结束页面）

<table data-full-width="true"><thead><tr><th width="137">场景名称</th><th>场景1-诱导切换</th><th>场景2-诱导点击</th><th>场景3-诱导点击</th><th>场景4-结束页</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1164).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1166).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1167).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1168).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>显示美女造型A，引导玩家点击右侧切换按钮</td><td>显示美女造型B，引导玩家点击确认按钮</td><td>显示美女造型C，引导玩家点击确认按钮</td><td>结束页，引导点击下载按钮</td></tr><tr><td><strong>动画</strong></td><td><p>【美女】：缩放缓动</p><p>【指引手指/箭头】：缩放缓动</p></td><td><p>【美女】：缩放缓动</p><p>【指引手指/箭头】：缩放缓动</p></td><td><p>【美女】：缩放缓动</p><p>【指引手指/箭头】：缩放缓动</p></td><td>【下载按钮】：缩放缓动</td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-左右箭头/确认按钮</p><p>触发操作：按下</p><p>响应事件：跳转指定场景</p></td><td><p>触发对象：图层-左右箭头/确认按钮</p><p>触发操作：按下</p><p>响应事件：跳转指定场景</p></td><td><p>触发对象：图层-左右箭头/确认按钮</p><p>触发操作：按下</p><p>响应事件：跳转指定场景</p></td><td><p>触发对象：图层-下载按钮</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【音频】：点击音效、换装音效</p><p>【图片】：美女造型图片、切换箭头图片、确认按钮图片、手指、指引文案背景图、logo、CTA按钮</p><p>【文本】：指引文案、确认按钮文案、下载文案</p><p>【粒子特效】</p></td><td><p>【音频】：点击音效、换装音效</p><p>【图片】：美女造型图片、切换箭头图片、确认按钮图片、手指、指引文案背景图、logo、CTA按钮</p><p>【文本】：指引文案、确认按钮文案、下载文案</p><p>【粒子特效】</p></td><td><p>【音频】：点击音效、换装音效</p><p>【图片】：美女造型图片、切换箭头图片、确认按钮图片、手指、指引文案背景图、logo、CTA按钮</p><p>【文本】：指引文案、确认按钮文案、下载文案</p><p>【粒子特效】</p></td><td><p>【图片】：背景图、logo、CTA按钮</p><p>【文本】：下载文案</p><p>【粒子特效】</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1169).png" alt=""><figcaption></figcaption></figure>

#### **2.全局场景**

1）在【全局场景】中添加常驻信息：logo、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1170).png" alt=""><figcaption></figcaption></figure>

**3..场景1-3**

1）在【场景1】中添加音效、美女造型图片、切换箭头、确认按钮、手指、指引文案、粒子特效

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1171).png" alt=""><figcaption></figcaption></figure>

注：因三个场景资产分布大体相同（场景1多一组指引手指），因此我们可以通过【复制场景】后微调来实现快速制作。

#### 4.**场景4** <a href="#tpuup" id="tpuup"></a>

1）在【场景4】中添加虚化背景图、LOGO、下载按钮、粒子特效，并打组

2）在右侧场景设置中勾选场景4为【结束场景】；同时场景4【取消启用全局场景】

<figure><img src="../../../../.gitbook/assets/image (1172).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.美女呼吸感**

1）在【场景1】左侧图层处选中人物组【role】，将锚点改为（50,100）

<figure><img src="../../../../.gitbook/assets/image (1173).png" alt=""><figcaption></figcaption></figure>

2）添加动画-通用-缩放缓动（作为美女进场动画）。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1174).png" alt=""><figcaption></figcaption></figure>

3）继续添加动画-通用-缩放缓动（作为美女呼吸感动画）。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1175).png" alt=""><figcaption></figcaption></figure>

注：场景2/场景3的美女动画同理场景1，可通过【复制/粘贴动画】来快速完成制作。

#### **2.下载按钮**

在【场景4】左侧图层处选中下载按钮组【ctat\_download】，添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1176).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

因场景2/场景3的事件设置同理场景1，所以在此仅以场景1举例说明，可通过【复制/粘贴事件】来快速完成场景2/场景3的事件设置；

另外，本案例有涉及【全局变量】，理解成本偏高且不影响此案例的教学，所以在此不做说明。

#### **1.场景1：图层事件-箭头**

1）选中右箭头组图层；

2）添加事件-按下；

3）添加响应事件-从头播放点击音效；从头播放右箭头缩放动画；

4）添加响应事件-执行延迟0.2s，跳转指定场景；

5）其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1177).png" alt=""><figcaption></figcaption></figure>

注：左箭头的事件设置同理右箭头，因此可通过【复制/粘贴事件】来快速完成制作。

#### **2.场景1：图层事件-确认按钮**

1）选中确认按钮组图层；

2）添加事件-按下；

3）添加响应事件-跳转指定场景（结束页）；跳转应用商店；

4）其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1178).png" alt=""><figcaption></figcaption></figure>

#### **3**.**场景1：场景事件**

1）在【场景1】下添加事件【定时触发】，设置执行延迟时间为0s；（即进入场景就生效）

2）添加响应事件-从头播放美女动画；从头播放操作指引动画；显示并播放粒子特效；从头播放粒子音效

<figure><img src="../../../../.gitbook/assets/image (1179).png" alt=""><figcaption></figcaption></figure>

#### 4.**场景4：场景事件** <a href="#j1kmp" id="j1kmp"></a>

1）在【场景4】下添加事件-按下；

2）添加响应事件-跳转应用商店；设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1180).png" alt=""><figcaption></figcaption></figure>

#### **5.全局场景：图层事件-CTA按钮**

选中【全局场景】中的下载按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1181).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1182).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1183).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1184).png" alt=""><figcaption></figcaption></figure>
