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

* 与旧的自适应视频集不兼容。 重新上传自适应视频集以允许播放。

## 常规 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 当用户放大到页面时，浏览器端缩放会导致用户界面和图像变得模糊。 用户界面格式也因缩放而显示不正确，并可全屏显示。
* 由于移动设备存在大小限制，混合媒体查看器使用幻灯片手势来交换嵌入图像集中的帧，而不是点按嵌入的色板组件。 组件作为可视指示器。
* 在Internet Explorer浏览器和某些触屏设备中，全屏模式不占用整个设备屏幕。 而是将应用程序的大小调整为浏览器窗口的大小。
* “关闭”按钮在iOS 8.0和iOS 8.1下不起作用，但在iOS 8.2下起作用。

## 银河二世 {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 在缩放和eCatalog查看器中出现内存泄漏。 在框架中重复导航会导致浏览器崩溃。
* 双击查看器会导致整个页面缩放，而不是仅使用启用了浏览器端缩放的查看器。

## 银河S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在纵向模式下，设备被检测为平板电脑，并在浏览器设置中选中全屏。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 双击查看器，会在启用浏览器端缩放的情况下，缩放整个页面，而不是仅缩放查看器。

## Galaxy Nexus 10和Galaxy平板电脑 {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog在纵向和横向方向上显示错误的页面跨页。

## HTC移动设备 {#section-dc42c80414c842e488738fc157c55b01}

* 无法禁用本机捏合缩放是HTC UI包装器(HTC Sense)的“功能”。 当在查看器上使用“捏合缩放”手势时，此功能可能会导致整个页面缩放。 请改用双击手势。
* 如果图像映射较小且很接近，则图像映射图标会重叠。

## HTML5视频查看器 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 仅软件HLS和FlashHDS播放支持修饰符。 当播放使用本机播放器时，该函数不起作用。
* 不支持OGG和WebM渐进式播放。
* 浏览器缩放导致视频播放器以不正确的大小显示(包括Windows®控制面板显示设置)。
* 在Safari上使用HLS流的视频搜索不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支持Quirks模式。
* 不支持兼容性模式。
* 不支持移动设备上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog导致浏览器在iPad 2上崩溃。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更高版本：Internet插件设置阻止Flash视频播放。
* 在Safari上使用HLS流的视频搜索不一致。
* 无法在使用HLS流的Safari 6上查找视频的结尾。
