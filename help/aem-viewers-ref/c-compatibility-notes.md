---
title: 兼容性说明
description: 操作系统、浏览器和移动设备的兼容性说明。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 1%

---

# 兼容性说明{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

操作系统、浏览器和移动设备的兼容性说明。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 与旧版自适应视频集不兼容。 重新上传自适应视频集以允许播放。

## 常规 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 浏览器端缩放会导致UI和图像在用户放大到页面时变得模糊。 用户界面格式也会根据缩放显示不正确，并会转移到全屏。
* 由于移动设备上的大小限制，混合媒体查看器使用幻灯片手势在嵌入的图像集中交换帧，而不是点按嵌入的样本组件。 组件以可视指示器的形式存在。
* 在Internet Explorer浏览器和某些触控设备中，全屏模式不会占用整个设备屏幕。 相反，它会将应用程序的大小调整为与浏览器窗口的大小相同。
* “关闭”按钮在iOS 8.0和iOS 8.1下不起作用，但在iOS 8.2下起作用。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 使用Zoom和eCatalog查看器时发现内存泄漏。 在帧中重复导航会导致浏览器崩溃。
* 双击查看器会导致整个页面缩放，而不仅仅是启用了浏览器端缩放的查看器。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在浏览器设置中选中“全屏”后，设备在纵向模式下被检测为平板电脑。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 在启用了浏览器端缩放的情况下，双击查看器会导致整个页面缩放，而不仅仅是查看器。

## Galaxy Nexus 10和Galaxy平板电脑 {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog显示错误的页面跨页，具有纵向和横向方向。

## HTC移动设备 {#section-dc42c80414c842e488738fc157c55b01}

* 无法禁用本机缩放，这是HTC UI包装器(HTC Sense)的“功能”。 在查看器上使用“捏合缩放”手势时，此功能可能会导致整个页面缩放。 请改用双击手势。
* 如果图像映射较小且彼此靠近，则图像映射图标会重叠。

## HTML5视频查看器 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 仅软件HLS和FlashHDS播放支持修饰符。 使用本机播放器播放时，此选项不起作用。
* 不支持OGG和WebM渐进式播放。
* 浏览器缩放导致视频播放器的显示大小不正确(包括Windows®控制面板显示设置)。
* 在Safari上使用HLS流播放的视频搜寻不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支持Quirks模式。
* 不支持兼容模式。
* 不支持移动设备上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog会导致浏览器在iPad 2上崩溃。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更高版本： Internet插件设置阻止Flash视频播放。
* 在Safari上使用HLS流播放的视频搜寻不一致。
* 无法使用HLS流在Safari 6上搜寻结束视频。
