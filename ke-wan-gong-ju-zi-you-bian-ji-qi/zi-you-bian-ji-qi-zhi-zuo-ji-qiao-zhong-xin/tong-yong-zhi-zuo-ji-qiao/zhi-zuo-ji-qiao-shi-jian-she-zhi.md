---
description: '#自由编辑器'
---

# 制作技巧-事件设置

## <mark style="color:blue;">一、全局变量计算交互次数-不同图层</mark>

### <mark style="background-color:orange;">1.应用场景</mark>

**想实现“多次交互，每次点击/拖拽不同图层，触发相同或不同的xx反馈”的效果**

* 例子1：点击找到5个目标物品后，跳转应用商店
* 例子2：将3块拼图全部成功拖拽到正确位置后，出现"下一关"诱导按钮
* 例子3：每消除1组元素，进度条前进一段；完成3组消除后跳转下一场景
* ... ...

### <mark style="background-color:orange;">2.案例预览</mark>

我们将以模板【考眼力找物品】为例，进行简易版的制作，重点讲解如何通过【全局变量】实现此类玩法的制作。[简易版](http://tinyurl.com/556k7nyx)玩法流程：

* 在画面中点击寻找猫咪
* 每找到1只猫咪，播放一次星星粒子反馈，同时已找到的文本数量+1
* 累计找到三只猫咪后，跳转结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (11).png" alt=""><figcaption></figcaption></figure>

</div>

### <mark style="background-color:orange;">3.步骤详解</mark>

制作此类玩法共需3步：添加数值类型的变量、给每个元素赋值、添加条件判断计算交互次数

#### <mark style="color:red;">**Step1：添加全局变量**</mark>

* 点击【全局变量】 - 【添加变量】
* 输入变量名称（如click times）
* 选择变量类型为【数值】
* 设置click times的初始值为0（即初始画面玩家还未点击）
* 保存

<figure><img src="../../../.gitbook/assets/image (1338).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**Step2：赋值**</mark>

* 选中猫咪1图层【cat1】 - 【添加事件】 - 【按下】
* <mark style="color:red;">【添加响应事件】 - 【赋值】：赋值：clicktimes+1</mark>（即按下一个猫咪点击次数就+1）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1344).png" alt=""><figcaption></figcaption></figure>

</div>

* 继续添加响应事件 -  【显示素材】cat1 - 【隐藏素材】粒子star1
* 添加完成后，我们点击【复制】按钮，复制该按下事件

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 然后依次粘贴到图层【cat2】和【cat3】，并更改对应生效的素材为cat2/star2、cat3/star3

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1347).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">**Step3：添加条件判断**</mark>

* 在当前**场景**下点击【事件】 - 【添加事件】 - 选择【条件判断】 - 【+条件判断】
* <mark style="color:red;">添加条件判断1 为：clicktimes=数值1，并勾选【只生效一次】</mark>（即当交互次数=1时）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1341).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

* 【添加响应事件】  - 【显示素材】text\_1 - 【隐藏素材】text\_0

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1342).png" alt=""><figcaption></figcaption></figure>

</div>

* 同理，继续添加2个条件判断：clicktimes=2（即交互次数=2时）、clicktimes=3（即交互次数=3时）
* 并依次添加响应事件：显示text\_2&隐藏text\_1、显示text\_3&隐藏text\_2
* <mark style="color:red;">**注意：**</mark>因为我们想实现“找到三只猫咪后进入结束页面”，所以需要在条件判断3（即当点击次数=3时）额外添加响应事件 - 跳转下一场景（执行延迟0.5s是预留的粒子播放时长）

<figure><img src="../../../.gitbook/assets/image (1345).png" alt=""><figcaption></figcaption></figure>

到这里，事件设置就全部完成了。当您制作遇到需要**“计算不同图层的交互次数 以触发xx反馈”**时，不妨尝试套用此制作逻辑与方法哦!



## <mark style="color:blue;">二、全局变量计算交互次数-相同图层</mark>

### <mark style="background-color:orange;">1.应用场景</mark>

**想实现“多次交互，每次点击/拖拽相同图层，触发相同或不同的xx反馈”的效果**

* 例子1：第1次点击转盘，转盘停在位置A；第二次点击转盘，转盘从位置A开始停在位置B；...
* 例子2：点击"生成"按钮，每点1次就出现一个新角色
* 例子3：点击某物品，每次点击都出现相同的粒子特效或其他反馈
* ... ...

### <mark style="background-color:orange;">2.案例预览</mark>

[本案例](https://tinyurl.com/26cnjbb3) 流程梳理：

* 初始转盘停在红色位置；
* 玩家第一次按下，转盘转到紫色位置停止；
* 玩家第二次按下，转盘从紫色位置继续旋转，到青色位置停止

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2005).png" alt=""><figcaption></figcaption></figure>

</div>

### <mark style="background-color:orange;">3.步骤详解</mark>

制作此类玩法共需2步：添加数值类型的变量、给图层事件添加条件判断并赋值

#### <mark style="color:red;">**Step1：添加全局变量**</mark>

* 点击【全局变量】 - 【添加变量】
* 输入变量名称（如Tap）
* 选择变量类型为【数值】
* 设置初始值为0（即初始画面玩家还未点击）
* 保存

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt="" width="317"><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">**Step2：添加条件判断并赋值**</mark>

* 选中需要被点击的图层 - 【添加事件】 - 【按下】
* <mark style="color:red;">添加条件判断1 为：tap=0</mark>（即交互次数=0）
* <mark style="color:red;">添加响应事件【赋值】：赋值tap+1</mark>（即交互次数=1）
* 添加响应事件：播放转盘的旋转动画1、播放1次反馈音效等

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

* <mark style="color:red;">继续添加条件判断2 为：tap=1</mark>（即交互次数=1）
* <mark style="color:red;">添加响应事件【赋值】：赋值tap+1</mark>（即交互次数=2）
* 添加响应事件：播放转盘的旋转动画2、播放1次反馈音效等
* **同理，若还需玩家点击第3次、第4次...，可依次设置tap=2、tap=3...**

<div align="left">

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

_转盘的旋转动画参数如下_

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

到这里，事件设置就全部完成了。当您制作遇到需要**“计算相同图层的交互次数 以触发xx反馈”**时，不妨尝试套用此制作逻辑与方法哦!



## <mark style="color:blue;">三、倒计时设置</mark>

### <mark style="background-color:orange;">1.应用场景</mark>

**初始画面设有倒计时**

* **当玩家在设定时间内 无任何操作 或 未完成xx目标时，触发倒计时，进入结局A**
* **当玩家在设定时间内 正确交互或完成xx目标，取消倒计时，进入结局B**

### <mark style="background-color:orange;">2.案例预览</mark>

[本案例](https://tinyurl.com/8de4wcw2) 流程梳理：

* 进入试玩，展示核心玩法与倒计时；
  * 若玩家在10s内完成画线，跳转胜利页面；
  * 若玩家在10s内未完成画线，跳转产品信息页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

### <mark style="background-color:orange;">3.步骤详解</mark>

设置一个完整的倒计时共需2步：触发倒计时、取消倒计时

#### <mark style="color:red;">**Step1：触发倒计时**</mark>

1）添加倒计时资产后，将倒计时序列帧设为"播放间隔1000ms" "入场自动播放1次"

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2007).png" alt=""><figcaption></figcaption></figure>

</div>

2）在核心玩法场景下添加事件 - 定时触发

3）设置执行延迟N秒后，触发失败结果（如10s后跳转场景3）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2006).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="color:red;">**Step2：取消倒计时**</mark>

**在正确交互的事件下 补充响应事件：取消执行延迟**，选择上一步所设置的定时器ID即可（如图，画线完成后跳转场景2，并取消定时器timer\_1）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2008).png" alt=""><figcaption></figcaption></figure>

</div>

_Tips：【预设库】内有多个倒计时预设可供使用哦！_ [yu-she-ku.md](../../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/yu-she-ku.md "mention")

<div align="left">

<figure><img src="../../../.gitbook/assets/image (7) (1) (1).png" alt="" width="330"><figcaption></figcaption></figure>

</div>
