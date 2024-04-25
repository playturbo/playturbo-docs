# 用户旅程使用方式

<mark style="background-color:orange;">**整体使用思路——【**</mark><mark style="background-color:orange;">从整体到局部</mark><mark style="background-color:orange;">**】**</mark>

1. 首先，纵观核心试玩流程相关的所有Action，定位用户流失最严重的环节，结合实际的埋点内容和创意内容，排查造成流失的因素；
2. 通过开头环节相关的流失和跳转数据，可考察素材在吸睛度、引导效果、理解成本上是否符合预期；
3. 如果素材根据用户操作不同，会导向不同结局（如胜利vs失败），可以了解平行剧情分支之间到达率和跳转率的差异，洞察玩家的交互倾向和不同结局的诱导效果；



## <mark style="color:blue;">一、使用方式</mark>

### STEP1：配置自定义埋点与用户旅程 <a href="#lna3o" id="lna3o"></a>

可直接查阅[yong-hu-lv-cheng-fen-xi.md](../ye-mian-mo-kuai-jie-shao/ke-wan-su-cai-jiao-hu-fen-xi/yong-hu-lv-cheng-fen-xi.md "mention")



### STEP2：查询用户旅程数据 <a href="#bpzyc" id="bpzyc"></a>

查看用户旅程数据的步骤如下：

1）进入Playturbo-创意洞察-试玩素材交互分析-用户旅程分析；

2）搜索框内输入项目关键词（产品名、版本名等），找到对应项目；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1624).png" alt=""><figcaption></figcaption></figure>

</div>

3）选择有投放数据的日期范围后，旅程图将自动在下方展示；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1625).png" alt=""><figcaption></figcaption></figure>

</div>

4）点击右上角预览，可确认Action的位置和效果；

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1626).png" alt="" width="332"><figcaption></figcaption></figure>

</div>



### STEP3：分析用户旅程数据，定位优化空间 <a href="#dzkou" id="dzkou"></a>

💡进入用户旅程分析界面后，可以通过以下4个核心指标对素材进行诊断；

<table><thead><tr><th width="154">用户旅程指标</th><th width="231">定义</th><th>数据解读方式</th></tr></thead><tbody><tr><td><strong>到达数</strong></td><td>=触发了该action的用户总数；</td><td>到达数/到达率低，说明多数用户未抵达该节点，没有体验该action的内容；原因可能为没有选择该剧情分支、在前面步骤已流失、或前面步骤已跳转等；</td></tr><tr><td><strong>流转到下一节点数</strong></td><td>=触发该action后，还触发了其他action的用户数量；</td><td><p><mark style="color:orange;">流转到下一节点数高，代表多数用户没有在该步骤离开试玩，可能与该部分对用户吸引力高、理解成本低等因素相关；</mark></p><p>流转到下一节点数低，代表多数用户没有继续试玩；应当改为关注该action的流失数和跳转数指标，了解具体原因；</p></td></tr><tr><td><strong>流失数</strong></td><td>=触发该action后，没有触发其他action或触发跳转的用户数量；</td><td>流失数/流失率高，代表多数用户在该步骤停止交互，可能为试玩动力不足、无法理解试玩内容等原因导致；</td></tr><tr><td><strong>跳转数</strong></td><td><p>=触发该action后至下个action前，跳转商店的用户数量；</p><p>*跳转后的触发的其他事件不会计入旅程统计；</p></td><td><p><mark style="color:orange;">跳转数/跳转率高，说明该action后的跳转机制有正常生效，且多数用户成功跳转了商店；</mark></p><p>对于跳转操作相关的action，如果跳转数/跳转率低，可能为诱导机制理解成本过高、没有吸引力等原因，导致玩家没有做出触发跳转的操作；</p></td></tr></tbody></table>

💡不同Action与指标之间，关联的规则如下：

* Action N到达数 = \[所有可以抵达Action N的其他action]的\[流转到下一节点数]之和
* Action N到达数= Action N 流失数+ Action N 跳转数 + Action N 流转到下一节点数



## <mark style="color:blue;">二、分析案例</mark>

接下来，我们以【丧尸塔防】这条可玩素材为案例，进行用户旅程分析

### 1.案例预览

[点击预览](https://tinyurl.com/3utmxvw6)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1628).png" alt=""><figcaption></figcaption></figure>

</div>









