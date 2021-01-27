---
description: eCatalog Viewer支持在主视图上方渲染图像映射图标。
seo-description: eCatalog Viewer支持在主视图上方渲染图像映射图标。
seo-title: 图像映射支持
solution: Experience Manager
title: 图像映射支持
topic: Dynamic Media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# 图像映射支持{#image-map-support}

eCatalog Viewer支持在主视图上方渲染图像映射图标。

映射图标的外观通过CSS进行控制，如[图像映射效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)中所述。

图像映射执行以下三种操作之一：重定向到外部网页、“信息”面板弹出激活和内部超链接。

## 重定向到外部网页{#section-32ebe3c3a7f74892a428c5d48801de4d}

图像映射的`href`属性具有指向外部资源的URL（显式指定）或打包到支持的JavaScript模板函数之一中：`loadProduct()`、`loadProductCW()`和`loadProductPW()`。

以下是简单URL重定向的示例：

`href=http://www.adobe.com`

在此示例中，同一URL用`loadProduct()`函数包装：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

请注意，将JavaScript代码添加到图像映射的`HREF`属性时，该代码将在客户端的计算机上运行。 因此，确保JavaScript代码是安全的。

## 信息面板弹出激活{#section-7aa036420af646d1ad8cdc388add0b57}

要使用“信息”面板，图像映射已设置`ROLLOVER_KEY`属性。 同时设置`href`属性，否则外部URL处理会干扰“信息”面板弹出激活。

最后，确保查看器配置包含`InfoPanelPopup.template`的适当值，以及（可选）`InfoPanelPopup.infoServerUrl`参数。

>[!NOTE]
>
>请注意，配置“信息面板弹出窗口”时，传递给“信息面板”的HTML代码和JavaScript代码在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码是安全的。

## 内部超链接{#section-6afa4fb2fe564c429e0201f019a95849}

单击图像映射可在查看器中执行内部页面交换。 要使用该功能，图像映射中的`href`属性具有以下特殊格式：

` href=target: *`idx`*`

其中`*`idx`*`是目录跨页的从零开始的索引。

以下是指向eCatalog中3D跨页的图像映射的`href`属性示例：

`href=target:2`
