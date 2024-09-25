---
description: '#自由编辑器 #空白制作 #模板自由制作'
---

# 作品制作-重要提示⚠️

请在导出作品前，确认已完成【设置跳转应用商店】以及【上报试玩结束】



<mark style="color:red;">注意：</mark>

* <mark style="color:red;">若在作品导出前未设置【跳转应用商店】和【上报试玩结束】，则会弹出以下提示，无法导出作品。</mark>

<div align="left">

<figure><img src="../.gitbook/assets/image (610).png" alt=""><figcaption></figcaption></figure>

</div>

* <mark style="color:red;">若不设置【跳转应用商店】或者【上报试玩结束】，都会导致素材无法进行正常投放，或者会直接影响素材投放效果。</mark>
* <mark style="color:red;">一般来说，模板本身自带【跳转应用商店】和【上报试玩结束】设置，但一旦有事件改动，建议进行额外检查。</mark>

## <mark style="color:blue;">跳转应用商店</mark>

在作品中合适的位置，添加【跳转应用商店】响应事件，确保用户体验时能顺利到达下载页面

### 常用设置方法

#### **1. 下载按钮触发跳转**

玩家主动交互任意按钮跳转商店

* 在图层处选中按钮或按钮组
* 点击【添加事件】并选择触发事件，如按下/点击
* 选择响应事件为【跳转应用商店】并保存

<div align="left">

<figure><img src="../.gitbook/assets/image (821).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2. 全屏幕触发跳转**

玩家在全屏范围内，交互任意地方跳转商店

* 选中结束场景
* 点击【添加事件】并选择触发事件，如按下/点击
* 选择响应事件为【跳转应用商店】并保存

<div align="left">

<figure><img src="../.gitbook/assets/image (672).png" alt=""><figcaption></figcaption></figure>

</div>

#### **3. 定时触发跳转**

任何跟操作不相关的自动跳转商店（注意：部分渠道规范不允许这类跳转）

* 选中结束场景
* 点击【添加事件】并选择【定时触发】
* 设置执行延迟时间，选择响应事件为【跳转应用商店】并保存

<div align="left">

<figure><img src="../.gitbook/assets/image (585).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">上报试玩结束</mark>

当前Vungle和Mintegral渠道，会要求可玩素材设置【上报试玩结束】，以确保素材内容流程完整，符合投放规范（其他渠道无硬性要求）。因此，<mark style="color:red;">若您的素材需要投放Vungle或Mintegral渠道，则需要在试玩结束的时候，设置【上报试玩结束】</mark>

### 常用设置方法

#### **1.直接勾选场景上报**

* 选中结束场景
* 在【场景设置】下勾选【结束场景】即可
* <mark style="color:red;">**注意：**</mark>在此处勾选【结束场景】，意味的是“一进入这个场景就会上报试玩结束”，而不是“等到试玩最后再上报试玩结束”。因此，<mark style="color:red;">当您的可玩项目仅有1个场景时，不建议直接勾选场景上报！请使用方法2</mark>

<div align="left">

<figure><img src="../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2.设置响应事件进行上报**

* 在试玩结束时，选中对应图层或场景
* 点击【添加事件】并选择触发事件，如按下/点击
* 选择响应事件为【上报试玩结束】并保存

<div align="left">

<figure><img src="../.gitbook/assets/image (700).png" alt=""><figcaption></figcaption></figure>

</div>
