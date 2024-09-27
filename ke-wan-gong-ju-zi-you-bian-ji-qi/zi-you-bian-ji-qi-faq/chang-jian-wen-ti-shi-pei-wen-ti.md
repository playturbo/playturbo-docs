---
description: '#自由编辑器'
---

# 常见问题-适配问题

## <mark style="color:blue;">1.怎么调整其他机型的素材</mark>

### **Q1：制作素材时，画布大小默认是以iPhone6屏幕大小展示的，那其他机型的画面怎么调整？** <a href="#q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k" id="q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k"></a>

**A：**首先，是<mark style="color:red;">不需要区分机型单独调整</mark>的，因为素材在不同机型上会等比放大，自动适配所有机型。然后绝大部分的资产也都不需要调整，因资产默认居中适配，在iPhone6屏幕下调整好的素材，放在其他机型上也都能完整展示。少部分资产需要单独调整屏幕适配方式（如产品信息/免责声明等），即可完美适配所有机型

相关阅读： [ping-mu-shi-pei-fang-shi.md](../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/ping-mu-shi-pei-fang-shi.md "mention")&#x20;



## <mark style="color:blue;">2.预览时资产没有全屏显示</mark>

### **Q1：在预览素材时发现部分机型会出现资产无法全屏显示的问题，或四周有白边？** <a href="#q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k" id="q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k"></a>

**A：**出现此类问题，是因为您在制作过程中没有做好屏幕适配，可从以下几方面排查：

* 检查资产原始尺寸：在默认居中适配的情况下，资产原始尺寸至少设为1800\*1800，才可以全屏覆盖所有机型（需注意：因视频尺寸的比例是固定的，所以无法铺满所有屏幕，需要您手动调节视频的位置大小到合适）
* 检查屏幕适配方式：看资产是否设置了非居中适配。若您需要让底图贴一侧适配，则图片尺寸还要再调大一些

（以上需注意：参数默认横竖屏拆分，竖屏调整完还需调整横屏）

* 设置背景图片：在【全局设置】下添加的背景图片，是会自动拉伸铺满屏幕的，可以适配所有机型。因此，我们建议您在制作每一个项目时都先添加一张背景图片进行兜底



### **Q2：预览iPhoneX和vivo机型上下有黑边？** <a href="#q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k" id="q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k"></a>

**A：**因iPhoneX和vivo这两款机型上方有刘海屏，为避免素材被刘海屏遮挡，会露出一定的黑边，无法避免哦



## <mark style="color:blue;">3.当图层有动画且要单独设置屏幕适配方式</mark>

### **Q1：如给产品信息组设置了入场的位移动画，希望实现"在玩家进入结束页面后，产品信息从屏幕外进入画内"的效果，同时给组设置了贴底适配。但实际预览时，发现在不同机型上，产品信息组最终固定的位置不一样？不全是贴底的** <a href="#q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k" id="q1-zai-shi-yong-mou-mu-ban-jin-xing-zi-you-zhi-zuo-shi-xiang-tiao-zheng-mou-ge-tu-ceng-de-dong-hua-k"></a>

**A：**因给产品信息组加了位移动画，其中的位移距离是绝对值，不会随着机型的大小而改变数值，所以在不同机型下预览会有位置上的偏移，没有全部实现贴底的效果。

**调整方法：**给产品信息组再套一个组，并把这个大组移动到画布贴底的位置，然后设置大组的"屏幕适配方式"为底部适配即可（因为大组的层级比组内图层要高，这样产品信息组的位移动画会照常播放，但最终停止的位置是以大组的位置为准的）
