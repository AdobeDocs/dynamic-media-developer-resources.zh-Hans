---
title: 热点支持
description: 热点支持
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
TQID: 'https://experienceleague.adobe.com/kvYBwi70uYXIK8D6MeNgZN74h3X6jBfmOLj1SjlKEzs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# 热点支持{#hotspot-support}

查看器支持在主视图顶部渲染热点图标。 热点图标的外观通过CSS进行控制，如热点部分中所述。

查看[热点](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点可以通过触发JavaScript回调在托管网页上激活概览功能，或将用户重定向到外部网页。

## 概览热点 {#section-cda48fc9730142d0bb3326bac7df3271}

这些类型的热点应使用Adobe Experience Manager Assets - On-demand的Dynamic Media中的“Quickview”操作类型进行创作。 当用户激活此类热点时，查看器运行`quickViewActivate` JavaScript回调并将热点数据传递给它。 嵌入网页应侦听此回调。 在触发页面时，它会打开自己的概览实施。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

在Experience Manager Assets的Dynamic Media中为操作类型“快速查看”创作的热点 — 按需将用户重定向到外部URL。 根据创作期间所做的设置，URL将在新的浏览器选项卡、同一窗口或指定的浏览器窗口中打开。
