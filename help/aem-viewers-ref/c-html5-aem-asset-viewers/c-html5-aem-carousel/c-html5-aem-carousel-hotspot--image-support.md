---
description: 热点和图像映射支持
solution: Experience Manager
title: 热点和图像映射支持
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# 热点和图像映射支持{#hotspot-and-image-maps-support}

查看器支持在主视图顶部渲染热点图标和图像映射区域。 如“自定义热点和图像映射”部分所述，热点图标和区域的外观通过CSS进行控制。

请参阅[热点和图像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点和区域可以通过触发JavaScript回调来激活托管网页上的快速视图功能，或者将用户重定向到外部网页。

## 快速视图热点{#section-cda48fc9730142d0bb3326bac7df3271}

应使用AEM的Dynamic Media中的“快速视图”操作类型创作这些类型的热点或图像映射。 当用户激活此类热点或图像映射时，查看器会运行`quickViewActivate` JavaScript回调并将热点或图像映射数据传递给它。 嵌入网页应侦听此回调。 触发页面时，它会打开自己的快速视图实现。

## 重定向至外部网页{#section-ef820c71251e4215800bb99c0c9ebe16}

为AEM的Dynamic Media中的操作类型“快速视图”创作的热点或图像映射将用户重定向到外部URL。 根据创作过程中所做的设置，URL将在新的浏览器选项卡、同一窗口中或指定的浏览器窗口中打开。
