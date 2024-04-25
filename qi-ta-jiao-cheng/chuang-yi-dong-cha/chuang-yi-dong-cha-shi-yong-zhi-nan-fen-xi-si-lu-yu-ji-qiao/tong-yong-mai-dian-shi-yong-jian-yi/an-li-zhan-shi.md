# 案例展示

## <mark style="color:blue;">一、场景1：素材问题诊断</mark>

### <mark style="color:orange;">**STEP1: 通过场景埋点，发现问题所属的试玩阶段**</mark>

💡锚定需要关注的素材和大致环节后，可以前往素材分析功能，剖析单条素材中埋点存在异常的具体位置；

1. 对于埋点表现相对较差的场景（如出现到达率低、首次交互率低、流失率高），参考以上表格的解读思路定位具体问题；
2. 针对定位到的流程、功能、效果问题，得出调整方向；
3. \*如有设置自定义埋点，可以推进STEP2的细化排查；

### <mark style="color:orange;">**STEP2：通过自定义埋点，精确验证流失点，完善优化方案**</mark>

💡自定义埋点是素材制作方规定的、与试玩细节紧密挂钩的事件，字段格式为actionXX；自定义埋点的数据能比基础埋点对应到更精确的试玩节点；

**自定义埋点的查看思路：**

确定每个action代表的含义，可能包含部分线性和非线性的埋点；

* 线性：如存在固定的时序先后的埋点；将线性埋点按顺序排列时，可计算每个自定义环节的流失率、到达率；
* 非线性：如不与流程固定挂钩的独立按钮；非线性埋点可用于与相关联的线性埋点对比，计算失败率等、特定道具使用率等特殊指标；

<figure><img src="../../../../.gitbook/assets/0 (153).png" alt=""><figcaption></figcaption></figure>

### **案例1：素材问题诊断**

[案例预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1852184/23/05/05/m\_en\_HairSalon\_ZQNcwp7zk\_ios\_ty/m\_en\_HairSalon\_ZQNcwp7zk\_ios\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)

![](<../../../../.gitbook/assets/image (138).png>)   ![](<../../../../.gitbook/assets/image (139).png>)

**1）素材基础埋点**

<table data-full-width="false"><thead><tr><th width="202.33333333333331">埋点字段</th><th width="122">数据</th><th>数据解读（橙色=重点结论）</th></tr></thead><tbody><tr><td>跳转率</td><td>40%</td><td>无明显异常，整体有优化空间</td></tr><tr><td>试玩时跳转率</td><td>0%</td><td>试玩中途没有跳转机制，考虑添加常驻下载按钮，增加整体跳转率</td></tr><tr><td>试玩结束时跳转率</td><td>40%</td><td>无明显异常，但整体有优化空间</td></tr><tr><td><mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">71%</mark></td><td><mark style="color:orange;">低于休闲垂类Playble首次互动率80%+的整体水准</mark></td></tr><tr><td>试玩结束率</td><td>52%</td><td>无明显异常，说明有五成左右用户试玩至结尾</td></tr><tr><td>重新试玩率</td><td>/</td><td>试玩没有重新试玩机制，不进行分析</td></tr><tr><td>首次交互平均时长</td><td>3s</td><td>表现优秀，用户可以快速理解玩法并进行互动</td></tr><tr><td><mark style="color:orange;">试玩平均时长</mark></td><td><mark style="color:orange;">26s</mark></td><td><mark style="color:orange;">试玩交互次数仅4次，但试玩平均时长接近半分钟，说明每个操作间存在大量等待（如看动画）；可以通过适当加速或剪短动画，降低等待时间的流失风险；</mark></td></tr><tr><td>有效交互次数</td><td>4</td><td>数值合理，试玩步骤数基本符合休闲换装游戏热门素材趋势</td></tr><tr><td><mark style="color:orange;">试玩时流失率</mark></td><td><mark style="color:orange;">38%</mark></td><td><mark style="color:orange;">试玩时比试玩结束时流失率更高，说明用户流失主要发生在游戏过程中，可能为理解成本过高、难度过高、等待时间过长等因素导致；</mark></td></tr><tr><td><mark style="color:orange;">试玩结束流失率</mark></td><td><mark style="color:orange;">22%</mark></td><td><mark style="color:orange;">试玩时比试玩结束时流失率更高，说明用户流失主要发生在游戏过程中，可能为理解成本过高、难度过高、等待时间过长等因素导致；</mark></td></tr><tr><td><mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">11%</mark></td><td><mark style="color:orange;">交互后流失率明显高于交互前，说明用户愿意进行首步交互，但交互后失去动力继续试玩，导致流失；</mark></td></tr><tr><td><mark style="color:orange;">交互后流失率</mark></td><td><mark style="color:orange;">49%</mark></td><td><mark style="color:orange;">交互后流失率明显高于交互前，说明用户愿意进行首步交互，但交互后失去动力继续试玩，导致流失；</mark></td></tr></tbody></table>

**2）分场景埋点**

<table data-full-width="false"><thead><tr><th width="203.33333333333331">埋点字段</th><th width="121">数据</th><th>数据解读（橙色=重点结论）</th></tr></thead><tbody><tr><td><mark style="color:orange;">场景1首次交互率</mark></td><td><mark style="color:orange;">60%</mark></td><td><p><mark style="color:orange;">场景1首次交互率明显低于场景2，说明用户对场景2更有兴趣，交互意愿更高；</mark></p><p><mark style="color:orange;">因此定位到：整体首次交互率低的问题主要源于场景一；</mark></p></td></tr><tr><td>场景1跳转其他场景率</td><td>60%</td><td>由于场景1仅有1步，所以跳转其他场景率与首次交互率相同</td></tr><tr><td>场景1跳转率</td><td>/</td><td>场景一没有跳转机制，不进行分析</td></tr><tr><td>场景1交互前流失率</td><td>20%</td><td>无明显异常，且交互前后流失率类似</td></tr><tr><td>场景1交互后流失率</td><td>18%</td><td></td></tr><tr><td><mark style="color:orange;">场景2首次交互率</mark></td><td><mark style="color:orange;">95%</mark></td><td><mark style="color:orange;">表现优秀，对比场景1提升明显，说明该场景有足够吸引力，进入场景的用户基本都会进行交互</mark></td></tr><tr><td>场景2跳转其他场景率</td><td>/</td><td>场景2为最后的场景，故没有跳转其他场景的机制，不进行分析</td></tr><tr><td>场景2跳转率</td><td>40%</td><td>无明显异常，但整体有优化空间</td></tr><tr><td><mark style="color:orange;">场景2交互前流失率</mark></td><td><mark style="color:orange;">19%</mark></td><td><p><mark style="color:orange;">场景2交互后流失率明显高于交互前；</mark></p><p><mark style="color:orange;">因此定位到：整体交互后流失的原因，主要为场景2试玩过程吸引力不足导致；</mark></p></td></tr><tr><td><mark style="color:orange;">场景2交互后流失率</mark></td><td><mark style="color:orange;">32%</mark></td><td><p><mark style="color:orange;">场景2交互后流失率明显高于交互前；</mark></p><p><mark style="color:orange;">因此定位到：整体交互后流失的原因，主要为场景2试玩过程吸引力不足导致；</mark></p></td></tr></tbody></table>

<mark style="color:orange;">**结合以上数据，得出问题诊断结论：**</mark>

**问题1：场景1吸引力不足，用户交互意愿较低；**

优化点1：省去开场的角色选择，直接从核心的装扮环节开始；或者调整场景1的创意和视觉效果，提升吸引力；

**问题2：试玩时长较长，大量用户试玩中途流失，且流失集中于场景2用户交互之后；**

优化点2：通过加速或简化等方式减少动画等待时间，避免用户的操作连贯性被破坏；并且强化操作效果反馈，提升场景2装扮体验；





## <mark style="color:blue;">二、场景2：A/B Test</mark>

💡如果想了解多个素材版本的A/B Test效果，可以直接**聚焦变量相关的试玩环节，对比该环节的自定义埋点数据情况**；

### <mark style="color:orange;">**STEP1:**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">对比不同版本的场景埋点，得出效果最佳场景组合</mark>

💡锚定需要关注的素材和大致环节后，可以前往素材分析功能，剖析单条素材中埋点存在异常的具体位置；

1. 首先，根据A/B Test的目标挑选需要关注的**试玩场景**和**关键指标**；

_例如测试目标为“开头增加指引是否会让用户更愿意交互”，则需要重点关注场景一中的首次交互率与跳转其他场景率；（字段定义同上表）_

2. 参考以上表格的解读思路，挑选每项关键指标**数据最优的版本**；
3. **整合每个最优版本对应素材环节的特征**，得出初步优化方向；
4. \*如有设置自定义埋点，可以推进STEP2的细化排查；

### <mark style="color:orange;">**STEP2：**</mark><mark style="color:orange;">确认相关的自定义埋点数据，验证优化方向猜想</mark>

💡自定义埋点是素材制作方规定的、与试玩细节紧密挂钩的事件，字段格式为actionXX；自定义埋点的数据能比基础埋点对应到更精确的试玩节点；

**自定义埋点的查看思路：**

确定每个action代表的含义，可能包含部分线性和非线性的埋点；

* 线性：如存在固定的时序先后的埋点；将线性埋点按顺序排列时，可计算每个自定义环节的流失率、到达率；
* 非线性：如不与流程固定挂钩的独立按钮；非线性埋点可用于与相关联的线性埋点对比，计算失败率等、特定道具使用率等特殊指标；

<figure><img src="../../../../.gitbook/assets/0 (153).png" alt=""><figcaption></figcaption></figure>

### **案例2：A/B Test**

**1）**[**案例A**预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1785028/23/01/31/m\_en\_230109\_K2inCg79z\_p\_an\_ty/m\_en\_230109\_K2inCg79z\_p\_an\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

</div>

<table><thead><tr><th width="296">埋点字段</th><th>数据</th></tr></thead><tbody><tr><td>👍<mark style="color:orange;">跳转率</mark></td><td><mark style="color:orange;">61%</mark></td></tr><tr><td>试玩时跳转率</td><td>0%</td></tr><tr><td>试玩结束时跳转率</td><td>61%</td></tr><tr><td>👍<mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">88%</mark></td></tr><tr><td>试玩结束率</td><td>63%</td></tr><tr><td>重新试玩率</td><td>/</td></tr><tr><td><mark style="color:orange;">首次交互平均时长</mark></td><td><mark style="color:orange;">5s</mark></td></tr><tr><td>试玩平均时长</td><td>10s</td></tr><tr><td>有效交互次数</td><td>1</td></tr><tr><td>试玩时流失率</td><td>20%</td></tr><tr><td>试玩结束流失率</td><td>27%</td></tr><tr><td><mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">30%</mark></td></tr><tr><td>交互后流失率</td><td>17%</td></tr></tbody></table>

**2）**[**案例B**预览](http://playable-portal.mintegral.com/viewer/mindwork-view.html?language=en,zh-cn,ja\&mw\_test=0\&orientation=3\&preview=true\&url=https://mmp-cdn.rayjump.com/ps/dist/1775769/23/01/05/m\_en\_12\_Klfsce7t1\_p\_an\_ty/m\_en\_12\_Klfsce7t1\_p\_an\_ty.html?preview=true\&itavideo=2\&vconsole=0\&mw\_test=0)

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

</div>

<table><thead><tr><th width="301">埋点字段</th><th>数据</th></tr></thead><tbody><tr><td><mark style="color:orange;">跳转率</mark></td><td><mark style="color:orange;">55%</mark></td></tr><tr><td>试玩时跳转率</td><td>0%</td></tr><tr><td>试玩结束时跳转率</td><td>55%</td></tr><tr><td><mark style="color:orange;">首次交互率</mark></td><td><mark style="color:orange;">69%</mark></td></tr><tr><td>试玩结束率</td><td>64%</td></tr><tr><td>重新试玩率</td><td>/</td></tr><tr><td><mark style="color:orange;">👍首次交互平均时长</mark></td><td><mark style="color:orange;">2.5s</mark></td></tr><tr><td>试玩平均时长</td><td>12s</td></tr><tr><td>有效交互次数</td><td>2</td></tr><tr><td>试玩时流失率</td><td>21%</td></tr><tr><td>试玩结束流失率</td><td>28%</td></tr><tr><td>👍<mark style="color:orange;">交互前流失率</mark></td><td><mark style="color:orange;">21%</mark></td></tr><tr><td>交互后流失率</td><td>26%</td></tr></tbody></table>

#### **3）A/B Test 结论：**

**背景：**

两条素材控制其他变量相同，主要测试不同开头引导方式的效果：

* 案例A跳过首步移动操作，自动播放动画，到第二步使用道具时才正式进行操作指引；
* 案例B的道具指引环节没有使用文案；

**数据对比结论：**

* 案例A跳转率更高，整体效果更好；
* 案例A首次交互率更高，说明开场使用简单动画，省去一步交互，直接从进入跑道时开始试玩效果更好；
* 然而，素材A中用户首次交互速度较慢、且交互前流失率较高，可能为指引理解成本较高、动画时间太久导致用户兴趣流失等原因导致；
* 案例均仅有1个场景，无需进行拆分场景的分析；



<mark style="color:orange;">**整合以上结论，可以得出整体的优化方向：**</mark>

1）开头可以添加一段动画，将玩家引入游戏氛围；动画长度不宜太长，可通过加速或剪辑控制在2s内，避免让用户兴趣流失或将素材错误理解为视频；

2）2步交互步骤效果比3步更好，可以在第二次交互时直接跳转商店；

3）操作指引需要清晰易懂，避免玩家因为不理解功能而延迟交互，提升流失概率；
