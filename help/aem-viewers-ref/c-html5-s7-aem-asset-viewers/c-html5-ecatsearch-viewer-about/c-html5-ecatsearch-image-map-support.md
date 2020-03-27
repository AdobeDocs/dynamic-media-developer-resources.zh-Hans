---
description: eCatalog Search Viewer支持在主视图上方呈现图像映射图标。
seo-description: eCatalog Search Viewer支持在主视图上方呈现图像映射图标。
seo-title: 图像映射支持
solution: Experience Manager
title: 图像映射支持
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像映射支持{#image-map-support}

eCatalog Search Viewer支持在主视图上方呈现图像映射图标。

如图像映射效果中所述，地图图标的外观通过CSS [进行控制](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)。

图像映射执行以下三个操作之一：重定向到外部网页、“信息”面板弹出激活和内部超链接。

## 重定向到外部网页 {#section-32ebe3c3a7f74892a428c5d48801de4d}

图 `href` 像映射的属性有一个指向外部资源的URL（显式指定），或包含在支持的JavaScript模板函数之一中： `loadProduct()`、 `loadProductCW()`和 `loadProductPW()`。

以下是简单URL重定向的示例：

`href=http://www.adobe.com`

在此示例中，同一URL与函数包 `loadProduct()` 装在一起：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. 因此，请确保JavaScript代码是安全的。

## 信息面板弹出式激活 {#section-7aa036420af646d1ad8cdc388add0b57}

要使用“信息”面板，图像映射已设置 `ROLLOVER_KEY` 属性。 同时设置 `href` 属性，否则外部URL处理会干扰“信息”面板弹出激活。

最后，确保查看器配置包含适当的参数 `InfoPanelPopup.template` 值和（可选）参 `InfoPanelPopup.infoServerUrl` 数。

>[!NOTE]
>
>请注意，配置“信息面板弹出窗口”时，传递给“信息面板”的HTML代码和JavaScript代码在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码是安全的。

## 内部超链接 {#section-6afa4fb2fe564c429e0201f019a95849}

单击图像映射可在查看器内执行内部页面交换。 要使用该功能，图像映 `href` 射中的属性具有以下特殊格式：

` href=target: *`idx`*`

其中 ` *`idx`*` 是目录跨页的从零开始的索引。

以下是指向eCatalog中 `href` 的3D跨页的图像映射属性示例：

`href=target:2`
