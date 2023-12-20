---
description: '#自由编辑器 #空白制作 #全局变量 #进阶难度'
---

# 拉环玩法-制作教程

温馨提示：本案例以拉环玩法为例，讲解**“多种操作顺序，触发多种结果”**的全局变量制作方法，但实际也适用于同类操作逻辑的其他玩法哦！

## <mark style="color:blue;">一、特征标签</mark> <a href="#nubzy" id="nubzy"></a>

* 【制作难度】：⭐⭐⭐⭐
* 【适用产品】：普遍适用
* 【交互方式】：点击
* 【线程】：多线程
* 【核心资产】：序列帧
* 【功能】：全局变量；响应事件禁用事件



## <mark style="color:blue;">二、效果预览</mark> <a href="#dlwsv" id="dlwsv"></a>

| 手机试玩效果最佳                                                                       | 竖屏                                                                                 | 横屏                                                                                 |
| ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (5).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (1) (1).png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/image (2) (1).png" alt="" data-size="original"> |
| 扫码试玩                                                                           | [点击试玩](http://tinyurl.com/26ffjzyf)                                                | [点击试玩](http://tinyurl.com/26ffjzyf)                                                |



## <mark style="color:blue;">三、玩法梳理</mark> <a href="#nbhek" id="nbhek"></a>

**我们在开始制作之前需要将本案例的玩法逻辑进行简单的梳理：**

1）进入试玩，展示【拉环待机画面】和【奖励金额文本】

2）玩家按下任一拉环，播放相应【拉环反馈】

* 将拉环分别标记为a b c，玩家操作顺序可能性分6种，对应反馈如下
  * a - b - c （火-水-金币，操作正确）
  * a - c - b （火-金币-水+金币，操作错误）
  * b - a - c （拉不动）
  * b - c - a （拉不动）
  * c - a - b （金币-火-水+金币，操作错误）
  * c - b - a （金币- 拉不动）

3）当三根拉环全部被拉出，根据最终【奖励金额】跳转对应结束页面

* 当金额为100：跳转成功结束页面
* 当金额不变依旧为0：跳转失败结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

</div>



## <mark style="color:blue;">四、制作思路</mark> <a href="#agjmh" id="agjmh"></a>

**核心思想：**场景拆分逻辑清晰，图层结构简单，单个场景里的动画和事件尽可能少

**场景拆分：**根据第三部分的玩法梳理，我们可以合理地将本案例拆分为3个场景（重点讲解场景1拉环玩法的制作思路）

<table data-full-width="false"><thead><tr><th width="120">场景名称</th><th width="296">场景1-拉环玩法</th><th width="165">场景2-成功结束页面</th><th>场景3-失败结束页面</th></tr></thead><tbody><tr><td><strong>效果图</strong></td><td><img src="../../../.gitbook/assets/image (1) (1).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (4) (1).png" alt="" data-size="original"></td><td><img src="../../../.gitbook/assets/image (5) (1).png" alt="" data-size="original"></td></tr><tr><td><strong>场景描述</strong></td><td>多种操作顺序，触发多种结果</td><td>成功结束页面</td><td>失败结束页面</td></tr><tr><td><strong>核心资产</strong></td><td><p>静帧图片：背景图、拉环、石头</p><p>序列帧：</p><ul><li>火：下落*1</li><li>水：下落*1</li><li>金币：下落*3（①从头落到底、②从头落到中间、③从中间落到底）</li><li>金额：数字滚动*1</li></ul></td><td>-</td><td>-</td></tr><tr><td><strong>核心动画</strong></td><td><p>拉环：位移缓动+透明度缓动</p><p>石头：淡入</p></td><td>-</td><td>-</td></tr><tr><td><strong>核心事件</strong></td><td><p>全局变量：布尔值类型</p><p>触发对象：图层-拉环a/拉环b/拉环c</p><p>触发事件：按下+条件判断</p><p>响应事件：赋值/禁用事件/播放动画&#x26;序列帧</p></td><td>-</td><td>-</td></tr></tbody></table>



## <mark style="color:blue;">五、制作指南</mark> <a href="#cria2" id="cria2"></a>

\*重点讲解拉环玩法的【逻辑设置】

### Step1 - 场景搭建 <a href="#wepzn" id="wepzn"></a>

#### **1.全局设置**

1）在【全局设置】中添加背景音乐、背景图片

2）在【全局场景】下添加常驻下载按钮、logo等产品信息

#### **2.场景1-3**

1）分别在场景1、场景2、场景3内添加相应资产

2）调整各资产到合适的位置大小

3）根据资产类型对资产进行编组、排序、命名

4）调整横屏排版及屏幕适配方式

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>



### Step2 - 动效设置 <a href="#tpuup" id="tpuup"></a>

#### **1.**拉环a/b/c

依次为拉环a/b/c添加动画-通用-位移缓动+透明度缓动，模拟拉环被拉出后的路径。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### **2.石头**

为石头添加动画-进场动画-淡入。参数设置如下：

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

#### 3.**序列帧**

将水/火/金币/金额所有序列帧的参数调整为【关闭入场自动播放】【关闭无限循环】，并隐藏金币②和③的序列帧图层

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



### <mark style="background-color:blue;">Step3 - 逻辑设置</mark> <a href="#umduz" id="umduz"></a>

有关【全局变量】的功能介绍可查看 [quan-ju-bian-liang.md](../../../ke-wan-gong-ju-zi-you-bian-ji-qi/zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/quan-ju-bian-liang.md "mention")

#### **1.添加全局变量**

我们共添加3个全局变量，来分别代表拉环a/拉环b/拉环c

1）点击【全局变量】-【添加变量】

2）输入变量名称（如key\_a\_switch）-选择变量类型为【布尔值】-选择初始值为【false】-保存

3）按照以上步骤，再依次添加拉环b/拉环c的全局变量

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### **2.设置触发与响应事件**

上一步，我们将变量拉环a/b/c的初始值设为了【false】，在后续的事件设置中，我们会一直用到响应事件【赋值】，如赋值【按下拉环a】=【true】。

这一操作我们可以通俗理解为：【true】=按了拉环a；【false】=没按拉环a。由此通过【true/false】来判断某根拉环是否已被拉出。

<div align="left">

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:red;">**拉环a：**</mark>

根据三根拉环的摆放位置，我们可以看出，无论是哪种操作顺序，拉动拉环a的结果只有一种（即序列帧火落下），不受拉环b与拉环c的影响，因此拉环a的事件设置比较简单。

1）选中拉环a图层-添加事件-按下

2）添加响应事件-赋值，为【按下拉环a】赋值【true】

3）继续添加响应事件-禁用事件，选择禁用【拉环a的按下事件】，也就是当前触发事件

<mark style="color:red;">**注：**</mark><mark style="color:red;">【禁用事件】的设置我们可以通俗理解为：仅允许拉环a被拉动一次。即拉动一次以后该事件会被禁止使用，避免出现玩家无限次拉动拉环a&无限次播放相应反馈的情况。</mark>

4）继续添加响应事件-从头播放拉环a的全部动画（位移缓动+透明度缓动）-显示并播放序列帧火落下-隐藏操作指引

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>



<mark style="background-color:red;">**拉环b：**</mark>

拉环b受操作顺序的影响，我们需要为其添加【条件判断】，来判断在当前【条件判断】下是哪种操作顺序。

首先选中拉环b图层-添加事件-按下

<mark style="color:red;">**条件判断1**</mark>

1）添加条件判断【拉环a=true】、【拉环c=false】，即当拉环a已被按下，拉环c还没被按下，也就是当操作顺序为【a-b-c】时，按下拉环b时会触发什么反馈

注：拉环顺序【a-b-c】为正确操作顺序

<div align="left">

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>

2）同样，我们要添加响应事件-赋值，为【按下拉环b】赋值【true】；添加禁用事件，选择禁用【拉环b的按下事件】

3）继续添加响应事件-从头播放拉环b的全部动画（位移缓动+透明度缓动）-显示并播放序列帧水落下-隐藏操作指引

4）添加响应事件-执行延迟，设置0.6s（即序列帧水落下的时长）后从头播放石头的全部动画（淡入动画）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**条件判断2**</mark>

1）添加条件判断【拉环a=true】、【拉环c=true】，即当拉环a和拉环c都已被按下，也就是当操作顺序为【a-c-b】或【c-a-b】时，按下拉环b时会触发什么反馈

注：拉环顺序【a-c-b】【c-a-b】都为错误操作顺序

<div align="left">

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

</div>

2）同样，我们添加响应事件-赋值，为【按下拉环b】赋值【true】；添加禁用事件，选择禁用【拉环b的按下事件】

3）继续添加响应事件 - 从头播放拉环b的全部动画（位移缓动+透明度缓动）- 显示并播放序列帧水落下-显示并播放序列帧金币③ - 隐藏序列帧金币② - 隐藏操作指引

4）添加响应事件-执行延迟，设置0.6s（即序列帧水和金币②落下的时长）后从头播放石头的全部动画（淡入动画）- 隐藏序列帧金币③

5）添加响应事件-执行延迟，设置1s后跳转到指定场景3，即失败结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**条件判断3**</mark>

1）添加条件判断【拉环a=false】，即当拉环a没有被按下时，按下拉环b会触发什么反馈（不受拉环c影响）

2）添加响应事件 - 从头播放错误音效 - 播放震屏反馈\


<div align="left">

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

</div>



<mark style="background-color:red;">**拉环c：**</mark>

拉环c受操作顺序的影响，我们需要为其添加【条件判断】，来判断在当前【条件判断】下是哪种操作顺序。

首先选中拉环c图层-添加事件-按下

<mark style="color:red;">**条件判断1**</mark>

1）因拉环b只有在拉环a已被拉出后才可拉出，所以我们只需要添加一个条件判断【拉环b=true】，就意味着此种情况是拉环a和拉环b都已被按下。也就是当操作顺序为【a-b-c】时，按下拉环c会触发什么反馈

注：拉环顺序【a-b-c】为正确操作顺序

<div align="left">

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

</div>

2）同样，我们添加响应事件-赋值，为【按下拉环c】赋值【true】；添加禁用事件，选择禁用【拉环c的按下事件】

3）继续添加响应事件 - 从头播放拉环c的全部动画（位移缓动+透明度缓动）- 显示并播放序列帧金币① - 隐藏操作指引

4）添加响应事件-执行延迟，设置0.6s（即序列帧金币①落下的时长）后显示并播放序列帧奖励金额

5）添加响应事件-执行延迟，设置1s后跳转到指定场景2，即成功结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**条件判断2**</mark>

1）添加条件判断【拉环b=false】，即当拉环b没有被按下，操作顺序为【a-c-b】或【c-a-b】时，按下拉环c会触发什么反馈（实际不受拉环a影响）

注：拉环顺序【a-c-b】【c-a-b】都为错误操作顺序

<div align="left">

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

</div>

2）同样，添加响应事件-赋值，为【按下拉环c】赋值【true】；添加禁用事件，选择禁用【拉环c的按下事件】

3）继续添加响应事件 - 从头播放拉环c的全部动画（位移缓动+透明度缓动）- 显示并播放序列帧金币② - 隐藏序列帧金币① - 隐藏操作指引

<div align="left">

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

</div>



### Step4 - 整体预览 <a href="#j1kmp" id="j1kmp"></a>

1）全部制作完成后，建议将拉环操作顺序的6种可能性都一一试玩一遍，检查有无问题

2）还可对不同机型/不同语言/横竖屏进行整体预览

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>
