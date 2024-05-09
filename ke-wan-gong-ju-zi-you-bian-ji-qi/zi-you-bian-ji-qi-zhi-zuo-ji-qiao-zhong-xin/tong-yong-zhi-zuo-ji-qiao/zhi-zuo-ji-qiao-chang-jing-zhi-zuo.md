---
description: '#自由编辑器'
---

# 制作技巧-场景制作

## <mark style="color:blue;">一、整体建议</mark>

建议合理拆分场景：不要添加过多的场景，同时在同一场景内不要添加过多资产、设置过多效果，否则会导致可玩广告在投放时出现加载慢、卡顿等性能问题。

具体制作建议：

* 建议尽量压缩第一个主场景中的资产大小，不要有过大的视频资产，否则会影响素材的加载完成率和开始互动率
* 建议不要使用较大视频和大量序列帧，会影响素材加载率
* 同一场景内视频数量不要超过4个



## <mark style="color:blue;">二、全局场景</mark>

建议将常驻信息放置于【全局场景】内，可以免去重复制作的麻烦，同时便于统一管理。

常驻信息一般包含：产品信息/下载按钮/免责声明。您也可根据实际情况，将那些会出现在每一个场景的内容放置于全局场景 [quan-ju-she-zhi.md](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/chang-jing-qu/quan-ju-she-zhi.md "mention")

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

在普通场景的场景设置中，可以根据实际制作情况灵活调整，支持选择是否要在当前场景启用【全局场景】，以及将【全局场景】置于当前场景的顶层还是底层。

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

举个例子：在结束页面想做遮罩效果时，可以选择将全局场景【置于场景底层】，更加美观

<div align="left">

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">三、普通场景</mark>

场景拆分核心思想：让单个场景里的动画和事件尽可能少，图层结构简单（便于后续检查动画和事件设置问题），同时还要避免添加过多场景导致试玩卡顿，所以我们通常建议将<mark style="color:orange;">核心玩法</mark>与<mark style="color:orange;">结果反馈</mark>分开制作。

**下面我们通过一个**[**案例**](../../../playturbo-an-li-jiao-xue-ji-di/ke-wan-zi-you-bian-ji-qi-an-li/tong-yong-zhi-zuo-an-li/chu-ji-jiao-xue-kong-bai-zhi-zuo-jiao-cheng/2d-playable-san-xuan-yi-duo-chang-jing-jiao-cheng.md)**进行详细说明：**

### 1.Scene1 ：核心玩法

展示素材核心玩法及操作指引，明确交互目标，诱导玩家操作

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 2.Scene2/3/4：对应结果A/B/C

已知在Scene1有三个选项可以选择，会对应生成三种不同的结果，因此我们将每个结果单独放置在一个场景

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 3.Scene5：结束页面

结束页面可作为用户跳转商店后返回的落地页，通常建议展示：产品信息、结算信息、奖励信息、福利信息等内容，并添加跳转按钮

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
