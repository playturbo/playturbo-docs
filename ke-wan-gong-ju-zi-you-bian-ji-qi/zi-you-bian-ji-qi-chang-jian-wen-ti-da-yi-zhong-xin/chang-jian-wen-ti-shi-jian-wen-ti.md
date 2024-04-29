---
description: '#自由编辑器'
---

# 常见问题-事件问题

## **普通事件相关问题**

### <mark style="color:blue;">1.如何上报试玩结束</mark>

<table><thead><tr><th width="165.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题</strong></td><td><strong>当项目只有一个场景或最后一个场景并非仅是结束页面时，怎么上报试玩结束？</strong></td><td>/</td></tr><tr><td>解决方法</td><td><ul><li>可通过设置响应事件的方式实现，和跳转应用商店的事件设置在一起（不包含常驻下载按钮），选择【上报试玩结束】</li><li>不建议在右侧直接勾选【结束场景】</li></ul></td><td><img src="../../.gitbook/assets/image (143).png" alt="" data-size="original"></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zuo-pin-zhi-zuo-zhong-yao-ti-shi.md">zuo-pin-zhi-zuo-zhong-yao-ti-shi.md</a> <a data-mention href="../zuo-pin-zhi-zuo-zhong-yao-ti-shi.md#shang-bao-shi-wan-jie-shu">#shang-bao-shi-wan-jie-shu</a></td><td>/</td></tr></tbody></table>



### <mark style="color:blue;">2.想为多个图层设置相同的事件</mark>

<table><thead><tr><th width="163.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题</strong></td><td><strong>想要为多个图层设置相同的事件，一个一个设置太麻烦，怎么操作更快捷呢？</strong></td><td><img src="../../.gitbook/assets/image (1210).png" alt="" data-size="original"></td></tr><tr><td>解决方法</td><td><ul><li>先设置好其中一个图层的事件</li><li>点击事件的【复制】按钮</li><li>按住Ctrl键（苹果电脑使用command键）选中所有要设置同样事件的图层</li><li>点击快捷操作区的粘贴按钮，选择【仅粘贴图层事件】即可</li></ul></td><td><img src="../../.gitbook/assets/image (1211).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (1212).png" alt=""><img src="../../.gitbook/assets/image (1213).png" alt=""></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/kuai-jie-cao-zuo-qu.md">kuai-jie-cao-zuo-qu.md</a> <a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/kuai-jie-cao-zuo-qu.md#4.-fu-zhi-nian-tie">#4.-fu-zhi-nian-tie</a></td><td>/</td></tr></tbody></table>



### <mark style="color:blue;">3.触发事件“拖拽到指定位置”相关问题</mark>

<table><thead><tr><th width="165.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题-1</strong></td><td><strong>想实现“拖拽图层A到指定位置后，图层A就位于该位置”的效果，已设置了响应事件【设置位置】，但在预览时发现位置会有偏移？</strong></td><td><img src="../../.gitbook/assets/image (88).png" alt="" data-size="original"></td></tr><tr><td>解决方法</td><td><ul><li>注意：响应事件中的【设置位置】代表图层的“绝对位置”，是一个固定值，不会随着横竖屏或其他机型的改变而自动适配。因此想要保证在不同机型不同屏幕下实现目标效果，就不建议使用【设置位置】这一响应事件</li><li>正确处理方法：把拖拽的图层和正确放置后的图层拆分为二，并隐藏正确放置后的图层；在拖拽图层下设置事件【拖拽到指定位置】，设置响应事件为【隐藏拖拽图层】【显示正确放置后的图层】即可</li></ul></td><td><img src="../../.gitbook/assets/image (142).png" alt="" data-size="original"></td></tr><tr><td><strong>问题-2</strong></td><td><strong>怎么实现当把某物体拖拽到指定位置时，播放一系列正确反馈？</strong></td><td>/</td></tr><tr><td>解决方法</td><td><ul><li>选中目标物品图层</li><li>添加事件【拖拽到指定区域】，并编辑拖拽位置，选择拖拽方向，保存</li><li>然后添加相应的响应事件（正确反馈），如隐藏原图层-显示新图层-播放相关动画和音效</li></ul></td><td><p></p><p><img src="../../.gitbook/assets/image (1216).png" alt="" data-size="original"></p></td></tr><tr><td><strong>问题-3</strong></td><td><strong>若某物体未被正确拖拽到指定区域，怎么实现立即弹回原位，并播放一系列错误反馈？</strong></td><td>/</td></tr><tr><td>解决方法</td><td><ul><li>工具默认未拖拽到指定区域会自动弹回原位，且无拖拽次数限制</li><li>若想设置错误反馈，可以选中目标物品图层，添加事件【抬起】</li><li>在【抬起】事件下添加相应的响应事件（错误反馈），如播放错误动画和音效</li></ul></td><td><img src="../../.gitbook/assets/image (1217).png" alt="" data-size="original"></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/can-shu-lei-xing-jie-shao/shi-jian/pu-tong-shi-jian/chu-fa-shi-jian.md">chu-fa-shi-jian.md</a> <a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/can-shu-lei-xing-jie-shao/shi-jian/pu-tong-shi-jian/xiang-ying-shi-jian.md">xiang-ying-shi-jian.md</a></td><td>/</td></tr></tbody></table>



### <mark style="color:blue;">4.响应事件的设置相关问题</mark>

<table><thead><tr><th width="173.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题-1</strong></td><td><strong>在预览时发现某个动画重复播放了2次，怎么关掉其中一个动画？</strong></td><td>/</td></tr><tr><td>解决方法</td><td><ul><li>出现这种情况大概率是设置了2个播放动画的响应事件：如一个是点击播放动画，一个是执行延迟播放动画</li><li>选择【点击】事件，在事件下添加一个响应事件为【取消执行延迟】，然后选择对应的定时器ID即可</li></ul></td><td><p></p><p></p><p><img src="../../.gitbook/assets/image (1049).png" alt="" data-size="original"></p></td></tr><tr><td><strong>问题-2</strong></td><td><strong>已经为某图层设置了动画，但在预览时并未播放，是什么原因？</strong></td><td><img src="../../.gitbook/assets/image (1218).png" alt="" data-size="original"></td></tr><tr><td>解决方法</td><td><ul><li>先查看图层状态是否为【隐藏】（若因制作需要隐藏图层，则要在响应事件中添加一条【显示素材】）</li><li>还需在响应事件下添加一条【从头播放全部动画】或【从头播放单个动画】，选择对应动画即可</li></ul></td><td><p></p><p><img src="../../.gitbook/assets/image (1050).png" alt="" data-size="original"></p></td></tr><tr><td><strong>问题-3</strong></td><td><strong>给某图层设置了动画A，又给图层的组设置了动画B，然后在响应事件中添加了【从头播放组的全部动画】，但在预览时却只播放了动画B？</strong></td><td><img src="../../.gitbook/assets/image (86).png" alt="" data-size="original"></td></tr><tr><td>解决方法</td><td><ul><li>注意：虽然在组上设置的动画会同时影响组内资产，但在添加响应事件时则需要分开添加</li><li>所以要分别设置2条响应事件：播放某图层的动画、播放图层组的动画</li></ul></td><td><img src="../../.gitbook/assets/image (87).png" alt="" data-size="original"></td></tr><tr><td><strong>问题-4</strong></td><td><strong>想实现“在屏幕上点击</strong><em><strong>除正确区域以外</strong></em><strong>的位置时，出现错误反馈，如弹出「✕」”，该怎么设置？</strong></td><td><img src="../../.gitbook/assets/image (90).png" alt="" data-size="original"></td></tr><tr><td>解决方法</td><td><ul><li>添加一个「✕」的图片或文本（可为其设置Q弹晃动的动画），然后调整好位置大小，隐藏掉该图层</li><li>添加若干手势区域，框选住错误区域</li><li>为其中一个手势区域添加事件-按下；添加响应事件-显示素材「✕」-从头播放「✕」的动画-执行延迟0.5s后隐藏「✕」</li><li>复制该事件到其他手势区域即可</li><li><mark style="color:red;">注意：工具暂时不能实现「✕」随点击位置的不同而出现在不同位置</mark></li></ul></td><td><img src="../../.gitbook/assets/image (91).png" alt="" data-size="original"></td></tr><tr><td><strong>问题-5</strong></td><td><strong>想实现“点击某图层/场景后，开始播放视频，当视频播放完，跳转指定场景”，该怎么设置？</strong></td><td>/</td></tr><tr><td>解决方法</td><td><ul><li>视频参数设置为“关闭入场自动播放”、“关闭无限循环”</li><li>选中该图层/场景，添加事件-按下；添加响应事件-显示视频-从头播放视频</li><li>再选中视频图层，添加事件-结束时；添加响应事件-跳转指定场景</li></ul></td><td><p><img src="../../.gitbook/assets/image (92).png" alt="" data-size="original"></p><p></p><p><img src="../../.gitbook/assets/image (93).png" alt=""></p></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/can-shu-she-zhi-qu/can-shu-lei-xing-jie-shao/shi-jian/pu-tong-shi-jian/xiang-ying-shi-jian.md">xiang-ying-shi-jian.md</a></td><td>/</td></tr></tbody></table>





## **全局变量相关问题**

### <mark style="color:blue;">1.全局变量跨场景</mark>

<table><thead><tr><th width="163.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题</strong></td><td><strong>全局变量设置的值，在跳转到其他场景后，是会重置还是继承前一个场景中的数值？</strong></td><td></td></tr><tr><td>解决方法</td><td><ul><li>全局变量是贯穿所有场景的，不会因切换场景就重置全局变量。除非有事件设置控制全局变量在切换场景后重置</li><li>也就是说在任一场景都可以对同一个全局变量进行设置</li></ul></td><td></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/quan-ju-bian-liang.md">quan-ju-bian-liang.md</a></td><td>/</td></tr></tbody></table>



### <mark style="color:blue;">2.条件判断相关问题</mark>

<table><thead><tr><th width="163.33333333333331"> </th><th width="390">具体描述</th><th>截图</th></tr></thead><tbody><tr><td><strong>问题</strong></td><td><strong>条件判断有办法复制吗，还是只能手动添加</strong></td><td></td></tr><tr><td>解决方法</td><td><ul><li>条件判断的整个事件是可以复制的</li><li>若同时存在多个条件判断，只想复制其中一个，暂时不可以，需要手动添加（若响应事件较多，可先复制整个条件判断，再删除其他不需要的）</li></ul></td><td><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td></tr><tr><td>关于解决方法的详细介绍可查看<span data-gb-custom-inline data-tag="emoji" data-code="1f449">👉</span></td><td><a data-mention href="../zi-you-bian-ji-qi-shi-yong-zhi-nan/bian-ji-ye-mian-fen-qu-jie-shao/ding-bu-zi-chan-ku/quan-ju-bian-liang.md">quan-ju-bian-liang.md</a></td><td>/</td></tr></tbody></table>
