# 用户旅程使用建议

## <mark style="color:blue;">一、使用方式</mark>

### STEP1：配置自定义埋点与用户旅程 <a href="#lna3o" id="lna3o"></a>

具体内容可查阅[yong-hu-lv-cheng-fen-xi.md](../ye-mian-mo-kuai-jie-shao/ke-wan-su-cai-jiao-hu-fen-xi/yong-hu-lv-cheng-fen-xi.md "mention")



### STEP2：查询用户旅程数据 <a href="#bpzyc" id="bpzyc"></a>

* 进入Playturbo-创意洞察-试玩素材交互分析-用户旅程分析；
* 搜索框内输入项目关键词（产品名、版本名等），找到对应项目；
* 选择有投放数据的日期范围后，旅程图将自动在下方展示

具体内容可查阅[yong-hu-lv-cheng-fen-xi.md](../ye-mian-mo-kuai-jie-shao/ke-wan-su-cai-jiao-hu-fen-xi/yong-hu-lv-cheng-fen-xi.md "mention")



### STEP3：分析用户旅程数据，定位优化空间 <a href="#dzkou" id="dzkou"></a>

💡进入用户旅程分析界面后，可以通过以下4个核心指标对素材进行诊断：

<table><thead><tr><th width="154">用户旅程指标</th><th width="231">定义</th><th>数据解读方式</th></tr></thead><tbody><tr><td><strong>到达数</strong></td><td>=触发了该action的用户总数；</td><td>到达数/到达率低，说明多数用户未抵达该节点，没有体验该action的内容；原因可能为没有选择该剧情分支、在前面步骤已流失、或前面步骤已跳转等；</td></tr><tr><td><strong>流转到下一节点数</strong></td><td>=触发该action后，还触发了其他action的用户数量；</td><td><p><mark style="color:orange;">流转到下一节点数高，代表多数用户没有在该步骤离开试玩，可能与该部分对用户吸引力高、理解成本低等因素相关；</mark></p><p>流转到下一节点数低，代表多数用户没有继续试玩；应当改为关注该action的流失数和跳转数指标，了解具体原因；</p></td></tr><tr><td><strong>流失数</strong></td><td>=触发该action后，没有触发其他action或触发跳转的用户数量；</td><td>流失数/流失率高，代表多数用户在该步骤停止交互，可能为试玩动力不足、无法理解试玩内容等原因导致；</td></tr><tr><td><strong>跳转数</strong></td><td><p>=触发该action后至下个action前，跳转商店的用户数量；</p><p>*跳转后的触发的其他事件不会计入旅程统计；</p></td><td><p><mark style="color:orange;">跳转数/跳转率高，说明该action后的跳转机制有正常生效，且多数用户成功跳转了商店；</mark></p><p>对于跳转操作相关的action，如果跳转数/跳转率低，可能为诱导机制理解成本过高、没有吸引力等原因，导致玩家没有做出触发跳转的操作；</p></td></tr></tbody></table>

💡不同Action与指标之间，关联的规则如下：

* Action N到达数 = \[所有可以抵达Action N的其他action]的\[流转到下一节点数]之和
* Action N到达数= Action N 流失数+ Action N 跳转数 + Action N 流转到下一节点数



## <mark style="color:blue;">二、案例分析</mark>

接下来，我们以【丧尸塔防】这条可玩素材为案例，进行用户旅程分析

### 1.案例预览

| 手机试玩效果最佳                                                                                                                            | 竖屏                                                                                                                                                                         | 横屏                                                                                              |
| ----------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"> | <p></p><p><img src="../../../.gitbook/assets/image (1628).png" alt="" data-size="original"></p> |
| 扫码试玩                                                                                                                                | [点击试玩](https://tinyurl.com/5bfn8zfv)                                                                                                                                       | [点击试玩](https://tinyurl.com/5bfn8zfv)                                                            |



### 2.用户旅程图

在本案例的项目中，我们设置了以下自定义埋点：

Action1：首次拖拽武器；

Action2：首次成功放置武器；

Action3：第二次成功放置武器

Action4：游戏胜利；

Action5：胜利页点击CTA

Action6：敌人抵达我方基地；

Action7：游戏失败；

Action8：失败页点击重新挑战

由此，在配置用户旅程后，得到了如下用户旅程图：

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>当前案例的用户旅程图</p></figcaption></figure>



### 3.分析思路概括

从整体到局部：

1）整体：纵观核心试玩流程相关的所有Action——流失最严重的节点为Action2，流失率为30%

2）局部：

* 开头引导——Action1流转到下一节点数高，占比99.5%
* 中途互动——Action2流失数高，流失率为30%
* 不同结局——Action4(胜利结局)和Action6/7(失败结局)，到达数差异大；Action4→Action5(胜利结局)和Action7→Action8(失败结局)，跳转数有差异

接下来，我们具体展开分析



### 4.具体内容分析

#### <mark style="color:red;">1）Part1：Action1流转到下一节点数高</mark>

【相关指标】：流转到下一节点数

【优化维度】：开头引导

【数据含义】：1000个开始拖拽武器的用户，99.5%都成功放置了武器

<mark style="color:orange;">**【结论】：无须优化开头引导**</mark>

* 放置功能正常生效；
* 放置指引清晰，基本不存在用户误解操作方式的情况；
* 用户有欲望体验放置武器后的效果，极少有操作到一半时放弃或退出的情况；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="391"><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">2）Part2：Action2流失数高</mark>

【相关指标】：流失数

【优化维度】：中途互动

【数据含义】：

* 试玩过程中，流失最严重的节点为Action2，流失率为30%；
* 说明首次成功放置武器后，30%玩家没有继续交互；

<mark style="color:orange;">**【结论】：用户中途的试玩动力需要优化**</mark>

* 可能为操作步骤数过多、玩法理解成本高、内容趣味性低、操作反馈较弱等原因；
* 对于本案例，Action2不存在新增游戏规则、且Action2前操作仅有1步；因此推测流失率高的主要原因为两方面：
  * 1）内容存在重复性，导致新鲜感与趣味性下降；
  * 2）操作反馈弱，用户未获得预期的射击爽感，无动力继续体验；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">3）Part3：胜利和失败结局，到达数差异大</mark>

【相关指标】：到达数

【优化维度】：游戏难度

【数据含义】：

* 游戏很难胜利：300个第二次放置武器（Action3）后继续试玩的用户中，只有100个抵达胜利页面（Action4），300个进入濒临失败的状态（Action6）；
* 濒临失败但仍然继续互动的350个玩家，没有人成功挽回局面，350人全部进入了失败页（Action7）

<mark style="color:orange;">**【结论】：游戏难度过高，需考虑降低难度**</mark>

* 失败数远高于胜利数；
* 需要结合后续Action的数据判断，如果失败结局的跳转效果不如胜利结局，是否需要调低难度，让更多用户胜利；

_\*注：Action6到达数>300，因为Action3之外还有其他Action也可以流转到Action6；_

<div align="left">

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="color:red;">4）Part4：胜利和失败结局，跳转效果有差异</mark>

【相关指标】：流转到下一节点数、跳转数

【优化维度】：结束页诱导效果

【数据含义】：

* 抵达失败页的用户，约有43%（14.3%+28.6%）直接跳转、或以点击重新挑战按钮（CTA）的形式跳转；
* 抵达胜利页的用户，约有75%（50%+25%）直接跳转、或以点击CTA按钮的形式跳转；

<mark style="color:orange;">**【结论】：提高抵达胜利结局的概率、或者强化失败页的诱导力度，能提高试玩整体的跳转数据**</mark>

* 胜利结局对比失败结局，整体的诱导效果更好；

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>失败结局</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>胜利结局</p></figcaption></figure>



### 5.问题总结&优化策略

结合以上分析，我们可以得出如下结论：

#### <mark style="color:red;">**1）素材核心问题**</mark>

* 问题1：首次成功放置武器后，有较多用户试玩动力不足，导致流失；
* 问题2：游戏难度较高，失败数高于胜利数，且失败页诱导效果不佳；

#### <mark style="color:red;">2）</mark><mark style="color:red;">**优化策略**</mark>

<mark style="background-color:yellow;">**【问题1】**</mark>

* 当前3种武器外观和攻击方式比较雷同，可通过拉开武器差异或增加猎奇武器的方式，增添趣味性，提升用户尝试继续放置武器的动力；
* 当前杀敌反馈平淡，可强化射击特效或添加combo统计效果，提升操作爽感，让用户在成就感驱动下继续交互；

<mark style="background-color:yellow;">**【问题2】**</mark>

* 考虑胜利页跳转效果较好，可通过降低敌人HP和攻击力等方式，降低游戏难度，提升胜利概率；
* 同时，可以加强失败页的诱导力度，让失败的用户也有更高概率跳转商店，如设置挑衅文案
