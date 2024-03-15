# 叉乘与时序叉乘

## 5.时序叉乘

* 主轨道上的资产组支持设置时序叉乘
* 至少添加两个资产组
* 原转场效果可能会受影响

<figure><img src="../../../../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

* 导出时，将开启参与叉乘的片段打乱重组，从而增加视频的组合数
* 被设置时序叉乘的组，在最终的组合结果中，其时间轴位置可能会被互换：如勾选A、B、C三个组时序叉乘，最后的主轨道资产组排序可能为：ABC/ACB/BAC/BCA/CAB/CBA 六种结果
* 时序叉乘会增加最终组合的视频数，为原组合生成的视频数的 N！=1\*2\*…\*n倍

<figure><img src="../../../../../.gitbook/assets/image (512).png" alt=""><figcaption></figcaption></figure>

* 将鼠标悬浮于【资产组组合数】或【时序叉乘组合数】，可查看计算规则与组合数的由来

<figure><img src="../../../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>
