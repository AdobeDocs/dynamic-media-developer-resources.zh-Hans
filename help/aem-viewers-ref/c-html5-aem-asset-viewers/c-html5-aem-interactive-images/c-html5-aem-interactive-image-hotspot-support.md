---
title: 热点支持
description: 热点支持
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 热点支持{#hotspot-support}

查看器支持在主视图顶部渲染热点图标。 热点图标的外观通过CSS进行控制，如热点部分中所述。

查看[热点](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点可以通过触发JavaScript回调在托管网页上激活概览功能，或将用户重定向到外部网页。

## 概览热点 {#section-cda48fc9730142d0bb3326bac7df3271}

应使用Dynamic Media中的“Quickview”操作类型(即Adobe Experience Manager Assets — 按需)创作这些类型的热点。 当用户激活此类热点时，查看器运行`quickViewActivate` JavaScript回调并将热点数据传递给它。 嵌入网页应侦听此回调。 在触发页面时，它会打开自己的概览实施。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

在Experience Manager Assets的Dynamic Media中为操作类型“快速视图”创作的热点 — 按需将用户重定向到外部URL。 根据创作期间所做的设置，URL将在新的浏览器选项卡、同一窗口或指定的浏览器窗口中打开。
