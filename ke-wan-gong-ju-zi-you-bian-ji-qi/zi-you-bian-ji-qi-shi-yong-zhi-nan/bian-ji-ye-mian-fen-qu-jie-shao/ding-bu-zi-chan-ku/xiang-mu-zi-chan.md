---
description: '#自由编辑器'
---

# 项目资产

入口：顶部资产库>>>项目资产

<figure><img src="../../../../.gitbook/assets/image (1029).png" alt=""><figcaption></figcaption></figure>

* 「项目资产」包含当前项目下的所有资产，包括已经添加到画布的资产和已上传未添加到画布的资产
* 所有已添加到画布的资产，会带有「已添加」的角标
* 您上传的个人资产、使用的公共资产，以及使用模板项目创建的ps项目中自带的资产，都会出现在「项目资产」列表中

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (815).png" alt=""><figcaption></figcaption></figure>

</div>

* 可通过右侧图标筛选项目资产的状态（已添加和未添加），帮助您更好地管理项目内的资产使用情况

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (811).png" alt=""><figcaption></figcaption></figure>

</div>

## 上传资产的两条路径

### 1.本地上传

点击项目资产内的「本地上传」按钮，打开选择本地文件的弹窗，可多选文件添加进资源池

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (652).png" alt=""><figcaption></figcaption></figure>

</div>

### 2.拖拽上传

拖拽本地文件至项目资产弹窗内或画布内，都可进行资产的添加

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (729).png" alt=""><figcaption></figcaption></figure>

</div>

资产上传成功后，右下角弹窗会显示上传成功

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (650).png" alt=""><figcaption></figcaption></figure>

</div>

## &#x20;<a href="#jjwkg" id="jjwkg"></a>

## 项目资产的相关操作 <a href="#jjwkg" id="jjwkg"></a>

### 1.添加资产到画布

* 点击「项目资产」对应资产右下角的「+」号，即可将资产添加到当前场景的画布中

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (725).png" alt=""><figcaption></figcaption></figure>

</div>

### 2.替换资产

* 点击「项目资产」对应资产右上角的「...」号，选择替换资产
* 仅「已添加」的资产能够替换
* <mark style="color:red;">**替换后原资产关联的所有节点将被替换为目标资产**</mark>（若只想替换单独某个资产，可选中该资产节点，在右侧参数调整区进行替换）

<figure><img src="../../../../.gitbook/assets/image (432).png" alt=""><figcaption></figcaption></figure>

#### 替换资产的两种方式

**1.本地上传**

若为「本地上传」，则跳出本地上传弹窗，要求选择本地符合格式要求的同类型资源进行上传并替换

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure>

</div>

**2.从资产库选用**

若为「从资产库选用」，则跳出弹窗，从「公共资产库」、「我的资产库」、「项目资产」中选择对应类型的资产进行替换

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (469).png" alt="" width="484"><figcaption></figcaption></figure>

</div>

### 3.下载资产

* 点击「项目资产」对应资产右上角的「...」号，选择下载，即可将该资产下载到本地

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (437).png" alt=""><figcaption></figcaption></figure>

</div>

### 4.裁剪资产

* 点击「项目资产」对应资产右上角的「...」号，选择裁剪/剪辑
* 裁剪图片资产时，在点击之后跳出裁剪弹窗，将图片裁剪为合适的尺寸和大小后，点击确定，将会新生成副本资产，并以该副本资产替换原资产
* 裁剪视频/音频资产时，在点击之后跳出剪辑弹窗，将视频/音频剪辑为合适的时长后，点击确定，将会新生成副本资产，并以该副本资产替换原资产

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure>

</div>

### 5.删除资产

* 点击「项目资产」对应资产右上角的「...」号，选择删除，将在项目资产中删除该资产
* <mark style="color:red;">**若该资产已经被添加到场景，则同时删除应用了该资产的所有节点**</mark>

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (430).png" alt=""><figcaption></figcaption></figure>

</div>



## 不同类型资产的格式要求

「项目资产」下细分视频、音频、图片、动图类别

### 1.视频

* 大小要求：3M以内
* 尺寸建议不大于750\*1334
* 分辨率：建议低于1080P
* 帧率：不能低于20，建议20—30
* 格式：mp4

### 2.音频

* 大小要求：1M以内
* 比特率：128kbps以内
* 格式：导出mp3格式效果佳

### 3.图片

* 大小要求：小于1M
* 格式：PNG，JPG

### 4.动图：分为序列帧和龙骨

#### **4.1 序列帧**

* 包含多个**png**的**zip**格式

<mark style="color:red;">（特别提示：zip压缩包内只能包含1个文件夹 或 直接包含多个png文件）</mark>

* 文件大小限制：最大8MB
* 命名限制：png命名需以数字结尾，且数字要按顺序进行编号
* 上传后可在右侧参数调整区拖动调整序列帧的顺序

#### 4.2 龙骨

* 包含2个json文件+1个png的zip格式
* 文件大小限制：小于1M+
* 龙骨内的资源网格需要关闭

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (795).png" alt=""><figcaption></figcaption></figure>

</div>

