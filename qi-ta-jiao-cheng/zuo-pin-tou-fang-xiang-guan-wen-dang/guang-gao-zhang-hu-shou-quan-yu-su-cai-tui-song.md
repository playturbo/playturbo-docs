---
description: '#订阅#定制'
---

# 广告账户授权与素材推送

您可以在Playturbo平台，对您的投放广告账户进行授权。授权广告账户后，您可以向授权成功的广告账户内推送试玩/视频素材用于投放，并且在后续的数据分析中，能够对您投放的素材数据进行分析。



## <mark style="color:red;">一、广告账户授权</mark>

### 1. 入口

左侧导航栏-「常用设置」-「授权管理」

<div align="left">

<figure><img src="../../.gitbook/assets/image (1188).png" alt="" width="241"><figcaption></figcaption></figure>

</div>

注：当前支持**Mintegral**和**Unity**两个广告平台的账号授权。后续会开放更多广告平台账号的授权。

### 2. 授权流程

1）点击右上角「+授权」按钮

2）需先选择平台：

&#x20;    a.对于Mintegral账号：需输入主账号的账号邮箱、Api\_Key、Access\_Key

&#x20;    b.对于Unity账号：需输入账号的邮箱、Api\_Key、Secret\_Key、Key\_id、Org\_id、Org\_Core\_id

3）确认信息输入正确，并勾选「已确认阅读保密协议」后，点击「授权」按钮

<div align="left">

<figure><img src="../../.gitbook/assets/image (1190).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

**4）补充：Mintegral子账号授权**

对于授权成功的Mintegral主账号，可以对主账号下的子账号进行授权，使素材可以推送到该子账号

<div align="left">

<figure><img src="../../.gitbook/assets/image (1191).png" alt=""><figcaption></figcaption></figure>

</div>

点击「子账号管理」按钮，跳出弹窗，可以对该主账号下的所有子账号进行「授权」或「取消授权」的操作

<div align="left">

<figure><img src="../../.gitbook/assets/image (1192).png" alt="" width="563"><figcaption></figcaption></figure>

</div>

### 3. 其他说明

#### 1）补充说明

* 授权成功后的账号，可以通过操作「取消授权」，以取消向该账户推送素材和拉取投放数据的权限
* 状态为「授权失败」的账号，可以通过再次操作「授权」，输入相关信息以授权原账号
* Mintegral最多同时授权一个主账号。且授权主账号后，30天内无法「取消授权」

<div align="left">

<figure><img src="../../.gitbook/assets/image (1193).png" alt=""><figcaption></figcaption></figure>

</div>

#### 2）Mintegral如何获得授权所需信息

登陆Mintegral平台，在「账号管理」-「基本信息」页面，获得所需的邮箱，Access Key 和 API Key

<div align="left">

<figure><img src="../../.gitbook/assets/image (1194).png" alt=""><figcaption></figcaption></figure>

</div>

#### 3）Unity如何获得授权所需信息

登陆Unity平台，进入「Dashboard 」界面。点击 「Growth」 > 「Setting」页面 ，即可获得 Organization ID 和 Org Core ID

<div align="left">

<figure><img src="../../.gitbook/assets/image (1196).png" alt=""><figcaption></figcaption></figure>

</div>

进入 「API Management」页面，即可获得 API Key

<div align="left">

<figure><img src="../../.gitbook/assets/image (1195).png" alt=""><figcaption></figcaption></figure>

</div>

点击 **Growth > API Management > Serviece account**，进入 **Service Accounts** 页面

<figure><img src="../../.gitbook/assets/image (1197).png" alt=""><figcaption></figcaption></figure>

点击 **Create service account**，在弹窗中对API Key 进行命名和添加描述，点击Create

<div align="left">

<figure><img src="../../.gitbook/assets/image (1198).png" alt=""><figcaption></figcaption></figure>

</div>

点击下图的 **Add ordanization role**，编辑API 权限。关于Growth 的8个权限都需勾选

<div align="left">

<figure><img src="../../.gitbook/assets/image (1199).png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="../../.gitbook/assets/image (1200).png" alt=""><figcaption></figcaption></figure>

</div>

在 Keys 栏点击 **Create new key**

<div align="left">

<figure><img src="../../.gitbook/assets/image (1201).png" alt=""><figcaption></figcaption></figure>

</div>

弹出窗口中复制 Key ID 和 Secret key

<figure><img src="../../.gitbook/assets/image (1202).png" alt=""><figcaption></figcaption></figure>



## <mark style="color:red;">二、素材推送</mark>

注：当前仅支持Mintegral/Unity两个渠道（后续会对接开放更多渠道）。仅支持推送到这两个渠道下已绑定的广告账号下。

### 1. 试玩素材推送操作

1）点击试玩项目列表或制作页面的「推送」按钮，跳出「推送」弹窗

<div align="left">

<figure><img src="../../.gitbook/assets/image (1203).png" alt=""><figcaption></figcaption></figure>

</div>

2）输入「素材名称前缀」，默认取的素材名称为项目名。最终生成的素材名将加上后缀

3）选择已绑定的Mintegral或Unity广告账号。若推送渠道为Unity，则需要选择推送到的产品

4）通过「包体控制」，使得包体大小满足各个渠道的要求

5）点击「推送」按钮，进行推送

<div align="left">

<figure><img src="../../.gitbook/assets/image (1204).png" alt=""><figcaption></figcaption></figure>

</div>



### 2. 视频素材推送操作

1）在「导出&下载历史」-「视频项目」的「导出任务」和「作品」页面，均可以操作「推送」，跳出「推送」弹窗

<div align="left">

<figure><img src="../../.gitbook/assets/image (1205).png" alt=""><figcaption></figcaption></figure>

</div>

2）输入「素材名称」，默认取的素材名称为项目名或作品名。最终生成的素材名将加上后缀

3）选择已绑定的Mintegral或Unity广告账号。若推送渠道为Unity，则需要选择推送到的产品

4）点击「推送」按钮，进行推送

<div align="left">

<figure><img src="../../.gitbook/assets/image (1206).png" alt=""><figcaption></figcaption></figure>

</div>

注：视频素材推送时不扣费，在导出时已对视频导出量进行扣减。
