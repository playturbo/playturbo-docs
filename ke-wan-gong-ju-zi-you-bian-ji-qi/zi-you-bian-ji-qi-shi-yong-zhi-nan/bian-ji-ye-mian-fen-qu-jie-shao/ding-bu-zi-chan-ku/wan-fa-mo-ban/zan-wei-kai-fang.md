---
description: '#自由编辑器 #模板自由制作 #空白制作'
---

# 【暂未开放】

入口：顶部资产库>>>玩法模板>>>组件库>>>连线

<figure><img src="../../../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## 一、连线组件是什么

### 1.通俗描述

* 在画线玩法类型的素材中，需要有画线功能来实现素材的画线能力，「连线组件」即为工具的画线功能
* 可通过「连线组件」来定义组件的范围、可画线区域、配对关系等
* 支持在【模板自由制作】与【空白制作】中使用

### 2.包含模块

* 组件库包含「连线组件」和「自由画线组件」
* 当前仅「连线组件」，后续会上线「自由画线组件」

### 3.适配玩法

<mark style="color:orange;">连线组件：</mark>适用于如连线配对、连连看等有固定的可连线区域 和 固定的配对组合的玩法

<mark style="color:orange;">自由画线组件：</mark>适用于在指定区域内自由画线，且无额外限制条件的玩法



## 二、连线组件使用操作

### 1.添加连线组件

* 点击「+」图标，即可往当前场景内添加一个连线组件
* 单个场景最多添加一个「连线组件」

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</div>

### 2.调整外观参数

* 选中连线组件，在右侧参数设置区可修改该连线组件的位置尺寸、屏幕适配方式、缩放比例
* 其宽高位置，决定了在试玩过程中能够画出线的范围

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

</div>

### 3.编辑起止区域

「起止区域」是连线组件的独有参数，一个连线组件有若干个起止区域和配对关系

<figure><img src="../../../../../.gitbook/assets/image (11) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **1）起止区域**

在该组件中设置若干个任意大小和位置的区域，该区域会和「配对关系」搭配使用，以产生具体的画线效果。

* 通过点击「添加起止区域」按钮，可以在画布中添加一个起止区域
* 可以在画布中编辑每个起止区域的大小和位置
* 通过选中起止区域，再点击「Backspace」键以删除该起止区域

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (14) (1).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

* 展开起止区域，可调整该区域的线条样式，即从该区域画出线的样式

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (13) (1) (1).png" alt="" width="462"><figcaption></figcaption></figure>

</div>

#### **2）配对关系**

配对关系决定了某个区域是否能画出线。

* 通过点击「添加配对关系」按钮以添加配对
* 每个配对关系需设置一个开始区域和结束区域，如下图中设置了配对1:1->2和配对2:4->5
* 配对1的含义：素材可以从区域1开始拖拽画出线，若最终手指松开的位置在区域2内，则画线被保留，若最终手指松开的位置不在区域2内，则画线不被保留
* 同理，配对2的含义：素材可以从区域4开始拖拽画出线，若最终手指松开的位置在区域5内，则画线被保留，若最终手指松开的位置不在区域5，则画线不被保留

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>

#### **3）连线配对**

影响配对关系。

* 若配置为「单向」，仅能从每个配对的前一个区域开始画线，连接到后一个区域则画线成功。则上述案例中，配对1只能由区域1开始画线，画线到区域2结束
* 若配置为「双向」，能从每个配对的任一区域开始画线，链接到另一个区域松开，则能画线成功。则上述案例中，配对1只能由区域1开始画线，画线到区域2结束，或从区域2开始画线，画线到区域1结束

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

</div>

#### **4）连线类型**

决定素材中具体画出的线条类型。

* 轨迹线：在画线过程中，手指位移的每一点都会被记录，形成一条弯曲的曲线
* 直线：在画线过程中，仅记录起点和当前的手指位置，形成一条直线

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

</div>



### 4.设置事件

连线组件上可以设置两类触发事件：「开始画线」、「画线完成」

和连线组件相关的响应事件则包含：「抹除连线线条」、「修改连线线条样式」、「启用/禁用配对关系」

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (21).png" alt="" width="329"><figcaption></figcaption></figure>

</div>

#### 1）**触发事件：开始画线**

需要选择「起始区域」。触发时机为，从指定的「起始区域」 开始画线时

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (22).png" alt="" width="329"><figcaption></figcaption></figure>

</div>

#### 2）**触发事件：画线完成**

需选择「是否匹配」与「配对关系」

* 若选择匹配，则触发时机为，指定配对的画线完成
* 若选择不匹配，则触发时机为，画线开始后，在某个位置松开，但并未完成指定的连线配对

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (23).png" alt="" width="326"><figcaption></figcaption></figure>

</div>

#### 3）**响应事件：抹除连线线条**

需要选择抹除的「配对」。该事件的响应结果为：指定配对已画完成的线条被抹除

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (24).png" alt="" width="477"><figcaption></figcaption></figure>

</div>

#### 4）**响应事件：修改连线线条样式**

需要选择修改的「区域」。该事件的响应结果为：该区域开始画出的线，及已经画完成的线条，修改样式为制定样式

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (25).png" alt="" width="316"><figcaption></figcaption></figure>

</div>

#### 5）**响应事件：启用/禁用配对关系**

需要选择启用/禁用的「配对」

* 若选择「禁用」，该事件的响应结果为：该配对关系，不再能够开始画线和结束画线
* 若选择「启用」，该事件的响应结果为：取消配对的「禁用」

<div align="left">

<figure><img src="../../../../../.gitbook/assets/image (26).png" alt="" width="323"><figcaption></figcaption></figure>

</div>
