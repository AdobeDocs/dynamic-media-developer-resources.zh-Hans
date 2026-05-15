---
title: 预加载图像
description: 预加载图像是一种静态资源预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预加载图像的目的在于直观地改善查看者的加载时间并向用户快速展示内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
TQID: 'https://experienceleague.adobe.com/0Gm-U-1l0osVADyWyLCH4rJRUCuRHgUJ8XNsbDNpkgc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# 预加载图像{#preload-image}

预加载图像是一种静态资源预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预加载图像的目的在于直观地改善查看者的加载时间并向用户快速展示内容。

预加载图像适用于最常见的查看器嵌入方法，即不受高度限制的响应式嵌入。 查看标题[具有不受限制高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，当使用其他嵌入方法或特定配置选项时，该功能有一定的限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器大小固定，且大小在查看器预设记录中使用`stagesize`配置属性或在顶级查看器容器元素的外部查看器CSS文件中定义时。
* 使用灵活大小嵌入时，采用宽度和高度定义的查看器嵌入方法。 查看标题[宽度和高度定义的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果在上面列出的操作模式之一中使用查看器，请使用`preloadImage`配置属性禁用预加载图像功能。

此外，如果查看器嵌入到DOM元素中使用`display:none` CSS设置是隐藏的，或者已从DOM树中分离，则不会使用预加载图像（即使在配置中启用了预加载图像）。
