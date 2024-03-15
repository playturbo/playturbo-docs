---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# IEC《二选一决策》教程

温馨提示：入门难度模板《二选一决策》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：1步跳转
* 【线程】：双线程
* 【核心资产】：静态图
* 【功能】：动画-缩放缓动、动画-位移缓动、事件-按下跳转应用商店



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                            | 竖屏                                                                                  | 横屏                                                                                  |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| <img src="../../../../.gitbook/assets/image (110).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (111).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (112).png" alt="" data-size="original"> |
| 扫码试玩                                                                                | [点击试玩](https://tinyurl.com/4xzhahfy)                                                | [点击试玩](https://tinyurl.com/4xzhahfy)                                                |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【丑女待改造】画面；
* 出现【二选一选项】和【选择指引】，引导玩家点击任一选项，帮助丑女完成改造；
* 玩家点击任一选项，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们判断本案例只需设置1个场景即可

<table><thead><tr><th width="178">场景名称</th><th>场景1-诱导选择</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (111).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>二选一决策，引导玩家点击任一选项帮助丑女完成改造</td></tr><tr><td><strong>动画</strong></td><td><p>【指引手指】：缩放缓动+位移缓动</p><p>【选项按钮】：缩放缓动+透明度缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-选项按钮组</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【音频】：背景音乐</p><p>【图片】：背景图片、丑女图片、指引手指、选项按钮（选项图片/选项背景/选项背景发光）、logo、CTA按钮</p><p>【文本】：指引文案、选项按钮文案、下载文案</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1**

1）在【场景1】中添加图片和文本：丑女图片、选项按钮、指引手指、指引文案、logo、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.指引手指**

因手指在引导二选一决策时，需要进行位移，同时要根据按钮的缩放同步进行缩放，因此我们为手指设置2个通用动画，分别为：缩放缓动、位移缓动；

1）在左侧图层处选中手指组【hand\_ani】，添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

#### **2.选项按钮**

1）选项1：选中选项按钮1的组节点【props1\_ani】，添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

2）选项2：复制组节点【props1\_ani】的缩放缓动动画，选中选项按钮2的组节点【props2\_ani】，点击【粘贴-仅粘贴图层动画】，然后仅修改曲线即可。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

选做：为使效果更为丰富，我们可以视情况为选项按钮添加外发光的效果。

3）选项外发光1：选中选项1的外发光图片，添加动画-通用-透明度缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

4）选项外发光2：选中选项2的外发光图片，添加动画-通用-透明度缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.**图层事件-选项按钮1&2

1）选中选项按钮1的组节点【props1\_ani】；

2）添加事件-按下；

3）添加响应事件-跳转应用商店；

4）其他响应事件：设置埋点信息/上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

5）点击复制按钮1的事件，选中选项按钮2的组节点【props2\_ani】，点击【粘贴-仅粘贴图层事件】，然后修改埋点信息即可。

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

**2.图层事件-CTA按钮**

选中按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">六、资源提供</mark>

在教程最后，我们为您**提供了本案例所使用到的全部资源，**点击压缩包即可下载。您可以用此资源跟着教程尝试制作，以便尽快上手使用自由编辑器

{% file src="../../../../.gitbook/assets/二选一决策_资源.zip" %}
