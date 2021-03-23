---
description: 操作系统、浏览器和移动设备的兼容性说明。
seo-description: 操作系统、浏览器和移动设备的兼容性说明。
seo-title: 兼容性说明
solution: Experience Manager
title: 兼容性说明
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
feature: Dynamic Media Classic，查看器，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---


# 兼容性说明{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

操作系统、浏览器和移动设备的兼容性说明。

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* 与早期的自适应视频集不兼容。 您可能需要重新上传自适应视频集以允许播放。

## 常规 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 浏览器端缩放可能导致用户放大页面时UI和图像变得模糊。 根据缩放情况，UI格式可能显示不正确。 这将转到全屏。
* 由于移动设备的大小限制，混合媒体查看器使用幻灯片手势来交换嵌入式图像集中的帧，而不是点击嵌入式色板组件。 组件作为可视指示器存在。
* 在Internet Explorer浏览器和某些触控设备中，全屏模式不占用整个设备屏幕。 而是将应用程序调整为浏览器窗口的大小。
* “关闭”按钮在iOS 8.0和iOS 8.1下不起作用，但在iOS 8.2下起作用。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 在缩放和电子目录查看器中发现内存泄漏。 在框架中重复导航可能会导致浏览器崩溃。
* 在查看器上点击多次可能会导致整个页面缩放，而不仅仅是启用浏览器侧缩放的查看器。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在纵向模式下检测到设备为平板电脑，并在浏览器设置中选中“全屏”。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 在启用浏览器侧缩放的情况下，点击查看器多次可能导致整个页面缩放，而不是仅缩放查看器。

## Galaxy Nexus 10和Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog以纵向和横向显示不正确的页面跨页。

## HTC移动设备{#section-dc42c80414c842e488738fc157c55b01}

* 无法禁用本机手指开合缩放是HTC UI包装器(HTC Sense)的“功能”。 在查看器上使用“捏合缩放”手势时，此功能可能导致整个页面缩放。 请改用多次点击手势。
* 如果图像映射很小并且很接近，则图像映射图标可能会重叠。

## HTML5视频查看器{#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 只有软件HLS和flash HDS回放才支持修改器。当播放使用本机播放器时，它不起作用。
* 不支持OGG和WebM渐进式播放。
* 浏览器缩放可能导致视频播放器以不正确的大小显示（包括Windows OS控制面板的“显示”设置）。
* 在Safari上使用HLS流的视频搜索可能不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支持Quirks模式。
* 不支持兼容模式。
* 不支持移动设备上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog可能导致浏览器在iPad 2上崩溃。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更高版本：Internet插件设置可能会阻止播放Flash视频。
* 在Safari上使用HLS流的视频搜索可能不一致。
* 无法使用HLS流在Safari 6上搜索视频结束。
