---
description: '#自由编辑器 #空白制作 #通用制作 #简单难度'
---

# 2D playable《三选一多场景》教程

本讲旨在讲解如何通过**自由编辑器**实现普通多场景的制作，同时将通过一个案例，教大家快速制作出“按钮三选一”玩法的可玩广告！

## 一、教学目的

* **多场景制作：**理解什么是“场景”，并学会通过<mark style="color:red;">**复制场景**</mark>功能来快速搭建新场景；
* **交互事件：**学会通过<mark style="color:red;">**“事件”**</mark>【包含触发事件（例如：按下）和一系列响应事件（例如：跳转应用商店）】来实现“场景和场景”之间的串联，从而形成一个完成的可玩素材；
* **场景模板（按钮选择）：**学会运用预设的<mark style="color:red;">**场景模板**</mark>快速完成按钮三选一的手指动画制作；



## 二、特征标签

* 【制作难度】：⭐⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【线程】：多线程
* 【功能】：复制场景、事件-按下、动画、场景模板



## 三、作品预览

<table><thead><tr><th>手机试玩效果最佳</th><th>竖屏</th><th>横屏</th><th data-hidden data-type="content-ref"></th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/image (858).png" alt=""></td><td><img src="../../../../.gitbook/assets/image (856).png" alt="" data-size="original"></td><td><img src="../../../../.gitbook/assets/image (859).png" alt="" data-size="original"></td><td><a href="https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fps%2Fpreview%2F1913727%2F23%2F08%2F02%2F64ca21629cbea%2Fgeneralscenes_0801.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn&#x26;mw_test=0&#x26;is_browser_tips=1&#x26;track_data=%7B%22pid%22%3A1913727%2C%22uid%22%3A109685%2C%22env%22%3A%22p%22%7D">https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fps%2Fpreview%2F1913727%2F23%2F08%2F02%2F64ca21629cbea%2Fgeneralscenes_0801.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn&#x26;mw_test=0&#x26;is_browser_tips=1&#x26;track_data=%7B%22pid%22%3A1913727%2C%22uid%22%3A109685%2C%22env%22%3A%22p%22%7D</a></td></tr><tr><td>扫码试玩</td><td><a href="https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fps%2Fpreview%2F1913727%2F23%2F08%2F02%2F64ca21629cbea%2Fgeneralscenes_0801.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn&#x26;mw_test=0&#x26;is_browser_tips=1&#x26;track_data=%7B%22pid%22%3A1913727%2C%22uid%22%3A109685%2C%22env%22%3A%22p%22%7D">点击试玩</a></td><td><a href="https://mmp-cdn.rayjump.com/mindworks-interactive-ads.html?url=https%3A%2F%2Fmmp-cdn.rayjump.com%2Fps%2Fpreview%2F1913727%2F23%2F08%2F02%2F64ca21629cbea%2Fgeneralscenes_0801.html%3Floading%3D1%26preview%3Dtrue%26lang%3Dzh-cn&#x26;mw_test=0&#x26;is_browser_tips=1&#x26;track_data=%7B%22pid%22%3A1913727%2C%22uid%22%3A109685%2C%22env%22%3A%22p%22%7D">点击试玩</a></td><td></td></tr></tbody></table>

##

## 四、玩法梳理

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

* 进入试玩，初始画面展示一个主要角色，主角色下方有三张不同角色的卡牌按钮。出现操作指引，引导玩家点击任意一个卡牌按钮来解锁新角色
  * 若玩家点击左侧卡牌按钮，则会弹出红色宝箱，解锁新角色A；
  * 若玩家点击中间卡牌按钮，则会弹出紫色宝箱，解锁新角色B；
  * 若玩家点击右侧卡牌按钮，则会弹出绿色宝箱，解锁新角色C；
* 无论玩家点击哪一张卡牌按钮，解锁出哪一个新角色，最终都会自动跳转到结束页面



## 五、制作思路

**核心思想：**让单个场景里的动画和事件尽可能少，场景拆分逻辑清晰，图层结构简单

**场景拆分：**根据第四部分的玩法梳理，我们可以将本案例拆分为以下5个场景

* 场景1：诱导选择（三选一）
* 场景2：选择结果展示
* 场景3：选择结果展示
* 场景4：选择结果展示
* 场景5：结束页面

<table><thead><tr><th width="117">场景名称</th><th width="203">场景1-诱导选择</th><th width="219">场景2/3/4-选择结果展示</th><th>场景5-结束页</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../../.gitbook/assets/3 (74).png" alt=""></td><td><img src="../../../../.gitbook/assets/4 (59).png" alt=""><img src="../../../../.gitbook/assets/5 (43).png" alt=""></td><td><img src="../../../../.gitbook/assets/6 (33).png" alt=""></td></tr><tr><td><strong>场景描述</strong></td><td>角色解锁场景，引导玩家点击任意一个卡牌按钮解锁新角色</td><td><p>玩家完成选择后，出现待开启的角色宝箱，引导玩家点击打开宝箱；</p><p>玩家点击后，出现新角色卡牌，然后跳转至结束页</p></td><td><p>展示产品内丰富的角色信息；</p><p>展示产品信息和CTA按钮</p></td></tr><tr><td><strong>动画</strong></td><td><p>【手指】：位移缓动+透明度缓动</p><p>【按钮外发光×3】：透明度缓动</p><p>【指引文案】：透明度缓动</p><p>【主角色】：缩放缓动</p></td><td><p>【散射光】：放大出现+旋转缓动</p><p>【宝箱】：放大出现+位移缓动+Q弹晃动+放大消失</p><p>【手指】：淡入+缩放缓动</p><p>【新角色卡牌】：放大出现+位移缓动</p></td><td><p>【角色】：位移缓动</p><p>【CTA按钮】：缩放缓动</p></td></tr><tr><td><strong>场景事件</strong></td><td><p>触发对象：按钮×3</p><p>触发操作：按下</p><p>响应事件：跳转指定场景2/3/4</p></td><td><p>触发对象：宝箱</p><p>触发操作：按下</p><p>响应事件：（详见第五部分Step3）</p></td><td><p>触发对象：CTA按钮</p><p>触发操作：按下</p><p>响应事件：跳转应用商店</p></td></tr><tr><td><strong>核心物料清单</strong></td><td><p>【图片】：主角色、卡牌按钮×3、按钮光晕×3（可选）、手指、logo、CTA按钮</p><p>【文本】：指引文案、下载文案</p><p>【背景音乐】【背景图片】</p></td><td><p>【图片】：宝箱×3、散射光、新角色卡牌×3、外发光序列帧、手指、logo、CTA按钮</p><p>【粒子】：爆炸、烟雾爆炸</p><p>【文本】：指引文案、下载文案</p><p>【音效】：礼花爆炸音效、闪光音效</p><p>【背景音乐】【背景图片】</p></td><td><p>【图片】：角色×3、CTA按钮×2、logo</p><p>【背景音乐】【背景图片】</p></td></tr></tbody></table>

###

## 六、制作指南

### Step1 - 基础场景搭建

| 图示                                            | 步骤                                                     |
| --------------------------------------------- | ------------------------------------------------------ |
| ![](<../../../../.gitbook/assets/7 (31).png>) | <p><strong>全局设置</strong></p><p>在【全局设置】中添加背景图片、背景音乐</p> |

### Step2 - 制作场景1（诱导选择）

**步骤概括：**运用预设的<mark style="color:red;">**场景模板**</mark>快速完成动画制作

<table><thead><tr><th width="248.33333333333331">图示</th><th width="304">步骤</th><th>事件设置</th></tr></thead><tbody><tr><td><p><img src="../../../../.gitbook/assets/8 (23).png" alt=""></p><p></p><p></p><p></p><p></p><p></p><p><img src="../../../../.gitbook/assets/9 (22).png" alt=""></p><p></p><p></p><p></p><p></p><p></p><p><img src="../../../../.gitbook/assets/10 (21).png" alt=""></p></td><td><p><strong>1.通过场景模板制作【操作指引】</strong></p><p>场景模板会预设好某些指定的效果和功能，其中包括图层、音频、动画、事件等，通过直接替换元素，即可快速完成制作。</p><p>1）添加场景模板：</p><p>在顶部资产库点击【场景模板】按钮，找到循环三选一模板并添加，自动生成新场景，以此作为场景1；</p><p><em>（Tips：可删除新建项目时默认出现的场景1）</em></p><p>2）替换卡牌按钮×3/手指样式</p><p>依次选中选项图层A/B/C和手指，在右侧参数设置区完成卡牌按钮和手指样式的替换；</p><p><em>（选做：因本案例选择不使用场景模板自带的按钮缩放缓动动画，因此需要删除原本的动画，重新制作外发光的透明度缓动动画）</em></p><p>3）调整指引文案的内容和位置</p><p>可直接将指引文案拖动到想要的位置，并在右侧参数设置区修改文本内容，调整样式；</p><p><em>Tips：如果想达到更完美、更个性化的效果，可自行添加外发光图片或指引文案背景图片</em></p></td><td><p><strong>图层事件1</strong></p><ul><li>选中卡牌按钮A1组</li><li>添加事件-按下；</li><li>添加响应事件-跳转指定场景 场景2</li></ul><p><strong>图层事件2</strong></p><ul><li>选中卡牌按钮B1组</li><li>添加事件-按下；</li><li>添加响应事件-跳转指定场景 场景3</li></ul><p><strong>图层事件3</strong></p><ul><li>选中卡牌按钮C1组</li><li>添加事件-按下；</li><li>添加响应事件-跳转指定场景 场景4</li></ul><p><strong>图层事件4</strong></p><ul><li>选中CTA按钮组</li><li>添加事件-按下；</li><li>添加响应事件-跳转应用商店</li></ul></td></tr><tr><td><img src="../../../../.gitbook/assets/11 (17).png" alt=""></td><td><p><strong>2.添加主角色图片</strong></p><p>1）导入主角色图片，调整图片位置大小至合适，并将图片拖动置于图层最底层；</p><p>2）选中主角色图层，将锚点修改为(50，100)，并添加缩放缓动动画，使人物看起来有呼吸感；</p></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/12 (16).png" alt=""></td><td><p><strong>3.添加产品信息+CTA按钮</strong></p><p>1）导入logo，调整位置大小至合适；</p><p>2）添加CTA按钮及文本，并打组</p></td><td></td></tr></tbody></table>

### Step3 - 制作场景2/3/4（选择结果展示）

**步骤概括：**先集中做其中一个选择结果，将这一个场景设置好后，再通过<mark style="color:red;">**复制场景**</mark>功能来快速搭建其余两个场景

_（说明：因点击卡牌按钮后，触发的反馈仅在“宝箱”和“新角色卡牌”的样式上有所区分，场景内其余内容都是相同的，因此我们采用“复制场景”功能来实现快速制作）_

<table><thead><tr><th>图示</th><th width="277.3333333333333">步骤（以场景2为例）</th><th>事件设置</th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/13 (16).png" alt=""></td><td><p><strong>1.复制图层</strong></p><p>1）直接将场景1内的“logo”、“CTA按钮”、“指引文案”、“手指”复制到场景2；</p><p>2）修改指引文案内容</p><p><em>（Tips：本场景内存在两条指引文案，因此在复制场景1内的指引文案组时，可再多复制一层，并修改文案内容）</em></p></td><td><p><strong>图层事件</strong></p><ul><li>选中宝箱组</li><li>添加事件-按下；</li><li>添加响应事件-隐藏操作指引1</li><li>添加响应事件-从头播放宝箱组的动画-从头播放闪光音效（即宝箱爆开时的动画与音效）</li><li>添加响应事件-执行延时，设置定时器时长为1s，继续添加响应事件-显示素材新角色卡牌组-显示操作指引2</li><li>添加响应事件-执行延时，设置定时器时长为2s，继续添加响应事件-跳转指定场景 场景5（结束页）</li></ul></td></tr><tr><td><p><img src="../../../../.gitbook/assets/14 (15).png" alt=""></p><p></p><p></p><p><img src="../../../../.gitbook/assets/15 (13).png" alt=""></p></td><td><p><strong>2.添加宝箱</strong></p><p>1）添加宝箱图片至画布内，调整位置大小至合适；</p><p>2）为宝箱图层添加“进场动画-放大出现”、“通用-位移缓动”动画，为宝箱赋予动态效果；</p><p>3）将宝箱打组，继续在组上添加“强调动画-Q弹晃动”、“退场动画-放大消失”动画，模拟点击后宝箱爆开的动态效果；</p><p><em>（注意：因为宝箱爆开是在玩家点击宝箱后才触发的，因此需要关闭宝箱爆开这两个动画的<strong>自动播放</strong>按钮）</em></p></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/16 (11).png" alt=""></td><td><p><strong>3.添加粒子动效</strong></p><p>1）在资产库-公共资产库中添加粒子动效“爆炸”、“烟雾爆炸”<em>（可视情况自行调整粒子参数）</em></p><p>2）添加散射光图片，调整位置大小至合适，并为散射光添加“进场动画-放大出现”、“通用-旋转缓动”动画</p><p>3）拖动三个动效图层置于宝箱图层之下</p></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/17 (10).png" alt=""></td><td><p><strong>4.添加手指动画</strong></p><p>为手指图层添加“进场动画-淡入”、“通用-缩放缓动”动画，模拟点击的效果</p></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/18 (9).png" alt=""></td><td><p><strong>5.添加新角色卡牌</strong></p><p>1）添加新角色卡牌与外发光序列帧动画，并打组，调整位置大小至合适；</p><p>2）为新角色卡牌组添加“进场动画-向上放大滑入”、“通用-位移缓动”动画，丰富画面效果</p><p><em>（Tips：在制作此步骤时，可暂时隐藏其余图层，方便操作）</em></p><p>3）调整完毕后，我们隐藏掉新角色卡牌组与第二组文案指引，通过事件设置，在玩家点击宝箱后再进行显示</p></td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/19 (9).png" alt=""></td><td><p><strong>6.复制场景</strong></p><p>1）场景2设置完成后，我们选中场景2右键选择【复制场景】，以此快速复制出场景3、场景4；</p><p>2）依次替换掉两个场景中的“宝箱”与“新角色卡牌”图层，我们的场景3与场景4就完成了</p></td><td></td></tr></tbody></table>

### Step4 - 制作场景5（结束页）

**步骤概括：**利用简单的<mark style="color:red;">**缩放缓动动画**</mark>，制作结束页CTA按钮交错呼吸的效果

<table><thead><tr><th>图示</th><th width="300.3333333333333">步骤</th><th>事件设置</th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/20 (9).png" alt=""></td><td><p><strong>1.添加多角色</strong></p><p>1）添加多个角色图片，并调整位置大小；</p><p>2）依次为角色添加“通用-位移缓动”动画，增加角色呼吸感</p><p><em>（Tips：为使画面看起来更自然，可分别设置三个角色的位移距离，使其往不同方向运动）</em></p></td><td><p><strong>图层事件</strong></p><ul><li>选中CTA按钮组</li><li>添加事件-按下；</li><li>添加响应事件-跳转应用商店</li></ul></td></tr><tr><td><p><img src="../../../../.gitbook/assets/21 (8).png" alt=""></p><p><img src="../../../../.gitbook/assets/22 (8).png" alt=""></p></td><td><p><strong>2.添加产品信息+CTA按钮</strong></p><p>1）添加logo，调整位置大小至合适；</p><p>2）添加两个同风格但不同颜色的CTA按钮及文本，并打组；</p><p>3）依次为两个按钮组添加“通用-缩放缓动”动画，通过曲线的不同，来实现按钮交错呼吸的效果</p></td><td></td></tr></tbody></table>

### Step5 - 整体预览

<table><thead><tr><th width="407">图示</th><th>步骤</th></tr></thead><tbody><tr><td><img src="../../../../.gitbook/assets/23 (7).png" alt=""></td><td><p><mark style="color:red;"><strong>补充说明-横屏排版</strong></mark></p><p>每个场景竖屏制作完成后，均需进行横屏排版（建议多使用“复用竖屏位置尺寸配置”按钮）</p></td></tr><tr><td><img src="../../../../.gitbook/assets/image (861).png" alt=""></td><td><p><mark style="color:red;"><strong>补充说明-屏幕适配</strong></mark></p><p>对各机型/横竖屏进行屏幕适配，并预览适配效果是否合适</p></td></tr><tr><td><img src="../../../../.gitbook/assets/image (862).png" alt=""></td><td><p><strong>整体预览</strong></p><p>全部制作完成后，可对不同机型/不同语言/横竖屏进行整体预览</p></td></tr></tbody></table>
