---
description: 热点支持
solution: Experience Manager
title: 热点支持
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,Business Practitioner
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 热点支持{#hotspot-support}

查看器支持在主视图顶部渲染热点图标。 热点图标的外观通过CSS进行控制，如热点部分中所述。

请参阅[热点](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点可以通过触发JavaScript回调来激活托管网页上的概览功能，或将用户重定向到外部网页。

## 概览热点 {#section-cda48fc9730142d0bb3326bac7df3271}

应使用AEM AssetsDynamic Media中的“快速查看”操作类型（按需）创作这些类型的热点。 当用户激活此类热点时，查看器会运行`quickViewActivate` JavaScript回调并将热点数据传递到该回调器。 嵌入网页应侦听此回调。 触发页面时，会打开其自身的概览实施。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

在AEM Assets的Dynamic Media中为操作类型“快速查看”创作的热点 — 按需将用户重定向到外部URL。 根据创作过程中的设置，URL会在新的浏览器选项卡、同一窗口或命名的浏览器窗口中打开。
