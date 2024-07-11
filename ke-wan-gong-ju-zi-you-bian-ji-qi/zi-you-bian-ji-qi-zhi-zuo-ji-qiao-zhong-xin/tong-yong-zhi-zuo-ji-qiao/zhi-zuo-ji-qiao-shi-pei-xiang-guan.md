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

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="351"><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">二、适配技巧</mark>

### 1.添加背景图片

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

<mark style="color:red;">**Tips：**</mark>通常，我们会将添加在**普通场景**中的背景图片尺寸做大一些，在制作时拉出画布外，以适应不同机型下的预览。当图片尺寸为1800\*1800时，基本可以保证覆盖到所有机型。

<figure><img src="../../../.gitbook/assets/image (1281).png" alt=""><figcaption></figcaption></figure>



### 2.调整屏幕适配方式

关于屏幕适配方式的功能介绍可查看[shi-pei-gui-ze-yu-shi-pei-fang-shi.md](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/shi-pei-gui-ze-yu-shi-pei-fang-shi.md "mention")

各类资产在被添加到项目中时，其屏幕适配方式都默认“水平居中&垂直居中”，即无论在哪种机型下预览素材，该资产都会位于屏幕中心位置

<figure><img src="../../../.gitbook/assets/image (1277).png" alt=""><figcaption></figcaption></figure>

大部分资产无需调整屏幕适配方式。但也有少部分资产，在制作时需要调整屏幕适配方式，以保证在不同机型预览下的最佳视觉效果。

常见需要调整屏幕适配方式的图层有：常驻产品信息、免责声明

#### 1）常驻信息（包含产品信息&下载按钮）

<table><thead><tr><th width="190">建议适配方向</th><th>图示</th><th>屏幕适配方式</th></tr></thead><tbody><tr><td>竖屏：顶部</td><td><img src="../../../.gitbook/assets/image (1285).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1286).png" alt="" data-size="original"></td></tr><tr><td>竖屏：底部</td><td><img src="../../../.gitbook/assets/image (1291).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1288).png" alt="" data-size="original"></td></tr><tr><td>横屏：左上角</td><td><img src="../../../.gitbook/assets/image (1290).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1289).png" alt="" data-size="original"></td></tr></tbody></table>

#### 2）免责声明

免责声明建议居中贴底适配

<table><thead><tr><th width="190">建议适配方向</th><th>图示</th><th>屏幕适配方式</th></tr></thead><tbody><tr><td>横屏/竖屏：底部</td><td><img src="../../../.gitbook/assets/image (1292).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (1293).png" alt="" data-size="original"></td></tr></tbody></table>

**注：**默认"\[屏幕适配方式]参数横竖屏拆分"。若图层在横竖屏下的位置不一致，则需分开设置屏幕适配方式；若一致，可取消勾选拆分



## <mark style="color:blue;">三、详细介绍:视频适配</mark>

因视频的尺寸是固定的，无法像图片一样通过拉伸去适配所有机型。因此在您使用视频制作时，可能会出现"视频在画面中占比过小影响试玩""视觉效果不美观"等问题，所以我们需要通过其他的方法来优化整体的排版与适配，以保证不同机型/横竖屏下的最佳视觉效果。

接下来，将为您详细介绍"竖版"/"方版"/"横版"这些不同尺寸视频的适配技巧，建议搭配[DEMO](https://tinyurl.com/45ddw6rv)食用效果更佳哦！

### <mark style="color:red;">1.竖版视频</mark>

#### 1）效果预览

| 竖屏iPhone                                                                                                                                                                                                                                   | 竖屏Android                                                                                                                                                                                                                                                                                                  | 竖屏iPad                                                                                                                                                                                                                                                             | 横屏iPhone                                                                                                                                                                                                                                       | 横屏Android                                                                                                                                                                                                              | 横屏iPad                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> |

#### 2）制作技巧 (参照DEMO场景1)

<mark style="background-color:yellow;">2-1）竖屏</mark>

* 导入竖版视频后，先将视频调整到合适的位置大小
* 建议宽度至少为750，铺满画布；高度调整到合适

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 在视频高度小于1800不足以覆盖到所有机型时，我们可在视频的上下两端添加图片进行填充，这样在大尺寸机型下预览时，可以利用这些填充图片来弥补画面的留白
* 建议尽量使用与视频画面一致的图片，来保证衔接处的自然

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 添加常驻内容，如产品信息、下载按钮等，并调整位置，进行编组
* 将产品信息组放在画面内留白较多的位置进行填补，如放在画面最下方，然后调整其屏幕适配方式
* 可视情况再添加指引文本

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:yellow;">2-2）横屏</mark>

完成竖屏的调整，我们还需切换至横屏模式进行微调（建议多使用"复制竖屏位置尺寸配置"功能）

* 在横屏状态下，可以看到视频的位置比较靠下，可以不需要下方的填充图片，所以我们选择将其"隐藏"
* 选中该填充图片，勾选右侧的"\[显示隐藏参数]横竖屏拆分"，然后隐藏即可

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 位于上方的填充图片，我们可以重新调整其位置大小，让图片的宽度和视频的宽度一致，然后将图片拖出画布外，贴紧画布上方
* 可以多多使用[参考线](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/zuo-pin-yu-lan-qu/can-kao-xian.md)，便于图层快速对齐

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;">2.方形视频</mark>

#### 1）效果预览

| 竖屏iPhone                                                                          | 竖屏Android                                                                         | 竖屏iPad                                                                            | 横屏iPhone                                                                          | 横屏Android                                                                         | 横屏iPad                                                                            |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1541).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1542).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1543).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1546).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1545).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1544).png" alt="" data-size="original"> |

#### 2）制作技巧 (参照DEMO场景2)

<mark style="background-color:yellow;">2-1）竖屏</mark>

* 同样，导入方形视频后，先将视频调整到合适的位置大小
* 建议宽度至少为750，铺满画布

<figure><img src="../../../.gitbook/assets/image (1553).png" alt=""><figcaption></figcaption></figure>

* 可以看出，此时的画布留白较多，看起来很空，所以需要我们添加一些内容来丰富画面
* 同样地，可以添加产品信息，并将其设置为贴底适配；然后在产品信息之上添加指引文本
* 还可以将视频内的部分元素分离出来，改在自由编辑器内单独制作。如本案例中的金额面板，可以单独添加在画面上方

<figure><img src="../../../.gitbook/assets/image (1554).png" alt=""><figcaption></figcaption></figure>

* 设置好"画布内"的内容，我们再导入图片对"画布外"也就是视频的左右两侧进行填充
* 调整图片的位置大小，让图片宽度和视频的宽度一致，然后将图片拖出画布外，贴紧画布的左右

<figure><img src="../../../.gitbook/assets/image (1555).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:yellow;">2-2）横屏</mark>

同样，完成竖屏的调整，我们还需切换至横屏模式进行微调（建议多使用"复制竖屏位置尺寸配置"功能）

* 由于金额面板比较长，不适用于横屏排版，所以我们在横屏下单独添加一张方形的面板图片
* 然后选中方形面板图片，勾选右侧的"\[显示隐藏参数]横竖屏拆分"，将竖屏下的状态设为"隐藏"；同样的方法，将矩形面板图片在横屏状态下设为"隐藏"
* 视排版情况，也可将下载按钮在横屏状态下设为"隐藏"

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1557).png" alt=""><figcaption></figcaption></figure>

</div>

* 然后仅需将左右两侧的填充图片分别移动到画布的上下方，贴紧画布即可
* 可以多多使用[参考线](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/zuo-pin-yu-lan-qu/can-kao-xian.md)，便于图层快速对齐

<figure><img src="../../../.gitbook/assets/image (1556).png" alt=""><figcaption></figcaption></figure>



### <mark style="color:red;">3.横版视频</mark>

#### 1）效果预览

| 竖屏iPhone                                                                          | 竖屏Android                                                                         | 竖屏iPad                                                                            | 横屏iPhone                                                                          | 横屏Android                                                                         | 横屏iPad                                                                            |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (1547).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1548).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1549).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1552).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1551).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1550).png" alt="" data-size="original"> |

#### 2）制作技巧 (参照DEMO场景3)

横版视频的适配方法和方形视频大体上是相同的

<mark style="background-color:yellow;">2-1）竖屏</mark>

* 导入横版视频后，先将视频调整到合适的位置大小
* 在本案例中，我们需要让核心视觉元素(老虎机)居中，所以视频的位置会比较靠左

<figure><img src="../../../.gitbook/assets/image (1558).png" alt=""><figcaption></figcaption></figure>

* 和方形视频的排版与适配相同，我们依次添加产品信息、指引文本、金额面板以及左右两侧的填充图片
* 将各资产调整到合适的位置大小，并合理排序、编组
* 若画布中的部分内容也需要遮挡，可将图片移入画布内

<figure><img src="../../../.gitbook/assets/image (1559).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:yellow;">2-2）横屏</mark>

同样，完成竖屏的调整，我们还需切换至横屏模式进行微调

* 由于视频本身是横版的，在横屏状态下，主要将视频调整到合适的位置大小就可以，尽量铺满画布
* 其他在竖屏状态下添加的内容可以视情况进行隐藏

<figure><img src="../../../.gitbook/assets/image (1561).png" alt=""><figcaption></figcaption></figure>

总之，在使用视频制作时，我们应尽量让画面的排版看起来协调、美观。当留白过多时，记得适当添加一些元素来丰富画面；当视频尺寸覆盖不到画布以外的区域时，也记得使用图片进行填充，以保证更佳的视觉效果！
