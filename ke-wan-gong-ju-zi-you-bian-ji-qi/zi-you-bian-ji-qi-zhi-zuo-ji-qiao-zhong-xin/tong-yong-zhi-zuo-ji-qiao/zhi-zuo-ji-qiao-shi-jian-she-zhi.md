---
description: '#自由编辑器'
---

# 制作技巧-事件设置

## 1. 全局变量-累计次数

### <mark style="background-color:orange;">1) 应用场景：</mark><mark style="color:red;">想实现“多次交互后，触发某种反馈”的效果</mark>

* 例子1：点击找到5个目标物品后，跳转应用商店
* 例子2：将3块拼图全部成功放置到正确位置后，出现彩带粒子特效
* 例子3：点击\[生成]按钮，每点一次就出现一个新角色
* ... ...

### <mark style="background-color:orange;">2) 案例预览</mark>

我们将以模板[【考眼力找物品】](http://tinyurl.com/5n82cjma)为例，进行简易版的制作，<mark style="color:red;">重点讲解如何通过【全局变量】实现此类玩法的逻辑制作</mark>。当您遇到需要制作“累计次数来实现xx效果”时，不妨试试此制作技巧噢!

[简易版](http://tinyurl.com/556k7nyx)玩法流程：

* 在画面中点击寻找猫咪
* 每找到一只猫咪，播放星星粒子反馈，已找到的文本数量+1
* 累计找到三只猫咪后，跳转结束页面

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

### <mark style="background-color:orange;">3) 操作步骤</mark>

#### <mark style="color:red;">**Step1：添加全局变量**</mark>

* 点击【全局变量】 - 【添加变量】
* 输入变量名称（如click times）
* 选择变量类型为【数值】
* 设置click times的初始值设为0
* 保存

<figure><img src="../../../.gitbook/assets/image (1338).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**Step2：添加条件判断**</mark>

* 在当前**场景**下点击【事件】
* 【添加事件】 - 选择【条件判断】
* 【添加条件】为：clicktimes=数值1，并勾选【只生效一次】

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1341).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

* 【添加响应事件】  - 【显示素材】text\_1 - 【隐藏素材】text\_0

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1342).png" alt=""><figcaption></figcaption></figure>

</div>

* 同理，继续添加2个条件判断：clicktimes=2、clicktimes=3
* 并依次添加响应事件：显示text\_2&隐藏text\_1、显示text\_3&隐藏text\_2
* <mark style="color:red;">**注意：**</mark>因为我们想实现“找到三只猫咪后进入结束页面”，所以需要在条件判断3（即当点击次数=3时）额外添加响应事件 - 跳转下一场景（执行延迟0.5s是预留的粒子播放时长）

<figure><img src="../../../.gitbook/assets/image (1345).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:red;">**Step3：赋值**</mark>

* 选中猫咪1图层【cat1】
* 【添加事件】 - 【按下】
* 【添加响应事件】 - 【赋值】，赋值：clicktimes+1（即按下一个猫咪点击次数就+1）

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1344).png" alt=""><figcaption></figcaption></figure>

</div>

* 继续添加响应事件 -  【显示素材】cat1 - 【隐藏素材】star1
* 添加完成后，我们点击【复制】按钮，复制该按下事件

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 然后依次粘贴到图层【cat2】和【cat3】，并更改对应生效的素材为cat2/star2、cat3/star3

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1347).png" alt=""><figcaption></figcaption></figure>

</div>

完成以上内容的设置，我们的素材就制作完成了。
