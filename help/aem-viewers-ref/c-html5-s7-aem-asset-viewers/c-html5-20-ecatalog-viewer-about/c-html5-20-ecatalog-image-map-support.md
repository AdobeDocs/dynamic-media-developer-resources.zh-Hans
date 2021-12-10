---
title: 图像映射支持
description: eCatalog查看器支持在主视图上方渲染图像映射图标。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 图像映射支持{#image-map-support}

eCatalog查看器支持在主视图上方渲染图像映射图标。

地图图标的外观通过CSS进行控制，如 [图像映射效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

图像映射执行以下三个操作之一：重定向到外部网页、“信息”面板弹出式激活和内部超链接。

## 重定向到外部网页 {#section-32ebe3c3a7f74892a428c5d48801de4d}

的 `href` 图像映射的属性具有指向外部资源的URL（显式指定），或者封装到支持的JavaScript模板函数之一中： `loadProduct()`, `loadProductCW()`和 `loadProductPW()`.

以下是简单URL重定向的示例：

`href=http://www.adobe.com`

在此示例中，同一URL用 `loadProduct()` 函数：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

在 `HREF` 属性，则代码将在客户端的计算机上运行。 因此，请确保JavaScript代码的安全。

## 信息面板弹出菜单激活 {#section-7aa036420af646d1ad8cdc388add0b57}

要使用“信息”面板，图像映射将 `ROLLOVER_KEY` 属性集。 此外，设置 `href` 属性，否则外部URL处理会干扰“信息”面板弹出激活。

最后，确保查看器配置包含 `InfoPanelPopup.template` 或者， `InfoPanelPopup.infoServerUrl` 参数。

>[!NOTE]
>
>配置“信息面板弹出窗口”时，传递到“信息面板”的HTML代码和JavaScript代码将在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码是安全的。

## 内部超链接 {#section-6afa4fb2fe564c429e0201f019a95849}

选择图像映射会在查看器内执行内部页面交换。 要使用该功能，请 `href` 图像映射中的属性具有以下特殊格式：

` href=target: *`idx`*`

其中 `*`idx`*` 是目录跨页的从零开始的索引。

以下是 `href` 指向eCatalog中3D跨页的图像映射的属性：

`href=target:2`
