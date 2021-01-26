---
description: 将属性设置为FXG根元素。
seo-description: 将属性设置为FXG根元素。
seo-title: setAttr.rootElement
solution: Experience Manager
title: setAttr.rootElement
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dda16612-57c7-4abe-8aa4-00e599a8ea69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---


# setAttr.rootElement{#setattr-rootelement}

将属性设置为FXG根元素。

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

此命令可以操作根元素的属性。

## 示例 {#section-2758a6e316c34b99b13b02147e5973bb}

如果我们具有以下根元素：

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

应用以下命令后：

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

根元素现在更改为：

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
