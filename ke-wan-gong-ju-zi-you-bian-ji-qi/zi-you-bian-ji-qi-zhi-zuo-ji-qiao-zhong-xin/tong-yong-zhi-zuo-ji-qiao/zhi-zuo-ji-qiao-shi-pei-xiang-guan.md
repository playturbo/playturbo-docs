---
description: '#自由编辑器'
---

# 制作技巧-适配相关

## <mark style="color:blue;">一、适配方向</mark>

在新建空白制作项目时，需要选择适配方向（模板默认为\[横屏&竖屏]）

* 若选择【横屏&竖屏】，则在制作时需要分别对竖屏和横屏进行排版制作<mark style="color:red;">（建议您在完成每个场景竖屏的排版后，及时切换到横屏进行调整，通过“复用竖屏位置尺寸配置”按钮可以大大提高效率）</mark>
* 若选择单方向【横屏】或【竖屏】，只需制作当前屏幕方向的素材即可，无需切换横竖屏

不同适配方向呈现出的效果可查看[zuo-pin-zhi-zuo-xin-jian-zhi-nan.md](../../zuo-pin-zhi-zuo-xin-jian-zhi-nan.md "mention") [#step3-xuan-ze-kuo-pei-fang-xiang](../../zuo-pin-zhi-zuo-xin-jian-zhi-nan.md#step3-xuan-ze-kuo-pei-fang-xiang "mention")

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1).png" alt="" width="351"><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">二、适配技巧</mark>

### 1.背景图片

无论您是否要在场景中添加背景图片，我们都建议您先在【全局设置】添加背景图片兜底。因为：

* 在【全局设置】添加的背景图片会自动适配所有机型，无论在多大尺寸屏幕下预览，背景图片都会被拉伸至铺满全屏，不会出现白边
* 如果仅在场景下添加图片，图片尺寸不够大时，在部分机型预览下就会露出白边
* 在【全局设置】添加的背景图片层级默认位于所有图层最底部，因此不会影响其他图层的排版

<figure><img src="../../../.gitbook/assets/image (1282).png" alt=""><figcaption></figcaption></figure>

所以通常，我们添加背景图片分两种情况：

1）背景图片样式简单/与核心玩法相关性小——此种情况，可直接在【全局设置】添加背景图片，无需在场景中二次添加

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1278).png" alt=""><figcaption></figcaption></figure>

</div>

2）背景图片的内容有用/与核心玩法密不可分——此种情况，可先在【全局设置】中添加一张模糊/纯色背景图片兜底，然后再进入场景添加该背景图片

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1279).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**Tips：**</mark>通常，我们会将添加在场景中的背景图片尺寸做大一些，在制作时拉出画布外，以适应不同机型下的预览。当图片尺寸为1800\*1800时，基本可以保证覆盖到所有机型。

<figure><img src="../../../.gitbook/assets/image (1281).png" alt=""><figcaption></figcaption></figure>



### 2.屏幕适配方式

关于屏幕适配方式的功能介绍可查看[shi-pei-gui-ze-yu-shi-pei-fang-shi.md](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/shi-pei-gui-ze-yu-shi-pei-fang-shi.md "mention")

所有图层的屏幕适配方式默认“水平居中&垂直居中”，即无论在哪种机型下预览素材，该图层都会位于屏幕最中心位置

<figure><img src="../../../.gitbook/assets/image (1277).png" alt=""><figcaption></figcaption></figure>

部分图层，我们在制作时需要调整其屏幕适配方式，以保证在不同机型预览下的视觉效果。

常见需要调整屏幕适配方式的图层有：常驻信息、免责声明

#### 1）常驻信息（包含产品信息&下载按钮）

<table><thead><tr><th width="190">适配方向</th><th>图示</th><th>屏幕适配方式</th></tr></thead><tbody><tr><td>竖屏：顶部</td><td><img src="../../../.gitbook/assets/image (1285).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1286).png" alt="" data-size="original"></td></tr><tr><td>竖屏：底部</td><td><img src="../../../.gitbook/assets/image (1291).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1288).png" alt="" data-size="original"></td></tr><tr><td>横屏：左上角</td><td><img src="../../../.gitbook/assets/image (1290).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1289).png" alt="" data-size="original"></td></tr></tbody></table>

#### 2）免责声明

免责声明默认居中贴底适配

<table><thead><tr><th width="190">适配方向</th><th>图示</th><th>屏幕适配方式</th></tr></thead><tbody><tr><td>横屏/竖屏：底部</td><td><img src="../../../.gitbook/assets/image (1292).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1293).png" alt="" data-size="original"></td></tr></tbody></table>

**注：**默认\[屏幕适配方式]参数横竖屏拆分。若图层在横竖屏下的位置不一致，则需分开设置屏幕适配方式；若一致，可取消勾选拆分



### 3.视频适配技巧

因视频的尺寸是固定的，无法像图片一样通过拉伸去适配所有机型。因此，在视频的适配上我们有以下两点制作技巧供您参考(以下截图仅做方法展示)：

#### 1）调整原视频

* 此方法适用于原视频可以被一定范围内放大尺寸 或 原视频内部分UI可单独制作
* 为了美观，建议先在外部调整视频尺寸或为视频上下部分添加遮罩，然后导出视频
* 将处理后的视频导入自由编辑器，直接调整位置尺寸即可
* 最终预览效果可参考iPad机型

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1295).png" alt=""><figcaption></figcaption></figure>

</div>

#### 2）不调整原视频

* 此方法适用于原视频需要被完整展示，不可被遮挡
* 需要先在画布内将视频调整到合适的位置大小
* 然后准备两张和视频同色的图片进行填充，放置于视频上下两端，并调整位置大小

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1297).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

* 最终效果参考：

<figure><img src="../../../.gitbook/assets/image (1294).png" alt=""><figcaption></figcaption></figure>
