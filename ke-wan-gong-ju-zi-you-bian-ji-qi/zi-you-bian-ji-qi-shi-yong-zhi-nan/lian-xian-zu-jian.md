---
description: '#自由编辑器 #模板自由制作 #模板自由制作'
---

# 连线组件

入口1：作品预览区>>>设置连线组件

入口2：图层区>>>连线组件

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:blue;">一、连线组件通俗介绍</mark>

* **「连线组件」仅存在于**<mark style="color:red;">**部分画线玩法的模板**</mark>**中，可通过【模板自由制作】进入**
* 适用于如连线配对、连连看等<mark style="color:red;">有固定可连线区域</mark>或<mark style="color:red;">固定配对组合</mark>的玩法
* 基于现有的「连线组件」，您可调整模板的可画线范围、画线的起止区域及样式、配对关系、连线类型等内容



## <mark style="color:blue;">二、连线组件使用说明</mark>

「连线组件」可调整的参数分3部分：「外观」、「起止区域」、「事件」

我们将结合模板[【画线回家】](http://tinyurl.com/5vsrhwjn)进行「连线组件」的使用说明

### 1.外观参数

* \[显示隐藏参数]横竖屏拆分：和各图层的外观参数相同，可分别调整该连线组件在横/竖屏下是否显示
* 位置尺寸：可以修改该连线组件的宽高、位置。其宽高位置，决定了能够画出线的范围（如下图，绿色覆盖范围即是在试玩过程中可画出线的范围）
* 屏幕适配方式：和各图层的外观参数相同，可调整该连线组件的屏幕适配方式
* 缩放比例：和各图层的外观参数相同，可调整该连线组件的比例

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>



### 2.起止区域

「起止区域」是连线组件独有的参数，一个连线组件有若干个起止区域和配对关系

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### **2）配对关系**

配对关系决定了某个区域是否能画出线：添加了配对关系的才可以画出线，未添加配对关系的即使有起止区域也画不出线

在【画线回家】模板中，共有4组配对关系：

* 每组配对关系需设置一个「开始区域」和「结束区域」，以及「配对类别」
* 「开始区域」只能选择一个，「结束区域」支持多选
* 「配对类别」分为true和false两种类别
* 支持修改每组配对关系的名称
* 支持删除配对关系（但不建议这么操作，可能会导致素材无法正常试玩）
* 支持预览已完成配对关系的所有连线线条

<div align="left">

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">共有4组配对关系：1->3、2->4、1->4、2->3</mark>

<mark style="background-color:yellow;">其中1->3、2->4被设置为「True」配对；1->4、2->3被设置为「False」配对</mark>

<mark style="background-color:yellow;">通过以上配对关系，素材可以从区域1、2拖拽画出线，若最终手指松开的位置在区域3、4内，则画线被保留，并触发相应的事件，否则画线不保留</mark>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



#### **3）连线配对**

影响配对关系

* 若选择「单向」，仅能从每个配对的前一个区域开始画线，后一个区域无法画出线。<mark style="background-color:yellow;">以模板【画线回家】的第一组配对关系为例，只能由区域1开始画线，到区域3结束，是无法从区域3开始画线的</mark>
* 若选择「双向」，则能从每组配对关系的任一区域开始画线。<mark style="background-color:yellow;">以模板【画线回家】的第一组配对关系为例，可从区域1开始画线到区域3，也可从区域3开始画线到区域1，两种都能成功完成画线</mark>

<div align="left">

<figure><img src="../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>

</div>



#### **4）连线类型**

决定画出的线条类型

* 自由绘制：简单来说，自由绘制就是跟随手指的画线轨迹所出现的曲线
* 直线：不受手指在画线过程中的轨迹影响，最终只形成直线

<div align="left">

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>



### 3.事件

「连线组件」包含两种**触发事件**：「开始画线」、「画线完成」

和「连线组件」相关的**响应事件**包含：「抹除连线线条」、「修改连线线条样式」、「启用/禁用配对关系」、「修改已连线配对的线条样式」、「启用/禁用起止区域」

<div align="left">

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>



#### 1-1）**触发事件：开始画线**

需要选择开始画线的区域并设置响应事件

**触发时机为：**<mark style="color:red;">**从已选择的「起止区域」开始画线时**</mark>

<mark style="background-color:yellow;">以模板【画线回家】为例，起止区域选择1和2，响应事件选择从头播放音效。则实现的效果是：当玩家从区域1或区域2任一位置开始画线时，会开始播放音效</mark>

<div align="left">

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

</div>

#### 1-2）**触发事件：画线完成**

需选择「是否匹配」以及「配对方式」下的「配对关系」或「配对类别」

* 若选择「匹配」-「配对关系」，还需选择具体是哪一组或哪几组配对关系
* 若选择「匹配」-「配对类别」，还需选择当配对类别是true或者false

**触发时机为：**<mark style="color:red;">**当已选择的配对关系或配对类别画线完成时**</mark>

<div align="left">

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">当设置「匹配」→「配对关系」→「配对1 -> 3」，响应事件为「跳转下一场景」时：则在区域1开始画线到区域3成功完成画线后，会跳转到下一场景</mark>

<mark style="background-color:yellow;">当设置「匹配」→「配对类别」→「true」，响应事件为「跳转下一场景」时：则在成功完成类别为True 的「1->3」或「2->4」</mark> <mark style="background-color:yellow;"></mark><mark style="background-color:yellow;">**任意**</mark><mark style="background-color:yellow;">一组画线时，都会跳转到下一场景</mark>

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* 若选择「不匹配」，直接添加对应响应事件即可

**触发时机为：当开始画线后，手指在**<mark style="color:red;">**所有配对关系以外的区域**</mark>**松开时，都属于不匹配**

<div align="left">

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

</div>

<mark style="background-color:yellow;">以模板【画线回家】为例：</mark>

<mark style="background-color:yellow;">当设置「不匹配」，响应事件为「跳转下一场景」时：从区域1开始画线，在区域3或区域4之外松开画线，则视为「不匹配」，会跳转到下一场景；同理，从区域2开始画线，在区域3或区域4之外松开画线，则视为「不匹配」，会跳转到下一场景</mark>

<div align="left">

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

</div>









#### 3）**响应事件：抹除连线线条**

需要选择抹除的「配对」。该事件的响应结果为：指定配对已画完成的线条被抹除

<div align="left">

<figure><img src="../../.gitbook/assets/image (24) (1).png" alt="" width="477"><figcaption></figcaption></figure>

</div>

#### 4）**响应事件：修改连线线条样式**

需要选择修改的「区域」。该事件的响应结果为：该区域开始画出的线，及已经画完成的线条，修改样式为制定样式

<div align="left">

<figure><img src="../../.gitbook/assets/image (25) (1).png" alt="" width="316"><figcaption></figcaption></figure>

</div>

#### 5）**响应事件：启用/禁用配对关系**

需要选择启用/禁用的「配对」

* 若选择「禁用」，该事件的响应结果为：该配对关系，不再能够开始画线和结束画线
* 若选择「启用」，该事件的响应结果为：取消配对的「禁用」

<div align="left">

<figure><img src="../../.gitbook/assets/image (26) (1).png" alt="" width="323"><figcaption></figcaption></figure>

</div>
