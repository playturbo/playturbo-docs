---
description: '#换肤编辑器 #自由编辑器'
---

# 通用埋点-分析思路

<mark style="background-color:orange;">**整体使用思路——【从宏观到微观】**</mark>

1. 先查看地区、渠道、系统等宏观维度的数据，了解各个维度的整体情况，方便定位不同渠道和地区中，不同的创意偏好；
2. 限定条件下（如相同地区、渠道等），对比查看不同素材的投放效果，识别优秀素材与待优化素材；
3. 根据不同的使用场景（A/B Test或素材诊断）对比目标素材的基础埋点情况，初步圈定存在问题的试玩环节；
4. 深入单条素材，查看数据异常体现在哪个试玩场景，或通过自定义埋点更精确地验证流失或跳转发生的节点，最终得出具体的优化迭代方案。



## 一、宏观投放数据

💡Playturbo事件分析看板中，可以通过趋势分析模块进行以下筛选，对比不同宏观维度的数据表现；

<table data-full-width="false"><thead><tr><th width="153.33333333333331">维度</th><th width="168">示例</th><th>使用思路建议</th></tr></thead><tbody><tr><td>广告网络</td><td>MTG/Unity</td><td><ul><li>对比不同广告渠道的素材投放效果；</li><li>定位不同渠道的创意偏好</li></ul></td></tr><tr><td>投放地区</td><td>CN/US/JP</td><td><ul><li>不同地区的素材整体投放效果有什么差异；</li><li>每个地区使用哪些创意效果最好；</li></ul></td></tr><tr><td>手机系统</td><td>IOS/Android</td><td><ul><li>IOS与Android系统的素材投放效果是否存在明显差异；</li></ul></td></tr><tr><td>广告类型</td><td>IV/RV</td><td><ul><li>RV和IV版位的展示逻辑不同，建议分开进行数据对比</li><li>IV和RV版位之间素材投放效果有什么差异；</li><li>如有指标存在整体较高/较低的情况，是否为某一版位的特性导致；</li></ul></td></tr><tr><td>项目名称/关联产品</td><td>-</td><td><ul><li>产品当前的投放状态如何，不同产品间数据是否有差异；</li><li>哪些项目整体投放效果优秀，以测出稳定出量的创意方向；哪些项目数据低于预期，存在提升空间；</li></ul></td></tr></tbody></table>

对于希望进一步了解数据表现的维度，建议参考下文思路推进跨素材和单条素材的分析；



## 二、素材基础埋点

💡通过对比不同素材的埋点表现，可以定位表现不佳的素材，初步判断哪个环节需要优化；

💡常用的埋点字段类型可以分为**转化指标**、**交互指标**、**流失指标**；

### STEP1：通过转化指标，了解素材是否正常跳转

<table data-full-width="true"><thead><tr><th width="183.33333333333331">常用指标</th><th width="195">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>跳转率</strong></td><td>=跳转数/试玩展示数</td><td><p><mark style="color:orange;">跳转率高，说明素材整体效果较好，用户有较高概率触发主动/被动的跳转；试玩的跳转机制数量足够、且已正常生效；进一步的优化重心可考虑放在提升交互率、安装率和其他深度指标上；</mark></p><p>跳转率低，可能为跳转引导不足或跳转机制没有正常生效；</p></td></tr><tr><td><strong>试玩时跳转率</strong></td><td>=试玩时跳转数/试玩展示数</td><td><p><mark style="color:orange;">左侧两个细分跳转率指标可用于确认跳转机制的生效情况，某一环节的跳转率高，说明该环节设置的跳转机制效果明显；</mark></p><p>如果某一环节有设置跳转机制，但对应环节跳转率低，需要排查跳转功能是否正常生效；</p></td></tr><tr><td><strong>试玩结束时跳转率</strong></td><td>=试玩结束时跳转数/试玩展示数</td><td></td></tr></tbody></table>

_技术逻辑拓展说明：_

1. _对于事件分析模块，所有转化指标都为请求数去重，不会重复统计；_
2. _所有转化指标都只计入首次，例如试玩中跳转后返回继续试玩，且游戏结束后再次跳转，仅会统计1次试玩中跳转；_
3. _上下文所有试玩展示数均为gamestart字段，代表试玩开始；_



### STEP2：通过交互指标，判断用户在关键节点的交互概况

<table data-full-width="true"><thead><tr><th width="159.33333333333331">常用指标</th><th width="223">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>首次交互率</strong></td><td>=首次交互数/试玩展示数</td><td><p><mark style="color:orange;">首次交互率高，代表进入试玩后的开场画面有吸引力，且游戏规则易上手，能够吸引用户进行首次的点击；</mark></p><p>首次交互率低，说明大量玩家在用户旅程的首个环节就已流失，应优先优化开场引导环节；</p></td></tr><tr><td><strong>试玩结束率</strong></td><td>=试玩结束数/试玩展示数</td><td><p><mark style="color:orange;">试玩结束率高或与首次互动率差异不大，说明开始试玩的用户都有较高的动力玩到底，试玩中途流失较少；因此素材的优化重心可以放在首次交互率和转化率上；</mark></p><p>试玩结束率低，可能是在试玩过程中用户失去目标或者动力，导致流失；建议从强化防停滞指引机制、提升整体创意趣味性、缩短试玩时长等方面优化；</p></td></tr><tr><td><strong>重新试玩率</strong></td><td>=重新试玩数/试玩展示数</td><td><p><mark style="color:orange;">重新试玩率高的素材，用户在失败时有较高概率点击重新试玩；</mark></p><ul><li><mark style="color:orange;">说明试玩有一定吸引力，能通过惯性或挑衅类创意套路激发玩家再次挑战的欲望；</mark></li><li><mark style="color:orange;">进阶建议：重新试玩率高的素材，迭代时可以考虑在重新挑战次数耗尽时对重新挑战按钮增加跳转事件，让玩家在惯性下前往转化；</mark></li></ul></td></tr><tr><td><strong>首次交互平均时长(TTE)</strong></td><td>=用户从素材展示到首次交互的平均时长（未触发首次交互的不计入）</td><td><p><mark style="color:orange;">TTE时间短，说明素材能在较短时间内引导用户触发首次交互；</mark></p><p>如果TTE时间较长，可能为客户交互动力不足、游戏理解成本高导致，建议对素材内容进行排查优化；</p></td></tr><tr><td><strong>试玩平均时长</strong></td><td>=用户从素材展示到试玩结束的平均时长（未触发试玩结束的不计入）</td><td><mark style="color:orange;">试玩平均时长可用于衡量试玩体量，可以通过对比和测试不同体量的素材投放效果，总结出最适合产品的试玩流程长度；</mark></td></tr><tr><td><strong>有效交互次数</strong></td><td><p>=用户触发游戏逻辑的交互行为数</p><p>（计入全部次数，不会在设备维度去重）</p></td><td><p><mark style="color:orange;">有效交互次数可用于模拟判断试玩操作的总步骤数和流程长度，从而辅助判断创意的投放效果；</mark></p><p>例如试玩结束率与跳转率低，但有效交互次数高，需要考虑是否流程过长或关卡数过多，用户难以抵达结束的跳转环节；</p></td></tr></tbody></table>

<mark style="color:green;">**转化指标参考值（待补充）**</mark>

<table data-full-width="true"><thead><tr><th width="156">广告类型</th><th width="101">RV</th><th>RV</th><th>RV</th><th>RV</th><th>RV</th><th>IV</th><th>IV</th><th>IV</th><th>IV</th><th>IV</th></tr></thead><tbody><tr><td><mark style="background-color:yellow;"><strong>垂类/参考值</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次互动率</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩结束率</strong></mark></td><td><mark style="background-color:yellow;"><strong>重新试玩率</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次交互平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次互动率</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩结束率</strong></mark></td><td><mark style="background-color:yellow;"><strong>重新试玩率</strong></mark></td><td><mark style="background-color:yellow;"><strong>首次交互平均时长</strong></mark></td><td><mark style="background-color:yellow;"><strong>试玩平均时长</strong></mark></td></tr><tr><td><strong>休闲</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>五垂</strong></td><td><mark style="color:orange;">93%</mark></td><td><mark style="color:orange;">35%</mark></td><td>待补充</td><td>待补充</td><td>待补充</td><td><mark style="color:orange;">89%</mark></td><td><mark style="color:orange;">28%</mark></td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>中重度</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr><tr><td><strong>非游应用</strong></td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td><td>待补充</td></tr></tbody></table>



### STEP3：通过流失指标，定位用户大量退出的试玩环节

<table data-full-width="true"><thead><tr><th width="173.33333333333331">常用指标</th><th width="247">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>试玩时流失率</strong></td><td>=试玩时流失数/试玩展示数</td><td><mark style="color:orange;">整体流失率低，说明用户有较高动力完成整个试玩，且多数用户都在页面停留到了游戏结束；优化时应侧重优化创意内容和结尾的诱导力度，增加跳转和安装概率；</mark></td></tr><tr><td><strong>试玩结束流失率</strong></td><td>=试玩结束流失数/试玩展示数</td><td>可用于与试玩时流失率对比，如果试玩时流失率明显高于试玩结束流失率，说明试玩中途流失情况更严重；</td></tr><tr><td><strong>交互前流失率</strong></td><td>=交互前流失数/试玩展示数</td><td><mark style="color:orange;">通过对比交互前后流失率，可以对流失情况进行归因；例如交互前流失率>交互后，说明素材开头吸引力有待提升；</mark></td></tr><tr><td><strong>交互后流失率</strong></td><td>=交互后流失数/试玩展示数</td><td><mark style="color:orange;">通过对比交互前后流失率，可以对流失情况进行归因；例如交互前流失率>交互后，说明素材开头吸引力有待提升；</mark></td></tr></tbody></table>

_技术逻辑拓展说明：_

1. _试玩时流失率的计算起点为首次点击；_
2. _只有试玩中途没触发跳转、且触发游戏结束（ge）请求的素材，才会计入试玩结束流失率；_

<mark style="color:green;">**流失指标参考值：待补充**</mark>



### 其他拓展指标

**关闭素材率**：关闭素材数/试玩展示数

关闭素材率如果接近试玩结束率，说明多数玩家在试玩中点击关闭按钮，并非正常完成；建议从强化防停滞指引机制、提升整体创意趣味性、缩短试玩时长等方面优化；



## 三、场景埋点与自定义埋点

💡**分析前提：**

1）明确分析目的为A/B Test还是素材诊断，选择合适的分析方式；

2）将目标素材的场景按照实际的逻辑顺序串联起来；

3）如需进行跨素材的对比，建议确保素材整体长度和制作方式类似，可比性更高；

<table data-full-width="true"><thead><tr><th width="212.33333333333331">指标</th><th width="206">定义</th><th>数据解读</th></tr></thead><tbody><tr><td><strong>场景N-到达数</strong></td><td>=用户到达该场景的次数</td><td>如果本场景对比上个场景到达数显著降低，说明多数用户在上个场景就停止了试玩，建议聚焦上个场景进行优化；</td></tr><tr><td><strong>场景N-跳转其他场景率</strong></td><td>=跳转其他场景数/场景N到达数</td><td><p><mark style="color:orange;">如果跳转其他场景率高，说明本场景用户试玩动力相对充足，多数用户完成了此场景；</mark></p><p>对于试玩最后一个场景，且试玩无重新挑战机制，该字段=0；</p></td></tr><tr><td><strong>场景N-停留平均时长</strong></td><td>=用户在该场景停留的平均时长（未跳转到其他场景的不计入）</td><td><mark style="color:orange;">停留平均时长长，说明本场景试玩耗时较久；如果该耗时不符合创意本身的设计，建议排查是否为试玩难度过高、程序BUG等因素导致；</mark></td></tr><tr><td><strong>场景N-跳转率</strong></td><td>=跳转数/场景N到达数</td><td><p>*如果场景本身没有设置跳转机制，可以忽略该指标；</p><p><mark style="color:orange;">跳转率高，说明该场景有效触发了跳转机制，抵达该场景的用户基本都触发了跳转；</mark></p><p>跳转率低，可能为跳转引导不足或跳转机制没有正常生效；</p></td></tr><tr><td><strong>场景N-首次交互率</strong></td><td>=首次交互数/场景N到达数</td><td><p><mark style="color:orange;">首次交互率高，代表场景有一定吸引力，用户进入场景后愿意进行首次互动；</mark></p><p>首次交互率低，说明大量玩家在看到该场景内容后就发生了流失，建议从流程趣味性、反馈强度、难易度等维度优化吸引力；</p></td></tr><tr><td><strong>场景N-试玩时流失率</strong></td><td>=试玩时流失数/场景N到达数</td><td><p><mark style="color:orange;">场景流失率低，说明用户有较高动力完成该场景的试玩内容；</mark></p><p>场景流失率高，说明用户在该阶段注意力和兴趣渐弱，导致流失，原因可能为流程乏味、反馈平淡、性能卡顿等；</p></td></tr><tr><td><strong>场景N-交互前流失率</strong></td><td>=交互前流失数/场景N到达数</td><td><mark style="color:orange;">通过对比一个场景交互前后流失率，可以对流失情况进行归因；例如交互前流失率&#x3C;交互后，可能为交互后的体验较差等原因导致，玩家缺乏继续试玩的动力，导致流失；</mark></td></tr><tr><td><strong>场景N-交互后流失率</strong></td><td>=交互后流失数/场景N到达数</td><td><mark style="color:orange;">通过对比一个场景交互前后流失率，可以对流失情况进行归因；例如交互前流失率&#x3C;交互后，可能为交互后的体验较差等原因导致，玩家缺乏继续试玩的动力，导致流失；</mark></td></tr></tbody></table>

_技术逻辑拓展说明：跳转其他场景数会计入重新挑战数，但不会计入跳转商店数_

<mark style="color:green;">**指标参考值：待补充**</mark>

（案例展示可查看[tong-yong-mai-dian-an-li-zhan-shi.md](tong-yong-mai-dian-an-li-zhan-shi.md "mention")）
