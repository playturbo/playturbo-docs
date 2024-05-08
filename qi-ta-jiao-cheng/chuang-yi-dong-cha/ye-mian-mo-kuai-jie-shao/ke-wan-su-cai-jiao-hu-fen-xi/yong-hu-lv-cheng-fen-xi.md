# 用户旅程分析

## <mark style="color:blue;">一、用户旅程分析简介</mark>

* 用户旅程由素材的自定义埋点(Action)串联而成，记录用户试玩时的关键交互行为
* 用户旅程分析**主要用于分析用户在试玩素材时的试玩深度、试玩路径及转化、流失情况**。例如，有多少用户试玩了素材的开头环节后，仍继续进行下一个环节的试玩，有多少发生了跳转商店，以及有多少流失，这些环节的数量都是多少。
* 使用Playturbo用户旅程分析功能，可以通过真实的交互行为数据，洞察用户的操作习惯、内容偏好、流失节点等信息，从而更精准地定位素材优化方向
* <mark style="color:red;">注意：定制项目和模板换肤项目，其自定义埋点和用户旅程已由Mindworks设置，无需您手动配置；若为自由编辑项目，请先在项目中添加自定义埋点</mark>[mai-dian-shuo-ming.md](../../chuang-yi-dong-cha-bi-xiu-ji-chu-zhi-shi/mai-dian-shuo-ming.md "mention")



## <mark style="color:blue;">二、用户旅程分析操作说明</mark>

使用用户旅程功能前，需要为素材设置自定义埋点，且串联为合理顺序（如下图），才可以获取到正确的用户旅程数据

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (1623).png" alt=""><figcaption></figcaption></figure>

</div>

### 1.选择素材

进行用户旅程分析前请先选择要分析的素材。选择素材有两种方式：

a. 在页面搜索框内输入项目关键词（产品名、版本名等），找到对应项目

b.在[「可玩素材分析」](../ke-wan-su-cai-fen-xi.md)页面，自定义列选择「素材名称」时，点击表格中的「分析」按钮，跳转到该页面

<figure><img src="../../../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

注：其中，**创意版本ID**用于标识创意的唯一性。创意展示层面相同的素材，共用一个创意版本ID。

如一个自由编辑项目，单次操作下载了Applovin、Facebook、Google，三个渠道的素材，虽然这些素材代码上稍有区别，但在创意呈现上是相同的，因此共用一个创意版本ID A；若在该项目中，替换/增加了视频/图片元件，修改了创意，再次导出，则创意版本ID则会改变为B。



### 2.配置用户旅程

#### 1）选择日期范围

选择项目后，在右侧筛选有投放数据的日期范围，然后旅程图将会自动展示在下方

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### **2）预览**

点击右上角预览，可查看该项目的埋点日志，确认Action的位置和效果

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt="" width="529"><figcaption></figcaption></figure>

</div>

#### **3）编辑**

* 点击【编辑】按钮，进入编辑模式，可对用户旅程进行调整

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (8) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* 【编辑方式】：从某个节点后拖拽拉出线条，连接到另一个节点

_例如素材共设置了4个埋点。埋点1:选择武器，埋点2:开始攻击，埋点3:击败敌人，埋点4:被敌人击败_

_用户在实际的试玩过程中可能出现的旅程分支为 ：1-2-3或1-2-4。您需要在旅程编辑模式中，连接1-2、2-3、3-4三条线_

* 编辑完成后，点击【展示旅程】，即可刷新保存调整后的用户旅程

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

</div>



### 3.旅程展示与数据筛选

#### 1）**数据筛选**

可以针对手机系统、广告类型、投放地区等不同维度进行筛选

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (9) (1) (1) (1).png" alt="" width="545"><figcaption></figcaption></figure>

</div>

#### 2）**数据展示**

对于每个自定义埋点(Action)，有4个数据指标：

* 到达数：触发了该action的用户总数；
* 流转到下一节点数：触发该action后，还触发了其他action的用户数量；
* 流失数：触发该action后，没有触发其他action或触发跳转的用户数量；
* 跳转数：触发该action后至下个action前，跳转商店的用户数量（\*跳转后的触发的其他事件不会计入旅程统计）

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="290"><figcaption></figcaption></figure>

</div>

对于action的每条连线，可以悬浮展示两个数据指标：

* 流转数：触发了前一个action后，再触发下一个action的用户数。_例如连线2-3的数量，即为触发了action2后，下一个事件为action3的用户数_
* 耗时：前一个action到下一个action的用户耗时。_如连线2-3的耗时为5s，则说明由action2到action3，用户消耗了5秒钟的时间_

<figure><img src="../../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **3）如何根据数据进行分析**

① 分析用户旅程的最大流量分支

* 分析该流量分支中的哪个环节流失率最高，并结合素材分析可能的流失原因并进行优化
* 分析该流量分支中的哪个环节跳转率最高

② 流失率结合耗时进行分析

如某个环节的流失率过高，可结合该环节的前后耗时，是否比预计的耗时长，若比预计耗时长，则可能存在玩法不明确、指引不清晰等问题，再进行针对性优化

③ 不同分支间的对比

可以对比不同分支的跳转率，若有某个分支的跳转率较高，可在素材制作上往该分支引导



✨具体分析思路及案例可查看[yong-hu-lv-cheng-shi-yong-jian-yi.md](../../chuang-yi-dong-cha-shi-yong-zhi-nan-fen-xi-si-lu-yu-ji-qiao/yong-hu-lv-cheng-shi-yong-jian-yi.md "mention")
