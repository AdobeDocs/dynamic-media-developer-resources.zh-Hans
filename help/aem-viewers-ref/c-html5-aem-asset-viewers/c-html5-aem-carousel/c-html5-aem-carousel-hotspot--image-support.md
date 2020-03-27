---
description: 'null'
seo-description: 'null'
seo-title: 热点和图像映射支持
solution: Experience Manager
title: 热点和图像映射支持
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 热点和图像映射支持{#hotspot-and-image-maps-support}

查看器支持在主视图上呈现热点图标和图像映射区域。 热点图标和区域的外观通过CSS进行控制，如自定义热点和图像映射部分中所述。

请参阅 [热点和图像映射](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

热点和区域可以通过触发JavaScript回调来激活托管网页上的“快速视图”功能，或将用户重定向到外部网页。

## 快速视图热点 {#section-cda48fc9730142d0bb3326bac7df3271}

应使用AEM的Dynamic Media中的“快速视图”操作类型创作这些类型的热点或图像映射。 当用户激活此类热点或图像映射时，查看器将运行 `quickViewActivate` JavaScript回调并将热点或图像映射数据传递给它。 预期嵌入网页会监听此回调。 在触发页面时，它会打开自己的快速视图实现。

## 重定向到外部网页 {#section-ef820c71251e4215800bb99c0c9ebe16}

为AEM的Dynamic Media中的操作类型“快速视图”创作的热点或图像映射将用户重定向到外部URL。 根据创作过程中所做的设置，URL将在新的浏览器选项卡、同一窗口中或指定的浏览器窗口中打开。
