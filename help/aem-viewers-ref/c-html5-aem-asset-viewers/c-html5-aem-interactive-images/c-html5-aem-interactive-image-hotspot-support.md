---
description: 热点支持
solution: Experience Manager
title: 热点支持
topic: Dynamic Media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# 热点支持{#hotspot-support}

查看器支持在主视图上呈现热点图标。 热点图标的外观通过CSS进行控制，如热点部分中所述。

请参阅[热点](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点可以通过触发JavaScript回调来激活托管网页上的快速视图功能，或者将用户重定向到外部网页。

## 快速视图热点{#section-cda48fc9730142d0bb3326bac7df3271}

应使用AEM AssetsDynamic Media的“快速视图”操作类型（按需）创作这些类型的热点。 当用户激活此类热点时，查看器将运行`quickViewActivate` JavaScript回调并将热点数据传递给它。 嵌入网页应监听此回调。 触发页面时，它会打开自己的快速视图实现。

## 重定向到外部网页{#section-ef820c71251e4215800bb99c0c9ebe16}

为AEM AssetsDynamic Media的操作类型“快速视图”创作的热点——按需将用户重定向到外部URL。 根据创作过程中所做的设置，URL将在新的浏览器选项卡、同一窗口或指定的浏览器窗口中打开。
