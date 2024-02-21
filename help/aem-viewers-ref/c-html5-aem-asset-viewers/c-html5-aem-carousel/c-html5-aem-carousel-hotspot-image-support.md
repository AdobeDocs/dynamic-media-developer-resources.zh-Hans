---
title: 热点和图像映射支持
description: 热点和图像映射支持
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 热点和图像映射支持{#hotspot-and-image-maps-support}

查看器支持在主视图顶部渲染热点图标和图像映射区域。 热点图标和区域的外观通过CSS进行控制，如自定义热点和图像映射部分中所述。

请参阅 [热点和图像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

热点和区域可以通过触发JavaScript回调在托管网页上激活概览功能，也可以将用户重定向到外部网页。

## 概览热点 {#section-cda48fc9730142d0bb3326bac7df3271}

这些类型的热点或图像映射应使用Adobe Experience Manager的Dynamic Media中的“快速视图”操作类型进行创作。 当用户激活此类热点或图像映射时，查看器运行 `quickViewActivate` JavaScript回调并将热点或图像映射数据传递给它。 嵌入网页应侦听此回调。 在触发页面时，它会打开自己的概览实施。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

在Experience Manager的Dynamic Media中为操作类型“快速视图”创作的热点或图像映射会将用户重定向到外部URL。 根据创作期间所做的设置，URL将在新的浏览器选项卡、同一窗口或指定的浏览器窗口中打开。
