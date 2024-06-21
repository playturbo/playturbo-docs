# 视频AI消除

**使用AI技术可以高效移除视频中的特定元素**（如画面中文本、字幕、水印或徽标等不需要的元素）。

常见应用场景如下：

1.消除视频画面中不需要的元素

2.替换视频画面中文本为其他文本内容

3.翻译视频画面中指定时间范围的文本



使用视频AI消除的步骤：

## <mark style="color:blue;">第一步：功能入口及添加消除区域</mark>

在使用布局模板编辑快速替换项目时，可以对已添加的主视频进行AI消除编辑。

1.选中主视频后，点击“**添加**”，展开该视频的AI消除区域编辑页面。

<figure><img src="../../../.gitbook/assets/image (1914).png" alt=""><figcaption></figcaption></figure>

2.在画面中框选标记需要处理的区域，即希望移除或替换的特定元素。默认情况下，系统会对视频的所有时间段进行消除，您也可以在添加选框后，手动调整时间轴上的消除时间范围。

<figure><img src="../../../.gitbook/assets/image (1915).png" alt=""><figcaption></figcaption></figure>

3.一个视频内可添加多个区域后，批量保存提交。

<figure><img src="../../../.gitbook/assets/image (1916).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:blue;">第二步：编辑任务属性</mark>

保存需要处理的区域后，返回素材上传页面，对已添加的框选区域进行消除任务属性编辑。

框选区域支持三种任务类型，以满足不同的编辑需求。

### 场景一：对象移除

* 对象移除：在指定时间范围内，擦除视频中框选区域的内容。
* 适用场景：用于移除原视频画面中的多余水印、徽标、字幕等不需要的元素。

<figure><img src="../../../.gitbook/assets/image (1917).png" alt=""><figcaption></figcaption></figure>



### 场景二：文本替换

* 文本替换：在指定时间范围内，擦除视频中框选区域的文字并替换为新的文本。该框选区域类似于布局模板中的文本占位符，可以添加多个文本（素材组合），最终可以批量导出多个版本的视频。
* 适用场景：修改原视频画面中的文本，并支持将修改后的文本翻译为其他语言。

<figure><img src="../../../.gitbook/assets/image (1918).png" alt=""><figcaption></figcaption></figure>

#### 消除后

<figure><img src="../../../.gitbook/assets/中文最新文本替换.jpg" alt=""><figcaption></figcaption></figure>

### 场景三：文本翻译

* 文本翻译：在指定时间范围内，将视频中框选区域的文字翻译为多种语言。
* 适用场景：将原视频画面中的文本内容翻译为其他语言。

<figure><img src="../../../.gitbook/assets/image (1919).png" alt=""><figcaption></figcaption></figure>

#### 消除后

<figure><img src="../../../.gitbook/assets/image (1932).png" alt=""><figcaption></figcaption></figure>

### 小结

下表展示了三种不同任务对多语言项目导出结果的影响。

| **任务类型** | **项目原语言（原视频）**   | **翻译语言（项目其他原语言）** |
| -------- | ---------------- | ----------------- |
| 对象移除     | 框选区域被消除          | 框选区域被消除           |
| 文本替换     | 框选区域被消除，并使用新文本填充 | 框选区域使用新文本的译文填充    |
| 文本翻译     | 原始视频内容           | 框选区域使用原文本的译文填充    |

## <mark style="color:blue;">第三步：提交任务</mark>

完成任务编辑后，点击“**开始消除**”按钮，批量提交该视频下的AI消除任务。&#x20;

<figure><img src="../../../.gitbook/assets/image (1920).png" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">任务提交后，您可以在导航栏的任务中心查看历史任务进展。</mark>&#x20;
