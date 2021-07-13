---
description: 热点和图像映射支持
solution: Experience Manager
title: 热点和图像映射支持
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 热点和图像映射支持{#hotspot-and-image-maps-support}

查看器支持在主视图顶部呈现热点图标和图像映射区域。 如自定义热点和图像映射部分中所述，热点图标和区域的外观通过CSS进行控制。

请参阅[热点和图像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点和区域可以通过触发JavaScript回调来激活托管网页上的概览功能，或将用户重定向到外部网页。

## 概览热点 {#section-cda48fc9730142d0bb3326bac7df3271}

应使用AEMDynamic Media中的“概览”操作类型创作这些类型的热点或图像映射。 当用户激活此类热点或图像映射时，查看器会运行`quickViewActivate` JavaScript回调并将热点或图像映射数据传递给它。 嵌入网页应侦听此回调。 触发页面时，会打开其自身的概览实施。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

在AEM的Dynamic Media中为操作类型“概览”创作的热点或图像映射，会将用户重定向到外部URL。 根据创作过程中的设置，URL会在新的浏览器选项卡、同一窗口或命名的浏览器窗口中打开。
