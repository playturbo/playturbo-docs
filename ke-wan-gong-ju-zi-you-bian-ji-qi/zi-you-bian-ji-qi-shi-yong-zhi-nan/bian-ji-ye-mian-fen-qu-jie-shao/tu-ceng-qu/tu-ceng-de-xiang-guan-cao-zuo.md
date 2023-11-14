# 图层的相关操作

图层展示逻辑

* 图层面板排序逻辑与画布展示逻辑一致，最上面的图层元素展示在画布最顶层
* 图层模块排序（由上到下）：普通资产>>视频资产>>音频资产

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (874).png" alt=""><figcaption></figcaption></figure>

</div>

## 1.调整图层顺序

### **1）方法1**

* 直接在图层面板中拖拽图层，即可调整顺序
* 拖拽方式支持在【普通资产】模块的任意层移动
* 视频资产与音频资产不可拖拽调整

### **2）方法2**

* 在图层面板中，点击选中需要调整顺序的图层
* 点击快捷操作区-图层顺序图标进行调整
* 快捷操作只支持置于顶层/置于底层/上移一层/下移一层4种移动方式

## 2.图层编组/解除编组

将多个资产编组后，对该组内资产的位置大小进行统一操作，或对该组增加动画事件等

### 1）如何进行图层编组

* 若对单个图层编组，可直接选中图层，点击编组按钮即可
* 若对多个图层编组，则需按住ctrl键，选择多个图层，再点击编组按钮

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure>

</div>

### 2）如何进行图层解组

* 选中该组图层
* a.鼠标右键单击，调起小弹窗，选择“解除编组”文字按钮，即可完成解组

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure>

</div>

* b.或在快捷操作区点击【解除编组】按钮

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

</div>

## 3.复制/粘贴图层

### **1）方法1**

* 选中需要复制的图层
* 鼠标右键单击，调起小弹窗，选择“复制图层”文字按钮
* 右键单击，调起小弹窗，选择“粘贴图层”文字按钮，即可完成图层的复制粘贴
* _名称默认为“原名称\_copy”_
* _只支持图层本身的复制粘贴_

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (876).png" alt=""><figcaption></figcaption></figure>

</div>

### **2）方法2**

* 选中需要复制的图层
* 点击快捷操作区快捷复制按钮
* 点击快捷操作区粘贴按钮，调起小弹窗
* 选择粘贴方式，即可完成图层的快速复制粘贴
* _支持快速复制图层，快速粘贴图层外观/位置大小/动画/事件/图层本身五种属性_

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (877).png" alt=""><figcaption></figcaption></figure>

</div>

## 4.删除图层

* 选中需要删除的图层
* 鼠标右键单击，调起小弹窗
* 点击选择“删除图层”文字按钮，即可成功删除图层

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (878).png" alt=""><figcaption></figcaption></figure>

</div>

## 5.锁定/解锁图层

* 将鼠标悬停到需要锁定的图层上，该图层会出现解锁状态的<img src="../../../../.gitbook/assets/0 (19).png" alt="image.png" data-size="line">图标
* 点击该图标即可进行锁定，<img src="../../../../.gitbook/assets/1 (91).png" alt="image.png" data-size="line">图标变成<img src="../../../../.gitbook/assets/2 (3).png" alt="image.png" data-size="line">图标
* 点击已锁定图标，即可进行图层解锁
* _图层默认不锁定；当图层锁定时，图层在画布中无法被选中_
* _锁定适用情况：多个场景同时存在，并且位置尺寸无需再被调整的元素_

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (879).png" alt=""><figcaption></figcaption></figure>

</div>

## 6.隐藏/显示图层

* 将鼠标悬停到需要隐藏的图层上，该图层会出现显示状态的<img src="../../../../.gitbook/assets/0 (34).png" alt="image.png" data-size="line">图标
* 点击该图标即可进行隐藏，<img src="../../../../.gitbook/assets/1 (8).png" alt="image.png" data-size="line">图标变成<img src="../../../../.gitbook/assets/2 (15).png" alt="image.png" data-size="line">图标
* 若需显示图层，点击已隐藏图标，即可将图层设置为显示状态
* _元素默认显示状态_
* _当元素隐藏时，图层在画布中不显示，可以通过事件设置让隐藏的图层显示出来（例如：双击后出现彩带礼花）_

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (880).png" alt=""><figcaption></figcaption></figure>

</div>

## 7.场景事件模式

* 元素默认：无场景事件，场景设置模式图标为<img src="../../../../.gitbook/assets/0 (39).png" alt="image.png" data-size="line">
* 当存在场景事件时，场景设置模式图标自动高亮为<img src="../../../../.gitbook/assets/1 (77).png" alt="image.png" data-size="line">

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (881).png" alt=""><figcaption></figcaption></figure>

</div>
