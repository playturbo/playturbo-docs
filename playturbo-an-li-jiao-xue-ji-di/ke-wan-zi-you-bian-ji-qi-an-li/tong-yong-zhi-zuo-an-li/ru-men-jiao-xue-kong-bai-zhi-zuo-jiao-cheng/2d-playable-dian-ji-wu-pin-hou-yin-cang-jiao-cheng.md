---
description: '#自由编辑器 #空白制作 #通用制作 #入门难度'
---

# 2D playable《点击物品后隐藏》教程

温馨提示：入门难度模板《点击物品后隐藏》就是按照这个教程制作的哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【交互次数】：3步跳转
* 【线程】：单线程
* 【核心资产】：静态图片
* 【功能】：动画-淡入、动画-缩小消失、动画-放大出现、事件-按下隐藏素材、事件-按下显示素材



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                             | 竖屏                                                                                   | 横屏                                                                                   |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| <img src="../../../../.gitbook/assets/image (1120).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1121).png" alt="" data-size="original"> | <img src="../../../../.gitbook/assets/image (1123).png" alt="" data-size="original"> |
| 扫码试玩                                                                                 | [点击试玩](https://tinyurl.com/muy57s72)                                                 | [点击试玩](https://tinyurl.com/muy57s72)                                                 |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，展示【初始金额】和桌面上错落摆放的六个礼盒；
* 出现【操作指引】，提示玩家点击打开礼盒A；
* 玩家第一次按下，打开礼盒A：播放【开奖反馈】，显示【第一次金额】；
* 再次出现【操作指引】，提示玩家点击打开礼盒B；
* 玩家第二次按下，打开礼盒B：播放【开奖反馈】，显示【第二次金额】；
* 弹出【奖励弹窗】，玩家全屏任意按下，跳转应用商店



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第三部分的玩法梳理，我们判断本案例设置1个场景即可

<table><thead><tr><th width="178">场景名称</th><th>场景1-诱导点击</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/image (1122).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>摆放有多个礼盒，引导玩家点击打开已解锁的礼盒</td></tr><tr><td><strong>动画</strong></td><td><p>【人物呼吸感】：缩放缓动</p><p>【金额文案】：缩小消失</p><p>【奖励弹窗】：淡入+缩放缓动</p><p>【散射光】：放大出现+旋转缓动</p></td></tr><tr><td><strong>核心事件</strong></td><td><p>触发对象：图层-手势区域</p><p>触发操作：按下</p><p>响应事件：隐藏素材；显示素材</p></td></tr><tr><td><strong>资产清单</strong></td><td><p>【音频】：背景音乐、音效（解锁音效/奖励音效/胜利音效）</p><p>【图片】：背景图片、人物图片、礼盒图片、金额面板图片、奖励弹窗图片、指引手指、logo、CTA按钮</p><p>【文本】：指引文案、金额文案、奖励弹窗文案、产品名称、下载文案、免责声明</p></td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

在【全局设置】中添加背景音乐、背景图片

<figure><img src="../../../../.gitbook/assets/image (1124).png" alt=""><figcaption></figcaption></figure>

#### **2.场景1**

1）在【场景1】中添加音频、金额面板图片及文本、奖励弹窗图片及文本、礼盒图片及文本、角色图片、操作指引、常驻信息及免责声明

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

<figure><img src="../../../../.gitbook/assets/image (1125).png" alt=""><figcaption></figcaption></figure>

### Step2 - 动效制作 <a href="#tpuup" id="tpuup"></a>

本案例涉及动画较多，但大多为丰富礼盒效果所做的动画，且相关动画在前面的教学案例中有涉及，所以在此不做详细教学，仅针对此前未介绍过的动画进行教学。

#### **1.**人物呼吸感

1）在左侧图层处选中人物图片【role】，将锚点改为（50,100）

<figure><img src="../../../../.gitbook/assets/image (1126).png" alt=""><figcaption></figcaption></figure>

2）再添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1127).png" alt=""><figcaption></figcaption></figure>

#### **2.金额文本**

在左侧图层处选中金额文本【money\_0】，添加动画-退场动画-缩小消失。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1128).png" alt=""><figcaption></figcaption></figure>

注：金额文本【money\_1】和【money\_2】需额外添加淡入+缩放缓动动画，具体参数设置可进项目内查看。

#### **3.奖励弹窗**

1）在左侧图层处选中奖励弹窗组【endboard】，添加动画-进场动画-淡入。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1129).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-缩放缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1130).png" alt=""><figcaption></figcaption></figure>

**4.散射光**

1）在左侧图层处选中散射光图片【light】，添加动画-进场动画-放大出现。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1131).png" alt=""><figcaption></figcaption></figure>

2）继续添加动画-通用-旋转缓动。参数设置如下：

<figure><img src="../../../../.gitbook/assets/image (1132).png" alt=""><figcaption></figcaption></figure>

### Step3 - 逻辑设置 <a href="#umduz" id="umduz"></a>

#### **1.图层事件-手势区域1（红礼盒）**

1）选中左侧手势区域1图层；

2）添加事件-按下；

3）添加响应事件-隐藏素材手势区域1；（即保证玩家仅可点击1次红礼盒）

4）添加响应事件-隐藏素材操作指引相关；

5）添加响应事件-从头播放红礼盒的退场动画；显示素材奖励，并播放相关奖励动画及特效音效；

6）添加响应事件-从头播放金额文本0的退场动画；显示素材金额文本1，并播放相关文本动画；

<figure><img src="../../../../.gitbook/assets/image (1133).png" alt=""><figcaption></figcaption></figure>

7）添加响应事件-执行延迟1s；

8）添加响应事件-播放蓝礼盒相关动画；显示素材操作指引相关，并播放相关动画；

9\)其他响应事件：设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1134).png" alt=""><figcaption></figcaption></figure>

#### **2.图层事件-手势区域2（蓝礼盒）**

蓝礼盒的事件设置同理红礼盒，可通过【复制/粘贴事件】后微调来快速完成制作。

有所区别的事件设置：

1）添加响应事件-执行延迟1s；

2）添加响应事件-显示奖励弹窗相关，并播放相关动画及特效音效；

3）其他响应事件：设置埋点信息；上报试玩结束

<figure><img src="../../../../.gitbook/assets/image (1135).png" alt=""><figcaption></figcaption></figure>

#### **3.图层事件-CTA按钮**

选中奖励弹窗下载按钮组，添加事件-按下，添加响应事件-跳转应用商店；设置埋点信息

<figure><img src="../../../../.gitbook/assets/image (1136).png" alt=""><figcaption></figcaption></figure>

选中常驻下载按钮组，添加事件-按下，添加响应事件-跳转应用商店

<figure><img src="../../../../.gitbook/assets/image (1137).png" alt=""><figcaption></figcaption></figure>

### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

#### <mark style="color:red;">**1.横屏排版**</mark>

每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）

<figure><img src="../../../../.gitbook/assets/image (1138).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**2.屏幕适配**</mark>

对各机型及其横竖屏进行屏幕适配，并预览适配效果是否合适

<figure><img src="../../../../.gitbook/assets/image (1139).png" alt=""><figcaption></figcaption></figure>

**3.整体预览**

全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../../.gitbook/assets/image (1140).png" alt=""><figcaption></figcaption></figure>
