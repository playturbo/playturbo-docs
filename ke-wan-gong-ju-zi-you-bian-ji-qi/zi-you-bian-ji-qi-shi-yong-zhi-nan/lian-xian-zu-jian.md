---
description: '#自由编辑器 #模板自由制作 #模板自由制作'
---

# 连线组件

入口1：作品预览区>>>设置连线组件

入口2：图层区>>>连线组件

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



## 一、连线组件通俗介绍

* **「连线组件」仅存在于**<mark style="color:red;">**部分画线玩法的模板**</mark>**中，可通过【模板自由制作】进入**
* 适用于如连线配对、连连看等<mark style="color:red;">有固定可连线区域</mark>或<mark style="color:red;">固定配对组合</mark>的玩法
* 基于现有的「连线组件」，您可调整模板的可画线范围、画线的起止区域及样式、配对关系、连线类型等内容



## 二、连线组件使用说明

「连线组件」可调整的参数分3部分：「外观」、「起止区域」、「事件」

我们将结合模板[【画线回家】](http://tinyurl.com/5vsrhwjn)进行「连线组件」的使用说明

### 1.外观参数

* \[显示隐藏参数]横竖屏拆分：和各图层的外观参数相同，可分别调整该连线组件在横/竖屏下是否显示
* 位置尺寸：可以修改该连线组件的宽高、位置。其宽高位置，决定了能够画出线的范围（如下图，绿色覆盖范围即是在试玩过程中可画出线的范围）
* 屏幕适配方式：和各图层的外观参数相同，可调整该连线组件的屏幕适配方式
* 缩放比例：和各图层的外观参数相同，可调整该连线组件的比例

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



### 2.起止区域

「起止区域」是连线组件独有的参数，一个连线组件有若干个起止区域和配对关系

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### **1）起止区域**

在该组件中设置若干个任意大小和位置的区域，该区域会和「配对关系」搭配使用，以产生具体的画线效果

在【画线回家】模板中：

* 支持修改已有的四个「起止区域」的线条样式：包含颜色及线条粗细
* 支持将某一起止区域的线条样式应用到当前全部起止区域
* 支持添加新的起止区域
* 对于每个起止区域，可在画布中调整其大小和位置
* 支持删除某一起止区域（不建议这么操作，可能会导致素材无法正常试玩）
* <mark style="color:red;">注意：起止区域的线条样式，代表的是从该区域画出的线条的样式</mark>

<div align="left">

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>

####

#### **2）配对关系**

配对关系决定了某个区域是否能画出线。

* 通过点击「添加配对关系」按钮以添加配对
* 每个配对关系需设置一个开始区域和结束区域，如下图中设置了配对1:1->2和配对2:4->5
* 配对1的含义：素材可以从区域1开始拖拽画出线，若最终手指松开的位置在区域2内，则画线被保留，若最终手指松开的位置不在区域2内，则画线不被保留
* 同理，配对2的含义：素材可以从区域4开始拖拽画出线，若最终手指松开的位置在区域5内，则画线被保留，若最终手指松开的位置不在区域5，则画线不被保留

<div align="left">

<figure><img src="../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### **3）连线配对**

影响配对关系。

* 若配置为「单向」，仅能从每个配对的前一个区域开始画线，连接到后一个区域则画线成功。则上述案例中，配对1只能由区域1开始画线，画线到区域2结束
* 若配置为「双向」，能从每个配对的任一区域开始画线，链接到另一个区域松开，则能画线成功。则上述案例中，配对1只能由区域1开始画线，画线到区域2结束，或从区域2开始画线，画线到区域1结束

<div align="left">

<figure><img src="../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>

</div>

#### **4）连线类型**

决定素材中具体画出的线条类型。

* 轨迹线：在画线过程中，手指位移的每一点都会被记录，形成一条弯曲的曲线
* 直线：在画线过程中，仅记录起点和当前的手指位置，形成一条直线

<div align="left">

<figure><img src="../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

</div>



### 4.设置事件

连线组件上可以设置两类触发事件：「开始画线」、「画线完成」

和连线组件相关的响应事件则包含：「抹除连线线条」、「修改连线线条样式」、「启用/禁用配对关系」

<div align="left">

<figure><img src="../../.gitbook/assets/image (21) (1).png" alt="" width="329"><figcaption></figcaption></figure>

</div>

#### 1）**触发事件：开始画线**

需要选择「起始区域」。触发时机为，从指定的「起始区域」 开始画线时

<div align="left">

<figure><img src="../../.gitbook/assets/image (22) (1).png" alt="" width="329"><figcaption></figcaption></figure>

</div>

#### 2）**触发事件：画线完成**

需选择「是否匹配」与「配对关系」

* 若选择匹配，则触发时机为，指定配对的画线完成
* 若选择不匹配，则触发时机为，画线开始后，在某个位置松开，但并未完成指定的连线配对

<div align="left">

<figure><img src="../../.gitbook/assets/image (23) (1).png" alt="" width="326"><figcaption></figcaption></figure>

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
