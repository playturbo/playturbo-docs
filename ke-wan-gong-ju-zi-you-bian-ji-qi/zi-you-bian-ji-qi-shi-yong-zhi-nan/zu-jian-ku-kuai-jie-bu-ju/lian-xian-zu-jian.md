---
description: '#自由编辑器 #模板自由制作 #空白制作'
---

# 连线组件

✨模板自由制作入口：作品预览区>>>连线组件按钮 或 图层区>>>Match Line Component

<figure><img src="../../../.gitbook/assets/image (1890) (1).png" alt=""><figcaption></figcaption></figure>

✨空白制作入口：玩法模板>>>组件库>>>连线组件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (26) (1) (1).png" alt="" width="416"><figcaption></figcaption></figure>

</div>

相关案例教学可查阅 [lian-xian-zu-jian-kong-bai-zhi-zuo-jiao-cheng.md](../../../playturbo-an-li-jiao-xue-ji-di/ke-wan-zi-you-bian-ji-qi-an-li/hua-xian-wan-fa-an-li/lian-xian-zu-jian-kong-bai-zhi-zuo-jiao-cheng.md "mention")



## <mark style="color:blue;">一、连线组件通俗介绍</mark>

* 适用于如连线配对、连连看等**有固定可连线区域**或**固定配对组合**的玩法
* 当前，<mark style="color:red;">【模板自由制作】和【空白制作】都支持使用"连线组件"</mark>。使用【模板自由制作】，您可以基于原模板的玩法对组件进行调整；使用【空白制作】，可以从零开始制作连线玩法的素材
* 基于现有的「连线组件」，您可调整模板的可画线范围、画线的起止区域及样式、配对关系、连线类型等内容
* <mark style="color:red;">注意：同个场景仅支持添加一个组件，但可跨场景添加组件或复制组件</mark>



## <mark style="color:blue;">二、连线组件使用说明</mark>

「连线组件」可调整的参数分3部分：「外观」、「起止区域」、「事件」

我们将结合模板[【画线回家】](http://tinyurl.com/5vsrhwjn)进行「连线组件」的使用说明

### 1.外观

* \[显示隐藏参数]横竖屏拆分：和各图层的外观参数相同，可分别调整该连线组件在横/竖屏下是否显示
* 位置尺寸：可以修改该连线组件的宽高、位置。其宽高位置，决定了能够画出线的范围（如下图，绿色覆盖范围即是在试玩过程中可画出线的范围）
* 屏幕适配方式：和各图层的外观参数相同，可调整该连线组件的屏幕适配方式
* 缩放比例：和各图层的外观参数相同，可调整该连线组件的比例

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (26).png" alt=""><figcaption></figcaption></figure>



### 2.起止区域

「起止区域」是连线组件独有的参数，一个连线组件有若干个起止区域和配对关系

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (5).png" alt=""><figcaption></figcaption></figure>

#### **1）起止区域**

在该组件中设置若干个任意大小和位置的区域，该区域会和「配对关系」搭配使用，以产生具体的画线效果

在【画线回家】模板中，共有4个起止区域：

* 支持修改已有「起止区域」的线条样式：包含颜色及线条粗细
* 支持将某一起止区域的线条样式应用到当前全部起止区域
* 支持添加新的起止区域
* 对于每个起止区域，可在画布中调整其大小和位置
* 支持删除某一起止区域（但不建议这么操作，可能会导致素材无法正常试玩）
* <mark style="color:red;">注意：起止区域的线条样式，代表的是从该区域画出的线条的样式</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### **2）配对关系**

<mark style="color:red;">配对关系决定了某个区域是否能画出线：添加了配对关系的才可以画出线，未添加配对关系的即使有起止区域也画不出线</mark>

在【画线回家】模板中，共有4组配对关系：

* 每组配对关系需设置「开始区域」和「结束区域」，以及「配对类别」
  * 「开始区域」只能选择一个，「结束区域」支持单选或多选
  * 「配对类别」分为true和false两种类别（空白制作支持自定义创建，后面详细说明）
* 支持修改每组配对关系的名称
* 支持删除配对关系（但不建议这么操作，可能会导致素材无法正常试玩）
* 支持预览已完成配对关系的所有连线线条
* <mark style="color:red;">注意：已完成连线的起始区域无法再画线</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (3).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">共有4组配对关系：1->3、2->4、1->4、2->3</mark>

<mark style="background-color:yellow;">其中1->3、2->4被设置为「True」配对；1->4、2->3被设置为「False」配对</mark>

<mark style="background-color:yellow;">通过以上配对关系，素材可以从区域1、2拖拽画出线，若最终手指松开的位置在区域3、4内，则画线被保留，并触发相应的事件，否则画线不保留</mark>

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (25).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">**注意：**</mark><mark style="color:red;">【空白制作】使用连线组件时，【配对类别】需自行添加。可根据实际制作情况添加多种配对类别。</mark>

点击图示设置按钮，调起【配对类别】弹窗，点击【添加配对类别】，输入名称即设置完成。成功添加后，可选择配对类别

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2004).png" alt=""><figcaption></figcaption></figure>

</div>



#### **3）连线配对**

影响配对关系

* 若选择「单向」，仅能从每个配对的前一个区域开始画线，后一个区域无法画出线。<mark style="background-color:yellow;">以模板【画线回家】的第一组配对关系为例，只能由区域1开始画线，到区域3结束，是无法从区域3开始画线的</mark>
* 若选择「双向」，则能从每组配对关系的任一区域开始画线。<mark style="background-color:yellow;">以模板【画线回家】的第一组配对关系为例，可从区域1开始画线到区域3，也可从区域3开始画线到区域1，两种都能成功完成画线</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### **4）连线类型**

决定画出的线条类型

* 自由绘制：简单来说，自由绘制就是跟随手指的画线轨迹所出现的曲线
* 直线：不受手指在画线过程中的轨迹影响，最终只形成直线

<div align="left">

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (4).png" alt=""><figcaption></figcaption></figure>

</div>



### 3.事件

「连线组件」包含两种**触发事件**：「开始画线」、「画线完成」

和「连线组件」相关的**响应事件**包含：「抹除连线线条」、「修改连线线条样式」、「启用/禁用配对关系」、「修改已连线配对的线条样式」、「启用/禁用起止区域」

<div align="left">

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (6).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:orange;">1-1）</mark><mark style="background-color:orange;">**触发事件：开始画线**</mark>

需要选择开始画线的区域（支持单选或多选）并设置响应事件

**触发时机为：**<mark style="color:red;">**从已选择的「起止区域」开始画线时**</mark>

<mark style="background-color:yellow;">以模板【画线回家】为例，起止区域选择1和2，响应事件选择从头播放音效。则实现的效果是：当玩家从区域1或区域2任一位置开始画线时，会开始播放音效</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### <mark style="background-color:orange;">1-2）</mark><mark style="background-color:orange;">**触发事件：画线完成**</mark>

需选择「是否匹配」以及「配对方式」下的「配对关系」或「配对类别」

* 若选择「匹配」-「配对关系」（支持单选或多选），还需选择具体是哪一组或哪几组配对关系
* 若选择「匹配」-「配对类别」，还需选择配对类别是true或者false

<mark style="color:red;">**注意:**</mark><mark style="color:red;">这里的true/false对应的是我们在前面「起止区域」部分所设置的配对关系的属性。</mark>在【画线回家】模板中，「配对1 -> 3」和「配对2-> 4」的类别为true，「配对1 -> 4」和「配对2-> 3」的类别为false

<figure><img src="../../../.gitbook/assets/image (1337).png" alt=""><figcaption></figcaption></figure>

**触发时机为：**<mark style="color:red;">**当已选择的配对关系或配对类别画线完成时**</mark>

**注意：**当我们多选了「配对关系」或者选择了某一「配对类别」时，只要<mark style="color:red;">其中任意一组「配对关系」完成画线</mark>，响应事件即会生效

<div align="left">

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">当设置「匹配」→「配对关系」→「配对1 -> 3」，响应事件为「跳转下一场景」时：则在区域1开始画线到区域3成功完成画线后，会跳转到下一场景</mark>

<mark style="background-color:yellow;">当设置「匹配」→「配对类别」→「true」，响应事件为「跳转下一场景」时：则在成功完成类别为true 的「1->3」</mark><mark style="color:red;background-color:yellow;">**或**</mark><mark style="background-color:yellow;">「2->4」</mark> <mark style="background-color:yellow;"></mark><mark style="background-color:yellow;">**任意**</mark><mark style="background-color:yellow;">一组画线时，都会跳转到下一场景</mark>

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* 若选择「不匹配」，直接添加对应响应事件即可

**触发时机为：当开始画线后，手指在**<mark style="color:red;">**所有配对关系以外的区域**</mark>**松开时，都属于不匹配**

<div align="left">

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">当设置「不匹配」，响应事件为「跳转下一场景」时：从区域1开始画线，在区域3或区域4之外松开画线，则视为「不匹配」，会跳转到下一场景；同理，从区域2开始画线，在区域3或区域4之外松开画线，则视为「不匹配」，会跳转到下一场景</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="color:red;">**注意：**</mark>「画线类别-false」和「不匹配」的区别：

「画线类别-false」 ：属于「配对关系」的一种（如模板中的配对1 -> 4）

「不匹配」：不包含任意一种「配对关系」（如模板中的配对1 -> 2）





#### <mark style="background-color:orange;">2-1）</mark><mark style="background-color:orange;">**响应事件：抹除连线线条**</mark>

需要选择抹除的「配对关系」。

该事件的响应结果为：所选择的配对关系中，**已画完的线条**会被抹除。

<mark style="color:red;">**注意：该响应事件仅对「直线」生效，对「自由绘制」不生效**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1332).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-2）</mark><mark style="background-color:orange;">**响应事件：修改连线线条样式**</mark>

需要选择修改的「起止区域」并设置线条样式。

该事件的响应结果为：所选择区域**开始画出的线及已经画完的线**，样式会修改为指定样式。

<mark style="color:red;">**注意：该响应事件**</mark>

* <mark style="color:red;">**针对「直线」：已画的和未画的线都生效**</mark>
* <mark style="color:red;">**针对「自由绘制」：已画的线不生效，未画的线生效**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1333).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-3）</mark><mark style="background-color:orange;">**响应事件：**</mark><mark style="background-color:orange;">修改已连线配对的线条样式</mark>

需要选择修改的「配对关系」并设置线条样式。

该事件的响应结果为：所选择的配对关系中，**已画完的线条**会被修改为指定样式

<mark style="color:red;">**注意：该响应事件仅对「直线」生效，对「自由绘制」不生效**</mark>

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1330).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-4）</mark><mark style="background-color:orange;">**响应事件：启用/禁用配对关系**</mark>

需要选择启用或禁用的「配对关系」。

* 若选择「禁用」，该事件的响应结果为：该配对关系，不再能够开始画线和结束画线
* 若选择「启用」，该事件的响应结果为：取消该配对关系的「禁用」事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1329).png" alt=""><figcaption></figcaption></figure>

</div>

#### <mark style="background-color:orange;">2-5）</mark><mark style="background-color:orange;">**响应事件：启用/禁用起止区域**</mark>

需要选择启用或禁用的「起止区域」。

* 若选择「禁用」，该事件的响应结果为：该起止区域，不再能够开始画线
* 若选择「启用」，该事件的响应结果为：取消该区域的「禁用」事件

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1331).png" alt=""><figcaption></figcaption></figure>

</div>
