---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 交互视频《多结局交互》教程

温馨提示：入门难度模板《多结局交互视频》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：2步跳转
* 【线程】：双线程
* 【核心资产】：视频（3段/连贯的）
* 【功能】：动画-缩放缓动、事件-按下跳转指定场景、事件-定时触发从头播放动画



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1099).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1100).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1101).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/yc388fpb)                                                 | [点击试玩](https://tinyurl.com/yc388fpb)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，循环播放视频【美女被骚扰】；
* 出现【左右选择指引】，引导玩家按下选项进行辨别；
* 玩家按下左侧【救她】选项时：进入救人结局
  * 播放1次视频【主角飞踢画面+美女感谢】
  * 再次出现【左右选择指引】，引导玩家按下选项进行辨别
  * 玩家全屏按下，跳转应用商店
*   玩家按下右侧【不救她】选项时：进入逃跑结局；

    * 播放1次视频【主角反向逃跑遇到BOSS】
    * 再次出现【左右选择指引】，引导玩家按下选项进行辨别
    * 玩家全屏按下，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们可将本案例设置为3个场景来制作

（场景1：诱导选择；场景2：结局A；场景3：结局B）

<table data-full-width="true"><thead><tr><th width="140">场景名称</th><th>场景1-诱导选择</th><th>场景2-结局A</th><th>场景3-结局B</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1102).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1103).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (1104).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>循环播放视频【美女被骚扰】，引导玩家做出选择</td><td>播放结局A视频，视频播放结束时引导玩家做出第二轮选择</td><td>播放结局B视频，视频播放结束时引导玩家做出第二轮选择</td></tr><tr><td><strong>动画</strong></td><td><p>【选项按钮】：缩放缓动</p><p>【指引手指】：缩放缓动+位移缓动</p></td><td><p>【选项按钮】：缩放缓动+透明度缓动</p><p>【指引手指】：缩放缓动+位移缓动</p></td><td><p>【选项按钮】：缩放缓动+透明度缓动</p><p>【指引手指】：缩放缓动+位移缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-手势区域</p><p>触发操作：按下</p><p>响应事件：跳转指定场景</p></td><td><p>触发对象：场景-场景2</p><p>触发操作：定时触发</p><p>响应事件：从头播放全部动画</p><hr><p>触发对象：场景-场景2</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td><td><p>触发对象：场景-场景3</p><p>触发操作：定时触发</p><p>响应事件：从头播放全部动画</p><hr><p>触发对象：场景-场景3</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【视频】：入场自动播放、无限循环</p><p>【音频】：点击音效</p><p>【图片】：指引文案、指引手指、选项按钮</p></td><td><p>【视频】：入场自动播放、关闭无限循环</p><p>【图片】：指引手指、选项按钮</p></td><td><p>【视频】：入场自动播放、关闭无限循环</p><p>【图片】：指引手指、选项按钮</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1105).png" alt=""><figcaption></figcaption></figure>

#### **2.全局场景**

1）在【全局场景】中添加常驻信息：logo、CTA按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1106).png" alt=""><figcaption></figcaption></figure>

**3.场景1**

1）在【场景1】中添加视频、音效、指引手指、指引文案、选项按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1107).png" alt=""><figcaption></figcaption></figure>

#### 4.**场景2-场景3** <a href="#tpuup" id="tpuup"></a>

1）在【场景2】【场景3】中分别添加视频、指引手指、选项按钮

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1108).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

#### **1.**场景1-指引手指

因手指在诱导选择时，需要进行位移，同时要根据按钮的缩放同步进行缩放，因此我们为手指设置2个通用动画，分别为：位移缓动、缩放缓动；

1）在场景1左侧图层处选中手指图片【gf\_hand】，添加动画-通用-位移缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1109).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1110).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1-选项按钮**

1）在场景1图层处选中左侧选项按钮组【left\_options】，添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1111).png" alt=""><figcaption></figcaption></figure>

2）复制动画到右侧选项按钮组【right\_options】，修改动画曲线即可：

<figure><img src="../../../../.gitbook/assets/image (1112).png" alt=""><figcaption></figcaption></figure>

#### **3**.场景2/场景3-透明度缓动

因场景2/场景3中的手指动画和选项按钮动画同场景1，因此我们可以【复制/粘贴动画】来快速完成制作。

另外，我们可以在此基础上新增透明度缓动动画，将资产的起始透明度设为0，即进入场景时手指和选项按钮处于不显示状态，待视频播放完成后再显示。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1113).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.场景1：图层事件-手势区域**

我们分别为左右两个选项按钮设置两个手势区域，先对左侧手势区域设置事件，再将事件复制到右侧手势区域，简单调整，来快速完成制作。

1）选中左侧手势区域图层；

2）添加事件-按下；

3）添加响应事件-暂停播放单个动画；（即选项按钮的缩放动画）

4）添加响应事件-执行延迟0.3s后跳转指定场景；（即在玩家按下按钮0.3s后跳转到对应结局）

5）其他响应事件：从头播放音效；设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1114).png" alt=""><figcaption></figcaption></figure>

#### **2.场景2/3：场景事件**

1）在场景2下添加事件-定时触发；

2）添加响应事件-执行延迟3s后从头播放全部动画；（即当视频播放结束时，从头播放手指和选项按钮动画）

3）添加事件-按下，添加响应事件-跳转应用商店，设置埋点信息，上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (1115).png" alt=""><figcaption></figcaption></figure>

注：场景3的事件设置同理场景2，可通过【复制/粘贴事件】来快速完成制作。

#### **3**.全局场景：图层事件-CTA按钮

在【全局场景】选中按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1116).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1117).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1118).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1119).png" alt=""><figcaption></figcaption></figure>
