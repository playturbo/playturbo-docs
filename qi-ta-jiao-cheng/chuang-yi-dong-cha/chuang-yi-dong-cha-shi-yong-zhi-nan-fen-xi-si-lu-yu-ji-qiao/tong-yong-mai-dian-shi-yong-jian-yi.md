# 通用埋点使用建议

## <mark style="color:blue;">一、宏观投放数据</mark>

💡Playturbo事件分析看板中，可以通过趋势分析模块进行以下筛选，对比不同宏观维度的数据表现；

<table data-full-width="false"><thead><tr><th width="153.33333333333331">维度</th><th width="168">示例</th><th>使用思路建议</th></tr></thead><tbody><tr><td>广告网络</td><td>Mintegral/Unity</td><td><ul><li>对比不同广告渠道的素材投放效果；</li><li>定位不同渠道的创意偏好</li></ul></td></tr><tr><td>投放地区</td><td>CN/US/JP</td><td><ul><li>不同地区的素材整体投放效果有什么差异；</li><li>每个地区使用哪些创意效果最好；</li></ul></td></tr><tr><td>手机系统</td><td>IOS/Android</td><td><ul><li>IOS与Android系统的素材投放效果是否存在明显差异；</li></ul></td></tr><tr><td>广告类型</td><td>IV/RV</td><td><ul><li>RV和IV版位的展示逻辑不同，建议分开进行数据对比</li><li>IV和RV版位之间素材投放效果有什么差异；</li><li>如有指标存在整体较高/较低的情况，是否为某一版位的特性导致；</li></ul></td></tr><tr><td>项目名称/关联产品</td><td>-</td><td><ul><li>产品当前的投放状态如何，不同产品间数据是否有差异；</li><li>哪些项目整体投放效果优秀，以测出稳定出量的创意方向；哪些项目数据低于预期，存在提升空间；</li></ul></td></tr></tbody></table>

对于希望进一步了解数据表现的维度，建议参考下文思路推进跨素材和单条素材的分析；



## <mark style="color:blue;">二、素材基础埋点</mark>

💡通过对比不同素材的埋点表现，可以定位表现不佳的素材，初步判断哪个环节需要优化；

💡常用的埋点字段类型可以分为**转化指标**、**交互指标**、**流失指标**；

### STEP1：通过转化指标，了解素材是否正常跳转

<table data-full-width="false"><thead><tr><th width="147.33333333333331">常用指标</th><th width="178">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>跳转率</strong></td><td>=跳转数/试玩展示数</td><td><p><mark style="color:orange;">跳转率高，说明素材整体效果较好，用户有较高概率触发主动/被动的跳转；试玩的跳转机制数量足够、且已正常生效；进一步的优化重心可考虑放在提升交互率、安装率和其他深度指标上；</mark></p><p>跳转率低，可能为跳转引导不足或跳转机制没有正常生效；</p></td></tr><tr><td><strong>试玩时跳转率</strong></td><td>=试玩时跳转数/试玩展示数</td><td><p><mark style="color:orange;">左侧两个细分跳转率指标可用于确认跳转机制的生效情况，某一环节的跳转率高，说明该环节设置的跳转机制效果明显；</mark></p><p>如果某一环节有设置跳转机制，但对应环节跳转率低，需要排查跳转功能是否正常生效；</p></td></tr><tr><td><strong>试玩结束时跳转率</strong></td><td>=试玩结束时跳转数/试玩展示数</td><td></td></tr></tbody></table>

_技术逻辑拓展说明：_

1. _对于事件分析模块，所有转化指标都为请求数去重，不会重复统计；_
2. _所有转化指标都只计入首次，例如试玩中跳转后返回继续试玩，且游戏结束后再次跳转，仅会统计1次试玩中跳转；_
3. _上下文所有试玩展示数均为gamestart字段，代表试玩开始；_



### STEP2：通过交互指标，判断用户在关键节点的交互概况

<table data-full-width="false"><thead><tr><th width="143.33333333333331">常用指标</th><th width="212">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>首次交互率</strong></td><td>=首次交互数/试玩展示数</td><td><p><mark style="color:orange;">首次交互率高，代表进入试玩后的开场画面有吸引力，且游戏规则易上手，能够吸引用户进行首次的点击；</mark></p><p>首次交互率低，说明大量玩家在用户旅程的首个环节就已流失，应优先优化开场引导环节；</p></td></tr><tr><td><strong>试玩结束率</strong></td><td>=试玩结束数/试玩展示数</td><td><p><mark style="color:orange;">试玩结束率高或与首次互动率差异不大，说明开始试玩的用户都有较高的动力玩到底，试玩中途流失较少；因此素材的优化重心可以放在首次交互率和转化率上；</mark></p><p>试玩结束率低，可能是在试玩过程中用户失去目标或者动力，导致流失；建议从强化防停滞指引机制、提升整体创意趣味性、缩短试玩时长等方面优化；</p></td></tr><tr><td><strong>重新试玩率</strong></td><td>=重新试玩数/试玩展示数</td><td><p><mark style="color:orange;">重新试玩率高的素材，用户在失败时有较高概率点击重新试玩；</mark></p><ul><li><mark style="color:orange;">说明试玩有一定吸引力，能通过惯性或挑衅类创意套路激发玩家再次挑战的欲望；</mark></li><li><mark style="color:orange;">进阶建议：重新试玩率高的素材，迭代时可以考虑在重新挑战次数耗尽时对重新挑战按钮增加跳转事件，让玩家在惯性下前往转化；</mark></li></ul></td></tr><tr><td><strong>首次交互平均时长(TTE)</strong></td><td>=用户从素材展示到首次交互的平均时长（未触发首次交互的不计入）</td><td><p><mark style="color:orange;">TTE时间短，说明素材能在较短时间内引导用户触发首次交互；</mark></p><p>如果TTE时间较长，可能为客户交互动力不足、游戏理解成本高导致，建议对素材内容进行排查优化；</p></td></tr><tr><td><strong>试玩平均时长</strong></td><td>=用户从素材展示到试玩结束的平均时长（未触发试玩结束的不计入）</td><td><mark style="color:orange;">试玩平均时长可用于衡量试玩体量，可以通过对比和测试不同体量的素材投放效果，总结出最适合产品的试玩流程长度；</mark></td></tr><tr><td><strong>有效交互次数</strong></td><td><p>=用户触发游戏逻辑的交互行为数</p><p>（计入全部次数，不会在设备维度去重）</p></td><td><p><mark style="color:orange;">有效交互次数可用于模拟判断试玩操作的总步骤数和流程长度，从而辅助判断创意的投放效果；</mark></p><p>例如试玩结束率与跳转率低，但有效交互次数高，需要考虑是否流程过长或关卡数过多，用户难以抵达结束的跳转环节；</p></td></tr></tbody></table>

<mark style="color:green;">**转化指标参考值（待补充）**</mark>

<table data-full-width="false"><thead><tr><th width="156">广告类型</th><th width="101">RV</th><th>RV</th><th>RV</th><th>RV</th><th>RV</th><th>IV</th><th>IV</th><th>IV</th><th>IV</th><th>IV</th></tr></thead><tbody><tr><td><mark style="background-color:yellow;"><strong>垂类/参考值</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次互动率</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩结束率</strong></mark></td><td><mark style="background-color:yellow;"><strong>重新试玩率</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次交互平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次互动率</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩结束率</strong></mark></td><td><mark style="background-color:yellow;"><strong>重新试玩率</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次交互平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩平均时长</strong></mark></td></tr><tr><td><strong>休闲</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>五垂</strong></td><td><mark style="color:orange;">93%</mark></td><td><mark style="color:orange;">35%</mark></td><td>待补充</td><td>待补充</td><td>待补充</td><td><mark style="color:orange;">89%</mark></td><td><mark style="color:orange;">28%</mark></td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>中重度</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>非游应用</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr></tbody></table>



### STEP3：通过流失指标，定位用户大量退出的试玩环节

<table data-full-width="false"><thead><tr><th width="161.33333333333331">常用指标</th><th width="226">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>试玩时流失率</strong></td><td>=试玩时流失数/试玩展示数</td><td><mark style="color:orange;">整体流失率低，说明用户有较高动力完成整个试玩，且多数用户都在页面停留到了游戏结束；优化时应侧重优化创意内容和结尾的诱导力度，增加跳转和安装概率；</mark></td></tr><tr><td><strong>试玩结束流失率</strong></td><td>=试玩结束流失数/试玩展示数</td><td>可用于与试玩时流失率对比，如果试玩时流失率明显高于试玩结束流失率，说明试玩中途流失情况更严重；</td></tr><tr><td><strong>交互前流失率</strong></td><td>=交互前流失数/试玩展示数</td><td><mark style="color:orange;">通过对比交互前后流失率，可以对流失情况进行归因；例如交互前流失率>交互后，说明素材开头吸引力有待提升；</mark></td></tr><tr><td><strong>交互后流失率</strong></td><td>=交互后流失数/试玩展示数</td><td><mark style="color:orange;">通过对比交互前后流失率，可以对流失情况进行归因；例如交互前流失率>交互后，说明素材开头吸引力有待提升；</mark></td></tr></tbody></table>

_技术逻辑拓展说明：_

1. _试玩时流失率的计算起点为首次点击；_
2. _只有试玩中途没触发跳转、且触发游戏结束（ge）请求的素材，才会计入试玩结束流失率；_

<mark style="color:green;">**流失指标参考值：待补充**</mark>



### 其他拓展指标

**关闭素材率**：关闭素材数/试玩展示数

关闭素材率如果接近试玩结束率，说明多数玩家在试玩中点击关闭按钮，并非正常完成；建议从强化防停滞指引机制、提升整体创意趣味性、缩短试玩时长等方面优化；



## <mark style="color:blue;">三、场景埋点与自定义埋点</mark>

💡**分析前提：**

1）明确分析目的为A/B Test还是素材诊断，选择合适的分析方式；

2）将目标素材的场景按照实际的逻辑顺序串联起来；

3）如需进行跨素材的对比，建议确保素材整体长度和制作方式类似，可比性更高；

<table data-full-width="false"><thead><tr><th width="186.33333333333331">指标</th><th width="191">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>场景N-到达数</strong></td><td>=用户到达该场景的次数</td><td>如果本场景对比上个场景到达数显著降低，说明多数用户在上个场景就停止了试玩，建议聚焦上个场景进行优化；</td></tr><tr><td><strong>场景N-跳转其他场景率</strong></td><td>=跳转其他场景数/场景N到达数</td><td><p><mark style="color:orange;">如果跳转其他场景率高，说明本场景用户试玩动力相对充足，多数用户完成了此场景；</mark></p><p>对于试玩最后一个场景，且试玩无重新挑战机制，该字段=0；</p></td></tr><tr><td><strong>场景N-停留平均时长</strong></td><td>=用户在该场景停留的平均时长（未跳转到其他场景的不计入）</td><td><mark style="color:orange;">停留平均时长长，说明本场景试玩耗时较久；如果该耗时不符合创意本身的设计，建议排查是否为试玩难度过高、程序BUG等因素导致；</mark></td></tr><tr><td><strong>场景N-跳转率</strong></td><td>=跳转数/场景N到达数</td><td><p>*如果场景本身没有设置跳转机制，可以忽略该指标；</p><p><mark style="color:orange;">跳转率高，说明该场景有效触发了跳转机制，抵达该场景的用户基本都触发了跳转；</mark></p><p>跳转率低，可能为跳转引导不足或跳转机制没有正常生效；</p></td></tr><tr><td><strong>场景N-首次交互率</strong></td><td>=首次交互数/场景N到达数</td><td><p><mark style="color:orange;">首次交互率高，代表场景有一定吸引力，用户进入场景后愿意进行首次互动；</mark></p><p>首次交互率低，说明大量玩家在看到该场景内容后就发生了流失，建议从流程趣味性、反馈强度、难易度等维度优化吸引力；</p></td></tr><tr><td><strong>场景N-试玩时流失率</strong></td><td>=试玩时流失数/场景N到达数</td><td><p><mark style="color:orange;">场景流失率低，说明用户有较高动力完成该场景的试玩内容；</mark></p><p>场景流失率高，说明用户在该阶段注意力和兴趣渐弱，导致流失，原因可能为流程乏味、反馈平淡、性能卡顿等；</p></td></tr><tr><td><strong>场景N-交互前流失率</strong></td><td>=交互前流失数/场景N到达数</td><td><mark style="color:orange;">通过对比一个场景交互前后流失率，可以对流失情况进行归因；例如交互前流失率&#x3C;交互后，可能为交互后的体验较差等原因导致，玩家缺乏继续试玩的动力，导致流失；</mark></td></tr><tr><td><strong>场景N-交互后流失率</strong></td><td>=交互后流失数/场景N到达数</td><td><mark style="color:orange;">通过对比一个场景交互前后流失率，可以对流失情况进行归因；例如交互前流失率&#x3C;交互后，可能为交互后的体验较差等原因导致，玩家缺乏继续试玩的动力，导致流失；</mark></td></tr></tbody></table>

_技术逻辑拓展说明：跳转其他场景数会计入重新挑战数，但不会计入跳转商店数_



## <mark style="color:blue;">四、案例分析</mark>

### 1.场景1：素材问题诊断

#### <mark style="color:orange;">**STEP1: 通过场景埋点，发现问题所属的试玩阶段**</mark>

💡锚定需要关注的素材和大致环节后，可以前往素材分析功能，剖析单条素材中埋点存在异常的具体位置；

1）对于埋点表现相对较差的场景（如出现到达率低、首次交互率低、流失率高），参考以上表格的解读思路定位具体问题；

2）针对定位到的流程、功能、效果问题，得出调整方向；

3）\*如有设置自定义埋点，可以推进STEP2的细化排查；

#### <mark style="color:orange;">**STEP2：通过自定义埋点，精确验证流失点，完善优化方案**</mark>

💡自定义埋点是素材制作方规定的、与试玩细节紧密挂钩的事件，字段格式为actionXX；自定义埋点的数据能比基础埋点对应到更精确的试玩节点；

**自定义埋点的查看思路：**

确定每个action代表的含义，可能包含部分线性和非线性的埋点；

* 线性：如存在固定的时序先后的埋点；将线性埋点按顺序排列时，可计算每个自定义环节的流失率、到达率；
* 非线性：如不与流程固定挂钩的独立按钮；非线性埋点可用于与相关联的线性埋点对比，计算失败率等、特定道具使用率等特殊指标；

<figure><img src="../../../.gitbook/assets/0 (153).png" alt=""><figcaption></figcaption></figure>



#### ✨<mark style="color:green;">**案例1：素材问题诊断**</mark>

[案例预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1852184/23/05/05/m\_en\_HairSalon\_ZQNcwp7zk\_ios\_ty/m\_en\_HairSalon\_ZQNcwp7zk\_ios\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)

![](<../../../.gitbook/assets/image (138).png>)   ![](<../../../.gitbook/assets/image (139).png>)

**1）素材基础埋点**

<table data-full-width="false"><thead><tr><th width="202.33333333333331">埋点字段</th><th width="122">数据</th><th>数据解读（橙色=重点结论）</th></tr></thead><tbody><tr><td>跳转率</td><td>40%</td><td>无明显异常，整体有优化空间</td></tr><tr><td>试玩时跳转率</td><td>0%</td><td>试玩中途没有跳转机制，考虑添加常驻下载按钮，增加整体跳转率</td></tr><tr><td>试玩结束时跳转率</td><td>40%</td><td>无明显异常，但整体有优化空间</td></tr><tr><td><mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">71%</mark></td><td><mark style="color:orange;">低于休闲垂类Playble首次互动率80%+的整体水准</mark></td></tr><tr><td>试玩结束率</td><td>52%</td><td>无明显异常，说明有五成左右用户试玩至结尾</td></tr><tr><td>重新试玩率</td><td>/</td><td>试玩没有重新试玩机制，不进行分析</td></tr><tr><td>首次交互平均时长</td><td>3s</td><td>表现优秀，用户可以快速理解玩法并进行互动</td></tr><tr><td><mark style="color:orange;">试玩平均时长</mark></td><td><mark style="color:orange;">26s</mark></td><td><mark style="color:orange;">试玩交互次数仅4次，但试玩平均时长接近半分钟，说明每个操作间存在大量等待（如看动画）；可以通过适当加速或剪短动画，降低等待时间的流失风险；</mark></td></tr><tr><td>有效交互次数</td><td>4</td><td>数值合理，试玩步骤数基本符合休闲换装游戏热门素材趋势</td></tr><tr><td><mark style="color:orange;">试玩时流失率</mark></td><td><mark style="color:orange;">38%</mark></td><td><mark style="color:orange;">试玩时比试玩结束时流失率更高，说明用户流失主要发生在游戏过程中，可能为理解成本过高、难度过高、等待时间过长等因素导致；</mark></td></tr><tr><td><mark style="color:orange;">试玩结束流失率</mark></td><td><mark style="color:orange;">22%</mark></td><td><mark style="color:orange;">试玩时比试玩结束时流失率更高，说明用户流失主要发生在游戏过程中，可能为理解成本过高、难度过高、等待时间过长等因素导致；</mark></td></tr><tr><td><mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">11%</mark></td><td><mark style="color:orange;">交互后流失率明显高于交互前，说明用户愿意进行首步交互，但交互后失去动力继续试玩，导致流失；</mark></td></tr><tr><td><mark style="color:orange;">交互后流失率</mark></td><td><mark style="color:orange;">49%</mark></td><td><mark style="color:orange;">交互后流失率明显高于交互前，说明用户愿意进行首步交互，但交互后失去动力继续试玩，导致流失；</mark></td></tr></tbody></table>

**2）分场景埋点**

<table data-full-width="false"><thead><tr><th width="203.33333333333331">埋点字段</th><th width="121">数据</th><th>数据解读（橙色=重点结论）</th></tr></thead><tbody><tr><td><mark style="color:orange;">场景1首次交互率</mark></td><td><mark style="color:orange;">60%</mark></td><td><p><mark style="color:orange;">场景1首次交互率明显低于场景2，说明用户对场景2更有兴趣，交互意愿更高；</mark></p><p><mark style="color:orange;">因此定位到：整体首次交互率低的问题主要源于场景一；</mark></p></td></tr><tr><td>场景1跳转其他场景率</td><td>60%</td><td>由于场景1仅有1步，所以跳转其他场景率与首次交互率相同</td></tr><tr><td>场景1跳转率</td><td>/</td><td>场景一没有跳转机制，不进行分析</td></tr><tr><td>场景1交互前流失率</td><td>20%</td><td>无明显异常，且交互前后流失率类似</td></tr><tr><td>场景1交互后流失率</td><td>18%</td><td></td></tr><tr><td><mark style="color:orange;">场景2首次交互率</mark></td><td><mark style="color:orange;">95%</mark></td><td><mark style="color:orange;">表现优秀，对比场景1提升明显，说明该场景有足够吸引力，进入场景的用户基本都会进行交互</mark></td></tr><tr><td>场景2跳转其他场景率</td><td>/</td><td>场景2为最后的场景，故没有跳转其他场景的机制，不进行分析</td></tr><tr><td>场景2跳转率</td><td>40%</td><td>无明显异常，但整体有优化空间</td></tr><tr><td><mark style="color:orange;">场景2交互前流失率</mark></td><td><mark style="color:orange;">19%</mark></td><td><p><mark style="color:orange;">场景2交互后流失率明显高于交互前；</mark></p><p><mark style="color:orange;">因此定位到：整体交互后流失的原因，主要为场景2试玩过程吸引力不足导致；</mark></p></td></tr><tr><td><mark style="color:orange;">场景2交互后流失率</mark></td><td><mark style="color:orange;">32%</mark></td><td><p><mark style="color:orange;">场景2交互后流失率明显高于交互前；</mark></p><p><mark style="color:orange;">因此定位到：整体交互后流失的原因，主要为场景2试玩过程吸引力不足导致；</mark></p></td></tr></tbody></table>

✨**结合以上数据，得出问题诊断结论：**

<mark style="color:orange;">**问题1：场景1吸引力不足，用户交互意愿较低；**</mark>

优化点1：省去开场的角色选择，直接从核心的装扮环节开始；或者调整场景1的创意和视觉效果，提升吸引力；

<mark style="color:orange;">**问题2：试玩时长较长，大量用户试玩中途流失，且流失集中于场景2用户交互之后；**</mark>

优化点2：通过加速或简化等方式减少动画等待时间，避免用户的操作连贯性被破坏；并且强化操作效果反馈，提升场景2装扮体验；





### 2.场景2：A/B Test

💡如果想了解多个素材版本的A/B Test效果，可以直接**聚焦变量相关的试玩环节，对比该环节的自定义埋点数据情况**；

#### <mark style="color:orange;">**STEP1:**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">对比不同版本的场景埋点，得出效果最佳场景组合</mark>

💡锚定需要关注的素材和大致环节后，可以前往素材分析功能，剖析单条素材中埋点存在异常的具体位置；

1）首先，根据A/B Test的目标挑选需要关注的**试玩场景**和**关键指标**；

_例如测试目标为“开头增加指引是否会让用户更愿意交互”，则需要重点关注场景一中的首次交互率与跳转其他场景率；（字段定义同上表）_

2）参考以上表格的解读思路，挑选每项关键指标**数据最优的版本**；

**3）整合每个最优版本对应素材环节的特征**，得出初步优化方向；

4）\*如有设置自定义埋点，可以推进STEP2的细化排查；

#### <mark style="color:orange;">**STEP2：**</mark><mark style="color:orange;">确认相关的自定义埋点数据，验证优化方向猜想</mark>

💡自定义埋点是素材制作方规定的、与试玩细节紧密挂钩的事件，字段格式为actionXX；自定义埋点的数据能比基础埋点对应到更精确的试玩节点；

**自定义埋点的查看思路：**

确定每个action代表的含义，可能包含部分线性和非线性的埋点；

* 线性：如存在固定的时序先后的埋点；将线性埋点按顺序排列时，可计算每个自定义环节的流失率、到达率；
* 非线性：如不与流程固定挂钩的独立按钮；非线性埋点可用于与相关联的线性埋点对比，计算失败率等、特定道具使用率等特殊指标；

<figure><img src="../../../.gitbook/assets/0 (153).png" alt=""><figcaption></figcaption></figure>



#### ✨<mark style="color:green;">**案例2：A/B Test**</mark>

**1）**[**案例A**预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1785028/23/01/31/m\_en\_230109\_K2inCg79z\_p\_an\_ty/m\_en\_230109\_K2inCg79z\_p\_an\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)   ![](<../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1).png>)

<table><thead><tr><th width="296">埋点字段</th><th>数据</th></tr></thead><tbody><tr><td>👍<mark style="color:orange;">跳转率</mark></td><td><mark style="color:orange;">61%</mark></td></tr><tr><td>试玩时跳转率</td><td>0%</td></tr><tr><td>试玩结束时跳转率</td><td>61%</td></tr><tr><td>👍<mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">88%</mark></td></tr><tr><td>试玩结束率</td><td>63%</td></tr><tr><td>重新试玩率</td><td>/</td></tr><tr><td><mark style="color:orange;">首次交互平均时长</mark></td><td><mark style="color:orange;">5s</mark></td></tr><tr><td>试玩平均时长</td><td>10s</td></tr><tr><td>有效交互次数</td><td>1</td></tr><tr><td>试玩时流失率</td><td>20%</td></tr><tr><td>试玩结束流失率</td><td>27%</td></tr><tr><td><mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">30%</mark></td></tr><tr><td>交互后流失率</td><td>17%</td></tr></tbody></table>

**2）**[**案例B**预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1775769/23/01/05/m\_en\_12\_Klfsce7t1\_p\_an\_ty/m\_en\_12\_Klfsce7t1\_p\_an\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)   ![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)

<table><thead><tr><th width="301">埋点字段</th><th>数据</th></tr></thead><tbody><tr><td><mark style="color:orange;">跳转率</mark></td><td><mark style="color:orange;">55%</mark></td></tr><tr><td>试玩时跳转率</td><td>0%</td></tr><tr><td>试玩结束时跳转率</td><td>55%</td></tr><tr><td><mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">69%</mark></td></tr><tr><td>试玩结束率</td><td>64%</td></tr><tr><td>重新试玩率</td><td>/</td></tr><tr><td><mark style="color:orange;">👍首次交互平均时长</mark></td><td><mark style="color:orange;">2.5s</mark></td></tr><tr><td>试玩平均时长</td><td>12s</td></tr><tr><td>有效交互次数</td><td>2</td></tr><tr><td>试玩时流失率</td><td>21%</td></tr><tr><td>试玩结束流失率</td><td>28%</td></tr><tr><td>👍<mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">21%</mark></td></tr><tr><td>交互后流失率</td><td>26%</td></tr></tbody></table>

#### **3）A/B Test 结论：**

**【背景】：**两条素材控制其他变量相同，主要测试不同开头引导方式的效果：

* 案例A跳过首步移动操作，自动播放动画，到第二步使用道具时才正式进行操作指引；
* 案例B的道具指引环节没有使用文案；

**【数据对比结论】：**

* 案例A跳转率更高，整体效果更好；
* 案例A首次交互率更高，说明开场使用简单动画，省去一步交互，直接从进入跑道时开始试玩效果更好；
* 然而，素材A中用户首次交互速度较慢、且交互前流失率较高，可能为指引理解成本较高、动画时间太久导致用户兴趣流失等原因导致；
* 案例均仅有1个场景，无需进行拆分场景的分析；



✨<mark style="color:orange;">**整合以上结论，可以得出整体的优化方向：**</mark>

1）开头可以添加一段动画，将玩家引入游戏氛围；动画长度不宜太长，可通过加速或剪辑控制在2s内，避免让用户兴趣流失或将素材错误理解为视频；

2）2步交互步骤效果比3步更好，可以在第二次交互时直接跳转商店；

3）操作指引需要清晰易懂，避免玩家因为不理解功能而延迟交互，提升流失概率；
